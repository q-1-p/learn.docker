FROM node:18-alpine

WORKDIR /app

COPY . .

RUN npm install

ARG DATABASE_URL
ENV DATABASE_URL=${DATABASE_URL}

RUN npx prisma generate

EXPOSE 3000

CMD ["npm", "run", "start"]
