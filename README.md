# auro-digital-test
dic = {}

pq = []

for i in range(len(root)):
  x = root[i].attrib
  if x['book'] not in dic:
    dic['book'] = len(pq_arr)
    pq_arr.append([[]])

  if x['operation'] == 'SELL':
    heapq.heappush(pq_arr[dic[x['book']]][0], x['price'])
