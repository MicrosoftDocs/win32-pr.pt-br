---
title: Formato de arquivo de tema
description: Este documento discute o formato dos arquivos de tema (. Theme). um arquivo. theme é um arquivo de texto .ini dividido em seções, que especificam elementos visuais que aparecem em uma área de trabalho Windows. Os nomes de seção são encapsulados entre colchetes (\ \) no arquivo .ini.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584e6d9785cf7660e017cadfb2a39d6bce6c2a87
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886636"
---
# <a name="theme-file-format"></a>Formato de arquivo de tema

Este documento discute o formato dos arquivos de tema (. Theme). um arquivo. theme é um arquivo de texto .ini dividido em seções, que especificam elementos visuais que aparecem em uma área de trabalho Windows. Os nomes de seção são encapsulados entre colchetes ( \[ \] ) no arquivo de .ini.

um novo formato de arquivo,. themepack, foi introduzido com Windows 7 para ajudar os usuários a compartilhar temas. os temas podem ser selecionados no painel de controle de personalização somente no Windows 7 Home Premium ou superior, ou somente no Windows Server 2008 R2 quando o componente da área de trabalho é instalado.

Os tópicos a seguir são discutidos neste artigo.

-   [Criando um arquivo de tema](#creating-a-theme-file)
-   [Descrição de um arquivo de tema](#description-of-a-theme-file)
    -   [\[Seção de tema \]](#theme-section)
    -   [\[Seção cores do painel de controle \\ \]](#control-panelcolors-section)
    -   [\[\\Seção cursores do painel de controle \]](#control-panelcursors-section)
    -   [\[\\Seção área de trabalho do painel de controle \]](#control-paneldesktop-section)
    -   [\[Seção de apresentação de slides \]](#slideshow-section)
    -   [\[Seção de métricas \]](#metrics-section)
    -   [\[Seção de estilos visuais \]](#visual-styles-section)
    -   [\[AppEvents de sons \] e \[ \] seções (sons)](#sounds-and-appevents-sections-sounds)
    -   [\[Seção de inicialização \]](#boot-section)
    -   [\[\]Seção MasterThemeSelector](#masterthemeselector-section)
-   [Exemplo de um arquivo de tema](#example-of-a-theme-file)
-   [Instalando arquivos de tema](#installing-theme-files)
-   [Pacotes de tema](#theme-packs)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-a-theme-file"></a>Criando um arquivo de tema

Um arquivo. Theme permite que você altere a aparência de determinados elementos da área de trabalho. Você pode criar ou modificar um arquivo. Theme de duas maneiras:

-   Modifique as configurações de personalização ou exibição no painel de controle e salve as configurações como um arquivo. Theme. consulte a ajuda do Windows para obter instruções.
-   Crie um arquivo. Theme manualmente para um nível maior de controle sobre os detalhes do seu tema.

Para disponibilizar seu tema para outros usuários, você deve fornecer o arquivo. theme, bem como a imagem de plano de fundo, a proteção de tela e os arquivos de ícones. Você pode fazer isso com um [pacote de temas](#theme-packs).

## <a name="description-of-a-theme-file"></a>Descrição de um arquivo de tema

Os arquivos de tema têm várias seções obrigatórias e opcionais. O exemplo a seguir descreve as seções de arquivos. Theme e fornece exemplos de como especificar alterações para os diferentes elementos.

### <a name="theme-section"></a>\[Seção de tema \]

> [!Note]  
> Esta seção é opcional. Se você não incluir esta seção no arquivo. theme, o sistema usará as configurações padrão.

 

A \[ \] seção tema identifica o nome do seu tema personalizado e especifica o logotipo da marca do tema e os ícones da área de trabalho.

A primeira parte da \[ seção Theme \] contém os dois elementos a seguir:



| Elemento                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName = nome<br/> ou<br/> DisplayName = @module ,-stringid<br/> exemplo: DisplayName = @themeui.dll ,-2013 | DisplayName é o nome do tema que aparecerá no painel de controle de personalização. Pode ser uma cadeia de caracteres ou uma referência a um nome localizado.<br/> Esse campo é opcional. Se ele estiver ausente, o nome de arquivo do tema será usado como tema.<br/>                                                                                                                                                                                                                                         |
| BrandImage = caminho para a imagem<br/> exemplo: BrandImage = c: \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 e posterior** BrandImage especifica o caminho para um arquivo gráfico com marca que é incorporado na visualização do tema no painel de controle de personalização.<br/> O ícone gráfico deve ser um arquivo PNG. O gráfico é dimensionado para 80x240 pixels, portanto, é recomendável que você forneça uma imagem desse tamanho. A Galeria de temas respeita as regiões transparentes de seu ícone de marca.<br/> Esse campo é opcional. Se estiver ausente, nenhum logotipo será exibido como o ícone de tema.<br/> |



 

O restante da \[ seção tema \] especifica ícones personalizados para recursos de área de trabalho, como computador, meus documentos, rede e lixeira. Se você não especificar ícones personalizados da área de trabalho, a área de trabalho exibirá os ícones padrão da área de trabalho do sistema.

Veja a seguir dois exemplos de como um arquivo. Theme define o ícone do **computador** .


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



estes são os valores para os ícones de área de trabalho padrão no Windows 7.


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a>\[Seção cores do painel de controle \\ \]

> [!Note]  
> Esta seção é opcional. Se você não incluir esta seção no arquivo. theme, o sistema usará as configurações padrão. Se seu tema usa o estilo visual Aero, você deve evitar substituir os valores padrão nesta seção.

 

A cor dos elementos, como barras de rolagem, texto e botões, é personalizável. O arquivo. Theme especifica os valores RGB a serem alterados para esses elementos. os valores substituem os valores padrão do estilo visual e são usados quando seu tema se baseia nos temas Windows clássico, Windows 7 Basic ou Alto Contraste.

Veja a seguir um exemplo de como as cores são definidas.


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a>\[\\Seção cursores do painel de controle \]

> [!Note]  
> Esta seção é opcional. Se você não incluir esta seção no arquivo. theme, o sistema usará cursores padrão.

 

Um tema também pode alterar a aparência dos cursores. para fazer isso, você cria arquivos. cur para substituir os cursores de Windows padrão. O exemplo a seguir é de um arquivo. Theme que define os cursores de um tema chamado *esportes*.


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a>\[\\Seção área de trabalho do painel de controle \]

> [!Note]  
> Esta seção é necessária. Se você não incluir esta seção no arquivo. theme, o sistema ignorará o tema e não exibirá o tema no painel de controle.

 

Você pode criar um plano de fundo personalizado da área de trabalho e especificar um caminho para o arquivo de imagem. O exemplo a seguir mostra como modificar a aparência da área de trabalho.


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a>\[Seção de apresentação de slides \]

**Windows 7 e posterior.**

> [!Note]  
> Esta seção é opcional. Se você não incluir esta seção no arquivo. theme, o sistema usará a imagem de plano de fundo da área de trabalho especificada na \[ seção área de trabalho do painel de controle \\ \] . Se você incluir esta seção, deverá especificar as configurações de apresentação de slides aqui.

 

O plano de fundo de seu tema pode ser uma apresentação de slides de imagens armazenadas localmente ou de imagens servidas por um RSS feed. A \[ \] seção de apresentação de slides do arquivo contém os seguintes atributos:




| Atributo | Descrição | 
|-----------|-------------|
| Intervalo = número de milissegundos | Obrigatório. Interval é um número que determina com que frequência o plano de fundo é alterado. É medido em milissegundos. | 
| Ordem aleatória = 0 ou 1 | Obrigatório. Ordem aleatória identifica se a ordem aleatória do plano de fundo.<br /> 0 = Desabilitado<br /> 1 = Habilitado<br /> | 
| RSSFeed=URL para RSS feed | Necessário se ImagesRootPath não for especificado. RSSFeed especifica um RSS feed a ser usado como a apresentação de slides em segundo plano. Para que o feed funcione, você precisa referenciar imagens de alta resolução aderindo ao padrão de "compartimentos" usado pelo <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS Platform</a>. Devido a essa limitação, os arquivos .theme que incluem um RSS feed devem ser criados manualmente. <br /><blockquote>[!Note]<br />Não é possível especificar um RSSFeed e ImagesRootPath.</blockquote><br /><br /> | 
| ImagesRootPath=path to image folder | Necessário se RSSFeed não for especificado. ImagesRootPath especifica um caminho para um conjunto de imagens que você deseja usar como a apresentação de slides em segundo plano. As imagens em subpastas não estão incluídas na apresentação de slides.<br /> ImagesRootPath dá suporte a substituições de Variável de Ambiente no caminho.<br /><blockquote>[!Note]<br />Não é possível especificar um RSSFeed e ImagesRootPath.</blockquote><br /><br /> | 
| Item<em>N</em>Path=path(s) para imagens específicas | Para uso com ImagesRootPath. <br /> O<em>Caminho N</em>do Item especifica caminhos para imagens específicas, para que você possa limitar a apresentação de slides a imagens específicas em vez de todas as imagens em uma pasta. Se nenhum caminho for especificado, todas as imagens no caminho ImagesRootPath serão usadas na apresentação de slides, incluindo imagens adicionadas depois de criar e instalar o tema.<br /> O<em>Caminho N</em>do Item dá suporte a substituições de Variável de Ambiente no caminho. <em>N</em> é 0, 1, 2 e assim por diante. <br /> | 




 

Os exemplos a seguir mostram como um arquivo .theme especifica a apresentação de slides para incluir um conjunto de imagens armazenadas localmente.


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



O exemplo a seguir é um modelo para um arquivo .theme que cria uma apresentação de slides da tela de fundo da área de trabalho usando imagens de um RSS feed. Siga estas etapas para personalizar o modelo:

1.  Copie o exemplo a seguir e copie-o em um editor de texto.
2.  Substitua {themename} pelo nome que você deseja que apareça na galeria de Painel de Controle de personalização.
3.  Substitua {rssfeedurl} pelo caminho completo para um RSS feed.
4.  Salve as alterações como um arquivo com a extensão ".theme".


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a>\[Seção \] Métricas

> [!Note]  
> Esta seção é opcional. Se você não incluir esta seção no arquivo .theme, o sistema usará as configurações de estilo visual padrão.

 

Você pode especificar métricas do sistema em um arquivo .theme. As métricas do sistema são as dimensões de vários elementos de exibição, como a largura da borda da janela, a altura do ícone ou a largura da barra de rolagem. Os valores NonclientMetrics e IconMetrics são estruturas binárias definidas por NONCLIENTMETRICS e ICONMETRICS em winuser.h. Veja a seguir um exemplo de como alterar as métricas do sistema.


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a>\[Seção Estilos \] Visuais

> [!Note]  
> Esta seção é necessária. Se você não incluir esta seção no arquivo .theme, o sistema ignorará o Tema e não exibirá o Tema Painel de Controle.

 

Você pode fornecer informações específicas sobre o tamanho e a cor dos elementos da área de trabalho em arquivos .msstyles. As seções de cor e tamanho dos arquivos .theme podem ser substituídas por arquivos .msstyles que permitem modificar elementos da área de trabalho mais detalhadamente. Esses arquivos são especificados na seção estilos visuais de um arquivo .theme. A seguir está um exemplo de uma seção de estilos visuais.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



Adicionar um elemento Path a um arquivo .msstyles é opcional. Se você fornecer um caminho, deverá remover as seções de métricas e cores do arquivo .theme. Quando essas seções são removidas, as cores, as fontes e os tamanhos de um tema vêm do arquivo .msstyles e corresponderem à intenção do autor .msstyles. A falha na remoção das seções de métrica e cor pode fazer com que Windows ou aplicativos tenham problemas de desenho.

**Windows Vista/Windows 7:** Quando o caminho aponta para Aero.msstyles, você pode especificar a Cor de Vidro desejada, conforme mostrado no exemplo a seguir.

**Windows 7:** Quando o caminho aponta para Aero.msstyles, você também pode especificar o valor de Transparência desejado, conforme mostrado no exemplo a seguir.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Se os valores ColorizationColor e Transparency corresponderem exatamente a uma cor do sistema, o Painel de Controle personalização exibirá o nome do sistema para a cor. Caso contrário, a cor será rotulada como "Personalizado".

O exemplo a seguir mostra uma seção VisualStyles para o Windows 7 Basic.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



O exemplo a seguir mostra uma seção VisualStyles para o Windows clássico.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



O exemplo a seguir mostra uma seção VisualStyles para um Alto Contraste preto.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[Seções \] \[ Sons e AppEvents \] (Sons)

> [!Note]  
> Esta seção é opcional. Se você não incluir esta seção no arquivo .theme, o sistema usará as configurações de som padrão.

 

O usuário pode selecionar o **ícone som** no Painel de Controle para associar sons a eventos que ocorrem em aplicativos. Por exemplo, um arquivo .wav pode ser reproduzir quando um aplicativo é aberto. Um arquivo .theme pode especificar arquivos .wav para substituir os padrão. O exemplo a seguir mostra como fazer isso.


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



**Windows 7 e posterior:** Um nome de esquema de som pode ser especificado em vez de listar cada som separadamente.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



O valor SchemeName especifica o nome do esquema de som ou o nome do esquema de som localizado, conforme mostrado no exemplo acima.

### <a name="boot-section"></a>\[Seção \] inicialização

> [!Note]  
> **Os Protetores de Tela foram preterido na Atualização de Windows 10 de Aniversário e além.**

 

> [!Note]  
> Esta seção é opcional. Se você não incluir esta seção no arquivo .theme, nenhuma economia de tela será usada.

 

No arquivo .theme, você pode especificar a economia de tela para Windows usar. O exemplo a seguir mostra a isso.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[Seção MasterThemeSelector \]

> [!Note]  
> Esta seção é necessária. Se você não incluir esta seção no arquivo .theme, o sistema ignorará o Tema e não exibirá o Tema Painel de Controle.

 

A seção do seletor de tema mestre do arquivo .theme sempre deve ser incluída como uma marca que indica que o arquivo é válido. Você não tem uma opção de valores para esse parâmetro. O exemplo a seguir mostra isso.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Exemplo de um arquivo de tema

O exemplo a seguir mostra um arquivo .theme completo.


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a>Instalando arquivos de tema

Quando Windows inicializado, o sistema operacional enumera os subdireários de primeiro nível de %WinDir% Recursos para identificar \\ \\ os temas disponíveis. Os arquivos de tema padrão do sistema estão localizados em %WinDir% \\ Temas \\ de Recursos. Os arquivos de tema do usuário são armazenados em %WinDir% nome de usuário usuários \\ \\ &lt; &gt; \\ AppData \\ Local Microsoft Windows \\ \\ \\ Temas.

Um arquivo .theme tem associações de arquivo; portanto, os aplicativos instalador de tema podem chamar [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) em um arquivo .theme para abrir a janela **Personalização** no Painel de Controle para o tema especificado.

## <a name="theme-packs"></a>Pacotes de tema

**Windows 7 e posterior.** Um pacote de tema é um .cab que contém não apenas o arquivo .theme, mas também os arquivos necessários para implementar o tema em outro computador, como arquivos de som e imagens. Os usuários podem criar pacotes de tema por meio do Painel de Controle.

Os tipos de arquivo com suporte incluem o seguinte:



| Tipo de arquivo    | Extensão                           |
|--------------|-------------------------------------|
| Tema        | .theme                              |
| Imagem        | .jpg, .jpeg, .bmp, .dib, .tif, .png |
| Som        | .wav                                |
| Cursor do mouse | .cur, .ani                          |
| Ícone da área de trabalho | .ico                                |
| Logotipo da marca   | .png                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos estilos visuais](visual-styles-overview.md)
</dt> </dl>

