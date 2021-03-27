---
description: Os formatos de área de transferência do shell são usados para identificar o tipo de dados do shell que está sendo transferido pela área de transferência.
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Formatos de área de transferência do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674ccc33db3a35a1a60abb549f5e1ab5b5c96760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646841"
---
# <a name="shell-clipboard-formats"></a>Formatos de área de transferência do Shell

Os formatos de área de transferência do shell são usados para identificar o tipo de dados do shell que está sendo transferido pela área de transferência. A maioria dos formatos de área de transferência do Shell identifica um tipo de dados, como uma lista de nomes de arquivos ou ponteiros para listas de identificadores de itens (PIDLs). No entanto, alguns formatos são usados para comunicação entre a origem e o destino. Eles podem agilizar o processo de transferência de dados oferecendo suporte a operações de Shell, como [movimentação otimizada](datascenarios.md) e [delete_on_paste](datascenarios.md). Os dados do Shell estão sempre contidos em um [objeto de dados](dataobject.md) que usa uma estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) como uma maneira mais geral de caracterizar dados. O membro **cfFormat** da estrutura é definido como o formato da área de transferência para o item de dados específico. Os outros membros fornecem informações adicionais, como o mecanismo de transferência de dados. Os dados estão contidos em uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que o acompanha.

> [!Note]  
> Os identificadores de formato padrão da área de transferência têm a forma CF_ *xxx*. Um exemplo comum é CF_TEXT, que é usado para transferir dados de texto ANSI. Esses identificadores têm valores predefinidos e podem ser usados diretamente com estruturas [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . Com exceção de [CF_HDROP](#cf_hdrop), os identificadores de formato de shell não são predefinidos. Com exceção de DragWindow, eles têm a forma CFSTR_ *xxx*. Para diferenciar esses valores dos formatos predefinidos, eles costumam ser chamados simplesmente de *formatos*. No entanto, diferentemente dos formatos predefinidos, eles devem ser registrados pela origem e pelo destino antes que possam ser usados para transferir dados. Para registrar um formato de Shell, inclua o arquivo de cabeçalho ShlObj. h e passe o identificador de formato do CFSTR_ *xxx* para [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). Essa função retorna um valor de formato de área de transferência válido, que pode ser usado como o membro **cfFormat** de uma estrutura **FORMATETC** .

 

Os formatos de área de transferência do shell são organizados aqui em três grupos, com base em como eles são usados.

-   [Formatos para transferir objetos do sistema de arquivos](#formats-for-transferring-file-system-objects)
    -   [CF_HDROP](#cf_hdrop)
    -   [CFSTR_FILECONTENTS](#cfstr_filecontents)
    -   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
    -   [CFSTR_FILENAME](#cfstr_filename)
    -   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
    -   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
    -   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
    -   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)
-   [Formatos para transferência de objetos virtuais](#formats-for-transferring-virtual-objects)
    -   [CFSTR_NETRESOURCES](#cfstr_netresources)
    -   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
    -   [CFSTR_INETURL](#cfstr_ineturl)
    -   [CFSTR_SHELLURL (preterido)](#cfstr_shellurl-deprecated)
-   [Formatos de comunicação entre a origem e o destino](#formats-for-communication-between-source-and-target)
    -   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
    -   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
    -   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
    -   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
    -   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
    -   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
    -   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
    -   [DragWindow](#dragwindow)

## <a name="formats-for-transferring-file-system-objects"></a>Formatos para transferir objetos do sistema de arquivos

Esses formatos são usados para transferir um ou mais arquivos ou outros objetos do Shell.

-   [CF_HDROP](#cf_hdrop)
-   [CFSTR_FILECONTENTS](#cfstr_filecontents)
-   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
-   [CFSTR_FILENAME](#cfstr_filename)
-   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
-   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
-   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
-   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)

### <a name="cf_hdrop"></a>CF_HDROP

Esse formato de área de transferência é usado ao transferir os locais de um grupo de arquivos existentes. Ao contrário dos outros formatos de Shell, ele é predefinido, portanto, não há necessidade de chamar [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). Os dados consistem em uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma estrutura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) como seu membro **HGLOBAL** .

O membro **pFiles** da estrutura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contém um deslocamento para uma matriz de caracteres dupla terminada com **nulo** que contém os nomes de arquivo. Se você estiver extraindo um formato de CF_HDROP de um objeto de dados, poderá usar [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) para extrair nomes de arquivo individuais do objeto de memória global. Se você estiver criando um formato de CF_HDROP a ser colocado em um objeto de dados, será necessário construir a matriz de nome de arquivo.

A matriz de nome de arquivo consiste em uma série de cadeias de caracteres, cada uma contendo um caminho totalmente qualificado de um arquivo, incluindo o caractere **nulo** de terminação. Um caractere **nulo** adicional é acrescentado à cadeia de caracteres final para encerrar a matriz. Por exemplo, se os arquivos c: \\temp1.txt e c: \\temp2.txt estiverem sendo transferidos, a matriz de caracteres terá esta aparência:


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> Neste exemplo, ' \\ 0 ' é usado para representar o caractere **nulo** , não os caracteres literais que devem ser incluídos.


Se o objeto foi copiado para a área de transferência como parte de uma operação de arrastar e soltar, o membro **pt** da estrutura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contém as coordenadas do ponto em que o objeto foi Descartado. Você pode usar [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) para extrair as coordenadas do cursor.

Se esse formato estiver presente em um objeto de dados, um loop de arrastar do OLE simulará [**WM_DROPFILES**](wm-dropfiles.md) funcionalidade com destinos de destino não OLE. Isso é importante se seu aplicativo for a origem de uma operação de arrastar e soltar em um sistema Windows 3,1.

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

Esse identificador de formato é usado com o formato de [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) para transferir dados como se fosse um arquivo, independentemente de como ele está realmente armazenado. Os dados consistem em uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que representa o conteúdo de um arquivo. Normalmente, o arquivo é representado como um objeto Stream, o que evita que você precise colocar o conteúdo do arquivo na memória. Nesse caso, o membro **TYMED** da estrutura **STGMEDIUM** é definido como TYMED_ISTREAM e o arquivo é representado por uma interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . O arquivo também pode ser um objeto de memória ou armazenamento global (TYMED_ISTORAGE ou TYMED_HGLOBAL). O formato de CFSTR_FILEDESCRIPTOR associado contém uma estrutura de [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) para cada arquivo que especifica o nome e os atributos do arquivo.

O destino trata os dados associados a um formato de CFSTR_FILECONTENTS como se fosse um arquivo. Quando o destino chama [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para extrair os dados, ele especifica um arquivo específico definindo o membro **Lindex** da estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) como o índice de base zero da estrutura [**filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) do arquivo no formato de [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) que o acompanha. Em seguida, o destino usa o ponteiro de interface retornado ou o identificador de memória global para extrair os dados.

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

Esse identificador de formato é usado com o formato de [CFSTR_FILECONTENTS](#cfstr_filecontents) para transferir dados como um grupo de arquivos. Esses dois formatos são a maneira preferida de transferir objetos do shell que não são armazenados como arquivos do sistema de arquivos. Por exemplo, esses formatos podem ser usados para transferir um grupo de mensagens de email como arquivos individuais, mesmo que cada email seja realmente armazenado como um bloco de dados em um banco de dado. Os dados consistem em uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma estrutura [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) seguida por uma matriz que contém uma estrutura de [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) para cada arquivo no grupo. Para cada estrutura de **FileDescriptor** , há um formato de CFSTR_FILECONTENTS separado que contém o conteúdo do arquivo. Para identificar um formato de CFSTR_FILECONTENTS de um arquivo específico, defina o valor **Lindex** da estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para o índice de base zero da estrutura **FileDescriptor** do arquivo.

O formato de CFSTR_FILEDESCRIPTOR é comumente usado para transferir dados como se fosse um grupo de arquivos, independentemente de como ele está realmente armazenado. Da perspectiva do destino, cada formato de CFSTR_FILECONTENTS representa um único arquivo e é tratado de acordo. No entanto, a origem pode armazenar os dados de qualquer forma que escolher. Embora um formato de CSFTR_FILECONTENTS possa corresponder a um único arquivo, ele também poderia, por exemplo, representar dados extraídos pela origem de um documento de um banco de dados ou de texto.

### <a name="cfstr_filename"></a>CFSTR_FILENAME

Esse identificador de formato é usado para transferir um único arquivo. Os dados consistem em uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma única cadeia de caracteres terminada em **nulo** que contém o caminho de arquivo totalmente qualificado do arquivo. Esse formato foi substituído por [CF_HDROP](#cf_hdrop), mas tem suporte para compatibilidade com versões anteriores com aplicativos do Windows 3,1.

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

Esse identificador de formato é usado quando um grupo de arquivos no formato [CF_HDROP](#cf_hdrop) está sendo renomeado e transferido. Os dados consistem em uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma matriz de caracteres dupla de terminação **nula**. Essa matriz contém um novo nome para cada arquivo, na mesma ordem em que os arquivos são listados no formato de CF_HDROP que o acompanha. O formato da matriz de caracteres é o mesmo usado pelo CF_HDROP para listar os arquivos transferidos.

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

Esse identificador de formato é usado para transferir um caminho em um volume montado. Ele é semelhante a [CF_HDROP](#cf_hdrop), mas contém apenas um único caminho e pode manipular as cadeias de caracteres de caminho mais longas que podem ser necessárias para representar um caminho quando o volume é montado em uma pasta. Os dados consistem em uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma única cadeia de caracteres terminada em **nulo** que contém o caminho de arquivo totalmente qualificado. A cadeia de caracteres de caminho deve terminar com um \\ caractere ' ', seguido pelo **nulo** de terminação.

Antes do Windows 2000, os volumes podiam ser montados somente em letras de unidade. Para sistemas Windows 2000 e posteriores com uma unidade formatada NTFS, você também pode montar volumes em pastas vazias. Esse recurso permite que um volume seja montado sem a necessidade de uma letra de unidade. O volume montado pode usar qualquer formato com suporte no momento, incluindo FAT, FAT32, NTFS e CDFS.

Você pode adicionar páginas a uma folha de propriedades de propriedades da unidade implementando um [manipulador de folha de propriedades](propsheet-handlers.md). Se o volume for montado em uma letra de unidade, o Shell passa as informações de caminho para o manipulador com o formato [CF_HDROP](#cf_hdrop) . Com o Windows 2000 e sistemas posteriores, o formato de CF_HDROP é usado quando um volume é montado em uma letra de unidade, assim como acontece com os sistemas anteriores. No entanto, se um volume for montado em uma pasta, o identificador de formato [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume) será usado em vez de CF_HDROP.

Se apenas letras de unidade forem usadas para montar volumes, somente [CF_HDROP](#cf_hdrop) serão usadas, e os manipuladores de folha de propriedades existentes funcionarão como faziam com os sistemas anteriores. No entanto, se você quiser que seu manipulador exiba uma página para volumes que são montados em pastas, bem como letras de unidade, o manipulador deve ser capaz de entender os formatos CSFTR_MOUNTEDVOLUME e CF_HDROP.

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

Esse identificador de formato é usado ao transferir os locais de um ou mais objetos de namespace existentes. Ele é usado quase da mesma forma que [CF_HDROP](#cf_hdrop), mas contém PIDLs em vez de caminhos do sistema de arquivos. O uso de PIDLs permite que o formato de CFSTR_SHELLIDLIST manipule objetos virtuais, bem como objetos do sistema de arquivos. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma estrutura [**cida**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) .

O membro **aoffset** da estrutura [**cida**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) é uma matriz que contém deslocamentos para o início da estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para cada PIDL que está sendo transferido. Para extrair um PIDL específico, primeiro determine seu índice. Em seguida, adicione o valor **aoffset** que corresponde a esse índice ao endereço da estrutura **cida** .

O primeiro elemento de **aoffset** contém um deslocamento para o PIDL totalmente qualificado de uma pasta pai. Se esse PIDL estiver vazio, a pasta pai será a área de trabalho. Cada um dos elementos restantes da matriz contém um deslocamento para um dos PIDLs a ser transferido. Todos esses PIDLs são relativos ao PIDL da pasta pai.

As duas macros a seguir podem ser usadas para recuperar PIDLs de uma estrutura [**cida**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) . A primeira pega um ponteiro para a estrutura e recupera o PIDL da pasta pai. O segundo usa um ponteiro para a estrutura e recupera um dos outros PIDLs, identificados por seu índice de base zero.


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> O valor retornado por essas macros é um ponteiro para a estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) do PIDL. Como essas estruturas variam em comprimento, você deve determinar o fim da estrutura percorrendo cada uma das estruturas [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) da estrutura de **ITEMIDLIST** até alcançar o **nulo** de dois bytes que marca o final.

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

Esse identificador de formato é usado com formatos como [CF_HDROP](#cf_hdrop), [CFSTR_SHELLIDLIST](#cfstr_shellidlist)e [CFSTR_FILECONTENTS](#cfstr_filecontents) para especificar a posição de um grupo de objetos após uma transferência. Os dados consistem em uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma matriz de estruturas de [**ponto**](/previous-versions//dd162805(v=vs.85)) . A primeira estrutura especifica as coordenadas da tela, em pixels, do canto superior esquerdo do retângulo que se aproxima do grupo. O restante das estruturas especifica os locais dos objetos individuais relativos à posição do grupo. Eles devem estar na mesma ordem usada para listar os objetos no formato associado.

## <a name="formats-for-transferring-virtual-objects"></a>Formatos para transferência de objetos virtuais

O formato de CFSTR_SHELLIDLIST pode ser usado para transferir o sistema de arquivos e objetos virtuais. No entanto, há também vários formatos especializados para transferir tipos específicos de objetos virtuais.

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (preterido)](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

Esse identificador de formato é usado ao transferir recursos de rede, como um domínio ou servidor. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma estrutura [**NRESARRAY**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) . O membro **NR** dessa estrutura indica uma estrutura de [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) cujo membro **lpRemoteName** contém uma cadeia de caracteres terminada em **nulo** que identifica o recurso de rede. O destino de soltura pode usar os dados com qualquer uma das funções de API do [WNet (rede do Windows)](../wnet/windows-networking-wnet-.md) , como [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona), para executar operações de rede no objeto.

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

Esse identificador de formato é usado ao transferir os nomes amigáveis de impressoras. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para uma cadeia de caracteres no mesmo formato usado com [CF_HDROP](#cf_hdrop). No entanto, o membro **pFiles** da estrutura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contém um ou mais nomes amigáveis de impressoras em vez de caminhos de arquivo.

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

Este identificador de formato substitui [CFSTR_SHELLURL (preterido)](#cfstr_shellurl-deprecated). Se você quiser que seu aplicativo manipule URLs da área de transferência, use CFSTR_INETURL em vez de CFSTR_SHELLURL (preterido). Esse formato fornece a melhor representação da área de transferência de uma única URL. Se o UNICODE não estiver definido, o aplicativo recuperará a versão CF_TEXT/CFSTR_SHELLURL da URL. Se o UNICODE estiver definido, o aplicativo recuperará a versão CF_UNICODE da URL.

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (preterido)

> [!Note]  
> Este identificador de formato foi preterido; em vez disso, use CFSTR_INETURL.

 

## <a name="formats-for-communication-between-source-and-target"></a>Formatos de comunicação entre a origem e o destino

Esses identificadores de formato permitem a comunicação entre a origem e o destino. Os formatos acompanham os dados e proporcionam aos aplicativos um grau maior de controle sobre as operações de arrastar-copiar-colar ou do tipo Drag-e-drop que envolvem objetos shell.

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [DragWindow](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

Esse identificador de formato é usado por um objeto de dados para indicar se ele está em um loop de arrastar e soltar. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para um valor **DWORD** . Se o valor **DWORD** for diferente de zero, o objeto de dados estará dentro de um loop de arrastar e soltar. Se o valor for definido como zero, o objeto de dados não estará dentro de um loop de arrastar e soltar.

Alguns destinos de soltura podem chamar [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) e tentar extrair dados enquanto o objeto ainda está dentro do loop do tipo "arrastar e soltar". A renderização total do objeto para cada ocorrência desse tipo pode fazer com que o cursor de arrastar seja interrompido. Se o objeto de dados der suporte a [CFSTR_INDRAGLOOP](#cfstr_indragloop), o destino poderá usar esse formato para verificar o status do loop do tipo "arrastar e soltar" e evitar a renderização intensiva da memória do objeto até que ele seja realmente removido. Os formatos que têm uso intensivo de memória para renderização ainda devem ser incluídos no enumerador [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e em chamadas para [**IDataObject:: QueryGetData**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata). Se o objeto de dados não definir CFSTR_INDRAGLOOP, ele deverá agir como se o valor fosse definido como zero.

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[Versão 5,0.](versions.md) Esse identificador de formato permite que uma fonte de soltar chame o método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) do objeto de dados para determinar o resultado de uma transferência de dados do Shell. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para um DWORD que contém um valor [**DROPEFFECT**](../com/dropeffect-constants.md) .

O identificador de formato de [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) foi projetado para permitir que o destino indique ao objeto de dados qual operação foi realmente realizada. No entanto, o Shell usa [movimentações otimizadas](datascenarios.md) para objetos do sistema de arquivos sempre que possível. Nesse caso, o Shell normalmente define o valor de CFSTR_PERFORMEDDROPEFFECT como DROPEFFECT_NONE, para indicar ao objeto de dados que os dados originais foram excluídos. Portanto, a origem não pode usar o valor CFSTR_PERFORMEDDROPEFFECT para determinar qual operação foi realizada. Embora a maioria das fontes não precise dessas informações, há algumas exceções. Por exemplo, embora as movimentações otimizadas eliminem a necessidade de uma origem excluir qualquer dado, a origem ainda pode precisar atualizar um banco de dados relacionado para indicar que os arquivos foram movidos ou copiados.

Se uma fonte precisar saber qual operação ocorreu, ela poderá chamar o método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) do objeto de dados e solicitar o formato CFSTR_LOGICALPERFORMEDDROPEFFECT. Esse formato essencialmente reflete o que acontece no ponto de vista do usuário depois que a operação é concluída. Se um novo arquivo for criado e o arquivo original for excluído, o usuário verá uma operação de movimentação e o valor de dados do formato será definido como DROPEFFECT_MOVE. Se o arquivo original ainda estiver lá, o usuário verá uma operação de cópia e o valor de dados do formato será definido como DROPEFFECT_COPY. Se um link tiver sido criado, o valor de dados do formato será DROPEFFECT_LINK.

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

Esse identificador de formato é usado pelo destino para informar o objeto de dados, por meio de seu método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) , que uma operação de exclusão ao colar foi bem-sucedida. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para um **DWORD** que contém um valor [**DROPEFFECT**](../com/dropeffect-constants.md) . Esse formato é usado para notificar o objeto de dados que ele deve concluir a operação de recorte e excluir os dados originais, se necessário. Para obter mais informações, consulte [operações de excluir em colar](datascenarios.md).

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

Esse identificador de formato é usado pelo destino para informar o objeto de dados por meio de seu método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do resultado de uma transferência de dados. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para um **DWORD** definido como o valor [**DROPEFFECT**](../com/dropeffect-constants.md) apropriado, normalmente DROPEFFECT_MOVE ou DROPEFFECT_COPY.

Esse formato normalmente é usado quando o resultado de uma operação pode ser mover ou copiar, como em uma operação de [movimentação otimizada](datascenarios.md) ou de exclusão ao colar. Ele fornece uma maneira confiável para o destino informar ao objeto de dados o que realmente aconteceu. Ele foi introduzido porque o valor de *pdwEffect* retornado por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) não indicou de forma confiável qual operação ocorreu. O formato de [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) é a maneira confiável de indicar que uma movimentação não otimizada foi feita.

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

Esse identificador de formato é usado pela origem para especificar se seu método preferencial de transferência de dados é mover ou copiar. Um destino de soltura solicita esse formato chamando o método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) do objeto de dados. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para um valor **DWORD** . Esse valor é definido como DROPEFFECT_MOVE se uma operação de movimentação for preferida ou DROPEFFECT_COPY se uma operação de cópia for preferida.

Esse recurso é usado quando uma fonte pode oferecer suporte a uma operação de movimentação ou cópia. Ele usa o formato [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect) para comunicar sua preferência ao destino. Como o destino não é obrigada a honrar a solicitação, o destino deve chamar o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) da origem com um formato [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) para informar ao objeto de dados qual operação foi realmente executada.

Com uma operação [Delete-on-Paste](datascenarios.md) , o formato CFSTR_PREFERREDDROPFORMAT é usado para informar ao destino se a origem fez uma recorte ou cópia. Com uma operação de arrastar e soltar, você pode usar CFSTR_PREFERREDDROPFORMAT para especificar a ação do Shell. Se esse formato não estiver presente, o Shell executará uma ação padrão, com base no contexto. Por exemplo, se um usuário arrastar um arquivo de um volume e o soltar em outro volume, a ação padrão do shell será copiar o arquivo. Ao incluir um formato de CFSTR_PREFERREDDROPFORMAT no objeto de dados, você pode substituir a ação padrão e dizer explicitamente ao shell para copiar, mover ou vincular o arquivo. Se o usuário optar por arrastar com o botão à direita, CFSTR_PREFERREDDROPFORMAT especificará o comando padrão no menu de atalho [arrastar e soltar](context-menu-handlers.md) . O usuário ainda está livre para escolher outros comandos no menu.

Antes do Microsoft Internet Explorer 4,0, um aplicativo indicou que ele estava transferindo tipos de arquivo de atalho, definindo FD_LINKUI no membro **dwFlags** da estrutura [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Os destinos precisavam usar uma chamada potencialmente demorada para [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para descobrir se o sinalizador de FD_LINKUI foi definido. Agora, a maneira preferida de indicar que os atalhos estão sendo transferidos é usar o formato CFSTR_PREFERREDDROPEFFECT definido como DROPEFFECT_LINK. No entanto, para compatibilidade com versões anteriores com sistemas mais antigos, as fontes ainda devem definir o sinalizador FD_LINKUI.

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

Esse identificador de formato é usado por um destino para fornecer seu CLSID à origem. Os dados são uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para o GUID do CLSID do destino de soltura.

Esse formato é usado principalmente para permitir que os objetos sejam excluídos arrastando-os para a lixeira. Quando um objeto é Descartado na lixeira, o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) da origem é chamado com um formato CFSTR_TARGETCLSID definido como o CLSID da lixeira (CLSID_RecycleBin). A origem pode então excluir o objeto original.

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

Esse identificador de formato é usado pelo Windows Internet Explorer e pelo shell do Windows para fornecer um mecanismo pelo qual bloquear ou solicitar operações de arrastar e soltar originadas do Internet Explorer em conjunto com o sinalizador de [**URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) .

**CFSTR_UNTRUSTEDDRAGDROP** é adicionado pela origem de uma operação de arrastar e soltar para especificar que o objeto de dados pode conter dados não confiáveis. Os dados são representados por uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que contém um objeto de memória global. O membro **HGLOBAL** da estrutura aponta para um **DWORD** definido como um sinalizador de [**ação de URL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) apropriado para fazer com que uma política Verifique o método [**IInternetSecurityManager::P rocessurlaction**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85)) , usando o sinalizador [**PUAF_ENFORCERESTRICTED**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85)) .

### <a name="dragwindow"></a>DragWindow

Esse formato é usado em uma operação de arrastar e soltar para identificar a imagem de arrastar de um objeto (janela) para que suas informações visuais possam ser atualizadas dinamicamente. Quando um objeto é arrastado sobre um destino de soltar, um aplicativo atualiza sua estrutura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) em resposta ao método [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) ou [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) . O **DROPDESCRIPTION** é atualizado com um novo valor [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) que indica a decoração a ser aplicada ao Visual da janela de arrastar; por exemplo, uma indicação de que o arquivo está sendo copiado em vez de movido ou que o objeto não pode ser Descartado para esse local. No entanto, até que o objeto receba uma mensagem de [**DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) , os visuais não serão atualizados. Esse formato fornece o **HWND** da janela de arrastar destinatário para o remetente da mensagem de **DDWM_UPDATEWINDOW** .

Os dados da área de transferência são do tipo [**TYMED_HGLOBAL**](/windows/win32/api/objidl/ne-objidl-tymed). É uma representação **DWORD** de um **HWND**. Os dados podem ser passados para a função **ULongToHandle** , definida em Basetsd. h, para fornecer um **HWND** de 64 bits para uso em janelas de 64 bits.

Esse formato não requer a inclusão de shlobj. h.

 

 
