
   find(collection, data) {
      if(!collection){return {err:'collection required!'}}
      if(!data){return {err:'conditions required!'}}
      let db = fs.readFileSync(`${filePath}/${collection}.json`, 'utf8')
      db = JSON.parse(db)
      return db.filter(item => {
         return data.every(data => {
            const [key, value] = data
            return item[key] === value
         })
      })
   }
