---
description: Os aplicativos podem controlar o local do qual uma DLL é carregada, especificando um caminho completo ou usando outro mecanismo, como um manifesto. Se esses métodos não forem usados, o sistema pesquisará a DLL no tempo de carregamento, conforme descrito neste tópico.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Ordem de pesquisa da biblioteca de Dynamic-Link
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 928cf9030e24c91145ae95e1eed680017bf68533
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/04/2021
ms.locfileid: "104500120"
---
# <a name="dynamic-link-library-search-order"></a>Ordem de pesquisa da biblioteca de Dynamic-Link

Um sistema pode conter várias versões da mesma DLL (biblioteca de vínculo dinâmico). Os aplicativos podem controlar o local do qual uma DLL é carregada, especificando um caminho completo ou usando outro mecanismo, como um manifesto. Se esses métodos não forem usados, o sistema pesquisará a DLL no tempo de carregamento, conforme descrito neste tópico.

-   [Fatores que afetam a pesquisa](#factors-that-affect-searching)
-   [Ordem de pesquisa para aplicativos UWP](#search-order-for-uwp-apps)
    -   [Ordem de pesquisa padrão para aplicativos UWP](#standard-search-order-for-uwp-apps)
    -   [Ordem de pesquisa alternativa para aplicativos UWP](#alternate-search-order-for-uwp-apps)
-   [Ordem de pesquisa para aplicativos da área de trabalho](#search-order-for-desktop-applications)
    -   [Ordem de pesquisa padrão para aplicativos da área de trabalho](#standard-search-order-for-desktop-applications)
    -   [Ordem de pesquisa alternativa para aplicativos de área de trabalho](#alternate-search-order-for-desktop-applications)
    -   [Ordem de pesquisa usando sinalizadores de **\_ \_ pesquisa da biblioteca de carregamento**](/windows)
-   [Tópicos relacionados](#related-topics)

## <a name="factors-that-affect-searching"></a>Fatores que afetam a pesquisa

Os seguintes fatores afetam se o sistema procura uma DLL:

-   Se uma DLL com o mesmo nome de módulo já estiver carregada na memória, o sistema verificará apenas o redirecionamento e um manifesto antes de resolver para a DLL carregada, não importa em qual diretório ele está. O sistema não pesquisa a DLL.
-   Se a DLL estiver na lista de DLLs conhecidas para a versão do Windows na qual o aplicativo está sendo executado, o sistema usará sua cópia da DLL conhecida (e as DLLs dependentes da DLL conhecida, se houver) em vez de Pesquisar a DLL. Para obter uma lista de DLLs conhecidas no sistema atual, consulte a seguinte chave do registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.
-   Se uma DLL tiver dependências, o sistema pesquisará as DLLs dependentes como se elas fossem carregadas com apenas seus nomes de módulo. Isso é verdadeiro mesmo que a primeira DLL tenha sido carregada especificando um caminho completo.

## <a name="search-order-for-uwp-apps"></a>Ordem de pesquisa para aplicativos UWP

Quando um aplicativo UWP para Windows 10 (ou um aplicativo da Store para Windows 8. x) carrega um módulo empacotado chamando a função [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) , a DLL deve estar no grafo de dependência do pacote do processo. Para obter mais informações, consulte **LoadPackagedLibrary**. Quando um aplicativo UWP carrega um módulo por outros meios e não especifica um caminho completo, o sistema procura a DLL e suas dependências no tempo de carregamento, conforme descrito nesta seção.

Antes que o sistema procure uma DLL, ele verifica o seguinte:

-   Se uma DLL com o mesmo nome de módulo já estiver carregada na memória, o sistema usará a DLL carregada, não importa em qual diretório ele está. O sistema não pesquisa a DLL.
-   Se a DLL estiver na lista de DLLs conhecidas para a versão do Windows na qual o aplicativo está sendo executado, o sistema usará sua cópia da DLL conhecida (e as DLLs dependentes da DLL conhecida, se houver). O sistema não pesquisa a DLL. Para obter uma lista de DLLs conhecidas no sistema atual, consulte a seguinte chave do registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.

Se o sistema precisar pesquisar um módulo ou suas dependências, ele sempre usará a ordem de pesquisa para aplicativos UWP, mesmo se uma dependência não for um código de aplicativo UWP.

### <a name="standard-search-order-for-uwp-apps"></a>Ordem de pesquisa padrão para aplicativos UWP

Se o módulo ainda não estiver carregado ou na lista de DLLs conhecidas, o sistema pesquisará esses locais nesta ordem:

1.  O grafo de dependência do pacote do processo. Esse é o pacote do aplicativo, além de quaisquer dependências especificadas como `<PackageDependency>` na `<Dependencies>` seção do manifesto do pacote do aplicativo. As dependências são pesquisadas na ordem em que aparecem no manifesto.
2.  O diretório do qual o processo de chamada foi carregado.
3.  O diretório do sistema (% SystemRoot% \\ System32).

Se uma DLL tiver dependências, o sistema pesquisará as DLLs dependentes como se elas fossem carregadas com apenas seus nomes de módulo. Isso é verdadeiro mesmo que a primeira DLL tenha sido carregada especificando um caminho completo.

### <a name="alternate-search-order-for-uwp-apps"></a>Ordem de pesquisa alternativa para aplicativos UWP

Se um módulo alterar a ordem de pesquisa padrão chamando a função [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) com **Load \_ com \_ o \_ \_ caminho de pesquisa alterado**, o sistema pesquisará o diretório no qual o módulo especificado foi carregado, em vez do diretório do processo de chamada. O sistema pesquisa esses locais nesta ordem:

1.  O grafo de dependência do pacote do processo. Esse é o pacote do aplicativo, além de quaisquer dependências especificadas como `<PackageDependency>` na `<Dependencies>` seção do manifesto do pacote do aplicativo. As dependências são pesquisadas na ordem em que aparecem no manifesto.
2.  O diretório do qual o módulo especificado foi carregado.
3.  O diretório do sistema (% SystemRoot% \\ System32).

## <a name="search-order-for-desktop-applications"></a>Ordem de pesquisa para aplicativos da área de trabalho

Os aplicativos de área de trabalho podem controlar o local do qual uma DLL é carregada, especificando um caminho completo, usando o [redirecionamento de dll](dynamic-link-library-redirection.md)ou usando um [manifesto](/windows/desktop/SbsCs/manifests). Se nenhum desses métodos for usado, o sistema pesquisará a DLL no tempo de carregamento, conforme descrito nesta seção.

Antes que o sistema procure uma DLL, ele verifica o seguinte:

-   Se uma DLL com o mesmo nome de módulo já estiver carregada na memória, o sistema usará a DLL carregada, não importa em qual diretório ele está. O sistema não pesquisa a DLL.
-   Se a DLL estiver na lista de DLLs conhecidas para a versão do Windows na qual o aplicativo está sendo executado, o sistema usará sua cópia da DLL conhecida (e as DLLs dependentes da DLL conhecida, se houver). O sistema não pesquisa a DLL. Para obter uma lista de DLLs conhecidas no sistema atual, consulte a seguinte chave do registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.

Se uma DLL tiver dependências, o sistema pesquisará as DLLs dependentes como se elas fossem carregadas com apenas seus nomes de módulo. Isso é verdadeiro mesmo que a primeira DLL tenha sido carregada especificando um caminho completo.

> [!IMPORTANT]
> Se um invasor obtiver o controle de um dos diretórios que é pesquisado, ele poderá fazer uma cópia mal-intencionada da DLL nesse diretório. Para obter maneiras de ajudar a evitar esses ataques, consulte [segurança da biblioteca de vínculo dinâmico](dynamic-link-library-security.md).

### <a name="standard-search-order-for-desktop-applications"></a>Ordem de pesquisa padrão para aplicativos da área de trabalho

A ordem de pesquisa padrão da DLL usada pelo sistema depende de se o modo de pesquisa de DLL seguro está habilitado ou desabilitado. O modo de pesquisa de DLL seguro coloca o diretório atual do usuário mais tarde na ordem de pesquisa.

O modo de pesquisa de DLL seguro é habilitado por padrão. Para desabilitar esse recurso, crie o valor do registro **HKEY \_ local \_ System do \\ sistema \\ CurrentControlSet \\ Control \\ Session Manager** \\ **SafeDllSearchMode** e defina-o como 0. Chamar a função [**SetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) efetivamente desabilita **SafeDllSearchMode** enquanto o diretório especificado está no caminho de pesquisa e altera a ordem de pesquisa, conforme descrito neste tópico.

Se **SafeDllSearchMode** estiver habilitado, a ordem de pesquisa será a seguinte:

1.  O diretório do qual o aplicativo foi carregado.
2.  O diretório do sistema. Use a função [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obter o caminho desse diretório.
3.  O diretório do sistema de 16 bits. Não há nenhuma função que obtenha o caminho desse diretório, mas ela é pesquisada.
4.  O diretório do Windows. Use a função [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obter o caminho desse diretório.
5.  O diretório atual.
6.  Os diretórios listados na variável de ambiente PATH. Observe que isso não inclui o caminho por aplicativo especificado pela chave do registro de **caminhos do aplicativo** . A chave de **caminhos do aplicativo** não é usada ao calcular o caminho de pesquisa da dll.

Se **SafeDllSearchMode** estiver desabilitado, a ordem de pesquisa será a seguinte:

1.  O diretório do qual o aplicativo foi carregado.
2.  O diretório atual.
3.  O diretório do sistema. Use a função [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obter o caminho desse diretório.
4.  O diretório do sistema de 16 bits. Não há nenhuma função que obtenha o caminho desse diretório, mas ela é pesquisada.
5.  O diretório do Windows. Use a função [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obter o caminho desse diretório.
6.  Os diretórios listados na variável de ambiente PATH. Observe que isso não inclui o caminho por aplicativo especificado pela chave do registro de **caminhos do aplicativo** . A chave de **caminhos do aplicativo** não é usada ao calcular o caminho de pesquisa da dll.

### <a name="alternate-search-order-for-desktop-applications"></a>Ordem de pesquisa alternativa para aplicativos de área de trabalho

A ordem de pesquisa padrão usada pelo sistema pode ser alterada chamando a função [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) com **Load \_ com o \_ \_ \_ caminho de pesquisa alterado**. A ordem de pesquisa padrão também pode ser alterada chamando a função [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) .

> [!NOTE]
> A ordem de pesquisa padrão do processo também será afetada chamando a função [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) no processo pai antes do início do processo atual.

Se você especificar uma estratégia de pesquisa alternativa, seu comportamento continuará até que todos os módulos executáveis associados tenham sido localizados. Depois que o sistema inicia o processamento de rotinas de inicialização de DLL, o sistema reverte para a estratégia de pesquisa padrão.

A função [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) dará suporte a uma ordem de pesquisa alternativa se a chamada especificar **Load com o \_ \_ \_ \_ caminho de pesquisa alterado** e o parâmetro *lpFileName* especificar um caminho absoluto.

Observe que a estratégia de pesquisa padrão e a estratégia de pesquisa alternativa especificada por [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) com **carga \_ com o \_ \_ \_ caminho de pesquisa alterado** diferem de apenas uma maneira: a pesquisa padrão começa no diretório do aplicativo de chamada e a pesquisa alternativa começa no diretório do módulo executável que o **LoadLibraryEx** está carregando.

Se **SafeDllSearchMode** estiver habilitado, a ordem de pesquisa alternativa será a seguinte:

1.  O diretório especificado por *lpFileName*.
2.  O diretório do sistema. Use a função [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obter o caminho desse diretório.
3.  O diretório do sistema de 16 bits. Não há nenhuma função que obtenha o caminho desse diretório, mas ela é pesquisada.
4.  O diretório do Windows. Use a função [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obter o caminho desse diretório.
5.  O diretório atual.
6.  Os diretórios listados na variável de ambiente PATH. Observe que isso não inclui o caminho por aplicativo especificado pela chave do registro de **caminhos do aplicativo** . A chave de **caminhos do aplicativo** não é usada ao calcular o caminho de pesquisa da dll.

Se **SafeDllSearchMode** estiver desabilitado, a ordem de pesquisa alternativa será a seguinte:

1.  O diretório especificado por *lpFileName*.
2.  O diretório atual.
3.  O diretório do sistema. Use a função [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obter o caminho desse diretório.
4.  O diretório do sistema de 16 bits. Não há nenhuma função que obtenha o caminho desse diretório, mas ela é pesquisada.
5.  O diretório do Windows. Use a função [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obter o caminho desse diretório.
6.  Os diretórios listados na variável de ambiente PATH. Observe que isso não inclui o caminho por aplicativo especificado pela chave do registro de **caminhos do aplicativo** . A chave de **caminhos do aplicativo** não é usada ao calcular o caminho de pesquisa da dll.

A função [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) dará suporte a uma ordem de pesquisa alternativa se o parâmetro *lpPathName* especificar um caminho. A ordem de pesquisa alternativa é a seguinte:

1.  O diretório do qual o aplicativo foi carregado.
2.  O diretório especificado pelo parâmetro *lpPathName* de [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya).
3.  O diretório do sistema. Use a função [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) para obter o caminho desse diretório. O nome desse diretório é system32.
4.  O diretório do sistema de 16 bits. Não há nenhuma função que obtenha o caminho desse diretório, mas ela é pesquisada. O nome desse diretório é System.
5.  O diretório do Windows. Use a função [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para obter o caminho desse diretório.
6.  Os diretórios listados na variável de ambiente PATH. Observe que isso não inclui o caminho por aplicativo especificado pela chave do registro de **caminhos do aplicativo** . A chave de **caminhos do aplicativo** não é usada ao calcular o caminho de pesquisa da dll.

Se o parâmetro *lpPathName* for uma cadeia de caracteres vazia, a chamada removerá o diretório atual da ordem de pesquisa.

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) efetivamente desabilita o modo de pesquisa de dll seguro enquanto o diretório especificado está no caminho de pesquisa. Para restaurar o modo de pesquisa de DLL seguro com base no valor de registro **SafeDllSearchMode** e restaurar o diretório atual para a ordem de pesquisa, chame **SetDllDirectory** com *lpPathName* como nulo.

### <a name="search-order-using-load_library_search-flags"></a>Ordem de pesquisa usando sinalizadores de **\_ \_ pesquisa da biblioteca de carregamento**

Um aplicativo pode especificar uma ordem de pesquisa usando um ou mais sinalizadores de **\_ \_ pesquisa da biblioteca de carregamento** com a função [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) . Um aplicativo também pode usar sinalizadores de **\_ \_ pesquisa da biblioteca de carregamento** com a função [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) para estabelecer uma ordem de pesquisa de dll para um processo. O aplicativo pode especificar diretórios adicionais para a ordem de pesquisa da DLL de processo usando as funções [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) ou [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) .

Os diretórios pesquisados dependem dos sinalizadores especificados com [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Se mais de um sinalizador for usado, os diretórios correspondentes serão pesquisados na seguinte ordem:

1.  O diretório que contém a DLL (**Load \_ library \_ Search \_ dll \_ de \_ carregamento da biblioteca de carregamento**). Esse diretório é pesquisado apenas para dependências da DLL a serem carregadas.
2.  O diretório do aplicativo (**Load \_ library Search Directory \_ \_ \_ dir**).
3.  Caminhos adicionados explicitamente com a função [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) (**diretórios de \_ usuário de pesquisa da biblioteca \_ \_ \_ de carregamento**) ou a função [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) . Se mais de um caminho tiver sido adicionado, a ordem na qual os caminhos são pesquisados não será especificada.
4.  O diretório do sistema (**Load \_ library \_ Search \_ System32**).

Se o aplicativo não chamar [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) com nenhum sinalizador **de \_ \_ pesquisa de biblioteca de carga** ou estabelecer uma ordem de pesquisa de dll para o processo, o sistema pesquisará DLLs usando a ordem de pesquisa padrão ou a ordem de pesquisa alternativa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[registro de Aplicativo](/windows/desktop/shell/app-registration)
</dt> <dt>

[Redirecionamento de biblioteca de vínculo dinâmico](dynamic-link-library-redirection.md)
</dt> <dt>

[Segurança da biblioteca de vínculo dinâmico](dynamic-link-library-security.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
</dt> <dt>

[**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)
</dt> <dt>

[**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)
</dt> <dt>

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)
</dt> <dt>

[Componentes lado a lado](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)
</dt> </dl>

 

 