---
description: Esta seção descreve as extensões do Winsock específicas para intercâmbio de pacotes de Internet/Intercâmbio de pacotes sequenciados (IPX/SPX). Ele também descreve aspectos de funções Winsock base que exigem uma consideração especial ou que podem apresentar comportamento exclusivo.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Anexo de IPX/SPX do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773009"
---
# <a name="winsock-ipxspx-annex"></a><span data-ttu-id="f7cfa-104">Anexo de IPX/SPX do Winsock</span><span class="sxs-lookup"><span data-stu-id="f7cfa-104">Winsock IPX/SPX Annex</span></span>

<span data-ttu-id="f7cfa-105">Esta seção descreve as extensões do Winsock específicas para intercâmbio de pacotes de Internet/Intercâmbio de pacotes sequenciados (IPX/SPX).</span><span class="sxs-lookup"><span data-stu-id="f7cfa-105">This section describes Winsock extensions specific to Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX).</span></span> <span data-ttu-id="f7cfa-106">Ele também descreve aspectos de funções Winsock base que exigem uma consideração especial ou que podem apresentar comportamento exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f7cfa-106">It also describes aspects of base Winsock functions that either require special consideration or may exhibit unique behavior.</span></span>



| <span data-ttu-id="f7cfa-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7cfa-107">Element</span></span>          | <span data-ttu-id="f7cfa-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7cfa-108">Description</span></span>                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7cfa-109">Nome (s) de protocolo</span><span class="sxs-lookup"><span data-stu-id="f7cfa-109">Protocol name(s)</span></span> | <span data-ttu-id="f7cfa-110">IPX, SPX</span><span class="sxs-lookup"><span data-stu-id="f7cfa-110">IPX, SPX</span></span>                                                                                                                                        |
| <span data-ttu-id="f7cfa-111">Description</span><span class="sxs-lookup"><span data-stu-id="f7cfa-111">Description</span></span>      | <span data-ttu-id="f7cfa-112">Fornece serviços de transporte pela camada de rede IPX: IPX para datagramas não confiáveis, SPX para fluxos de mensagens confiáveis e orientados a conexão.</span><span class="sxs-lookup"><span data-stu-id="f7cfa-112">Provides transport services over the IPX networking layer: IPX for unreliable datagrams, SPX for reliable, connection-oriented message streams.</span></span> |
| <span data-ttu-id="f7cfa-113">Família de endereços</span><span class="sxs-lookup"><span data-stu-id="f7cfa-113">Address family</span></span>   | <span data-ttu-id="f7cfa-114">\_IPX AF</span><span class="sxs-lookup"><span data-stu-id="f7cfa-114">AF\_IPX</span></span>                                                                                                                                         |
| <span data-ttu-id="f7cfa-115">Arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f7cfa-115">Header file</span></span>      | <span data-ttu-id="f7cfa-116">Wsipx. h</span><span class="sxs-lookup"><span data-stu-id="f7cfa-116">Wsipx.h</span></span>                                                                                                                                         |



 

<span data-ttu-id="f7cfa-117">Esta seção discute como usar o Winsock com a família de protocolos IPX, permitindo que os aplicativos IPX tradicionais sejam portados para o Winsock.</span><span class="sxs-lookup"><span data-stu-id="f7cfa-117">This section discusses how to use Winsock with the IPX family of protocols, enabling traditional IPX applications to be ported to Winsock.</span></span> <span data-ttu-id="f7cfa-118">As redes IPX operam de maneira fundamentalmente diferente das redes IP, portanto, essas diferenças devem ser consideradas ao usar o IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="f7cfa-118">IPX networks operate in a fundamentally different manner than IP networks, so such differences must be considered when using IPX/SPX.</span></span>

 

 



