---
description: Usando o utilitário Checkv4.exe para modificar seu aplicativo IPv4 para dar suporte ao IPv6.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Usando o utilitário Checkv4.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558370"
---
# <a name="using-the-checkv4exe-utility"></a><span data-ttu-id="00f38-103">Usando o utilitário Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="00f38-103">Using the Checkv4.exe utility</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00f38-104">O utilitário *Checkv4.exe* não é fornecido no SDK (Kit de desenvolvimento de software) do Windows para Windows 8, nem em versões posteriores do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="00f38-104">The *Checkv4.exe* utility doesn't ship in the Windows Software Development Kit (SDK) for Windows 8, nor in later versions of the Windows SDK.</span></span>

<span data-ttu-id="00f38-105">O utilitário *Checkv4.exe* foi projetado para fornecer um parceiro de porta de código; um utilitário que percorre sua base de código com você, identifica possíveis problemas ou realça código que pode se beneficiar de funções ou estruturas compatíveis com IPv6 e faz recomendações.</span><span class="sxs-lookup"><span data-stu-id="00f38-105">The *Checkv4.exe* utility is designed to provide you with a code porting partner; a utility that steps through your code base with you, identifies potential problems or highlights code that could benefit from IPv6-capable functions or structures, and makes recommendations.</span></span> <span data-ttu-id="00f38-106">Com o utilitário Checkv4.exe, a tarefa de modificar um aplicativo IPv4 existente para dar suporte ao IPv6 torna-se muito mais fácil.</span><span class="sxs-lookup"><span data-stu-id="00f38-106">With the Checkv4.exe utility, the task of modifying an existing IPv4 application to support IPv6 becomes much easier.</span></span>

<span data-ttu-id="00f38-107">O utilitário *Checkv4.exe* é instalado como parte do SDK (Software Development Kit) do Microsoft Windows lançado para o Windows Vista e SDKs posteriores (até, mas não incluindo, o SDK (Software Development Kit) do Windows para Windows 8).</span><span class="sxs-lookup"><span data-stu-id="00f38-107">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later SDKs (up to, but not including, the Windows Software Development Kit (SDK) for Windows 8).</span></span>

<span data-ttu-id="00f38-108">Uma versão anterior do utilitário de *Checkv4.exe* com recursos mais limitados também foi disponibilizada como parte do Microsoft IPv6 Technology Preview anterior para Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="00f38-108">An earlier version of the *Checkv4.exe* utility with more limited features was also made available as part of the earlier Microsoft IPv6 Technology Preview for Windows 2000.</span></span>

<span data-ttu-id="00f38-109">As seções a seguir descrevem como usar o utilitário *Checkv4.exe* e, em seguida, explicam a abordagem recomendada para modificar um aplicativo IPv4 existente para dar suporte ao IPv6.</span><span class="sxs-lookup"><span data-stu-id="00f38-109">The following sections describe how to use the *Checkv4.exe* utility, then explain the recommended approach for modifying an existing IPv4 application to support IPv6.</span></span>

## <a name="recommendations-for-running-checkv4exe"></a><span data-ttu-id="00f38-110">Recomendações para execução de Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="00f38-110">Recommendations for Running Checkv4.exe</span></span>

-   <span data-ttu-id="00f38-111">O utilitário *Checkv4.exe* é simples.</span><span class="sxs-lookup"><span data-stu-id="00f38-111">The *Checkv4.exe* utility is straightforward.</span></span> <span data-ttu-id="00f38-112">Basta executar *Checkv4.exe* na linha de comando com o nome do arquivo que você deseja verificar como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="00f38-112">Simply execute *Checkv4.exe* at the command line with the name of the file you want to check as the parameter.</span></span> <span data-ttu-id="00f38-113">*Checkv4.exe* analisa o arquivo e fornece comentários sobre onde existem problemas de porta IPv6 nesse arquivo.</span><span class="sxs-lookup"><span data-stu-id="00f38-113">*Checkv4.exe* parses the file and provides feedback as to where IPv6 porting issues exist in that file.</span></span> <span data-ttu-id="00f38-114">Colocar o *Checkv4.exe* no caminho do computador torna a execução do utilitário de *Checkv4.exe* de qualquer lugar em sua estrutura de diretórios de código-fonte muito mais fácil.</span><span class="sxs-lookup"><span data-stu-id="00f38-114">Placing the *Checkv4.exe* into your computer's path makes running the *Checkv4.exe* utility from anywhere in your source code directory structure much easier.</span></span> <span data-ttu-id="00f38-115">Por exemplo, colocar *Checkv4.exe* em% windir% permite que você inicie o *Checkv4.exe* de qualquer diretório no computador sem incluir seu caminho.</span><span class="sxs-lookup"><span data-stu-id="00f38-115">For example, placing *Checkv4.exe* into %windir% enables you to launch *Checkv4.exe* from any directory on your computer without including its path.</span></span>

