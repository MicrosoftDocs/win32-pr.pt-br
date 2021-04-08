---
description: A API do auxiliar de protocolo de Internet (IP Helper) permite a recuperação e a modificação de definições de configuração de rede para o computador local.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827053"
---
# <a name="ip-helper"></a><span data-ttu-id="19d02-103">Auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="19d02-103">IP Helper</span></span>

## <a name="purpose"></a><span data-ttu-id="19d02-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="19d02-104">Purpose</span></span>

<span data-ttu-id="19d02-105">A API do auxiliar de protocolo de Internet (IP Helper) permite a recuperação e a modificação de definições de configuração de rede para o computador local.</span><span class="sxs-lookup"><span data-stu-id="19d02-105">The Internet Protocol Helper (IP Helper) API enables the retrieval and modification of network configuration settings for the local computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="19d02-106">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="19d02-106">Where applicable</span></span>

<span data-ttu-id="19d02-107">A API auxiliar de IP é aplicável em qualquer ambiente computacional no qual a manipulação programática da rede e da configuração de TCP/IP é útil.</span><span class="sxs-lookup"><span data-stu-id="19d02-107">The IP Helper API is applicable in any computing environment where programmatically manipulating network and TCP/IP configuration is useful.</span></span> <span data-ttu-id="19d02-108">Os aplicativos típicos incluem protocolos de roteamento IP e agentes SNMP (Simple Network Management Protocol).</span><span class="sxs-lookup"><span data-stu-id="19d02-108">Typical applications include IP routing protocols and Simple Network Management Protocol (SNMP) agents.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="19d02-109">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="19d02-109">Developer audience</span></span>

<span data-ttu-id="19d02-110">A API auxiliar de IP foi projetada para ser usada por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="19d02-110">The IP Helper API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="19d02-111">Os programadores também devem estar familiarizados com os conceitos de rede do Windows e de rede TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="19d02-111">Programmers should also be familiar with Windows networking and TCP/IP networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="19d02-112">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="19d02-112">Run-time requirements</span></span>

<span data-ttu-id="19d02-113">A API auxiliar de IP pode ser usada em todas as plataformas Windows.</span><span class="sxs-lookup"><span data-stu-id="19d02-113">The IP Helper API can be used on all Windows platforms.</span></span> <span data-ttu-id="19d02-114">Nem todos os sistemas operacionais dão suporte a todas as funções.</span><span class="sxs-lookup"><span data-stu-id="19d02-114">Not all operating systems support all functions.</span></span> <span data-ttu-id="19d02-115">Quando determinadas implementações ou recursos de restrições de plataforma do Windows Sockets 2 existem, eles são claramente indicados na documentação.</span><span class="sxs-lookup"><span data-stu-id="19d02-115">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span> <span data-ttu-id="19d02-116">Se uma função auxiliar de IP for chamada em uma plataforma que não oferece suporte à função, o erro \_ não \_ terá suporte será retornado.</span><span class="sxs-lookup"><span data-stu-id="19d02-116">If an IP Helper function is called on a platform that does not support the function, ERROR\_NOT\_SUPPORTED is returned.</span></span> <span data-ttu-id="19d02-117">Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte as seções de requisitos na documentação do.</span><span class="sxs-lookup"><span data-stu-id="19d02-117">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19d02-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="19d02-118">In this section</span></span>



| <span data-ttu-id="19d02-119">Tópico</span><span class="sxs-lookup"><span data-stu-id="19d02-119">Topic</span></span>                                                              | <span data-ttu-id="19d02-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="19d02-120">Description</span></span>                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19d02-121">O que há de novo no auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="19d02-121">What's New in IP Helper</span></span>](what-s-new-in-ip-helper.md)<br/>  | <span data-ttu-id="19d02-122">Informações sobre novos recursos para o auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="19d02-122">Information on new features for IP Helper.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="19d02-123">Sobre o auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="19d02-123">About IP Helper</span></span>](about-ip-helper.md)<br/>                  | <span data-ttu-id="19d02-124">Informações gerais sobre as considerações e os recursos de programação do auxiliar de IP disponíveis para os desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="19d02-124">General information about IP Helper programming considerations and capabilities available to developers.</span></span><br/>                                                                                               |
| [<span data-ttu-id="19d02-125">Usando o auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="19d02-125">Using IP Helper</span></span>](using-ip-helper.md)<br/>                  | <span data-ttu-id="19d02-126">Procedimentos e técnicas de programação usados com o auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="19d02-126">Procedures and programming techniques used with IP Helper.</span></span> <span data-ttu-id="19d02-127">Esta seção inclui técnicas básicas de programação de IP auxiliar, como [introdução com o auxiliar de IP](getting-started-with-ip-helper.md).</span><span class="sxs-lookup"><span data-stu-id="19d02-127">This section includes basic IP Helper programming techniques, such as [Getting Started With IP Helper](getting-started-with-ip-helper.md).</span></span><br/> |
| [<span data-ttu-id="19d02-128">Referência auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="19d02-128">IP Helper reference</span></span>](ip-helper-function-reference.md)<br/> | <span data-ttu-id="19d02-129">Documentação de referência para as funções, estruturas e enumerações do IP Helper.</span><span class="sxs-lookup"><span data-stu-id="19d02-129">Reference documentation for the IP Helper functions, structures, and enumerations.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="19d02-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19d02-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19d02-131">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="19d02-131">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="19d02-132">Serviço de Roteamento e Acesso Remoto</span><span class="sxs-lookup"><span data-stu-id="19d02-132">Routing and Remote Access Service</span></span>](../rras/routing-start-page.md)
</dt> </dl>

 

