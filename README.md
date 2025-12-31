datasource db {
  provider = "sqlite"
  url      = "file:./dev.db"
}

generator client {
  provider = "prisma-client-js"
}

model Paste {
  id             String   @id
  content        String
  createdAt      DateTime @default(now())
  expiresAt      DateTime?
  maxViews       Int?
  remainingViews Int?
}
