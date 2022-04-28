# surfs_up
June_results = session.query(Measurement.date, Measurement.prcp).\
    filter(extract('month', Measurement.date)==6).all()
june_df = pd.DataFrame(June_results,columns=[ "date","June prcp"])
june_df.describe()
Dec_results = session.query(Measurement.date, Measurement.prcp).\
    filter(extract('month', Measurement.date)==12).all()
dec_df = pd.DataFrame(Dec_results, columns=[ "date","Dec prcp"])
dec_df.describe()

<img width="610" alt="Screen Shot 2022-04-28 at 10 40 55 AM" src="https://user-images.githubusercontent.com/100738688/165778426-fd74fa92-b01b-40c2-a9d4-6970be922f56.png">

