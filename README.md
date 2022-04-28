# surfs_up
June_results = session.query(Measurement.date, Measurement.prcp).\
    filter(extract('month', Measurement.date)==6).all()
june_df = pd.DataFrame(June_results,columns=[ "date","June prcp"])
june_df.describe()
Dec_results = session.query(Measurement.date, Measurement.prcp).\
    filter(extract('month', Measurement.date)==12).all()
dec_df = pd.DataFrame(Dec_results, columns=[ "date","Dec prcp"])
dec_df.describe()
summary_df = june_df.merge(dec_df, left_index=True, right_index=True)
summary_df

<img width="590" alt="Screen Shot 2022-04-28 at 10 38 45 AM" src="https://user-images.githubusercontent.com/100738688/165777884-09267bb4-a913-4dce-967f-2d9db0e3385b.png">

