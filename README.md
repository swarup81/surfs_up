# surfs_up
June_results = session.query(Measurement.date, Measurement.prcp).\
     filter(extract('month', Measurement.date)==6).all()
     
june_temps_list = [temp.prcp for temp in June_results]
june_temps_list

june_df = pd.DataFrame(june_temps_list,columns=[ "June prcp"])

june_df.describe()

Dec_results = session.query(Measurement.date, Measurement.prcp).\
    filter(extract('month', Measurement.date)==12).all()
    
dec_temps_list = [temp.prcp for temp in Dec_results]
dec_temps_list

dec_df = pd.DataFrame(dec_temps_list, columns=[ "Dec prcp"])

dec_df.describe()

june_stats = june_df.describe()
dec_stats = dec_df.describe()

<img width="636" alt="Screen Shot 2022-04-28 at 10 54 05 AM" src="https://user-images.githubusercontent.com/100738688/165781829-d07388d3-9dc0-4d21-a531-950f73623775.png">


