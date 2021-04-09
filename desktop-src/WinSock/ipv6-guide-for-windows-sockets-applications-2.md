---
description: Este guia fornece as informações necessárias para permitir que seu aplicativo do Microsoft Windows Use a próxima geração de protocolo de Internet, versão 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guia IPv6 para aplicativos do Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090381"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a><span data-ttu-id="d4be8-103">Guia IPv6 para aplicativos do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d4be8-103">IPv6 Guide for Windows Sockets Applications</span></span>

<span data-ttu-id="d4be8-104">Este guia fornece as informações necessárias para permitir que seu aplicativo do Microsoft Windows Use a próxima geração de protocolo de Internet, versão 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="d4be8-104">This guide provides the information you need to enable your Microsoft Windows application to use the next generation of Internet Protocol, version 6 (IPv6).</span></span> <span data-ttu-id="d4be8-105">A adição do recurso IPv6 ao seu aplicativo não é necessariamente um processo de portabilidade.</span><span class="sxs-lookup"><span data-stu-id="d4be8-105">Adding IPv6 capability to your application is not necessarily a porting process.</span></span> <span data-ttu-id="d4be8-106">Para portar um aplicativo sugere a modificação do código para funcionar em uma plataforma diferente, o que implica deixar a plataforma anterior por trás.</span><span class="sxs-lookup"><span data-stu-id="d4be8-106">To port an application suggests modifying code to work on a different platform, which implies leaving the previous platform behind.</span></span> <span data-ttu-id="d4be8-107">Este guia é especificamente estruturado para ajudar a adicionar funcionalidades IPv6 a um aplicativo e, ao mesmo tempo, manter a funcionalidade IPv4.</span><span class="sxs-lookup"><span data-stu-id="d4be8-107">This guide is specifically structured to help add IPv6 capability to an application while retaining IPv4 functionality.</span></span>

<span data-ttu-id="d4be8-108">Este guia aborda os problemas associados à adição da funcionalidade IPv6 e, em seguida, direciona as áreas de desenvolvimento mais afetadas pela transição.</span><span class="sxs-lookup"><span data-stu-id="d4be8-108">This guide discusses the issues associated with adding IPv6 functionality, then targets the areas of development most affected by the transition.</span></span> <span data-ttu-id="d4be8-109">Cada área recebe uma explicação completa das armadilhas a serem observadas, as estratégias sugeridas para evitá-las e dicas sobre como fazer o melhor uso de novos elementos programáticos do [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funções e estruturas).</span><span class="sxs-lookup"><span data-stu-id="d4be8-109">Each area receives a thorough explanation of the pitfalls to watch out for, the strategies suggested to avoid them, and tips on how to make the best use of new [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) programmatic elements (functions and structures).</span></span> <span data-ttu-id="d4be8-110">Para obter informações adicionais sobre o IPv6, consulte [suporte a IPv6](ipv6-support-2.md).</span><span class="sxs-lookup"><span data-stu-id="d4be8-110">For additional information on IPv6, see [IPv6 Support](ipv6-support-2.md).</span></span>

<span data-ttu-id="d4be8-111">Este guia também fornece exemplos de código para dar a você experiência prática e representações visuais dos problemas que você pode encontrar ao modificar seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d4be8-111">This guide also provides code examples to give you hands-on experience and visual representations of the issues you could encounter when modifying your applications.</span></span> <span data-ttu-id="d4be8-112">Os exemplos vêm de exemplos completos e funcionais de um aplicativo simples do Windows Sockets que foi modificado para dar suporte a IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="d4be8-112">The examples come from complete, working examples of a simple Windows Sockets application that has been modified to support both IPv4 and IPv6.</span></span> <span data-ttu-id="d4be8-113">O código-fonte para esses exemplos de trabalho está incluído em sua totalidade em dois apêndices no final deste documento: [Apêndice A: o código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md) inclui o código-fonte de um aplicativo antes que ele seja modificado para dar suporte a IPv6; [Apêndice B: o código-fonte independente da versão IP](appendix-b-ip-version-agnostic-source-code-2.md) fornece o código-fonte após o aplicativo ter sido habilitado para IPv6.</span><span class="sxs-lookup"><span data-stu-id="d4be8-113">Source code for these working examples is included in its entirety in two appendixes at the end of this document: [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) includes the source code for an application before it is modified to support IPv6; [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md) provides the source code after the application has been IPv6-enabled.</span></span>

