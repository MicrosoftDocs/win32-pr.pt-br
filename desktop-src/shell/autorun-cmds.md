---
description: Este tópico é uma referência para as entradas que podem ser usadas em um arquivo Autorun.inf. Uma entrada consiste em uma chave e um valor.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Entradas Autorun.inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221e0a99e6352b5cfe50f3c3c0c2939933ff6c6f862e1a03b54127968b9c1838
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937156"
---
# <a name="autoruninf-entries"></a>Entradas Autorun.inf

Este tópico é uma referência para as entradas que podem ser usadas em um arquivo Autorun.inf. Uma entrada consiste em uma chave e um valor.

-   [\[Chaves \] de AutoRun](#autorun-keys)
    -   [action](#parameters)
    -   [CustomEvent](#customevent)
    -   [ícone](#parameters)
    -   [label](#parameters)
    -   [open](#parameters)
    -   [UseAutoPlay](#parameters)
    -   [Shellexecute](#shellexecute)
    -   [Shell](#autoruninf-entries)
    -   [verbo \\ shell](#shellverb)
-   [\[Chaves de \] conteúdo](#content-keys)
-   [\[Chaves ExclusiveContentPaths \]](#exclusivecontentpaths-keys)
-   [\[Chaves IgnoreContentPaths \]](#ignorecontentpaths-keys)
-   [\[Chaves de Instalação do \] Dispositivo](#deviceinstall-keys)
    -   [DriverPath](#driverpath)

## <a name="autorun-keys"></a>\[Chaves \] de AutoRun

-   [action](#parameters)
-   [CustomEvent](#customevent)
-   [ícone](#parameters)
-   [label](#parameters)
-   [open](#parameters)
-   [UseAutoPlay](#parameters)
-   [Shellexecute](#shellexecute)
-   [Shell](#autoruninf-entries)
-   [verbo \\ shell](#shellverb)

### <a name="action"></a>ação

A **entrada** de ação especifica o texto usado na caixa de diálogo Reprodução Automática para o manipulador que representa o programa especificado na entrada [open](#parameters) ou [shellexecute](#shellexecute) no arquivo Autorun.inf da mídia. O valor pode ser expresso como texto ou como um recurso armazenado em um binário.


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a>Parâmetros

-   *ActionText*

    Texto usado na caixa de diálogo Reprodução automática para o manipulador que representa o programa especificado na entrada [open](#parameters) ou [shellexecute](#shellexecute) no arquivo Autorun.inf da mídia.

-   *Filepath*

    Uma cadeia de caracteres que contém o caminho totalmente qualificado do diretório que contém o arquivo binário que contém a cadeia de caracteres. Se nenhum caminho for especificado, o arquivo deverá estar no diretório raiz da unidade.

-   *Filename*

    Uma cadeia de caracteres que contém o nome do arquivo binário.

-   *Resourceid*

    A ID da cadeia de caracteres dentro do arquivo binário.

### <a name="remarks"></a>Comentários

A **chave** de ação só é usada no Windows XP Service Pack 2 (SP2) ou posterior. Só há suporte para unidades do tipo UNIDADE \_ REMOVÍVEL e UNIDADE \_ FIXA. No caso de UNIDADE \_ REMOVÍVEL, a **chave de** ação é necessária. Um  comando de ação no arquivo Autorun.inf de um CD de áudio ou DVD de filme é ignorado e essas mídias continuam se comportando como no WINDOWS XP Service Pack 1 (SP1) e anteriores.

A cadeia de caracteres exibida na caixa de diálogo Reprodução  Automática é construída combinando o texto especificado na entrada de ação com texto codificado nomeando o provedor, fornecido pelo Shell. O [ícone](#parameters) é exibido ao lado dele. Essa entrada sempre aparece como a primeira opção na caixa de diálogo Reprodução Automática e é selecionada por padrão. Se o usuário aceitar a opção , o aplicativo especificado pela entrada [open](#parameters) ou [shellexecute](#shellexecute) no arquivo Autorun.inf da mídia será lançado. A **opção Sempre fazer a ação** selecionada não está disponível nessa situação.

As [teclas](#parameters) [de ação e](#parameters) ícone definem a representação do aplicativo que é vista pelo usuário final na caixa de diálogo Reprodução automática. Eles devem ser compostos de forma que os usuários possam identificá-los facilmente. Eles devem indicar o aplicativo a ser executado, a empresa que o criou e qualquer identidade visual associada.

Para compatibilidade com backward, **a entrada de** ação é opcional para dispositivos do tipo DRIVE \_ FIXED. Para esse tipo, uma entrada padrão será usada  na caixa de diálogo Reprodução Automática se nenhuma entrada de ação estiver presente no arquivo Autorun.inf.

A **entrada** de ação é obrigatória para dispositivos do tipo DRIVE REMOVABLE, que até agora não tinha suporte para \_ Autorun.inf. Se nenhuma **entrada** de ação estiver presente, a caixa de diálogo Reprodução Automática será exibida, mas sem nenhuma opção para iniciar o conteúdo adicional.

### <a name="customevent"></a>CustomEvent

A **entrada CustomEvent** especifica um evento de conteúdo autoPlay personalizado.


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a>Parâmetros

-   *CustomEventName*

    Uma cadeia de caracteres de texto que contém o nome do evento de conteúdo de Reprodução Automática. O nome não deve ter mais de 100 caracteres alfanuméricos.

### <a name="remarks"></a>Comentários

Você pode incluir um nome de evento personalizado no arquivo Autorun.inf de um volume. Quando o AutoPlay solicita que o usuário use um aplicativo com o volume, ele exibe apenas os aplicativos que se registraram para o nome do evento personalizado especificado. Para obter informações sobre como você pode registrar um aplicativo como [](/previous-versions/windows/apps/hh452731(v=win.10)) um manipulador para seu evento de conteúdo autoPlay personalizado, consulte Iniciando automaticamente com a Reprodução Automática ou Como registrar [um manipulador de eventos](how-to-register-an-event-handler.md).

O exemplo a seguir especifica o valor "MyContentOnArrival" como um novo evento de conteúdo de Reprodução Automática.


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a>ícone

A **entrada** de ícone especifica um ícone que representa a unidade habilitada para AutoRun na Windows do usuário.


```
icon=iconfilename[,index]
```



### <a name="parameters"></a>Parâmetros

-   *iconfilename*

    Nome de um arquivo .ico, .bmp, .exe ou .dll que contém as informações do ícone. Se um arquivo contiver mais de um ícone, você também deverá especificar o índice baseado em zero do ícone.

### <a name="remarks"></a>Comentários

O ícone, junto com o rótulo, representa a unidade habilitada para AutoRun na interface Windows usuário. Por exemplo, no Windows Explorer, a unidade é representada por esse ícone em vez do ícone de unidade padrão. O arquivo do ícone deve estar no mesmo diretório que o arquivo especificado pelo [comando](#parameters) open.

O exemplo a seguir especifica o segundo ícone no arquivo MyProg.exe dados.


```
icon=MyProg.exe,1
```



### <a name="label"></a>label

A **entrada** de rótulo especifica um rótulo de texto que representa a unidade habilitada para AutoRun na Windows do usuário.


```
label=LabelText
```



### <a name="parameters"></a>Parâmetros

-   *Labeltext*

    Uma cadeia de caracteres de texto que contém o rótulo. Ele pode conter espaços e não deve ter mais de 32 caracteres.

> [!Note]  
> É possível colocar um valor no parâmetro **LabelText** que excede 32 caracteres e não recebe nenhuma mensagem de erro. No entanto, o sistema exibe apenas os primeiros 32 caracteres. Todos os caracteres após o 32º são truncados e não são exibidos. Por exemplo, se **LabelText** for o seguinte: label="Este CD foi projetado para ser o CD de música final". o seguinte será exibido, "Este CD foi projetado para ser o ul".

 

### <a name="remarks"></a>Comentários

O rótulo, junto com um ícone, representa a unidade habilitada para AutoRun na Windows do usuário.

O exemplo a seguir especifica o valor "My Drive Label" como o rótulo da unidade.


```
label=My Drive Label
```



### <a name="open"></a>Abrir

A **entrada** aberta especifica o caminho e o nome do arquivo do aplicativo que a AutoRun inicia quando um usuário insere um disco na unidade.


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a>Parâmetros

-   *exefile*

    Caminho totalmente qualificado de um arquivo executável que é executado quando o CD é inserido. Se apenas um nome de arquivo for especificado, ele deverá estar no diretório raiz da unidade. Para localizar o arquivo em um subdiretório, você deve especificar um caminho. Você também pode incluir um ou mais parâmetros de linha de comando para passar para o aplicativo de inicialização.

### <a name="useautoplay"></a>UseAutoPlay

no Windows XP, a entrada **UseAutoPlay** especifica que a reprodução automática deve ser usada em vez de AutoRun.

no Windows Vista e posterior, essa entrada faz com que todas as ações especificadas para AutoRun (usando as entradas **open** ou **shellexecute** ) sejam suprimidas da caixa de diálogo de reprodução automática. essa entrada não tem nenhum efeito nas versões do Windows anteriores ao Windows XP.

no Windows 8 e posterior, a especificação de um valor de 0 desabilitará a reprodução automática para este dispositivo.

### <a name="parameters"></a>Parâmetros

Para usar essa opção, adicione uma entrada para **UseAutoPlay** ao arquivo autorun. inf e defina a entrada igual a 1. não há suporte para nenhum outro valor em versões do Windows anteriores a Windows 8.

em Windows 8 e posterior, especifique um valor de 0 para desabilitar a reprodução automática para este dispositivo.


```
UseAutoPlay=1
```



### <a name="remarks"></a>Comentários

atualmente, **UseAutoPlay** é aplicável somente no Windows XP ou posterior e somente em uma unidade que [**getdrivetype**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determina para ser do tipo **unidade \_ CDROM**.

quando **UseAutoPlay** é usado, qualquer ação especificada pelas entradas **open** ou **shellexecute** em Autorun. inf é ignorada no Windows XP e omitida da caixa de diálogo de reprodução automática no Windows Vista.

A execução automática normalmente é usada para executar ou carregar automaticamente algo contido na mídia inserida, enquanto a reprodução automática apresenta uma caixa de diálogo que inclui uma lista de ações relevantes que podem ser tomadas e permite que o usuário escolha a ação a ser tomada. Para obter mais informações sobre a diferença entre AutoRun e AutoPlay, consulte [criando um aplicativo de CD-ROM habilitado para autorun](autoplay.md) e [usando e configurando a reprodução automática](autoplay2k-using.md), respectivamente.

### <a name="usage-example"></a>Exemplo de uso

Um CD contém três arquivos: autorun. inf, Readme.txt e Music. WMA. dependendo da versão do Windows em uso e das opções especificadas em autorun. inf, o CD pode ser tratado por Autorun ou reprodução automática quando for inserido (supondo que a execução de autorun/autoplay esteja habilitada para a unidade na qual o CD está inserido).

Primeiro, considere um arquivo autorun. inf com o conteúdo a seguir, observando que **UseAutoPlay = 1** não está especificado:


```
[AutoRun]
shellexecute="Readme.txt"
```



a ação realizada pelo Shell quando este CD é inserido depende da versão do Windows em uso:

-   no Windows XP ou anterior, esse CD é tratado por AutoRun quando é inserido. Nesse caso, a entrada **ShellExecute** é lida e o Shell invoca o manipulador de arquivos associado a .txt arquivos; normalmente, isso abriria Readme.txt em Bloco de notas.
-   no Windows Vista, a presença de um arquivo Autorun. inf com uma entrada **shellexecute** faz com que a mídia seja identificada como o tipo "Software and games" de reprodução automática. Nesse caso, o usuário recebe uma caixa de diálogo de reprodução automática que inclui a ação especificada pela entrada **ShellExecute** (apresentada como "carregar Readme.txt" na caixa de diálogo), juntamente com as ações padrão associadas à mídia do tipo "software e jogos".

para indicar que a reprodução automática deve ser usada em vez de AutoRun no Windows XP, e que a ação especificada pela entrada de shellexecute de execução automática deve ser suprimida da caixa de diálogo de reprodução automática no Windows Vista, insira **UseAutoPlay** no arquivo autorun. inf da seguinte maneira:


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



mais uma vez, a ação realizada pelo Shell quando este CD é inserido depende da versão do Windows em uso.

-   nas versões do Windows anteriores ao Windows XP, o AutoRun ainda é usado e a ação especificada por **shellexecute** é executada, conforme descrito anteriormente. (observe que somente o AutoRun está disponível em versões do Windows anteriores ao Windows XP.)
-   no Windows XP, a entrada **UseAutoPlay** faz com que a reprodução automática seja usada no lugar do AutoRun. nesse caso, a reprodução automática determina que a mídia contém um arquivo de áudio de mídia Windows (. wma) e categoriza o conteúdo como "arquivos de música". O usuário recebe uma caixa de diálogo de reprodução automática que contém manipuladores registrados para o tipo de mídia de reprodução automática "arquivos de música"; a entrada de ShellExecute de execução automática é ignorada.

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

o fragmento Autorun. inf de exemplo a seguir associa o verbo *readit* com a cadeia de caracteres de comando "Bloco de notas abc \\readme.txt". O texto do menu é "Read me" e ' M' ' é definido como a tecla de atalho do item. quando o usuário seleciona esse comando, o arquivo abcreadme.txt da unidade \\ é aberto com o Microsoft Bloco de notas.


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a>\[Chaves de conteúdo \]

Há três chaves de tipo de arquivo: **MusicFiles**, **PictureFiles** e **VideoFiles**.

Se um desses conteúdos for definido como true por meio de um dos valores 1, y, Yes, t ou true, a interface de usuário da reprodução automática exibirá os manipuladores associados a esse tipo de conteúdo, independentemente de o conteúdo desse tipo existir na mídia.

Se um desses conteúdos for definido como falso por meio de um valor de não diferenciação de maiúsculas e minúsculas 0, n, não, f ou false, a interface do usuário da reprodução automática não exibirá os manipuladores associados a esse tipo de conteúdo, mesmo que o conteúdo desse tipo seja detectado na mídia.

O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção de conteúdo à reprodução automática. Por exemplo, um CD pode ser Categorizado como contendo apenas conteúdo de música, embora também tenha imagens e vídeos e, de outra forma, seria visto como tendo conteúdo misto.

a seção de **\[ conteúdo \]** só tem suporte no Windows Vista e versões posteriores.


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a>\[Chaves ExclusiveContentPaths \]

As pastas listadas nesta seção limitam a reprodução automática para pesquisar apenas essas pastas e suas subpastas quanto ao conteúdo. Eles podem ser dados com ou sem uma faixa invertida à frente ( \\ ). Em ambos os casos, eles são feitos como caminhos absolutos do diretório raiz da mídia. No caso de pastas com espaços em seus nomes, não coloque-os entre aspas, pois as aspas são tiradas literalmente como parte do caminho.

O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção do conteúdo para Reprodução Automática e reduzam o tempo de verificação limitando a verificação a determinadas áreas significativas da mídia.

A seguir estão todos os caminhos válidos


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



A **\[ seção ExclusiveContentPaths \]** só tem suporte no Windows Vista e posterior.

## <a name="ignorecontentpaths-keys"></a>\[Chaves IgnoreContentPaths \]

As pastas listadas nesta seção e suas subpastas são ignoradas pela reprodução automática ao pesquisar conteúdo em uma mídia. Eles podem ser dados com ou sem uma faixa invertida à frente ( \\ ). Em ambos os casos, eles são feitos como caminhos absolutos do diretório raiz da mídia. No caso de pastas com espaços em seus nomes, não coloque-os entre aspas, pois as aspas são tiradas literalmente como parte do caminho.

Os caminhos nesta seção têm precedência sobre caminhos na **\[ seção ExclusiveContentPaths. \]** Se um caminho determinado em **\[ IgnoreContentPaths \]** for uma subpasta de um caminho determinado em **\[ ExclusiveContentPaths, \]** ele ainda será ignorado.

O uso desta seção destina-se a permitir que os autores de conteúdo comuniquem a intenção do conteúdo para Reprodução Automática e reduzam o tempo de verificação limitando a verificação a determinadas áreas significativas da mídia.

A seguir estão todos os caminhos válidos


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



A **\[ seção IgnoreContentPaths \]** só tem suporte no Windows Vista e posterior.

## <a name="deviceinstall-keys"></a>\[Chaves de Instalação do \] Dispositivo

### <a name="driverpath"></a>DriverPath

A **entrada DriverPath** especifica um diretório para pesquisar recursivamente arquivos de driver. Esse comando é usado durante uma instalação do driver e não faz parte de uma operação de AutoRun. A **\[ seção \] DeviceInstall** só tem suporte no Windows XP.


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a>Parâmetros

-   *Directorypath*

    Um caminho para um diretório que Windows pesquisa arquivos de driver, juntamente com todos os seus subdireários.

### <a name="remarks"></a>Comentários

Não use letras de unidade no *caminho do* diretório, pois elas mudam de um computador para o outro.

Para pesquisar vários diretórios, adicione uma **entrada DriverPath** para cada diretório, como neste exemplo.


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



Se nenhuma **entrada DriverPath** for fornecida na seção **\[ \] DeviceInstall** ou a entrada **DriverPath** não tiver nenhum valor, essa unidade será ignorada durante uma pesquisa de arquivos de driver.

 

 
