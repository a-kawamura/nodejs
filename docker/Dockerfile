FROM node:18

# アプリケーションディレクトリを作成する
WORKDIR /usr/arc/app

# アプリケーションの依存関係をインストールする
# ワイルドカードを使用して、package.jsonとpackage-lock.jsonの両方が確実にコピーされるようにすます。
# 可能であれば(npm@5+)
COPY package*.json ./

RUN npm install
# 本番用にコードを作成している場合
# RUN npm install --only-production

# アプリケーションのソースをバンドルする
COPY server.js ./

EXPOSE 8080

CMD [ "node", "server.js" ]