<span data-ttu-id="d4be8-114">A Microsoft fornece um utilitário chamado Checkv4.exe que ajuda você a encontrar código potencialmente sensível à portabilidade no código do aplicativo e também faz recomendações para correções.</span><span class="sxs-lookup"><span data-stu-id="d4be8-114">Microsoft provides a utility called Checkv4.exe that helps you find potentially porting-sensitive code in your application code, and also makes recommendations for fixes.</span></span> <span data-ttu-id="d4be8-115">O utilitário Checkv4.exe é demonstrado neste documento, usando o aplicativo de exemplo incluído nos apêndices, juntamente com capturas de tela que exibem a saída que o utilitário Checkv4.exe produz.</span><span class="sxs-lookup"><span data-stu-id="d4be8-115">The Checkv4.exe utility is demonstrated in this document, using the sample application included in the appendixes, along with screen shots displaying the output that the Checkv4.exe utility produces.</span></span> <span data-ttu-id="d4be8-116">Para obter mais informações, consulte [usando o utilitário Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="d4be8-116">For more information, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>

<span data-ttu-id="d4be8-117">As áreas de programação abordadas por este guia são:</span><span class="sxs-lookup"><span data-stu-id="d4be8-117">The programming areas addressed by this guide are:</span></span>

-   [<span data-ttu-id="d4be8-118">Alterando estruturas de dados para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="d4be8-118">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
-   [<span data-ttu-id="d4be8-119">Chamadas de função para aplicativos Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="d4be8-119">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
-   [<span data-ttu-id="d4be8-120">Uso de endereços IPv4 codificados</span><span class="sxs-lookup"><span data-stu-id="d4be8-120">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
-   [<span data-ttu-id="d4be8-121">Problemas de interface do usuário para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="d4be8-121">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
-   [<span data-ttu-id="d4be8-122">Protocolos subjacentes para aplicativos Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="d4be8-122">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
-   [<span data-ttu-id="d4be8-123">Soquetes de pilha dupla para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="d4be8-123">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)

<span data-ttu-id="d4be8-124">Como não há nenhuma sequência uniforme de eventos, as seções que resolvem problemas de habilitação de IPv6 não são organizadas de maneira sequencialmente significativa, para que você possa fazer referência a qualquer seção a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="d4be8-124">Because there is no uniform sequence of events, the sections that address IPv6-enabling issues are not arranged in a sequentially significant manner, so you can reference any section at any time.</span></span> <span data-ttu-id="d4be8-125">É altamente recomendável que você examine cada seção enquanto adiciona a funcionalidade IPv6 ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4be8-125">It is strongly recommended that you review each section while adding IPv6 capability to your application.</span></span> <span data-ttu-id="d4be8-126">Também é aconselhável ler sobre o utilitário Checkv4.exe, pois ele inclui dicas sobre a ordem em que os problemas de habilitação do IPv6 são abordados.</span><span class="sxs-lookup"><span data-stu-id="d4be8-126">It is also advisable to read about the Checkv4.exe utility, as it includes tips on the order in which to address IPv6-enabling issues.</span></span>

<span data-ttu-id="d4be8-127">Para examinar o utilitário Checkv4.exe e examinar a ordem na qual você deve abordar o processo de portabilidade em seus aplicativos, consulte [usando o utilitário Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="d4be8-127">To look at the Checkv4.exe utility, and to review the order in which you should approach the porting process in your applications, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span> <span data-ttu-id="d4be8-128">Esta seção inclui informações sobre um sinalizador de tempo de compilação que verifica estritamente os elementos de programação incompatíveis com o IPv6.</span><span class="sxs-lookup"><span data-stu-id="d4be8-128">This section includes information on a compile-time flag that strictly checks for programming elements incompatible with IPv6.</span></span>

<span data-ttu-id="d4be8-129">Para ir direto para o aplicativo de exemplo, consulte [o apêndice a: código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md) e [Apêndice B: código-fonte independente da versão IP](appendix-b-ip-version-agnostic-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="d4be8-129">To go straight to the sample application, see [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) and [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4be8-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4be8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4be8-131">Protocolo IP versão 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="d4be8-131">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="d4be8-132">Suporte a IPv6</span><span class="sxs-lookup"><span data-stu-id="d4be8-132">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="d4be8-133">Versão prévia da tecnologia IPv6 para Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d4be8-133">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[<span data-ttu-id="d4be8-134">Usando o utilitário Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="d4be8-134">Using the Checkv4.exe Utility</span></span>](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[<span data-ttu-id="d4be8-135">Apêndice A: código-fonte somente IPv4</span><span class="sxs-lookup"><span data-stu-id="d4be8-135">Appendix A: IPv4-only Source Code</span></span>](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[<span data-ttu-id="d4be8-136">Apêndice B: código-fonte independente da versão IP</span><span class="sxs-lookup"><span data-stu-id="d4be8-136">Appendix B: IP-version Agnostic Source Code</span></span>](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



