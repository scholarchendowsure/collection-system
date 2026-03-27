FROM node:20-alpine

WORKDIR /app

# 创建数据目录
RUN mkdir -p /app/data

# 复制 package.json
COPY package*.json ./

# 安装依赖
RUN npm ci

# 复制源代码
COPY . .

# 构建
RUN npm run build

# 暴露端口
EXPOSE 3001

# 启动命令
CMD ["node", "dist/index.js"]
