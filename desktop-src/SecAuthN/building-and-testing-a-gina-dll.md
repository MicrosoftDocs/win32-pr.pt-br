---
description: Todas as funções, protótipos, estruturas e constantes são definidas no arquivo de cabeçalho Winwlx. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Criando e testando uma DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298058"
---
# <a name="building-and-testing-a-gina-dll"></a><span data-ttu-id="3055e-103">Criando e testando uma DLL GINA</span><span class="sxs-lookup"><span data-stu-id="3055e-103">Building and Testing a GINA DLL</span></span>

<span data-ttu-id="3055e-104">Todas as funções, protótipos, estruturas e constantes são definidas no arquivo de cabeçalho Winwlx. h.</span><span class="sxs-lookup"><span data-stu-id="3055e-104">All functions, prototypes, structures, and constants are defined in the Winwlx.h header file.</span></span>

> [!Note]  
> <span data-ttu-id="3055e-105">As DLLs GINAs são ignoradas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3055e-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="3055e-106">Para testar uma dll [*Gina*](/windows/desktop/SecGloss/g-gly) , use o Winlogon.exe de uma versão verificada do sistema operacional, que está disponível com o Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="3055e-106">To test a [*GINA*](/windows/desktop/SecGloss/g-gly) DLL, use the Winlogon.exe from a checked version of the operating system, which is available with the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="3055e-107">A versão verificada do [*Winlogon*](/windows/desktop/SecGloss/w-gly) dá suporte à depuração de ginas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3055e-107">The checked version of [*Winlogon*](/windows/desktop/SecGloss/w-gly) supports debugging GINAs as follows:</span></span>

-   <span data-ttu-id="3055e-108">Você pode usar a sintaxe a seguir para criar uma seção em Win.ini para especificar opções de depuração do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="3055e-108">You can use the following syntax to create a section in Win.ini to specify Winlogon debugging options.</span></span>

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    <span data-ttu-id="3055e-109">Se especificado, o **logfile** deverá conter o nome totalmente qualificado do arquivo que será usado para registrar informações de depuração.</span><span class="sxs-lookup"><span data-stu-id="3055e-109">If specified, **LogFile** should contain the fully qualified name of the file that will be used to log debugging information.</span></span> <span data-ttu-id="3055e-110">Se o arquivo não existir, ele será criado.</span><span class="sxs-lookup"><span data-stu-id="3055e-110">If the file does not exist, it will be created.</span></span>

    <span data-ttu-id="3055e-111">As opções **DebugFlags** especificam quais tipos de informações de depuração gravar no arquivo de log ou depurador.</span><span class="sxs-lookup"><span data-stu-id="3055e-111">The **DebugFlags** options specify which kinds of debugging information to write to the log file, or debugger.</span></span> <span data-ttu-id="3055e-112">**DebugFlags** pode conter um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3055e-112">**DebugFlags** can contain one or more of the following flags.</span></span>

    

    | <span data-ttu-id="3055e-113">Sinalizador de depuração</span><span class="sxs-lookup"><span data-stu-id="3055e-113">Debugging flag</span></span> | <span data-ttu-id="3055e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3055e-114">Description</span></span>                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="3055e-115">CoolSwitch</span><span class="sxs-lookup"><span data-stu-id="3055e-115">CoolSwitch</span></span>     | <span data-ttu-id="3055e-116">A combinação de teclas CTRL + ALT + SHIFT + TAB causará uma interrupção de depuração no Winlogon.</span><span class="sxs-lookup"><span data-stu-id="3055e-116">The CTRL+ALT+SHIFT+TAB key combination will cause a debug break in Winlogon.</span></span>                                                                                               |
    | <span data-ttu-id="3055e-117">Erro</span><span class="sxs-lookup"><span data-stu-id="3055e-117">Error</span></span>          | <span data-ttu-id="3055e-118">Erros de impressão.</span><span class="sxs-lookup"><span data-stu-id="3055e-118">Print errors.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="3055e-119">Init</span><span class="sxs-lookup"><span data-stu-id="3055e-119">Init</span></span>           | <span data-ttu-id="3055e-120">Imprimir mensagens de inicialização e progresso.</span><span class="sxs-lookup"><span data-stu-id="3055e-120">Print initialization and progress messages.</span></span>                                                                                                                                |
    | <span data-ttu-id="3055e-121">Notificar</span><span class="sxs-lookup"><span data-stu-id="3055e-121">Notify</span></span>         | <span data-ttu-id="3055e-122">Imprimir mensagens do pacote de notificação.</span><span class="sxs-lookup"><span data-stu-id="3055e-122">Print notification package messages.</span></span>                                                                                                                                       |
    | <span data-ttu-id="3055e-123">SAS</span><span class="sxs-lookup"><span data-stu-id="3055e-123">SAS</span></span>            | <span data-ttu-id="3055e-124">Imprimir informações sobre notificações de [*sequência de atenção segura*](/windows/desktop/SecGloss/s-gly) (SAS).</span><span class="sxs-lookup"><span data-stu-id="3055e-124">Print information about [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) notifications.</span></span> |
    | <span data-ttu-id="3055e-125">Estado</span><span class="sxs-lookup"><span data-stu-id="3055e-125">State</span></span>          | <span data-ttu-id="3055e-126">Imprimir mensagens quando o Winlogon mudar de estado.</span><span class="sxs-lookup"><span data-stu-id="3055e-126">Print messages when Winlogon changes state.</span></span>                                                                                                                                |
    | <span data-ttu-id="3055e-127">Tempo limite</span><span class="sxs-lookup"><span data-stu-id="3055e-127">Timeout</span></span>        | <span data-ttu-id="3055e-128">Imprimir mensagens quando um limite de tempo for definido ou um limite de tempo for atingido.</span><span class="sxs-lookup"><span data-stu-id="3055e-128">Print messages when a time limit is set or a time limit is reached.</span></span>                                                                                                        |
    | <span data-ttu-id="3055e-129">Trace</span><span class="sxs-lookup"><span data-stu-id="3055e-129">Trace</span></span>          | <span data-ttu-id="3055e-130">Imprimir informações de rastreamento detalhado.</span><span class="sxs-lookup"><span data-stu-id="3055e-130">Print verbose trace information.</span></span>                                                                                                                                           |
    | <span data-ttu-id="3055e-131">Aviso</span><span class="sxs-lookup"><span data-stu-id="3055e-131">Warn</span></span>           | <span data-ttu-id="3055e-132">Imprimir avisos.</span><span class="sxs-lookup"><span data-stu-id="3055e-132">Print warnings.</span></span>                                                                                                                                                            |

    

     

-   <span data-ttu-id="3055e-133">Para iniciar a versão verificada do Winlogon em um depurador, adicione a seguinte entrada ao registro:</span><span class="sxs-lookup"><span data-stu-id="3055e-133">To start the checked version of Winlogon in a debugger, add the following entry to the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> <span data-ttu-id="3055e-134">Você deve usar o depurador simbólico do Windows (NTSD) para depurar o Winlogon.</span><span class="sxs-lookup"><span data-stu-id="3055e-134">You must use the Windows symbolic debugger (NTSD) to debug Winlogon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3055e-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3055e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3055e-136">Carregando e executando uma DLL GINA</span><span class="sxs-lookup"><span data-stu-id="3055e-136">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="3055e-137">Funções de exportação GINA</span><span class="sxs-lookup"><span data-stu-id="3055e-137">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="3055e-138">Estruturas GINA</span><span class="sxs-lookup"><span data-stu-id="3055e-138">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="3055e-139">Funções de GINA de serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="3055e-139">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
