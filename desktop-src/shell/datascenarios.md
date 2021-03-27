---
description: Este documento apresenta cenários comuns de transferência de dados do Shell e discute como implementar cada um em seu aplicativo.
ms.assetid: 7fce555c-a93d-4414-9119-7ae9acdd4d89
title: Manipulação de cenários de Transferência de Dados do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35855b66e4108580d5bac305855837563ca59785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967341"
---
# <a name="handling-shell-data-transfer-scenarios"></a>Manipulação de cenários de Transferência de Dados do Shell

O documento de [objeto de dados do Shell](dataobject.md) abordou a abordagem geral usada para transferir dados do shell com o recurso de arrastar e soltar ou a área de transferência. No entanto, para implementar a transferência de dados do Shell em seu aplicativo, você também deve entender como aplicar esses princípios e técnicas gerais à variedade de maneiras que os dados do Shell podem ser transferidos. Este documento apresenta cenários comuns de transferência de dados do Shell e discute como implementar cada um em seu aplicativo.

-   [Diretrizes gerais](#general-guidelines)
-   [Copiando nomes de arquivo da área de transferência para um aplicativo](#copying-file-names-from-the-clipboard-to-an-application)
    -   [Extraindo os nomes de arquivo do objeto de dados](#extracting-the-file-names-from-the-data-object)
-   [Copiando o conteúdo de um arquivo descartado em um aplicativo](#copying-the-contents-of-a-dropped-file-into-an-application)
    -   [Usando o \_ formato FILEcontent CFSTR para extrair dados de um arquivo](/windows)
-   [Lidando com operações de movimentação otimizadas](#handling-optimized-move-operations)
-   [Manipulando operações de exclusão em colar](#handling-delete-on-paste-operations)
-   [Transferindo dados de e para pastas virtuais](#transfering-data-to-and-from-virtual-folders)
    -   [Aceitando dados de uma pasta virtual](#accepting-data-from-a-virtual-folder)
    -   [Transferindo dados de e para uma extensão de NameSpace](#transferring-data-to-and-from-a-namespace-extension)
-   [Descartando arquivos na lixeira](#dropping-files-on-the-recycle-bin)
-   [Criando e importando arquivos de recorte](#creating-and-importing-scrap-files)
    -   [Suporte a viagens de ida e volta](#round-trip-support)
    -   [Formatos de dados em cache](#cached-data-formats)
    -   [Renderização atrasada](#delayed-rendering)
-   [Arrastando e soltando objetos do Shell de forma assíncrona](#dragging-and-dropping-shell-objects-asynchronously)
    -   [Usando IASyncOperation/IDataObjectAsyncCapability](#using-iasyncoperationidataobjectasynccapability)

> [!Note]  
> Embora cada um desses cenários discuta uma operação de transferência de dados específica, muitos deles se aplicam a uma variedade de cenários relacionados. Por exemplo, a principal diferença entre a maioria das transferências de área de transferência e arrastar e soltar está em como o objeto de dados chega ao destino. Depois que o destino tiver um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados, os procedimentos para extração de informações serão basicamente os mesmos para os dois tipos de transferência de dados. No entanto, alguns dos cenários são limitados a um tipo específico de operação. Consulte o cenário individual para obter detalhes.

 

## <a name="general-guidelines"></a>Diretrizes gerais

Cada uma das seções a seguir aborda um cenário de transferência de dados único e razoavelmente específico. No entanto, as transferências de dados geralmente são mais complexas e podem envolver aspectos de vários cenários. Normalmente, você não sabe, com antecedência, qual cenário você realmente precisará manipular. Aqui estão algumas diretrizes gerais para ter em mente.

Para fontes de dados:

-   Os formatos de área de transferência do Shell, com exceção de [CF \_ HDROP](clipboard.md), não são predefinidos. Cada formato que você deseja usar deve ser registrado chamando [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Os formatos nos objetos de dados são fornecidos na ordem de preferência da origem. Enumere o objeto de dados e escolha o primeiro que você pode consumir.
-   Inclua quantos formatos você puder dar suporte. Em geral, você não sabe onde o objeto de dados será Descartado. Essa prática melhora as chances de que o objeto de dados contenha um formato que o destino de soltar possa aceitar.
-   Os arquivos existentes devem ser oferecidos com o formato [ \_ HDROP do CF](clipboard.md) .
-   Ofereça dados como arquivos com [CFSTR \_ FileContent](clipboard.md) / [CFSTR formatos de \_ FileDescriptor](clipboard.md) . Essa abordagem permite que o destino crie um arquivo de um objeto de dados sem precisar saber nada sobre o armazenamento de dados subjacente. Normalmente, você deve apresentar os dados como uma interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Esse mecanismo de transferência de dados é mais flexível do que um objeto de memória global e usa muito menos memória.
-   As fontes de arrastar devem oferecer o formato [CFSTR \_ SHELLIDLIST](clipboard.md) ao arrastar itens de Shell. Os objetos de dados para itens podem ser adquiridos por meio dos métodos [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) ou [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) . As fontes de dados podem criar uma implementação de objeto de dados padrão que dê suporte ao formato [CFSTR \_ SHELLIDLIST](clipboard.md) usando [**SHCreateDataObject**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject).
-   Os destinos de destino que desejam saber sobre os itens que estão sendo arrastados usando o modelo de programação de item de shell podem converter um IDataObject em um [**IShellitemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) usando [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).
-   Use cursores de comentários padrão.
-   Suporte para arrastar para a esquerda e para a direita.
-   Use o objeto de dados em si por meio de um objeto inserido. Essa abordagem permite que seu aplicativo Recupere todos os formatos extras que o objeto de dados tem a oferecer e evita a criação de uma camada extra de confinamento. Por exemplo, um objeto incorporado do servidor A é arrastado do servidor/contêiner B e descartado no contêiner C. C deve criar um objeto inserido do servidor A, não um objeto incorporado do servidor B que contém um objeto incorporado do servidor A.
-   Lembre-se de que o Shell pode usar operações [otimizadas de movimentação](#handling-optimized-move-operations) ou [exclusão](#handling-delete-on-paste-operations) ao mover arquivos. Seu aplicativo deve ser capaz de reconhecer essas operações e responder adequadamente.

Para destinos de dados:

-   Os formatos de área de transferência do Shell, com exceção de [CF \_ HDROP](clipboard.md), não são predefinidos. Cada formato que você deseja usar deve ser registrado chamando [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Implemente e registre um destino OLE drop. Evite usar destinos do Windows 3,1 ou a mensagem do [**WM \_ DropFiles**](wm-dropfiles.md) , se possível.
-   Os formatos contidos por um objeto de dados variam de acordo com a origem do objeto. Como você geralmente não sabe com antecedência de onde vem um objeto de dados, não presuma que um determinado formato estará presente. O objeto de dados deve enumerar os formatos em ordem de qualidade, começando com o melhor. Portanto, para obter o melhor formato disponível, os aplicativos normalmente enumeram os formatos disponíveis e usam o primeiro formato na enumeração para o qual eles podem dar suporte.
-   Dê suporte ao arrastar com o botão direito. Você pode personalizar o menu de atalho arrastar criando um [manipulador de arrastar e soltar](context-menu-handlers.md).
-   Se seu aplicativo aceitar arquivos existentes, ele deverá ser capaz de manipular o formato [ \_ HDROP do CF](clipboard.md) .
-   Em geral, os aplicativos que aceitam arquivos também devem lidar com os formatos de fileCFSTR do [CFSTR \_ FileContent](clipboard.md) / [ \_ ](clipboard.md) . Embora os arquivos do sistema de arquivos tenham o formato de [ \_ HDROP do CF](clipboard.md) , os arquivos de provedores como extensões de namespace geralmente usam [CFSTR \_ FileContent](clipboard.md) / [CFSTR \_ FileDescriptor](clipboard.md). Os exemplos incluem pastas Windows CE, pastas protocolo FTP (FTP), pastas da Web e pastas CAB. Normalmente, a origem implementa uma interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) para apresentar dados de seu armazenamento como um arquivo.
-   Lembre-se de que o Shell pode usar operações [otimizadas de movimentação](#handling-optimized-move-operations) ou [exclusão](#handling-delete-on-paste-operations) ao mover arquivos. Seu aplicativo deve ser capaz de reconhecer essas operações e responder adequadamente.

## <a name="copying-file-names-from-the-clipboard-to-an-application"></a>Copiando nomes de arquivo da área de transferência para um aplicativo

**Cenário:** Um usuário seleciona um ou mais arquivos no Windows Explorer e os copia para a área de transferência. Seu aplicativo extrai os nomes dos arquivos e os cola no documento.

Esse cenário pode ser usado, por exemplo, para permitir que um usuário crie um link HTML Recortando e colando o arquivo em seu aplicativo. Em seguida, seu aplicativo pode extrair o nome do arquivo do objeto de dados e processá-lo para criar uma marca de âncora.

Quando um usuário seleciona um arquivo no Windows Explorer e o copia para a área de transferência, o Shell cria um objeto de dados. Em seguida, ele chama [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) para posicionar um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados na área de transferência.

Quando o usuário seleciona o comando **colar** no menu ou na barra de ferramentas do seu aplicativo:

1.  Chame [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) para recuperar a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados.
2.  Chame [**IDataObject:: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) para solicitar um objeto enumerador.
3.  Use a interface [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) do objeto enumerador para enumerar os formatos contidos no objeto de dados.

> [!Note]  
> As duas etapas finais deste procedimento estão incluídas para fins de integridade. Normalmente, eles não são necessários para transferências de arquivo simples. Todos os objetos de dados usados para esse tipo de transferência de dados devem conter o formato de [ \_ HDROP do CF](clipboard.md) , que pode ser usado para determinar os nomes dos arquivos contidos no objeto. No entanto, para transferências de dados mais gerais, você deve enumerar os formatos e selecionar o melhor que seu aplicativo pode manipular.

 

### <a name="extracting-the-file-names-from-the-data-object"></a>Extraindo os nomes de arquivo do objeto de dados

A próxima etapa é extrair um ou mais nomes de arquivo do objeto de dados e colá-los em seu aplicativo. Observe que o procedimento discutido nesta seção para extrair um nome de arquivo de um objeto de dados aplica-se igualmente bem às transferências de arrastar e soltar.

A maneira mais simples de recuperar nomes de arquivo de um objeto de dados é o formato de [ \_ HDROP do CF](clipboard.md) :

1.  Chamar [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Defina o membro **cfFormat** da estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) como [CF \_ HDROP](clipboard.md) e o membro **TYMED** como [TYMED \_ HGLOBAL](dataobject.md). O membro **dwAspect** normalmente é definido como DVASPECT \_ Content. No entanto, se você precisar ter o caminho do arquivo em formato curto (8,3), defina **dwAspect** como DVASPECT \_ short.

    Quando [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) retorna, o membro **HGlobal** da estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) aponta para um objeto de memória global que contém os dados.

2.  Crie uma variável HDROP e defina-a como o membro **HGLOBAL** da estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . A variável HDROP agora é um identificador para uma estrutura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) seguida por uma cadeia de caracteres dupla terminada com nulo que contém os caminhos de arquivo totalmente qualificados dos arquivos copiados.
3.  Determine Quantos caminhos de arquivo estão na lista chamando [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) com o parâmetro *ifile* definido como 0xFFFFFFFF. A função retorna o número de caminhos de arquivo na lista. O índice de base zero do caminho do arquivo nessa lista é usado na próxima etapa para identificar um determinado caminho.
4.  Extraia os caminhos de arquivo do objeto de memória global chamando [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) uma vez para cada arquivo, com *ifile* definido como o índice do arquivo.
5.  Processe os caminhos de arquivo conforme necessário e cole-os em seu aplicativo.
6.  Chame [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) e passe o ponteiro para a estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que você passou para [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) na etapa 1. Depois de lançar a estrutura, o valor de HDROP que você criou na etapa 2 não será mais válido e não deverá ser usado.

## <a name="copying-the-contents-of-a-dropped-file-into-an-application"></a>Copiando o conteúdo de um arquivo descartado em um aplicativo

**Cenário:** Um usuário arrasta um ou mais arquivos do Windows Explorer e os descarta na janela do aplicativo. Seu aplicativo extrai o conteúdo dos arquivos e cola-o em seu aplicativo.

Esse cenário usa o recurso de arrastar e soltar para transferir os arquivos do Windows Explorer para o aplicativo. Antes da operação, seu aplicativo deve:

1.  Chame [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para registrar todos os formatos de área de transferência do Shell necessários.
2.  Chame [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) para registrar uma janela de destino e a interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do seu aplicativo.

Depois que o usuário iniciar a operação selecionando um ou mais arquivos e começando a arrastá-los:

1.  O Windows Explorer cria um objeto de dados e carrega os formatos com suporte nele.
2.  O Windows Explorer chama [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) para iniciar o loop de arrastar.
3.  Quando a imagem de arrastar atingir sua janela de destino, o sistema o notificará chamando [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter).
4.  Para determinar o que o objeto de dados contém, chame o método [**IDataObject:: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) do objeto de dados. Use o objeto enumerador retornado pelo método para enumerar os formatos contidos no objeto de dados. Se seu aplicativo não quiser aceitar nenhum desses formatos, retorne DROPEFFECT \_ nenhum. Para os fins deste cenário, seu aplicativo deve ignorar todos os objetos de dados que não contêm formatos usados para transferir arquivos, como o [CF \_ HDROP](clipboard.md).
5.  Quando o usuário remove os dados, o sistema chama [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop).
6.  Use a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) para extrair o conteúdo dos arquivos.

Há várias maneiras diferentes de extrair o conteúdo de um objeto de Shell de um objeto de dados. Em geral, use a seguinte ordem:

-   Se o arquivo contiver um formato de [ \_ texto do CF](clipboard.md) , os dados serão texto ANSI. Você pode usar o formato de texto do CF \_ para extrair os dados, em vez de abrir o próprio arquivo.
-   Se o arquivo contiver um objeto OLE vinculado ou incorporado, o objeto de dados conterá um \_ formato CF incorporado. Use técnicas OLE padrão para extrair os dados. [Os arquivos de recorte](#creating-and-importing-scrap-files) sempre contêm um \_ formato CF incorporado.
-   Se o objeto Shell for do sistema de arquivos, o objeto de dados conterá um formato de [ \_ HDROP do CF](clipboard.md) com os nomes dos arquivos. Extraia o nome de arquivo do [CF \_ HDROP](clipboard.md) e chame [**OleCreateFromFile**](/windows/win32/api/ole2/nf-ole2-olecreatefromfile) para criar um novo objeto vinculado ou inserido. Para obter uma discussão sobre como recuperar um nome de arquivo de um formato [ \_ HDROP do CF](clipboard.md) , consulte [copiando nomes de arquivo da área de transferência para um aplicativo](#copying-file-names-from-the-clipboard-to-an-application).
-   Se o objeto de dados contiver um formato de [ \_ FileDescriptor CFSTR](clipboard.md) , você poderá extrair o conteúdo de um arquivo do formato [CFSTR \_ filecontents](clipboard.md) do arquivo. Para obter uma discussão sobre esse procedimento, consulte [usando o \_ formato FileContent CFSTR para extrair dados de um arquivo](/windows).
-   Antes da [versão](versions.md)do Shell 4,71, um aplicativo indicou que ele estava transferindo um tipo de arquivo de atalho definindo **FD \_ LINKUI** no membro **dwFlags** da estrutura [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Para versões posteriores do Shell, a maneira preferida de indicar que os atalhos estão sendo transferidos é usar o formato [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) definido como DROPEFFECT \_ link. Essa abordagem é muito mais eficiente do que extrair a estrutura do **FileDescriptor** apenas para verificar um sinalizador.

Se o processo de extração de dados for longo, talvez você queira fazer a operação de forma assíncrona em um thread em segundo plano. O thread principal pode prosseguir sem atrasos desnecessários. Para obter uma discussão sobre como lidar com a extração de dados assíncronos, consulte [arrastando e soltando objetos do Shell de forma assíncrona](#dragging-and-dropping-shell-objects-asynchronously).

### <a name="using-the-cfstr_filecontents-format-to-extract-data-from-a-file"></a>Usando o \_ formato FILEcontent CFSTR para extrair dados de um arquivo

O [formato \_ FileContent CFSTR](clipboard.md) fornece uma maneira muito flexível e eficiente de transferir o conteúdo de um arquivo. Não é nem necessário que os dados sejam armazenados como um único arquivo. Tudo o que é necessário para esse formato é que o objeto de dados apresente os dados ao destino como se fosse um arquivo. Por exemplo, os dados reais podem ser uma seção de um documento de texto ou um bloco de dados extraídos de um banco de dado. O destino pode tratar os dados como um arquivo e não precisa saber nada sobre o mecanismo de armazenamento subjacente.

Extensões de namespace normalmente usam [CFSTR \_ FileContent](clipboard.md) para transferir dados porque esse formato não assume nenhum mecanismo de armazenamento específico. Uma extensão de namespace pode usar qualquer mecanismo de armazenamento que seja conveniente e usar esse formato para apresentar seus objetos aos aplicativos como se fossem arquivos.

O mecanismo de transferência de dados para [CFSTR \_ FileContent](clipboard.md) é normalmente [TYMED \_ IStream](dataobject.md). A transferência de um ponteiro de interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) requer muito menos memória do que carregar os dados em um objeto de memória global, e **IStream** é uma maneira mais simples de representar dados do que o [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage).

Um [formato \_ FileContent CFSTR](clipboard.md) é sempre acompanhado por um formato de [ \_ FileDescriptor CFSTR](clipboard.md) . Primeiro, você deve examinar o conteúdo desse formato. Se mais de um arquivo estiver sendo transferido, o objeto de dados conterá, na verdade, vários formatos [ \_ FileContent CFSTR](clipboard.md) , um para cada arquivo. O formato de [ \_ FileDescriptor CFSTR](clipboard.md) contém o nome e os atributos de cada arquivo e fornece um valor de índice para cada arquivo que é necessário para extrair um formato de [CFSTR \_ filecontents](clipboard.md) de um arquivo específico.

Para extrair um [formato \_ FileContent CFSTR](clipboard.md) :

1.  Extraia o formato de [ \_ FileDescriptor CFSTR](clipboard.md) como um valor de [ \_ HGLOBAL TYMED](dataobject.md) .
2.  O membro **HGLOBAL** da estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) retornada aponta para um objeto de memória global. Bloqueie esse objeto passando o valor de **HGLOBAL** para [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock).
3.  Converta o ponteiro retornado por [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) em um ponteiro [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) . Ele apontará para uma estrutura **FILEGROUPDESCRIPTOR** seguida por uma ou mais estruturas [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Cada estrutura de **FileDescriptor** contém uma descrição de um arquivo que está contido em um dos formatos de [ \_ FileContent CFSTR](clipboard.md) que o acompanha.
4.  Examine as estruturas do [**descritor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) de arquivos para determinar qual delas corresponde ao arquivo que você deseja extrair. O índice de base zero dessa estrutura de **FileDescriptor** é usado para identificar o formato [ \_ FileContent](clipboard.md) do arquivo CFSTR. Como o tamanho de um bloco de memória global não é preciso de byte, use os membros **nFileSizeLow** e **nFileSizeHigh** da estrutura para determinar quantos bytes representam o arquivo no objeto de memória global.
5.  Chame [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) com o membro **CfFormat** da estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) definida como o valor [ \_ fileconters CFSTR](clipboard.md) e o membro **Lindex** definido como o índice que você determinou na etapa anterior. O membro **TYMED** normalmente é definido como [TYMED \_ HGLOBAL](dataobject.md) \| TYMED \_ IStream \| TYMED \_ ISTORAGE. O objeto de dados pode escolher seu mecanismo de transferência de dados preferencial.
6.  A estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que o [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) retornará conterá um ponteiro para os dados do arquivo. Examine o membro **TYMED** da estrutura para determinar o mecanismo de transferência de dados.
7.  Se **TYMED** for definido como [TYMED \_ IStream](dataobject.md) ou TYMED \_ ISTORAGE, use a interface para extrair os dados. Se **TYMED** for definido como TYMED \_ HGLOBAL, os dados ficarão contidos em um objeto de memória global. Para obter uma discussão sobre como extrair dados de um objeto de memória global, consulte a seção *extraindo um objeto de memória global de um* objeto de dados do [objeto de dados do Shell](dataobject.md).
8.  Chame [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) para desbloquear o objeto de memória global que você bloqueou na etapa 2.

## <a name="handling-optimized-move-operations"></a>Lidando com operações de movimentação otimizadas

**Cenário:** Um arquivo é movido do sistema de arquivos para uma extensão de namespace usando uma movimentação otimizada.

Em uma operação de movimentação convencional, o destino faz uma cópia dos dados e a origem exclui o original. Esse procedimento pode ser ineficiente porque requer duas cópias dos dados. Com objetos grandes, como bancos de dados, uma operação de movimentação convencional pode não ser ainda prática.

Com uma movimentação otimizada, o destino usa sua compreensão de como os dados são armazenados para lidar com toda a operação de movimentação. Nunca há uma segunda cópia dos dados, e não há necessidade de que a origem exclua os dados originais. Os dados do shell são adequados para movimentações otimizadas porque o destino pode manipular toda a operação usando a API do Shell. Um exemplo típico é A movimentação de arquivos. Depois que o destino tiver o caminho de um arquivo a ser movido, ele poderá usar [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para movê-lo. Não é necessário que a origem exclua o arquivo original.

> [!Note]  
> O Shell normalmente usa uma movimentação otimizada para mover arquivos. Para lidar corretamente com a transferência de dados do Shell, seu aplicativo deve ser capaz de detectar e lidar com uma movimentação otimizada.

 

As movimentações otimizadas são tratadas da seguinte maneira:

1.  A origem chama [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) com o parâmetro *DWEFFECT* definido como DROPEFFECT \_ move para indicar que os objetos de origem podem ser movidos.
2.  O destino recebe o \_ valor de movimentação DROPEFFECT por meio de um de seus métodos [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) , indicando que uma movimentação é permitida.
3.  O destino copia o objeto (movimentação não otimizada) ou move o objeto (movimentação otimizada).
4.  O destino, em seguida, informa à origem se precisa excluir os dados originais.

    Uma movimentação otimizada é a operação padrão, com os dados excluídos pelo destino. Para informar à fonte que uma movimentação otimizada foi executada:

    -   -   O destino define o valor de *pdwEffect* recebido por meio de seu [**IDropTarget::D método ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) para algum valor diferente de DROPEFFECT \_ move. Normalmente, ele é definido como DROPEFFECT \_ None ou DROPEFFECT \_ Copy. O valor será retornado para a origem por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
        -   O destino também chama o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do objeto de dados e passa a ele um identificador de formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) definido como DROPEFFECT \_ None. Essa chamada de método é necessária porque alguns destinos de remoção podem não definir o parâmetro *pdwEffect* de [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) corretamente. O formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) é a maneira confiável de indicar que uma movimentação otimizada foi feita.

    Se o destino tiver feito uma movimentação não otimizada, os dados deverão ser excluídos pela origem. Para informar à fonte que uma movimentação não otimizada foi executada:

    -   -   O destino define o valor de *pdwEffect* recebido por meio de seu [**IDropTarget::D método ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) para DROPEFFECT \_ mover. O valor será retornado para a origem por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
        -   O destino também chama o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do objeto de dados e passa a ele um identificador de formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) definido como DROPEFFECT \_ move. Essa chamada de método é necessária porque alguns destinos de remoção podem não definir o parâmetro *pdwEffect* de [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) corretamente. O formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) é a maneira confiável de indicar que uma movimentação não otimizada foi feita.

5.  A origem inspeciona os dois valores que podem ser retornados pelo destino. Se ambos estiverem definidos como DROPEFFECT \_ move, ele concluirá a movimentação não otimizada excluindo os dados originais. Caso contrário, o destino fez uma movimentação otimizada e os dados originais foram excluídos.

## <a name="handling-delete-on-paste-operations"></a>Manipulando operações de exclusão em colar

**Cenário:** Um ou mais arquivos são recortados de uma pasta no Windows Explorer e colados em uma extensão de namespace. O Windows Explorer deixa os arquivos realçados até receber comentários sobre o resultado da operação de colagem.

Tradicionalmente, quando um usuário recorta os dados, ele desaparece imediatamente da exibição. Isso pode não ser eficiente e pode levar a problemas de usabilidade se o usuário se preocupar com o que aconteceu com os dados. Uma abordagem alternativa é usar uma operação de exclusão ao colar.

Com uma operação de exclusão na colagem, os dados selecionados não são removidos imediatamente da exibição. Em vez disso, o aplicativo de origem marca-o como selecionado, talvez alterando a cor da fonte ou do plano de fundo. Depois que o aplicativo de destino colar os dados, ele notificará a origem sobre o resultado da operação. Se o destino tiver executado uma [movimentação otimizada](#handling-optimized-move-operations), a origem poderá simplesmente atualizar sua exibição. Se o destino tiver realizado uma movimentação normal, a origem também deverá excluir sua cópia dos dados. Se a colagem falhar, o aplicativo de origem restaurará os dados selecionados para sua aparência original.

> [!Note]  
> O Shell normalmente usa excluir-em-colar quando uma operação de recortar/colar é usada para mover arquivos. As operações de exclusão ao colar com objetos shell normalmente usam uma [movimentação otimizada](#handling-optimized-move-operations) para mover os arquivos. Para lidar corretamente com a transferência de dados do Shell, seu aplicativo deve ser capaz de detectar e manipular operações de exclusão no colar.

 

O requisito essencial para excluir-em-colar é que o destino deve relatar o resultado da operação para a origem. No entanto, técnicas de área de transferência padrão não podem ser usadas para implementar Delete-on-Paste porque não fornecem uma maneira para o destino se comunicar com a origem. Em vez disso, o aplicativo de destino usa o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do objeto de dados para relatar o resultado ao objeto de dados. O objeto de dados pode então se comunicar com a origem por meio de uma interface privada.

O procedimento básico para uma operação de exclusão em colar é o seguinte:

1.  A fonte marca a exibição da tela dos dados selecionados.
2.  A origem cria um objeto de dados. Ele indica uma operação de recorte adicionando o formato [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) com um valor de dados de DROPEFFECT \_ move.
3.  A origem coloca o objeto de dados na área de transferência usando [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard).
4.  O destino recupera o objeto de dados da área de transferência usando [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard).
5.  O destino extrai os dados do [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) . Se estiver definido como somente DROPEFFECT \_ mover, o destino poderá fazer uma movimentação otimizada ou simplesmente copiar os dados.
6.  Se o destino não fizer uma movimentação otimizada, ele chamará o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) com o formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) definido como DROPEFFECT \_ move.
7.  Quando a colagem é concluída, o destino chama o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) com o formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) definido como DROPEFFECT \_ move.
8.  Quando o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) da origem é chamado com o formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) definido como DROPEFFECT \_ move, ele deve verificar se ele também recebeu o formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) definido como DROPEFFECT \_ mover. Se ambos os formatos forem enviados pelo destino, a fonte terá que excluir os dados. Se apenas o formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) for recebido, a fonte poderá simplesmente remover os dados de sua exibição. Se a transferência falhar, a origem atualizará a exibição para sua aparência original.

## <a name="transfering-data-to-and-from-virtual-folders"></a>Transferindo dados de e para pastas virtuais

**Cenário:** Um usuário arrasta um objeto do ou o descarta em uma pasta virtual.

As pastas virtuais contêm objetos que geralmente não fazem parte do sistema de arquivos. Algumas pastas virtuais, como a lixeira, podem representar dados armazenados no disco rígido, mas não como objetos comuns do sistema de arquivos. Alguns podem representar dados armazenados que estão em um sistema remoto, como um PC portátil ou um site FTP. Outros, como a pasta impressoras, contêm objetos que não representam dados armazenados. Embora algumas pastas virtuais façam parte do sistema, os desenvolvedores também podem criar e instalar pastas virtuais personalizadas implementando uma extensão de namespace.

Independentemente do tipo de dados ou de como eles são armazenados, os objetos de pasta e arquivo contidos em uma pasta virtual são apresentados pelo shell como se fossem arquivos e pastas normais. É responsabilidade da pasta virtual pegar quaisquer dados que ele contenha e apresentá-los ao shell adequadamente. Esse requisito significa que as pastas virtuais normalmente dão suporte a transferências de dados de arrastar e soltar e de área de transferência.

Há, portanto, dois grupos de desenvolvedores que precisam se preocupar com a transferência de dados de e para as pastas virtuais:

-   Os desenvolvedores cujos aplicativos precisam aceitar dados transferidos de uma pasta virtual.
-   Os desenvolvedores cujas extensões de namespace precisam dar suporte adequado à transferência de dados.

### <a name="accepting-data-from-a-virtual-folder"></a>Aceitando dados de uma pasta virtual

As pastas virtuais podem representar praticamente qualquer tipo de dados e podem armazenar esses dados de qualquer forma que escolherem. Algumas pastas virtuais podem realmente conter arquivos e pastas normais do sistema de arquivos. Outros podem, por exemplo, empacotar todos os seus objetos em um único documento ou banco de dados.

Quando um objeto do sistema de arquivos é transferido para um aplicativo, o objeto de dados normalmente contém um formato de [ \_ HDROP do CF](clipboard.md) com o caminho totalmente qualificado do objeto. Seu aplicativo pode extrair essa cadeia de caracteres e usar as funções normais do sistema de arquivos para abrir o arquivo e extrair seus dados. No entanto, como as pastas virtuais normalmente não contêm objetos normais do sistema de arquivos, geralmente não usam o [ \_ HDROP do CF](clipboard.md).

Em vez [da \_ HDROP do CF](clipboard.md), os dados são normalmente transferidos de pastas virtuais com os formatos [CFSTR \_ FileDescriptor](clipboard.md) / [CFSTR \_ fileconters](clipboard.md) . O [formato \_ FileContent CFSTR](clipboard.md) tem duas vantagens sobre o [CF \_ HDROP](clipboard.md):

-   Nenhum método específico de armazenamento de dados é assumido.
-   O formato é mais flexível. Ele dá suporte a três mecanismos de transferência de dados: um objeto de memória global, uma interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) ou uma interface [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) .

Os objetos de memória global raramente são usados para transferir dados de ou para objetos virtuais, pois os dados devem ser copiados na memória em sua totalidade. A transferência de um ponteiro de interface requer quase nenhuma memória e é muito mais eficiente. Com arquivos muito grandes, um ponteiro de interface pode ser o único mecanismo de transferência de dados prático. Normalmente, os dados são representados por um ponteiro de [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , pois essa interface é um pouco mais flexível do que [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage). O destino extrai o ponteiro do objeto de dados e usa os métodos de interface para extrair os dados.

Para obter mais informações sobre como lidar com os formatos de [fileCFSTR do CFSTR \_ FileDescriptor](clipboard.md) / , consulte [usando o \_ formato CFSTR FileContent para extrair dados de um arquivo](/windows).[ \_ ](clipboard.md)

### <a name="transferring-data-to-and-from-a-namespace-extension"></a>Transferindo dados de e para uma extensão de NameSpace

Ao implementar uma extensão de namespace, normalmente você desejará dar suporte a recursos de arrastar e soltar. Siga as recomendações para remover origens e destinos discutidos em [diretrizes gerais](#general-guidelines). Em particular, uma extensão de namespace deve:

-   Ser capaz de lidar com os formatos de [ \_ filedescriptores CFSTR fileCFSTR](clipboard.md) / [ \_ ](clipboard.md) . Esses dois formatos normalmente são usados para transferir objetos de e para extensões de namespace.
-   Ser capaz de lidar com as [movimentações otimizadas](#handling-optimized-move-operations). O Shell espera que os objetos do Shell serão movidos com uma movimentação otimizada.
-   Ser capaz de lidar com uma operação de [exclusão na colagem](#handling-delete-on-paste-operations) . O Shell usa excluir-em-colar quando os objetos são movidos do shell com uma operação de recortar/colar.
-   Ser capaz de lidar com a transferência de dados por meio de uma interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) ou [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . A transferência de dados de ou para uma pasta virtual normalmente é manipulada pela transferência de um desses dois ponteiros de interface, normalmente um ponteiro de **IStream** . Em seguida, o destino chama os métodos de interface para extrair os dados:
    -   -   Como uma fonte de soltar, a extensão do namespace deve extrair os dados do armazenamento e passá-los por meio dessa interface para o destino.
        -   Como destino de soltar, uma extensão de namespace deve aceitar dados de uma fonte por meio dessa interface e armazená-los corretamente.

## <a name="dropping-files-on-the-recycle-bin"></a>Descartando arquivos na lixeira

**Cenário:** O usuário remove um arquivo na **Lixeira**. Seu aplicativo ou extensão de namespace exclui o arquivo original.

A lixeira é uma pasta virtual que é usada como um repositório para arquivos que não são mais necessários. Desde que a lixeira não tenha sido esvaziada, o usuário poderá recuperar o arquivo posteriormente e retorná-lo ao sistema de arquivos.

Para a maior parte, a transferência de objetos do Shell para a lixeira funciona de forma muito semelhante a qualquer outra pasta. No entanto, quando um usuário remove um arquivo na **Lixeira**, a origem precisa excluir o original, mesmo se os comentários da pasta indicarem uma operação de cópia. Normalmente, uma fonte de soltar não tem como saber em qual pasta seu objeto de dados foi Descartado. No entanto, para sistemas Windows 2000 e posteriores, quando um objeto de dados é Descartado na **Lixeira**, o Shell chamará o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do objeto de dados com um formato [ \_ TARGETCLSID CFSTR](clipboard.md) definido como o CLSID (identificador de classe) da Lixeira (CLSID \_ RecycleBin). Para manipular o caso da lixeira corretamente, o objeto de dados deve ser capaz de reconhecer esse formato e comunicar as informações à fonte por meio de uma interface privada.

> [!Note]  
> Quando [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) é chamado com um [formato \_ TARGETCLSID CFSTR](clipboard.md) definido como CLSID \_ RecycleBin, a fonte de dados deve fechar qualquer identificador aberto para os objetos que estão sendo transferidos antes de retornar do método. Caso contrário, você pode criar violações de compartilhamento.

 

## <a name="creating-and-importing-scrap-files"></a>Criando e importando arquivos de recorte

**Cenário:** Um usuário arrasta alguns dados do arquivo de dados de um aplicativo OLE e o descarta no desktop ou no Windows Explorer.

O Windows permite que os usuários arrastem um objeto do arquivo de dados de um aplicativo OLE e o Soltem na área de trabalho ou em uma pasta do sistema de arquivos. Esta operação cria um *arquivo de recorte*, que contém os dados ou um link para os dados. O nome do arquivo é obtido do nome curto registrado para o CLSID do objeto e os dados [de \_ texto do CF](clipboard.md) . Para que o Shell crie um arquivo de recorte contendo dados, a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do aplicativo deve oferecer suporte ao formato de área de transferência do CF \_ . Para criar um arquivo que contém um link, **IDataObject** deve dar suporte ao formato de link do CF \_ .

Também há três recursos opcionais que um aplicativo pode implementar para dar suporte a arquivos de recorte:

-   Suporte a viagens de ida e volta
-   Formatos de dados em cache
-   Renderização atrasada

### <a name="round-trip-support"></a>Suporte a viagens de ida e volta

Uma *viagem* de ida e volta envolve a transferência de um objeto de dados para outro contêiner e, em seguida, para o documento original. Por exemplo, um usuário pode transferir um grupo de células de uma planilha para a área de trabalho, criando um arquivo de recorte com os dados. Se o usuário transferir a reversão para a planilha, os dados precisarão ser integrados ao documento como era antes da transferência original.

Quando o Shell cria o arquivo de recorte, ele representa os dados como um objeto de incorporação. Quando a sucata é transferida para outro contêiner, ela é transferida como um objeto de incorporação, mesmo que esteja sendo retornada ao documento original. Seu aplicativo é responsável por determinar o formato de dados contido na sucata e colocar os dados de volta em seu formato nativo, se necessário.

Para estabelecer o formato do objeto inserido, determine seu CLSID recuperando o formato do objectdescriptor do CF do objeto \_ . Se o CLSID indicar um formato de dados que pertence ao aplicativo, ele deverá transferir os dados nativos em vez de chamar [**OleCreateFromData**](/windows/win32/api/ole2/nf-ole2-olecreatefromdata).

### <a name="cached-data-formats"></a>Formatos de dados em cache

Quando o Shell cria um arquivo de recorte, ele verifica o registro para obter a lista de formatos disponíveis. Por padrão, há dois formatos disponíveis: CF \_ embed e CF \_ LinkId. No entanto, há vários cenários em que os aplicativos podem precisar ter arquivos de sucata em formatos diferentes:

-   Para permitir que as recortes sejam transferidas para contêineres não OLE, o que não aceita formatos de objeto inseridos.
-   Para permitir que conjuntos de aplicativos se comuniquem com um formato privado.
-   Para facilitar a manipulação de viagens de ida e volta.

Os aplicativos podem adicionar formatos à sucata armazenando-os em cache no registro. Há dois tipos de formatos em cache:

-   Formatos de cache de prioridade. Para esses formatos, os dados são copiados em sua totalidade na sucata do objeto de dados.
-   Formatos renderizados com atraso. Para esses formatos, o objeto de dados não é copiado para a sucata. Em vez disso, a renderização é atrasada até que um destino solicite os dados. A renderização de atraso é discutida mais detalhadamente na próxima seção.

Para adicionar um cache de prioridade ou um formato processado por atraso, crie uma subchave **DataFormat** sob a chave **CLSID** do aplicativo que é a origem dos dados. Sob essa subchave, crie uma subchave **PriorityCacheFormats** ou **DelayRenderFormats** . Para cada cache de prioridade ou formato processado com atraso, crie uma subchave numerada começando com zero. Defina o valor dessa chave como uma cadeia de caracteres com o nome registrado do formato ou um \# valor x, em que X representa o número de formato de um formato de área de transferência padrão.

O exemplo a seguir mostra os formatos em cache para dois aplicativos. O aplicativo MyProg1 tem o formato Rich-Text como um formato de cache de prioridade e um formato privado "My Format" como um formato reproduzido por atraso. O aplicativo MyProg2 tem o formato de bitmap do CF \_ ( \# 8 ") como um formato de cache de prioridade.

```
HKEY_CLASSES_ROOT
   CLSID
      {GUID}
         (Default) = MyProg1
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = Rich Text Format
            DelayRenderFormats
               0
                  (Default) = My Format
      {GUID}
         (Default) = MyProg2
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = #8
```

Formatos adicionais podem ser adicionados criando subchaves numeradas adicionais.

### <a name="delayed-rendering"></a>Renderização atrasada

Um formato de renderização atrasado permite que um aplicativo crie um arquivo de recorte, mas adie a despesa de renderizar os dados até que ele seja solicitado por um destino. A interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de uma sucata oferecerá os formatos de renderização atrasados para o destino, juntamente com os dados nativos e armazenados em cache. Se o destino solicitar um formato de renderização atrasado, o Shell executará o aplicativo e fornecerá os dados para o destino do objeto ativo.

> [!Note]  
> Como a renderização atrasada é um pouco arriscada, ela deve ser usada com cautela. Ele não funcionará se o servidor não estiver disponível ou em aplicativos que não são habilitados para OLE.

 

## <a name="dragging-and-dropping-shell-objects-asynchronously"></a>Arrastando e soltando objetos do Shell de forma assíncrona

**Cenário:** Um usuário transfere um grande bloco de dados da origem para o destino. Para evitar o bloqueio de ambos os aplicativos por uma quantidade significativa de tempo, o destino extrai os dados de forma assíncrona.

Normalmente, o recurso de arrastar e soltar é uma operação síncrona. Em resumo:

1.  A origem de soltura chama [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) e bloqueia seu thread principal até que a função retorne. Bloquear o thread principal normalmente bloqueia o processamento da interface do usuário.
2.  Depois que o método [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) do destino é chamado, o destino extrai os dados do objeto de dados em seu thread primário. Esse procedimento normalmente bloqueia o processamento da interface do usuário do destino para a duração do processo de extração.
3.  Depois que os dados são extraídos, o destino retorna a chamada [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) , o sistema retorna [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)e ambos os threads podem continuar.

Em suma, a transferência de dados síncrona pode bloquear os principais threads de ambos os aplicativos por um período significativo. Em particular, os dois threads devem aguardar enquanto o destino extrai os dados. Para pequenas quantidades de dados, o tempo necessário para extrair dados é pequeno e a transferência de dados síncrona funciona muito bem. No entanto, a extração síncrona de grandes quantidades de dados pode causar atrasos longos e interferir na interface do usuário de destino e de origem.

A interface [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) é uma interface opcional que pode ser implementada por um objeto de dados. Ele dá ao destino de soltura a capacidade de extrair dados do objeto de dados de forma assíncrona em um thread em segundo plano. Depois que a extração de dados é transferida para o thread em segundo plano, os principais threads de ambos os aplicativos são gratuitos para continuar.

### <a name="using-iasyncoperationidataobjectasynccapability"></a>Usando IASyncOperation/IDataObjectAsyncCapability

> [!Note]  
> A interface foi originalmente denominada [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)), mas ela foi alterada posteriormente para [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability). Caso contrário, as duas interfaces são idênticas.

 

A finalidade do [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) é permitir que a origem do descarte e o destino de soltura negociem se os dados podem ser extraídos de forma assíncrona. O procedimento a seguir descreve como a origem de soltura usa a interface:

1.  Crie um objeto de dados que expõe [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability).
2.  Chame [**Setasyncmode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode) com *FDoOpAsync* definido como **Variant \_ true** para indicar que há suporte para uma operação assíncrona.
3.  Após o retorno de [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) , chame [**inoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation):
    -   Se a [**inoperação**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) falhar ou retornar a **variante \_ false**, ocorrerá uma transferência de dados síncrona normal e o processo de extração de dados será concluído. A origem deve fazer qualquer limpeza necessária e continuar.
    -   Se [**inoperação**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) retornar **Variant \_ true**, os dados serão extraídos de forma assíncrona. As operações de limpeza devem ser manipuladas pela [**Endoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).
4.  Libere o objeto de dados.
5.  Quando a transferência de dados assíncrona é concluída, o objeto de dados normalmente notifica a origem por meio de uma interface privada.

O procedimento a seguir descreve como o destino de soltura usa a interface [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) para extrair dados de forma assíncrona:

1.  Quando o sistema chama [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop), chame [**IDataObject:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e solicite [](/previous-versions//bb776309(v=vs.85))uma / interface [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) IAsyncOperation (IID \_ IAsyncOperation/IID \_ IDataObjectAsyncCapability) do objeto de dados.
2.  Chame [**Getasyncmode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode). Se o método retornar **Variant \_ true**, o objeto de dados dará suporte à extração de dados assíncronos.
3.  Crie um thread separado para manipular a extração de dados e chamar [**StartOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-startoperation).
4.  Retorne a chamada [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) , como você faria para uma operação de transferência de dados normal. [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) retornará e desbloqueará a origem do descarte. Não chame [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para indicar o resultado de uma operação otimizada para mover ou excluir ao colar. Aguarde até que a operação seja concluída.
5.  Extraia os dados no thread em segundo plano. O thread principal do destino é desbloqueado e gratuito para continuar.
6.  Se a transferência de dados foi uma operação de movimentação ou [exclusão](#handling-delete-on-paste-operations) [otimizada](#handling-optimized-move-operations) , chame [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para indicar o resultado.
7.  Notifique o objeto de dados que a extração é concluída chamando [**Endoperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).

 

 
