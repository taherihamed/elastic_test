PUT my-index/_create/1
{
    "mapping": 
    {
        "properties": 
        {
            "name":
            {
                "type": "keyword"
            },
            "family":
            {
                "type": "keyword"
            },
            "date":
            {
                "type": "date"
            },
            "age":
            {
                "type": "short"
            },
            "educational background": 
            {
                "type": "nested",
                "properties": 
                {
                    "degree level":
                    {
                        "type": "keyword"
                    },
                    "univercity":
                    {
                        "type": "keyword"
                    },
                    "thesis":
                    {
                        "type": "nested",
                        "properties": 
                        {
                            "title":
                            {
                                "type": "keyword"
                            },
                            "grade":
                            {
                                "type": "short"
                            }
                        }
                    },
                    "address":
                    {
                        "type": "nested",
                        "properties":
                        {
                            "state":
                            {
                                "type": "keyword"
                            },
                            "city":
                            {
                                "type": "keyword"
                            },
                            "details":
                            {
                                "type": "text"
                            }
                        }
                    }
                }

            }
        }
      
    }
}