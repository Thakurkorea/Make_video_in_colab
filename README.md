# Make_video_in_colab
figs=[]     # latter this figs will be used without saving .png file

for i in range(184):
  fig, ax = plt.subplots(nrows=1, ncols=1, figsize=(10, 8))
  sc=ax.scatter(df['x'],df['y'], c=df[f'{i+1}'],s=20, cmap='RdYlGn',vmin=0.1, vmax=0.5)
  cbar = fig.colorbar(sc, ax=ax,ticks=v)
  cbar.set_label('NDVI')
  ax.set_xlabel('Longitude ')
  ax.set_ylabel('Latitude')
  ax.set_title(file_name)
  ax.legend([f'Time-{i+1}'],markerscale=0,frameon=False,loc="upper right")
