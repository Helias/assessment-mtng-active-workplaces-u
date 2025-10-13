**Backend API Endpoint**
- Create `GET /transactions/nft-stats` endpoint in `server/routes/transactions.js`
- Return JSON: `{ totalNFTs: number, walletConnected: boolean }`
- Return mock data or query from database (can use simple count)
- Handle errors with appropriate status codes

**Blockchain Integration**
- Check wallet connection status in frontend using existing wallet context/hooks
- Display wallet address in truncated format (0x1234...5678) when connected

**Frontend Component**
- Create `src/components/NFTStats.js` component
- Fetch from `/transactions/nft-stats` using `src/api/Api.js` service
- Display two cards: total NFTs count, wallet connection status (green badge if connected, red if not)
- Implement loading spinner
- Use existing styling patterns from `src/scss`

**Integration**
- Add route `/dashboard/nft-stats` in `src/routes/routes.js`

**Verification**
- Cards display with correct data from API
- Wallet connection status badge shows correct color (green/red)
- Component renders correctly in dashboard layout
