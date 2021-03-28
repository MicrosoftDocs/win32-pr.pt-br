---
description: Este tópico é uma referência para as entradas que podem ser usadas em um arquivo autorun. inf. Uma entrada consiste em uma chave e um valor.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Entradas autorun. inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164319"
---
# <a name="autoruninf-entries"></a>Entradas autorun. inf

Este tópico é uma referência para as entradas que podem ser usadas em um arquivo autorun. inf. Uma entrada consiste em uma chave e um valor.

-   [\[Chaves de AutoRun \]](#autorun-keys)
    -   [action](#parameters)
    -   [CustomEvent](#customevent)
    -   [cone](#parameters)
    -   [label](#parameters)
    -   [open](#parameters)
    -   [UseAutoPlay](#parameters)
    -   [ShellExecute](#shellexecute)
    -   [Shell](#autoruninf-entries)
    -   [verbo do Shell \\](#shellverb)
-   [\[Chaves de conteúdo \]](#content-keys)
-   [\[\]Chaves ExclusiveContentPaths](#exclusivecontentpaths-keys)
-   [\[\]Chaves IgnoreContentPaths](#ignorecontentpaths-keys)
-   [\[\]Chaves DeviceInstall](#deviceinstall-keys)
    -   [DriverPath](#driverpath)

## <a name="autorun-keys"></a>\[Chaves de AutoRun \]

-   [action](#parameters)
-   [CustomEvent](#customevent)
-   [cone](#parameters)
-   [label](#parameters)
-   [open](#parameters)
-   [UseAutoPlay](#parameters)
-   [ShellExecute](#shellexecute)
-   [Shell](#autoruninf-entries)
-   [verbo do Shell \\](#shellverb)

### <a name="action"></a>ação

A entrada de **ação** especifica o texto que é usado na caixa de diálogo de reprodução automática para o manipulador que representa o programa especificado na entrada [Open](#parameters) ou [ShellExecute](#shellexecute) no arquivo autorun. inf da mídia. O valor pode ser expresso como texto ou como um recurso armazenado em um binário.


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a>Parâmetros

-   *ActionText*

    Texto usado na caixa de diálogo de reprodução automática para o manipulador que representa o programa especificado na entrada de [Open](#parameters) ou [ShellExecute](#shellexecute) no arquivo autorun. inf da mídia.

-   *FilePath*

    Uma cadeia de caracteres que contém o caminho totalmente qualificado do diretório que contém o arquivo binário que contém a cadeia de caracteres. Se nenhum caminho for especificado, o arquivo deverá estar no diretório raiz da unidade.

-   *nome do arquivo*

    Uma cadeia de caracteres que contém o nome do arquivo binário.

-   *Identificação*

    A ID da cadeia de caracteres no arquivo binário.

### <a name="remarks"></a>Comentários

A chave de **ação** só é usada no Windows XP Service Pack 2 (SP2) ou posterior. Só há suporte para unidades do tipo unidade \_ removível e unidade \_ corrigida. No caso da unidade \_ removível, a chave de **ação** é necessária. Um comando de **ação** no arquivo autorun. inf de um CD de áudio ou DVD de filme é ignorado e essas mídias continuam a se comportar como no Windows XP Service Pack 1 (SP1) e versões anteriores.

A cadeia de caracteres exibida na caixa de diálogo de reprodução automática é construída combinando o texto especificado na entrada de **ação** com o texto embutido em código que nomeia o provedor, fornecido pelo shell. O [ícone](#parameters) é exibido ao lado dele. Essa entrada sempre aparece como a primeira opção na caixa de diálogo de reprodução automática e é selecionada por padrão. Se o usuário aceitar a opção, o aplicativo especificado pela entrada [Open](#parameters) ou [ShellExecute](#shellexecute) no arquivo autorun. inf da mídia será iniciado. A opção **sempre fazer a ação selecionada** não está disponível nessa situação.

As teclas de [ação](#parameters) e [ícone](#parameters) juntas definem a representação do aplicativo que é visto pelo usuário final na caixa de diálogo de reprodução automática. Eles devem ser compostos de forma que os usuários possam identificá-los facilmente. Eles devem indicar o aplicativo a ser executado, a empresa que o criou e qualquer identidade visual associada.

Para compatibilidade com versões anteriores, a entrada de **ação** é opcional para dispositivos do tipo unidade \_ fixa. Para esse tipo, uma entrada padrão será usada na caixa de diálogo de reprodução automática se nenhuma entrada de **ação** estiver presente no arquivo autorun. inf.

A entrada de **ação** é obrigatória para dispositivos do tipo unidade \_ removível, que até agora não tinha suporte a autorun. inf. Se nenhuma entrada de **ação** estiver presente, a caixa de diálogo de reprodução automática será exibida, mas sem a opção de iniciar o conteúdo adicional.

### <a name="customevent"></a>CustomEvent

A entrada **CustomEvent** especifica um evento de conteúdo de reprodução automática personalizado.


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a>Parâmetros

-   *CustomEventName*

    Uma cadeia de texto que contém o nome do evento de conteúdo de reprodução automática. O nome não deve ter mais de 100 caracteres alfanuméricos.

### <a name="remarks"></a>Comentários

Você pode incluir um nome de evento personalizado no arquivo autorun. inf de um volume. Quando o AutoPlay solicita ao usuário que um aplicativo use com o volume, ele exibe somente os aplicativos que se registraram para o nome do evento personalizado especificado. Para obter informações sobre como você pode registrar um aplicativo como um manipulador para seu evento personalizado de conteúdo de reprodução automática, consulte [inicialização automática com reprodução](/previous-versions/windows/apps/hh452731(v=win.10)) automática ou [como registrar um manipulador de eventos](how-to-register-an-event-handler.md).

O exemplo a seguir especifica o valor "MyContentOnArrival" como um novo evento de conteúdo de reprodução automática.


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a>ícone

A entrada de **ícone** especifica um ícone que representa a unidade habilitada para autorun na interface do usuário do Windows.


```
icon=iconfilename[,index]
```



### <a name="parameters"></a>Parâmetros

-   *IconFilename*

    Nome de um arquivo. ico,. bmp,. exe ou. dll que contém as informações do ícone. Se um arquivo contiver mais de um ícone, você também deverá especificar o índice de base zero do ícone.

### <a name="remarks"></a>Comentários

O ícone, junto com o rótulo, representa a unidade habilitada para AutoRun na interface do usuário do Windows. Por exemplo, no Windows Explorer, a unidade é representada por esse ícone em vez do ícone de unidade padrão. O arquivo do ícone deve estar no mesmo diretório que o arquivo especificado pelo comando [abrir](#parameters) .

O exemplo a seguir especifica o segundo ícone no arquivo de MyProg.exe.


```
icon=MyProg.exe,1
```



### <a name="label"></a>label

A entrada de **rótulo** especifica um rótulo de texto que representa a unidade habilitada para autorun na interface do usuário do Windows.


```
label=LabelText
```



### <a name="parameters"></a>Parâmetros

-   *LabelText*

    Uma cadeia de texto que contém o rótulo. Ele pode conter espaços e não deve ter mais de 32 caracteres.

> [!Note]  
> É possível colocar um valor no parâmetro **LabelText** que exceda 32 caracteres e não receber nenhuma mensagem de erro. No entanto, o sistema só exibe os primeiros 32 caracteres. Todos os caracteres após os 32 º são truncados e não são exibidos. Por exemplo, se o **LabelText** for o seguinte: label = "este CD foi projetado para ser o CD de música final". será exibido o seguinte: "este CD foi projetado para ser o UL".

 

### <a name="remarks"></a>Comentários

O rótulo, junto com um ícone, representa a unidade habilitada para AutoRun na interface do usuário do Windows.

O exemplo a seguir especifica o valor "meu rótulo de unidade" como o rótulo da unidade.


```
label=My Drive Label
```



### <a name="open"></a>Abrir

A entrada **aberta** especifica o caminho e o nome de arquivo do aplicativo que o autorun inicia quando um usuário insere um disco na unidade.


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a>Parâmetros

-   *exefile*

    Caminho totalmente qualificado de um arquivo executável que é executado quando o CD é inserido. Se apenas um nome de arquivo for especificado, ele deverá estar no diretório raiz da unidade. Para localizar o arquivo em um subdiretório, você deve especificar um caminho. Você também pode incluir um ou mais parâmetros de linha de comando para passar para o aplicativo de inicialização.

### <a name="useautoplay"></a>UseAutoPlay

No Windows XP, a entrada **UseAutoPlay** especifica que a reprodução automática deve ser usada em vez de Autorun.

No Windows Vista e posterior, essa entrada faz com que todas as ações especificadas para AutoRun (usando as entradas **Open** ou **ShellExecute** ) sejam suprimidas da caixa de diálogo de reprodução automática. Essa entrada não tem nenhum efeito nas versões do Windows anteriores ao Windows XP.

No Windows 8 e posterior, a especificação de um valor de 0 desabilitará a reprodução automática para este dispositivo.

### <a name="parameters"></a>Parâmetros

Para usar essa opção, adicione uma entrada para **UseAutoPlay** ao arquivo autorun. inf e defina a entrada igual a 1. Nenhum outro valor tem suporte em versões do Windows anteriores ao Windows 8.

No Windows 8 e posterior, especifique um valor de 0 para desabilitar a reprodução automática para este dispositivo.


```
UseAutoPlay=1
```



### <a name="remarks"></a>Comentários

Atualmente, o **UseAutoPlay** é aplicável somente no Windows XP ou posterior e somente em uma unidade que o [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determina para ser do tipo **unidade de \_ cdrom**.

Quando **UseAutoPlay** é usado, qualquer ação especificada pelas entradas **Open** ou **ShellExecute** em Autorun. inf é ignorada no Windows XP e omitida da caixa de diálogo de reprodução automática no Windows Vista.

A execução automática normalmente é usada para executar ou carregar automaticamente algo contido na mídia inserida, enquanto a reprodução automática apresenta uma caixa de diálogo que inclui uma lista de ações relevantes que podem ser tomadas e permite que o usuário escolha a ação a ser tomada. Para obter mais informações sobre a diferença entre AutoRun e AutoPlay, consulte [criando um aplicativo de CD-ROM habilitado para autorun](autoplay.md) e [usando e configurando a reprodução automática](autoplay2k-using.md), respectivamente.

### <a name="usage-example"></a>Exemplo de uso

Um CD contém três arquivos: autorun. inf, Readme.txt e Music. WMA. Dependendo da versão do Windows em uso e das opções especificadas em Autorun. inf, o CD pode ser tratado por AutoRun ou reprodução automática quando é inserido (supondo que a execução de AutoRun/AutoPlay esteja habilitada para a unidade na qual o CD é inserido).

Primeiro, considere um arquivo autorun. inf com o conteúdo a seguir, observando que **UseAutoPlay = 1** não está especificado:


```
[AutoRun]
shellexecute="Readme.txt"
```



A ação realizada pelo shell quando este CD é inserido depende da versão do Windows em uso:

-   No Windows XP ou anterior, esse CD é tratado por AutoRun quando é inserido. Nesse caso, a entrada **ShellExecute** é lida e o Shell invoca o manipulador de arquivos associado a arquivos. txt; Normalmente, isso abriria Readme.txt no bloco de notas.
-   No Windows Vista, a presença de um arquivo autorun. inf com uma entrada **ShellExecute** faz com que a mídia seja identificada como o tipo "software and Games" de reprodução automática. Nesse caso, o usuário recebe uma caixa de diálogo de reprodução automática que inclui a ação especificada pela entrada **ShellExecute** (apresentada como "carregar Readme.txt" na caixa de diálogo), juntamente com as ações padrão associadas à mídia do tipo "software e jogos".

Para indicar que a reprodução automática deve ser usada em vez de AutoRun no Windows XP, e que a ação especificada pela entrada de ShellExecute de execução automática deve ser suprimida da caixa de diálogo de reprodução automática no Windows Vista, insira **UseAutoPlay** no arquivo autorun. inf da seguinte maneira:


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



Mais uma vez, a ação realizada pelo shell quando este CD é inserido depende da versão do Windows em uso.

-   Nas versões do Windows anteriores ao Windows XP, o AutoRun ainda é usado e a ação especificada por **ShellExecute** é executada, conforme descrito anteriormente. (Observe que apenas o AutoRun está disponível em versões do Windows anteriores ao Windows XP.)
-   No Windows XP, a entrada **UseAutoPlay** faz com que a reprodução automática seja usada no lugar do autorun. Nesse caso, a reprodução automática determina que a mídia contém um arquivo de áudio do Windows Media (. WMA) e categoriza o conteúdo como "arquivos de música". O usuário recebe uma caixa de diálogo de reprodução automática que contém manipuladores registrados para o tipo de mídia de reprodução automática "arquivos de música"; a entrada de ShellExecute de execução automática é ignorada.

### <a name="shellexecute"></a>ShellExecute

[Versão 5,0.](versions.md) A entrada **ShellExecute** especifica um aplicativo ou arquivo de dados que o autorun usará para chamar [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a>Parâmetros

-   *FilePath*

    Uma cadeia de caracteres que contém o caminho totalmente qualificado do diretório que contém os dados ou o arquivo executável. Se nenhum caminho for especificado, o arquivo deverá estar no diretório raiz da unidade.

-   *nome do arquivo*

    Uma cadeia de caracteres que contém o nome do arquivo. Se for um arquivo executável, ele será iniciado. Se for um arquivo de dados, ele deverá ser um membro de um [tipo de arquivo](fa-file-types.md). [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) inicia o comando padrão associado ao tipo de arquivo.

-   *paramx*

    Contém parâmetros adicionais que devem ser passados para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

### <a name="remarks"></a>Comentários

Essa entrada é semelhante à [aberta](#parameters), mas permite que você use informações de [Associação de arquivo](fa-intro.md) para executar o aplicativo.

### <a name="shell"></a>shell

A entrada do **shell** especifica um comando padrão para o menu de atalho da unidade.


```
shell=verb
```



### <a name="parameters"></a>Parâmetros

-   *verbo*

    O verbo que corresponde ao comando de menu. O verbo e seu comando de menu associado devem ser definidos no arquivo autorun. inf com uma entrada de [ \\ verbo de shell](#shellverb) .

### <a name="remarks"></a>Comentários

Quando um usuário clica com o botão direito do mouse no ícone da unidade, um menu de atalho é exibido. Se um arquivo autorun. inf estiver presente, o comando de menu de atalho padrão será obtido dele. Esse comando também é executado quando o usuário clica duas vezes no ícone da unidade.

Para especificar o comando de menu de atalho padrão, primeiro defina seu verbo, Cadeia de caracteres de comando e texto de menu com o [ \\ verbo do Shell](#shellverb). Em seguida, use o Shell para transformá-lo no comando de menu de atalho padrão. Caso contrário, o texto do item de menu padrão será "AutoPlay", que inicia o aplicativo especificado pela entrada [aberta](#parameters) .

### <a name="shellverb"></a>verbo do Shell \\

A entrada de **\\ verbo do Shell** adiciona um comando personalizado ao menu de atalho da unidade.


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a>Parâmetros

-   *verbo*

    O verbo do comando de menu. A entrada de *_\\ comando_* do _verbo_ do **shell \\** associa o verbo a um arquivo executável. Os verbos não devem conter espaços inseridos. Por padrão, *Verb* é o texto que é exibido no menu de atalho.

-   *Filename.exe*

    O caminho e o nome do arquivo do aplicativo que executa a ação.

-   *MenuText*

    Esse parâmetro especifica o texto que é exibido no menu de atalho. Se for omitido, *verbo* será exibido. *MenuText* pode ser com maiúsculas e minúsculas e pode conter espaços. Você pode definir uma tecla de atalho para o item de menu colocando um e comercial (&) na frente da letra.

### <a name="remarks"></a>Comentários

Quando um usuário clica com o botão direito do mouse no ícone da unidade, um menu de atalho é exibido. Adicionar entradas de **\\ verbo de shell** ao arquivo autorun. inf da unidade permite que você adicione comandos a esse menu de atalho.

Há duas partes nessa entrada, que devem estar em linhas separadas. A primeira parte é o *_\\ comando_* de _verbo_ do **shell \\**. É obrigatório. Ele associa uma cadeia de caracteres, chamada de *verbo*, com o aplicativo a ser iniciado quando o comando é executado. A segunda parte é a entrada de _verbo_ do **shell \\**. É opcional. Você pode incluí-lo para especificar o texto que é exibido no menu de atalho.

Para especificar um comando de menu de atalho padrão, defina o verbo com o **\\ verbo Shell** e torne-o o comando padrão com a entrada [shell](#autoruninf-entries) .

O fragmento autorun. inf de exemplo a seguir associa o verbo *readit* com a cadeia de caracteres de comando "Notepad ABC \\readme.txt". O texto do menu é "Read me" e ' M' ' é definido como a tecla de atalho do item. Quando o usuário seleciona esse comando, o arquivo ABCreadme.txt da unidade \\ é aberto com o bloco de notas da Microsoft.


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a>\[Chaves de conteúdo \]

Há três chaves de tipo de arquivo: **MusicFiles**, **PictureFiles** e **VideoFiles**.

Se um desses conteúdos for definido como true por meio de um dos valores 1, y, Yes, t ou true, a interface de usuário da reprodução automática exibirá os manipuladores associados a esse tipo de conteúdo, independentemente de o conteúdo desse tipo existir na mídia.

Se um desses conteúdos for definido como falso por meio de um valor de não diferenciação de maiúsculas e minúsculas 0, n, não, f ou false, a interface do usuário da reprodução automática não exibirá os manipuladores associados a esse tipo de conteúdo, mesmo que o conteúdo desse tipo seja detectado na mídia.

O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção de conteúdo à reprodução automática. Por exemplo, um CD pode ser Categorizado como contendo apenas conteúdo de música, embora também tenha imagens e vídeos e, de outra forma, seria visto como tendo conteúdo misto.

A seção de **\[ conteúdo \]** só tem suporte no Windows Vista e posterior.


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a>\[\]Chaves ExclusiveContentPaths

As pastas listadas nesta seção limitam a reprodução automática para pesquisar somente as pastas e suas subpastas de conteúdo. Eles podem ser fornecidos com ou sem uma barra invertida à esquerda ( \\ ). Em ambos os casos, eles são usados como caminhos absolutos do diretório raiz da mídia. No caso de pastas com espaços em seus nomes, não as coloque entre aspas à medida que as aspas são feitas literalmente como parte do caminho.

O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção de conteúdo à reprodução automática e reduzam o tempo de varredura limitando a verificação a determinadas áreas significativas da mídia.

A seguir estão todos os caminhos válidos


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



A seção **\[ ExclusiveContentPaths \]** só tem suporte no Windows Vista e posterior.

## <a name="ignorecontentpaths-keys"></a>\[\]Chaves IgnoreContentPaths

As pastas listadas nesta seção e suas subpastas são ignoradas pela reprodução automática durante a pesquisa de conteúdo em uma mídia. Eles podem ser fornecidos com ou sem uma barra invertida à esquerda ( \\ ). Em ambos os casos, eles são usados como caminhos absolutos do diretório raiz da mídia. No caso de pastas com espaços em seus nomes, não as coloque entre aspas à medida que as aspas são feitas literalmente como parte do caminho.

Os caminhos nesta seção têm precedência sobre caminhos na seção **\[ ExclusiveContentPaths \]** . Se um caminho fornecido em **\[ IgnoreContentPaths \]** for uma subpasta de um caminho fornecido em **\[ ExclusiveContentPaths \]**, ele ainda será ignorado.

O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção de conteúdo à reprodução automática e reduzam o tempo de varredura limitando a verificação a determinadas áreas significativas da mídia.

A seguir estão todos os caminhos válidos


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



A seção **\[ IgnoreContentPaths \]** só tem suporte no Windows Vista e posterior.

## <a name="deviceinstall-keys"></a>\[\]Chaves DeviceInstall

### <a name="driverpath"></a>DriverPath

A entrada **DriverPath** especifica um diretório a ser pesquisado recursivamente para arquivos de driver. Esse comando é usado durante uma instalação de driver e não faz parte de uma operação de AutoRun. A seção **\[ DeviceInstall \]** só tem suporte no Windows XP.


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a>Parâmetros

-   *DirectoryPath*

    Um caminho para um diretório que o Windows procura por arquivos de driver, juntamente com todos os seus subdiretórios.

### <a name="remarks"></a>Comentários

Não use letras de unidade no *DirectoryPath* , pois elas são alteradas de um computador para o outro.

Para pesquisar vários diretórios, adicione uma entrada **DriverPath** para cada diretório como neste exemplo.


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



Se nenhuma entrada **DriverPath** for fornecida na seção **\[ DeviceInstall \]** ou a entrada **DriverPath** não tiver nenhum valor, essa unidade será ignorada durante uma pesquisa de arquivos de driver.

 

 
