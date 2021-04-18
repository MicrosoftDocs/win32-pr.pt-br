---
description: Ao transformar o código de atualização da célula de vida, várias diretrizes para escrever aplicativos de rede de alto desempenho foram descobertas.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Práticas recomendadas para aplicativos interativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771356"
---
# <a name="best-practices-for-interactive-applications"></a><span data-ttu-id="a32df-103">Práticas recomendadas para aplicativos interativos</span><span class="sxs-lookup"><span data-stu-id="a32df-103">Best Practices for Interactive Applications</span></span>

<span data-ttu-id="a32df-104">Ao transformar o código de atualização da célula de vida, várias diretrizes para escrever aplicativos de rede de alto desempenho foram descobertas.</span><span class="sxs-lookup"><span data-stu-id="a32df-104">In morphing the Life cell update code, several guidelines for writing high performance network applications have been uncovered.</span></span> <span data-ttu-id="a32df-105">Algumas estratégias gerais a serem aplicadas ao escrever esses tipos de aplicativos são:</span><span class="sxs-lookup"><span data-stu-id="a32df-105">Some general strategies to apply when writing these types of applications are:</span></span>

-   <span data-ttu-id="a32df-106">Torne o fluxo de dados o máximo possível, em vez de entrar em partes.</span><span class="sxs-lookup"><span data-stu-id="a32df-106">Make the data stream as much as possible, rather than going in chunks.</span></span>
-   <span data-ttu-id="a32df-107">Use algumas transações grandes em vez de muitas pequenas.</span><span class="sxs-lookup"><span data-stu-id="a32df-107">Use a few large transactions rather than many small ones.</span></span> <span data-ttu-id="a32df-108">As transações grandes também podem ser transmitidas com eficiência.</span><span class="sxs-lookup"><span data-stu-id="a32df-108">Large transactions can also be efficiently streamed.</span></span>
-   <span data-ttu-id="a32df-109">Reconheça que a rede é um recurso lento e não confiável e desenvolva cada aplicativo para minimizar sua dependência na rede.</span><span class="sxs-lookup"><span data-stu-id="a32df-109">Recognize that the network is a slow, unreliable resource and develop each application to minimize its reliance on the network.</span></span>
-   <span data-ttu-id="a32df-110">Use uma representação bem arquitetada dos dados na rede.</span><span class="sxs-lookup"><span data-stu-id="a32df-110">Use a well-architected representation of the data on the network.</span></span> <span data-ttu-id="a32df-111">A representação de dados deve ser independente da arquitetura do computador, não conter FAT e possivelmente compactada.</span><span class="sxs-lookup"><span data-stu-id="a32df-111">The data representation should be computer-architecture agnostic, contain no fat, and possibly be compressed.</span></span>
-   <span data-ttu-id="a32df-112">Durante a inicialização e o desligamento, não faça o usuário esperar que a rede seja inicializada ou desligada.</span><span class="sxs-lookup"><span data-stu-id="a32df-112">During initialization and shutdown, do not make the user wait for the network to start up or shut down.</span></span> <span data-ttu-id="a32df-113">A inicialização relacionada à rede pode levar um tempo relativamente longo.</span><span class="sxs-lookup"><span data-stu-id="a32df-113">Network related initialization could take a relatively long time.</span></span> <span data-ttu-id="a32df-114">Separe o código de rede não crítico.</span><span class="sxs-lookup"><span data-stu-id="a32df-114">Separate the noncritical network code.</span></span>
-   <span data-ttu-id="a32df-115">Manipule erros conforme apropriado para seu impacto.</span><span class="sxs-lookup"><span data-stu-id="a32df-115">Handle errors as appropriate to their impact.</span></span> <span data-ttu-id="a32df-116">Nem todos os erros são críticos.</span><span class="sxs-lookup"><span data-stu-id="a32df-116">Not all errors are critical.</span></span> <span data-ttu-id="a32df-117">Implemente mecanismos de recuperação e forneça comentários de usuários não intrusivos.</span><span class="sxs-lookup"><span data-stu-id="a32df-117">Implement recovery mechanisms and provide nonintrusive user feedback.</span></span>
-   <span data-ttu-id="a32df-118">Use RPC (chamadas de procedimento remoto) somente quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="a32df-118">Use remote procedure calls (RPC) only when appropriate.</span></span> <span data-ttu-id="a32df-119">O RPC é síncrono no Windows me/98 e sempre resulta em protocolos de Fat informais quando usados para enviar pequenas quantidades de dados.</span><span class="sxs-lookup"><span data-stu-id="a32df-119">RPC is synchronous on Windows Me/98 and always results in chatty, fat protocols when used to send small amounts of data.</span></span>
-   <span data-ttu-id="a32df-120">Meça sua sobrecarga de rede usando netstat; Você pode ficar surpreso com o que suas medidas revelam.</span><span class="sxs-lookup"><span data-stu-id="a32df-120">Measure your network overhead using Netstat; you may be surprised at what your measurements reveal.</span></span>
-   <span data-ttu-id="a32df-121">Teste o aplicativo em uma variedade de redes, especialmente redes lentas ou sujeitas a perda.</span><span class="sxs-lookup"><span data-stu-id="a32df-121">Test the application on a variety of networks, especially slow or loss-prone networks.</span></span> <span data-ttu-id="a32df-122">Redes LAN sem fio, Modems e VPN (redes virtuais privadas) pela Internet são boas redes para teste.</span><span class="sxs-lookup"><span data-stu-id="a32df-122">Wireless LAN networks, modems, and virtual private networks (VPN) over the Internet are good networks for testing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a32df-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a32df-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a32df-124">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a32df-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



