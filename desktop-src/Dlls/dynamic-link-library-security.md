---
description: Quando um aplicativo carrega dinamicamente uma biblioteca de vínculo dinâmico sem especificar um nome de caminho totalmente qualificado, o Windows tenta localizar a DLL pesquisando um conjunto bem definido de diretórios em uma ordem específica, conforme descrito em Dynamic-Link ordem de pesquisa da biblioteca. Se um invasor obtiver o controle de um dos diretórios no caminho de pesquisa da DLL, ele poderá fazer uma cópia mal-intencionada da DLL nesse diretório. Isso às vezes é chamado de ataque de pré-carregamento de DLL ou um ataque de binary planting.
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Segurança da biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4016139762461784702ac0190c1ee65d8bc6e72d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759001"
---
# <a name="dynamic-link-library-security"></a>Segurança da biblioteca de Dynamic-Link

Quando um aplicativo carrega dinamicamente uma biblioteca de vínculo dinâmico sem especificar um nome de caminho totalmente qualificado, o Windows tenta localizar a DLL pesquisando um conjunto bem definido de diretórios em uma ordem específica, conforme descrito em [ordem de pesquisa da biblioteca de vínculo dinâmico](dynamic-link-library-search-order.md). Se um invasor obtiver o controle de um dos diretórios no caminho de pesquisa da DLL, ele poderá fazer uma cópia mal-intencionada da DLL nesse diretório. Isso às vezes é chamado de *ataque de pré-carregamento de dll* ou um ataque de *Binary planting*. Se o sistema não encontrar uma cópia legítima da DLL antes de Pesquisar no diretório comprometido, ele carregará a DLL mal-intencionada. Se o aplicativo estiver sendo executado com privilégios de administrador, o invasor poderá ter sucesso na elevação de privilégio local.

Por exemplo, suponha que um aplicativo seja projetado para carregar uma DLL do diretório atual do usuário e falhar normalmente se a DLL não for encontrada. O aplicativo chama [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) apenas com o nome da dll, o que faz com que o sistema procure a dll. Supondo que o modo de pesquisa de DLL seguro esteja habilitado e o aplicativo não esteja usando uma ordem de pesquisa alternativa, o sistema pesquisará os diretórios na seguinte ordem:

1.  O diretório do qual o aplicativo foi carregado.
2.  O diretório do sistema.
3.  O diretório do sistema de 16 bits.
4.  O diretório do Windows.
5.  O diretório atual.
6.  Os diretórios listados na variável de ambiente PATH.

Continuando o exemplo, um invasor com conhecimento do aplicativo obtém o controle do diretório atual e coloca uma cópia mal-intencionada da DLL nesse diretório. Quando o aplicativo emite a chamada **LoadLibrary** , o sistema procura a dll, localiza a cópia mal-INTENCIONADA da dll no diretório atual e a carrega. A cópia mal-intencionada da DLL é executada dentro do aplicativo e obtém os privilégios do usuário.

Os desenvolvedores podem ajudar a proteger seus aplicativos contra ataques de pré-carregamento de DLL seguindo estas diretrizes:

-   Sempre que possível, especifique um caminho totalmente qualificado ao usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)ou [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) .
-   Use os sinalizadores de pesquisa da biblioteca de carregamento \_ \_ com a função [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) ou use esses sinalizadores com a função [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) para estabelecer uma ordem de pesquisa de dll para um processo e, em seguida, use as funções [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) ou [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) para modificar a lista. Para obter mais informações, consulte [ordem de pesquisa da biblioteca de vínculo dinâmico](dynamic-link-library-search-order.md).

    **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Esses sinalizadores e funções estão disponíveis em sistemas com o [KB2533623](https://support.microsoft.com/kb/2533623) instalado.

-   Em sistemas com o [KB2533623](https://support.microsoft.com/kb/2533623) instalado, use os \_ sinalizadores de pesquisa da biblioteca de carregamento \_ com a função [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) ou use esses sinalizadores com a função [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) para estabelecer uma ordem de pesquisa de dll para um processo e, em seguida, use as funções [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) ou [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) para modificar a lista. Para obter mais informações, consulte [ordem de pesquisa da biblioteca de vínculo dinâmico](dynamic-link-library-search-order.md).
-   Considere usar o [redirecionamento de dll](dynamic-link-library-redirection.md) ou um [manifesto](/windows/desktop/SbsCs/manifests) para garantir que seu aplicativo use a dll correta.
-   Ao usar a ordem de pesquisa padrão, verifique se o modo de pesquisa de DLL seguro está habilitado. Isso colocará o diretório atual do usuário mais tarde na ordem de pesquisa, aumentando as chances de o Windows encontrar uma cópia legítima da DLL antes de uma cópia mal-intencionada. O modo de pesquisa de dll seguro é habilitado por padrão a partir do Windows XP com Service Pack 2 (SP2) e é controlado pelo valor de registro de SafeDllSearchMode do **\_ sistema de \_ máquina local \\ \\ CurrentControlSet \\ Control \\ Session Manager** \\  . Para obter mais informações, consulte [ordem de pesquisa da biblioteca de vínculo dinâmico](dynamic-link-library-search-order.md).
-   Considere remover o diretório atual do caminho de pesquisa padrão chamando [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) com uma cadeia de caracteres vazia (""). Isso deve ser feito uma vez no início da inicialização do processo, não antes e depois das chamadas para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Lembre-se de que o **SetDllDirectory** afeta todo o processo e que vários threads que chamam **SetDllDirectory** com valores diferentes podem causar um comportamento indefinido. Se seu aplicativo carregar DLLs de terceiros, teste cuidadosamente para identificar as incompatibilidades.
-   Não use a função [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para recuperar um caminho para uma dll para uma chamada de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) subsequente, a menos que o modo de pesquisa de processo seguro esteja habilitado. Quando o modo de pesquisa de processo seguro não está habilitado, a função **SearchPath** usa uma ordem de pesquisa diferente de **LoadLibrary** e provavelmente procura primeiro o diretório atual do usuário na DLL especificada. Para habilitar o modo de pesquisa de processo seguro para a função **SearchPath** , use a função [**SetSearchPathMode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) com o caminho de pesquisa de base \_ habilitar o \_ \_ \_ \_ searchmode seguro. Isso move o diretório atual para o final da lista de pesquisa do **SearchPath** para a vida útil do processo. Observe que o diretório atual não é removido do caminho de pesquisa, portanto, se o sistema não encontrar uma cópia legítima da DLL antes de atingir o diretório atual, o aplicativo ainda estará vulnerável. Assim como com [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya), chamar **SetSearchPathMode** deve ser feito antecipadamente na inicialização do processo e afeta todo o processo. Se seu aplicativo carregar DLLs de terceiros, teste cuidadosamente para identificar as incompatibilidades.
-   Não faça suposições sobre a versão do sistema operacional com base em uma chamada [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) que procura por uma dll. Se o aplicativo estiver em execução em um ambiente em que a DLL está legitimamente ausente, mas uma cópia mal-intencionada da DLL estiver no caminho de pesquisa, a cópia mal-intencionada da DLL poderá ser carregada. Em vez disso, use as técnicas recomendadas descritas em [obtendo a versão do sistema](/windows/desktop/SysInfo/getting-the-system-version).

A ferramenta Process Monitor pode ser usada para ajudar a identificar as operações de carregamento de DLL que podem estar vulneráveis. A ferramenta Process Monitor pode ser baixada de <https://technet.microsoft.com/sysinternals/bb896645.aspx> .

O procedimento a seguir descreve como usar o Process Monitor para examinar as operações de carregamento de DLL em seu aplicativo.

**Para usar o Process Monitor para examinar as operações de carregamento de DLL em seu aplicativo**

1.  Inicie o Process Monitor.
2.  No Process Monitor, inclua os seguintes filtros:
    -   A operação é CreateFile
    -   A operação é LoadImage
    -   Caminho contém. cpl
    -   Caminho contém. dll
    -   Caminho contém. drv
    -   Caminho contém. exe
    -   Caminho contém. ocx
    -   Caminho contém. SCR
    -   Caminho contém. sys
3.  Exclua os seguintes filtros:
    -   O nome do processo é procmon.exe
    -   O nome do processo é Procmon64.exe
    -   O nome do processo é System
    -   A operação começa com IRP \_ MJ\_
    -   A operação começa com FASTIO\_
    -   O resultado é SUCCESS
    -   O caminho termina com pagefile.sys
4.  Tente iniciar o aplicativo com o diretório atual definido como um diretório específico. Por exemplo, clique duas vezes em um arquivo com uma extensão cujo manipulador de arquivo é atribuído ao seu aplicativo.
5.  Verifique a saída do monitor de processos para caminhos que parecem suspeitos, como uma chamada para o diretório atual para carregar uma DLL. Esse tipo de chamada pode indicar uma vulnerabilidade em seu aplicativo.

 

 