-   <span data-ttu-id="00f38-116">Emita o seguinte comando no prompt de comando para analisar o arquivo Simplec. c:</span><span class="sxs-lookup"><span data-stu-id="00f38-116">Issue the following command at the command prompt to parse the file Simplec.c:</span></span>

    <span data-ttu-id="00f38-117">**Checkv4 simplec. c**</span><span class="sxs-lookup"><span data-stu-id="00f38-117">**Checkv4 simplec.c**</span></span>

    <span data-ttu-id="00f38-118">Observe que algumas das recomendações feitas pelo utilitário de *Checkv4.exe* exigem estruturas disponíveis somente em versões recentes do arquivo de cabeçalho *Ws2tcpip. h* , como a estrutura **SOCKADDR \_ In6** .</span><span class="sxs-lookup"><span data-stu-id="00f38-118">Note that some of the recommendations made by the *Checkv4.exe* utility require structures available only in recent versions of the *Ws2tcpip.h* header file, such as the **SOCKADDR\_IN6** structure.</span></span> <span data-ttu-id="00f38-119">Esses arquivos de cabeçalho estão incluídos no SDK do Windows lançado para Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="00f38-119">These header files are included in the Windows SDK released for Windows Vista and later.</span></span> <span data-ttu-id="00f38-120">Esses arquivos de cabeçalho também estão incluídos no SDK (Kit de desenvolvimento de software) da plataforma anterior lançado para o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="00f38-120">These header files are also included in the earlier Platform Software Development Kit (SDK) released for Windows Server 2003.</span></span> <span data-ttu-id="00f38-121">Esses arquivos de cabeçalho também são incluídos como parte de uma assinatura do MSDN ou por download.</span><span class="sxs-lookup"><span data-stu-id="00f38-121">These header files are also included as part of an MSDN subscription or by download.</span></span>

    <span data-ttu-id="00f38-122">A captura de tela a seguir exibe os resultados do uso do utilitário *Checkv4.exe* no arquivo Simplec. c incluído no apêndice A:</span><span class="sxs-lookup"><span data-stu-id="00f38-122">The following screen shot displays the results of using the *Checkv4.exe* utility on the Simplec.c file included in Appendix A:</span></span>

    ![checkv4.exe relata incompatibilidades de IPv6 no arquivo simplec. c](images/portingguide002.jpg)

    <span data-ttu-id="00f38-124">A captura de tela a seguir exibe os resultados do uso do utilitário *Checkv4.exe* no arquivo simples. c, que também está incluído no apêndice A:</span><span class="sxs-lookup"><span data-stu-id="00f38-124">The following screen shot displays the results of using the *Checkv4.exe* utility on the Simples.c file, which is also included in Appendix A:</span></span>

    ![checkv4.exe relata incompatibilidades de IPv6 no arquivo simples. c](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a><span data-ttu-id="00f38-126">O processo de modificação do aplicativo: onde começar</span><span class="sxs-lookup"><span data-stu-id="00f38-126">The Application Modification Process: Where to Start</span></span>

<span data-ttu-id="00f38-127">Há um procedimento recomendado associado à adição do recurso IPv6 aos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="00f38-127">There is a recommended procedure associated with adding IPv6 capability to applications.</span></span> <span data-ttu-id="00f38-128">Seguir essa sequência é benéfico, pois permite aos desenvolvedores garantir que todas as etapas necessárias para modificar um aplicativo IPv4 existente para dar suporte ao IPv6 sejam tiradas.</span><span class="sxs-lookup"><span data-stu-id="00f38-128">Following this sequence is beneficial, because it enables developers to ensure that all steps necessary to modify an existing IPv4 application to support IPv6 are taken.</span></span> <span data-ttu-id="00f38-129">Determinados aplicativos podem exigir uma atenção mais abrangente para uma dessas sequências; por exemplo, um serviço do sistema provavelmente terá menos problemas de interface do usuário do que um FTP (programa de transferência de arquivos) gráfico.</span><span class="sxs-lookup"><span data-stu-id="00f38-129">Certain applications may require more extensive attention to one of these sequences; for example, a system service would likely have less user interface issues than a graphical file transfer program (FTP).</span></span>

<span data-ttu-id="00f38-130">**Para modificar aplicativos IPv4 para dar suporte a IPv6**</span><span class="sxs-lookup"><span data-stu-id="00f38-130">**To modify IPv4 applications to support IPv6**</span></span>

1.  <span data-ttu-id="00f38-131">Corrija estruturas e declarações para habilitar a compatibilidade com IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="00f38-131">Fix structures and declarations to enable IPv6 and IPv4 compatibility.</span></span>
2.  <span data-ttu-id="00f38-132">Modifique as chamadas de função para tirar proveito das funções habilitadas para IPv6, como as funções [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="00f38-132">Modify function calls to take advantage of IPv6-enabled functions, such as the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>
3.  <span data-ttu-id="00f38-133">Revise o código-fonte para o uso de endereços IPv4 embutidos em código, como o endereço de loopback ou o uso de outras cadeias de caracteres literais.</span><span class="sxs-lookup"><span data-stu-id="00f38-133">Review source code for the use of hard-coded IPv4 addresses such as the loopback address, or the use of other literal strings.</span></span>
4.  <span data-ttu-id="00f38-134">Execute uma revisão completa da interface do usuário, incluindo caixas de diálogo informativas.</span><span class="sxs-lookup"><span data-stu-id="00f38-134">Perform a thorough review of the user interface, including informational dialog boxes.</span></span> <span data-ttu-id="00f38-135">Pense se é apropriado para os aplicativos habilitados para IPv6 especificar ou fornecer informações baseadas em endereço IP.</span><span class="sxs-lookup"><span data-stu-id="00f38-135">Give thought to whether it is appropriate for IPv6-enabled applications to specify or provide IP-address based information.</span></span>
5.  <span data-ttu-id="00f38-136">Determine se seu aplicativo depende de protocolos subjacentes, como RPC, e faça as alterações programáticas apropriadas para lidar com endereços IPv6.</span><span class="sxs-lookup"><span data-stu-id="00f38-136">Determine whether your application relies on underlying protocols, such as RPC, and make appropriate programmatic changes to handle IPv6 addresses.</span></span>
6.  <span data-ttu-id="00f38-137">Use o sinalizador de tempo de compilação IPV6STRICT ao compilar aplicativos no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="00f38-137">Use the compile-time flag IPV6STRICT when compiling applications on Windows XP and later.</span></span> <span data-ttu-id="00f38-138">Esse sinalizador resulta na falha da compilação de um código incompatível, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="00f38-138">This flag results in incompatible code failing to compile, as follows:</span></span>

    <span data-ttu-id="00f38-139">Aplicativos do Windows Sockets 1. x com código incompatível falha ao compilar e retornar a mensagem de erro "WINSOCK2 necessário".</span><span class="sxs-lookup"><span data-stu-id="00f38-139">Windows Sockets 1.x applications with incompatible code fail to compile and return the error message "WINSOCK2 Required."</span></span>

    <span data-ttu-id="00f38-140">Os aplicativos do Windows Sockets 2. x com código incompatível causam um erro de tempo de compilação para cada instância de código incompatível.</span><span class="sxs-lookup"><span data-stu-id="00f38-140">Windows Sockets 2.x applications with incompatible code cause a compile time error for each instance of incompatible code.</span></span> <span data-ttu-id="00f38-141">Uma mensagem de erro é gerada no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="00f38-141">An error message is generated in the following format:</span></span>

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    <span data-ttu-id="00f38-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="00f38-142">For example:</span></span>

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



