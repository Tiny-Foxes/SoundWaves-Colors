# SoundWaves-Colors

Community made color schemes for SoundWaves.

## Installing

1. Enter the color sheme you want to grab
![](https://media.discordapp.net/attachments/688182781263609868/757342498736570478/unknown.png)

2. Enter Modules and then Option.Prefs
![](https://cdn.discordapp.com/attachments/688182781263609868/757343016548827167/unknown.png)

3. Copy SoundwavesSubTheme
![](https://cdn.discordapp.com/attachments/688182781263609868/757343295788679198/unknown.png)

4. Go to your actual SoundWaves theme folder, enter Modules, open Options.Prefs and replace the SoundwavesSubTheme that's in this file with the one you copied
![](https://cdn.discordapp.com/attachments/688182781263609868/757344049957961808/unknown.png)

5. Go back to the folder of the color scheme you want to install and open Theme.Colors
![](https://cdn.discordapp.com/attachments/688182781263609868/757344342481567814/unknown.png)

6. Copy everything **that is inside** the ``Items`` variable
![](https://cdn.discordapp.com/attachments/688182781263609868/757344572216049666/unknown.png)

7. Repeat step 4 but open Theme.Colors instead of Option.Prefs, place what you copied right after the last color scheme
![](https://cdn.discordapp.com/attachments/688182781263609868/757346338345320458/unknown.png)

8. Select the installed color scheme in Options > User Experience > Appearance Options
![](https://cdn.discordapp.com/attachments/688182781263609868/757346956891652177/2020-09-20_180602.jpg)


## Installing more than one color scheme

Each table in Theme.Colors counts as a number, starting at 1.

```Lua
return {
	SoundwavesSubTheme =
	{
		Default = 1,
		Choices = { OptionNameString('swClassic'), OptionNameString('swVaporwave'), OptionNameString('swGrass'), OptionNameString('swRetro'), OptionNameString('swFire')},
		Values = {1,2,3,4,5}
	},
}
```

Notice that Classic is the first index of the ``Choices`` table, if you look at Theme.Colors, Classic is also the first table inside the ``Items`` variable. So it's recommended that you always install new color schemes after the last color scheme so you just need to add the name of the color sheme and a number in the ``Values`` table.

```Lua
return {
	SoundwavesSubTheme =
	{
		Default = 1,
		Choices = { OptionNameString('swClassic'), OptionNameString('swVaporwave'), OptionNameString('swGrass'), OptionNameString('swRetro'), OptionNameString('swFire'), 'Discord'},
		Values = {1,2,3,4,5,6}
	},
}
```

Here I installed the Discord color scheme, the only thing I would need to do now is add the color scheme table in ``Theme.Colors`` as the 6°th table inside the ``Items`` variable.