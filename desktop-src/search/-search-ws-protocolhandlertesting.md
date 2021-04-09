---
description: Integralmente para testar e depurar suas implementações de manipulador de protocolo é entender como os manipuladores de protocolo são iniciados.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Depuração de manipuladores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090054"
---
# <a name="debugging-protocol-handlers"></a><span data-ttu-id="72ae6-103">Depuração de manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="72ae6-103">Debugging Protocol Handlers</span></span>

<span data-ttu-id="72ae6-104">Integralmente para testar e depurar suas implementações de manipulador de protocolo é entender como os manipuladores de protocolo são iniciados.</span><span class="sxs-lookup"><span data-stu-id="72ae6-104">Integral to testing and debugging your protocol handler implementations is understanding how protocol handlers are launched.</span></span>

<span data-ttu-id="72ae6-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="72ae6-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="72ae6-106">Sobre a depuração de manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="72ae6-106">About Debugging Protocol Handlers</span></span>](#about-debugging-protocol-handlers)
-   [<span data-ttu-id="72ae6-107">Configurando a depuração</span><span class="sxs-lookup"><span data-stu-id="72ae6-107">Setting Up Debugging</span></span>](#setting-up-debugging)
-   [<span data-ttu-id="72ae6-108">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="72ae6-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="72ae6-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72ae6-109">Related topics</span></span>](#related-topics)

## <a name="about-debugging-protocol-handlers"></a><span data-ttu-id="72ae6-110">Sobre a depuração de manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="72ae6-110">About Debugging Protocol Handlers</span></span>

<span data-ttu-id="72ae6-111">O processo SearchIndexer (searchindexer.exe) inicia uma cópia do processo SearchProtocolHost (SearchProtocolHost.exe) no contexto do sistema e outra cópia no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="72ae6-111">The SearchIndexer process (searchindexer.exe) launches one copy of the SearchProtocolHost process (SearchProtocolHost.exe) in the system context and another copy in the user context.</span></span> <span data-ttu-id="72ae6-112">Em seguida, os manipuladores de protocolo são carregados no processo SearchProtocolHost, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="72ae6-112">Then, the protocol handlers are loaded in the SearchProtocolHost process as needed.</span></span> <span data-ttu-id="72ae6-113">Eles não são descarregados até que o serviço de pesquisa seja interrompido.</span><span class="sxs-lookup"><span data-stu-id="72ae6-113">They are not unloaded until the search service is stopped.</span></span> <span data-ttu-id="72ae6-114">A mesma instância de um manipulador de protocolo é reutilizada quantas vezes o serviço estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="72ae6-114">The same instance of a protocol handler is reused any number of times while the service is running.</span></span>

<span data-ttu-id="72ae6-115">Os processos SearchIndexer e SearchProtocolHost se comunicam frequentemente durante a indexação.</span><span class="sxs-lookup"><span data-stu-id="72ae6-115">The SearchIndexer and SearchProtocolHost processes communicate frequently during indexing.</span></span> <span data-ttu-id="72ae6-116">Se você pausar ou parar o processo SearchProtocolHost para depurar, o SearchIndexer abrirá um novo processo SearchProtocolHost, invalidando a sessão de depuração.</span><span class="sxs-lookup"><span data-stu-id="72ae6-116">If you pause or stop the SearchProtocolHost process to debug, the SearchIndexer will launch a new SearchProtocolHost process, invalidating your debugging session.</span></span> <span data-ttu-id="72ae6-117">Além disso, se você anexar o depurador diretamente ao processo SearchProtocolHost, poderá interromper o identificador-herança de searchindexer.exe para searchprotocolhost.exe e os dois processos não poderão se comunicar.</span><span class="sxs-lookup"><span data-stu-id="72ae6-117">Also, if you attach your debugger directly to the SearchProtocolHost process, you can break handle-inheritance from searchindexer.exe to searchprotocolhost.exe, and the two processes will be unable to communicate.</span></span>

<span data-ttu-id="72ae6-118">Para evitar esses problemas, você precisa notificar o serviço de pesquisa que está Depurando, e você precisa anexar o depurador ao processo SearchIndexer com instruções para depurar processos filho, conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="72ae6-118">To avoid these problems, you need to notify the search service that you are debugging, and you need to attach the debugger to the SearchIndexer process with instructions to debug child processes, as described next.</span></span>

## <a name="setting-up-debugging"></a><span data-ttu-id="72ae6-119">Configurando a depuração</span><span class="sxs-lookup"><span data-stu-id="72ae6-119">Setting Up Debugging</span></span>

<span data-ttu-id="72ae6-120">Siga estas etapas para configurar a depuração para o manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="72ae6-120">Follow these steps to set up debugging for your protocol handler.</span></span>

1.  <span data-ttu-id="72ae6-121">Notifique o serviço de pesquisa que você está depurando definindo o valor de DebugFilters como 1 no registro:</span><span class="sxs-lookup"><span data-stu-id="72ae6-121">Notify the search service that you are debugging by setting the DebugFilters value to 1 in the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  <span data-ttu-id="72ae6-122">Anexar um depurador usando a chave do registro de opções de execução do arquivo de imagem:</span><span class="sxs-lookup"><span data-stu-id="72ae6-122">Attach a debugger using the Image File Execution Options registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    <span data-ttu-id="72ae6-123">As opções para um depurador de exemplo são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="72ae6-123">The options for a sample debugger are described in the following table.</span></span>

    

    <span data-ttu-id="72ae6-124">**Exemplo usando o depurador do depurador do NTSD**   *= C: \\ depuradores \\ntsd.exe-odGx-C: "sXe LD mydll.dll; g"*</span><span class="sxs-lookup"><span data-stu-id="72ae6-124">**Example using the ntsd debugger**   *Debugger = C:\\debuggers\\ntsd.exe -odGx -c: "sxe ld mydll.dll;g"*</span></span><br/>

3.  <span data-ttu-id="72ae6-125">Reinicie searchindexer.exe no depurador usando compmgmt. msc, Services. msc ou uma janela de comando com comandos semelhantes ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="72ae6-125">Restart searchindexer.exe under the debugger using compmgmt.msc, services.msc, or a command window with commands similar to the following:</span></span>
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

<span data-ttu-id="72ae6-126">Para distinguir entre um processo SearchProtocolHost em execução no contexto do sistema e outro em execução no contexto do usuário, você pode examinar as cadeias de caracteres do ambiente.</span><span class="sxs-lookup"><span data-stu-id="72ae6-126">To distinguish between a SearchProtocolHost process running in the system context and one running in the user context, you can review the environment strings.</span></span> <span data-ttu-id="72ae6-127">Com ntsd.exe, por exemplo, você pode usar o comando de extensão **! PEB** para exibir uma exibição formatada das informações no bloco de ambiente do processo (PEB).</span><span class="sxs-lookup"><span data-stu-id="72ae6-127">With ntsd.exe, for example, you can use extension command **!peb** to display a formatted view of the information in the process environment block (PEB).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72ae6-128">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="72ae6-128">Additional Resources</span></span>

-   <span data-ttu-id="72ae6-129">Para obter informações sobre como criar manipuladores, consulte [registrando extensões de shell](../shell/reg-shell-exts.md).</span><span class="sxs-lookup"><span data-stu-id="72ae6-129">For information on creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="72ae6-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72ae6-130">Related topics</span></span>

<dl> <span data-ttu-id="72ae6-131"><dt><a href="-search-3x-wds-phaddins.md">Manipuladores de protocolos de desenvolvimento</a></dt> <dt>**conceituados**</dt> que <dt><a href="-search-3x-wds-extidx-prot-implementing.md">compreendem manipuladores de protocolo</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">notificando o índice das alterações</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">adicionando ícones e menus de contexto</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">exemplo de código: extensões de Shell para manipuladores de protocolo</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">criando um conector de pesquisa para um manipulador de protocolo</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Instalando e Registrando manipuladores de protocolo</a></dt> </span><span class="sxs-lookup"><span data-stu-id="72ae6-131"><dt>**Conceptual**</dt> <dt><a href="-search-3x-wds-phaddins.md">Developing Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Understanding Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">Notifying the Index of Changes</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Adding Icons and Context Menus</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">Code Sample: Shell Extensions for Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">Creating a Search Connector for a Protocol Handler</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Installing and Registering Protocol Handlers</a></dt> </span></span></dl>

 

 
