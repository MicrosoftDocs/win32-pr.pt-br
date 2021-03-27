---
description: Este tópico descreve algumas das coisas a considerar ao usar bibliotecas em seu programa.
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: Usando bibliotecas em seu programa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2812a66b148d9bd16fc3951efab64a4d37afaaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297720"
---
# <a name="using-libraries-in-your-program"></a>Usando bibliotecas em seu programa

Este tópico descreve algumas das coisas a considerar ao usar bibliotecas em seu programa.

Neste tópico:

-   [Visão geral de programação de biblioteca](#library-programming-overview)
-   [Programação com bibliotecas](#programming-with-libraries)
    -   [Movendo de pastas conhecidas para bibliotecas](#moving-from-known-folders-to-libraries)
    -   [Grupo doméstico e bibliotecas compartilhadas](#homegroup-and-shared-libraries)
-   [Usando uma caixa de diálogo de arquivo comum com bibliotecas](#using-a-common-file-dialog-box-with-libraries)
-   [Habilitando a seleção de biblioteca na interface do usuário](#enabling-library-selection-from-the-user-interface)
-   [Acessando o conteúdo da biblioteca em um programa](#accessing-library-content-in-a-program)
    -   [Acessando o conteúdo da biblioteca com a interface IShellLibrary](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [Acessando o conteúdo da biblioteca com as APIs do Shell](#accessing-library-content-with-the-shell-apis)
-   [Salvando o conteúdo do usuário em uma biblioteca](#saving-user-content-in-a-library)
-   [Suporte a operações de arrastar e soltar em uma biblioteca](#supporting-drag-and-drop-operations-in-a-library)
-   [Mantendo a sincronização com uma biblioteca](#keeping-in-sync-with-a-library)
    -   [Atualização em Massa](#bulk-update)
    -   [Notificação da API do Shell](#shell-api-notification)
    -   [Notificação da API do sistema de arquivos](#file-system-api-notification)
-   [Tópicos relacionados](#related-topics)

## <a name="library-programming-overview"></a>Visão geral de programação de biblioteca

As bibliotecas permitem que os usuários organizem seu conteúdo baseado em arquivo de uma maneira que seja significativa para eles e não sejam limitados pela organização do sistema de arquivos. Quando o programa oferece suporte a bibliotecas, ele permite que o usuário encontre seu conteúdo de uma maneira que faça sentido para eles ao mesmo tempo em que apresenta uma interface do usuário consistente com a experiência do usuário do Windows 7. As bibliotecas também facilitam o seu programa de localizar conteúdo baseado em arquivo armazenado em pastas diferentes ou em computadores diferentes.

Os tópicos nesta seção descrevem como você pode adicionar suporte à biblioteca para seu programa e aproveitar os novos recursos oferecidos pelas bibliotecas. Por padrão, o Windows 7 fornece um pouco desse suporte. Se o programa não modificar as caixas de diálogo de arquivo comuns que ele usa atualmente, ele poderá exigir muito pouca programação adicional para oferecer suporte a bibliotecas.

Esta seção descreve alguns dos principais recursos que as bibliotecas fornecem e como dar suporte a elas em seu programa. Com essas informações, você pode decidir quais recursos fornecerão a melhor experiência de usuário do seu programa. Se o programa personalizar as caixas de diálogo de arquivo comum, as informações contidas nesta seção podem ajudá-lo a determinar como usar as caixas de diálogo do novo arquivo comum para usar bibliotecas e fornecer funcionalidade equivalente no Windows 7.

## <a name="programming-with-libraries"></a>Programação com bibliotecas

O modelo de programação do shell do Windows descreve como um programa interage com objetos de programação do shell do Windows. Embora os objetos do sistema de arquivos, como arquivos e diretórios, sejam representados por objetos do shell do Windows, nem todos os objetos do Windows Shell são representados pelo sistema de arquivos. As bibliotecas, por exemplo, são objetos de shell do Windows que não têm um sistema de arquivos equivalente. O uso de objetos do shell do Windows em seu programa permite que seu programa acesse todos os objetos do Shell e não apenas os objetos do sistema de arquivos.

Para obter melhores resultados, seu programa usaria a [**API da biblioteca do Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) para interagir com bibliotecas e acessar seu conteúdo. Embora as bibliotecas contenham itens de sistema de arquivos, como pastas e arquivos, as bibliotecas não são itens do sistema de arquivos. Dessa forma, as APIs do sistema de arquivos não podem ser usadas para acessar os recursos da biblioteca ou o conteúdo da biblioteca.

Se você tiver um programa existente que atualmente usa muitas APIs de sistema de arquivos, seu programa ainda poderá aproveitar os recursos de biblioteca. A [**API da biblioteca do Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) pode fornecer referências de sistema de arquivos para os itens encontrados em uma biblioteca e essas referências de sistema de arquivos, como o nome do arquivo e o caminho, podem ser passadas para as APIs do sistema de arquivos existentes que estão no seu programa existente.

### <a name="moving-from-known-folders-to-libraries"></a>Movendo de pastas conhecidas para bibliotecas

Antes do Windows 7, era comum usar uma pasta conhecida, como a pasta meus documentos, como a pasta padrão nas operações salvar arquivo ou abrir arquivo. No Windows 7, a biblioteca correspondente deve ser usada para que o usuário tenha a mesma experiência em seu programa como faria com outros programas do Windows 7, como o Windows Explorer.

Se você estiver usando a API do shell do Windows no seu programa, adicionar suporte à biblioteca será simples. Por exemplo, se você chamar a função [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) no momento para obter o local da pasta meus documentos, poderá substituir o valor [**KNOWNFOLDERID**](knownfolderid.md) da pasta meus documentos conhecidos pelo valor **KNOWNFOLDERID** da biblioteca correspondente.

A tabela a seguir mostra a relação entre os valores de [**KNOWNFOLDERID**](knownfolderid.md) de pastas conhecidas e o valor **KNOWNFOLDERID** da biblioteca correspondente no Windows 7. 

| Valores de KNOWNFOLDERID de pasta conhecidos | Valores de KNOWNFOLDERID de biblioteca |
|-----------------------------------|------------------------------|
| Documentos de FOLDERid \_               | PASTA de \_ DocumentsLibrary   |
| Imagens de FOLDERid \_                | PASTA de \_ PicturesLibrary    |
| PASTA de \_ músicas                   | PASTA de \_ MusicLibrary       |
| PASTA de \_ RecordedTV              | PASTA de \_ RecordedTVLibrary  |



 

### <a name="homegroup-and-shared-libraries"></a>Grupo doméstico e bibliotecas compartilhadas

Adicionar suporte de biblioteca ao seu programa permitirá o suporte para bibliotecas compartilhadas em um grupo doméstico. O grupo doméstico é identificado por seu valor de [**KNOWNFOLDERID**](knownfolderid.md) do [**\_ grupo de pastas**](knownfolderid.md). Seu programa pode localizar identificar o local de salvamento padrão particular ou compartilhado do usuário, definindo o valor [**DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) na chamada para o método [**IShellLibrary:: GetDefaultSaveFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder) .

## <a name="using-a-common-file-dialog-box-with-libraries"></a>Usando uma caixa de diálogo de arquivo comum com bibliotecas

Usando uma caixa de diálogo de arquivo comum com bibliotecas, a caixa de diálogo arquivo comum foi atualizada para dar suporte a bibliotecas no Windows 7. A ilustração a seguir mostra como a caixa de diálogo arquivo comum aparece para um usuário no Windows 7.

![captura de tela da caixa de diálogo arquivo comum mostrando bibliotecas](images/libraries-commonfiledialog.png)

No Windows 7, se seu programa atualmente exibir uma caixa de diálogo de arquivo comum e não alterar o modelo da caixa de diálogo nem vincular nenhum de seus eventos, ele exibirá a nova versão do Windows 7 da caixa de diálogo automaticamente. Especificamente, na chamada para a função de caixa de diálogo Common File, os membros **lpfnHook**, **HINSTANCE**, **lpTemplatename** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) devem ser **nulos** e os sinalizadores OFN **\_ ENABLEHOOK** e **OFN \_ ENABLETEMPLATE** devem ser claros.

No Windows 7, as interfaces relacionadas ao [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)substituem as funções comuns de caixa de diálogo de arquivo que foram usadas em versões anteriores do Windows. As funções anteriores da caixa de diálogo arquivo comum ainda têm suporte no Windows 7, mas não fornecem a experiência completa do usuário do Windows 7 e não oferecem suporte a bibliotecas. Alguns dos novos recursos com suporte nas interfaces relacionadas ao **IFileDialog** incluem:

-   O usuário pode acessar as propriedades de arquivo com suporte pelo Windows Explorer do Windows 7 para pesquisar e selecionar os arquivos.
-   O programa pode usar interfaces e métodos da API de namespace do Shell para trabalhar com os itens.
-   O programa pode usar um modelo de personalização controlado por dados em vez de um modelo de personalização controlado por arquivo-recurso para adicionar novos controles às caixas de diálogo de arquivo comuns.

Você deve usar as interfaces relacionadas ao [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)quando:

-   Você precisa personalizar a caixa de diálogo arquivo comum para seu programa no Windows 7. Isso permitirá que o seu programa trabalhe com bibliotecas e dê suporte à personalização da caixa de diálogo.
-   você deseja que o usuário possa selecionar vários arquivos em uma caixa de diálogo de arquivo comum. Isso garantirá que você obtenha os caminhos corretos para o objeto selecionado, pois uma biblioteca pode ter conteúdo armazenado em pastas diferentes.

Para obter mais informações sobre as interfaces relacionadas ao [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), consulte:

-   [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>Habilitando a seleção de biblioteca na interface do usuário

Se o seu programa permitir que o usuário selecione uma pasta, como para funções de importação ou exportação, no Windows 7, ele também deverá permitir que o usuário selecione uma biblioteca. A interface [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) e a função [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) permitem que o usuário selecione uma biblioteca quando for solicitado a selecionar uma pasta. A interface **IFileOpenDialog** é preferida sobre a função **SHBrowseForFolder** porque o **IFileOpenDialog** dá suporte à interface do usuário do Windows 7.

Para permitir que os usuários selecionem pastas ao usar a interface [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) , chame SetOptions com o \_ sinalizador FOS PICKFOLDERS definido e verifique se o \_ sinalizador FOS FORCEFILESYSTEM está claro.


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



Para permitir que os usuários selecionem pastas ao chamar a função SHBrowseForFolder, no membro ulFlags da estrutura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) , defina o \_ sinalizador BSE USENEWUI e desmarque o \_ sinalizador BSE RETURNONLYFSDIRS.


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>Acessando o conteúdo da biblioteca em um programa

Para acessar o conteúdo de uma biblioteca, você deve usar a API do shell do Windows. As funções da API do sistema de arquivos não podem ser usadas para acessar o conteúdo da biblioteca porque as bibliotecas não são objetos do sistema de arquivos. Se o seu programa usar um navegador de arquivos personalizado baseado na API do sistema de arquivos, ele não poderá procurar bibliotecas ou acessar o conteúdo da biblioteca.

Esta seção descreve como você pode acessar o conteúdo da biblioteca para que você possa selecionar a melhor maneira de atualizar o programa para trabalhar com bibliotecas.

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>Acessando o conteúdo da biblioteca com a interface IShellLibrary

A maneira mais fácil de um programa acessar o conteúdo da biblioteca é usar a [**API da biblioteca do Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary). Se você estiver trabalhando em um programa que usa a API do sistema de arquivos, a **API da biblioteca do Shell** poderá retornar as pastas do sistema de arquivos de uma biblioteca, o que minimiza a alteração em seu código de programa existente.


```C++
IShellLibrary *picturesLibrary;

hr = SHLoadLibraryFromKnownFolder(FOLDERID_PicturesLibrary, 
                                  STGM_READ, 
                                  IID_PPV_ARGS(&picturesLibrary));

// picturesLibrary now points to the user's picture library
    
IShellItemArray *pictureFolders; 

hr = pslLibrary->GetFolders(LFF_FORCEFILESYSTEM, IID_PPV_ARGS(&pictureFolders));

// pictureFolders now contains an array of Shell items that
// represent the folders found in the user's pictures library
```



### <a name="accessing-library-content-with-the-shell-apis"></a>Acessando o conteúdo da biblioteca com as APIs do Shell

Como os objetos de biblioteca fazem parte do modelo de programação shell, eles podem ser usados com outras APIs de shell do Windows. Por exemplo, você pode usar as interfaces [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) e [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) em seu programa, juntamente com funções auxiliares relacionadas, para acessar o conteúdo de uma biblioteca da mesma maneira como você enumeraria pastas e conteúdos de pasta para acessar o conteúdo com as APIs do sistema de arquivos.

As APIs do shell do Windows dão suporte a dois modos de enumeração para acessar o conteúdo de uma biblioteca:

-   **Procurar enumeração**

    Procurar enumeração é o modo de enumeração padrão e enumera o conteúdo de uma pasta de biblioteca. Desmarque o \_ sinalizador de enumeração de navegação SHCONTF \_ para usar esse modo.

-   **Enumeração de navegação**

    A enumeração de navegação enumera as pastas de biblioteca. Defina o \_ sinalizador de enumeração de navegação SHCONTF \_ para usar esse modo.

Se o seu programa usar um controle de árvore personalizado para navegar pelas pastas do usuário, a enumeração das pastas no modo de enumeração de navegação fornecerá uma lista das pastas de uma biblioteca que é consistente com o modo como o Windows Explorer enumera as pastas no Windows 7.

Para obter exemplos de como usar esses recursos em um programa, consulte o exemplo ShellStorage no SDK do Windows.

## <a name="saving-user-content-in-a-library"></a>Salvando o conteúdo do usuário em uma biblioteca

Seu programa pode salvar o conteúdo do usuário em uma biblioteca, bem como em uma pasta na biblioteca. Da mesma forma, o usuário pode salvar em uma pasta específica em uma biblioteca ou pode apenas salvar na biblioteca.

Cada biblioteca tem uma pasta que é designada como o local de salvamento padrão. O local de salvamento padrão é definido quando a biblioteca é criada; no entanto, o usuário pode reatribuir o local de salvamento padrão para qualquer pasta na biblioteca. Embora o usuário não precise configurar um local de salvamento padrão, ele tem a opção de alterá-lo. Se o usuário excluir a pasta que está definida atualmente como o local de salvamento padrão, a biblioteca configurará automaticamente a próxima pasta na biblioteca para ser o local de salvamento padrão.

Há várias maneiras de salvar o conteúdo do usuário em uma biblioteca.

-   **API do Shell**

    Se você estiver usando o modelo de programação shell e salvar um item de Shell, conforme representado por um [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem), IStorage ou IStream, em um objeto de biblioteca, o item de shell será armazenado automaticamente no local de salvamento padrão da biblioteca.

-   **API do sistema de arquivos**

    Se você tiver um programa existente que usa muitas chamadas à API do sistema de arquivos, poderá obter um caminho para a pasta que está definida como o local de salvamento padrão da biblioteca. O caminho da pasta pode ser passado para uma API do sistema de arquivos.

Para obter exemplos de como usar esses recursos em um programa, consulte o exemplo ShellStorage no SDK do Windows.

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>Suporte a operações de arrastar e soltar em uma biblioteca

Se o seu programa der suporte a ações de arrastar e soltar, elas deverão ser atualizadas para dar suporte à interação correta da biblioteca. Se um arquivo for descartado em uma biblioteca, o arquivo Descartado deverá ser salvo no local de salvamento padrão. Se uma pasta for descartada em uma biblioteca, a pasta descartada deverá ser adicionada como uma nova pasta à biblioteca. Se um arquivo for descartado em uma pasta existente que não seja o local de salvamento padrão, o arquivo deverá ser adicionado à pasta selecionada.

Para obter exemplos de como adicionar suporte à biblioteca para a funcionalidade de arrastar e soltar dos seus programas, consulte o exemplo ShellLibraryCommandLine no SDK do Windows.

## <a name="keeping-in-sync-with-a-library"></a>Mantendo a sincronização com uma biblioteca

Este tópico descreve como um programa pode manter sua exibição do conteúdo de uma biblioteca atualizada.

### <a name="bulk-update"></a>Atualização em Massa

Como o usuário pode modificar as pastas de uma biblioteca interativamente quando o programa não estiver em execução, seu programa deverá chamar [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) quando começar a descobrir e armazenar quaisquer alterações na biblioteca. A API do Shell fornece a função **SHResolveLibrary** para permitir que um programa obtenha o conteúdo atual de uma biblioteca e os locais atuais de qualquer pasta que a biblioteca possa conter.

Observe que [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) é uma função de bloqueio que pode levar muito tempo para retornar, dependendo do que foi alterado na biblioteca. Como tal, ele não deve ser chamado de um thread de interface do usuário.

Depois que o programa for atualizado, ele poderá se registrar para as notificações de alteração para manter uma exibição atual.

### <a name="shell-api-notification"></a>Notificação da API do Shell

A API do shell do Windows fornece a função [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) , que é a maneira preferida para que processos que não sejam de serviço sejam notificados sobre uma alteração na biblioteca.

Para detectar alterações em itens em uma biblioteca usando a API do shell do Windows, chame [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) para registrar seu programa para notificações de alterações em itens em uma pasta de biblioteca. Essa função pode notificar seu programa se houver uma alteração em qualquer biblioteca ou apenas em uma biblioteca específica. As notificações são enviadas imediatamente quando uma biblioteca é alterada.

### <a name="file-system-api-notification"></a>Notificação da API do sistema de arquivos

As notificações do sistema de arquivos devem ser usadas em processos de serviço.

Para detectar alterações em itens em uma biblioteca usando a API do sistema de arquivos, enumere as pastas na biblioteca e chame [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) para cada pasta a ser monitorada. Seu programa receberá uma notificação quando uma pasta monitorada for alterada. Para localizar o arquivo específico de arquivos que foram alterados na pasta, chame [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw). Para detectar alterações no arquivo de descrição da biblioteca, monitore a pasta que a contém. O arquivo de descrição da biblioteca pode ser encontrado na pasta [**\_ bibliotecas FolderId**](knownfolderid.md) . O arquivo de descrição da biblioteca, no entanto, não deve ser aberto ou modificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Links do Shell](./links.md)
</dt> <dt>

[Pastas conhecidas](known-folders.md)
</dt> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[**\_argumentos de PPV de IID \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
