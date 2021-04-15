---
description: Uma rede é exibida como o mecanismo de transporte que transmite dados de um ponto para outro.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461208"
---
# <a name="network"></a><span data-ttu-id="ed0f6-103">Rede</span><span class="sxs-lookup"><span data-stu-id="ed0f6-103">Network</span></span>

<span data-ttu-id="ed0f6-104">Uma rede é exibida como o mecanismo de transporte que transmite dados de um ponto para outro.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-104">A network is viewed as the transport mechanism that conveys data from one point to another.</span></span> <span data-ttu-id="ed0f6-105">Os provedores de serviços TAPI lidam com os protocolos específicos necessários para executar operações, como o estabelecimento de uma sessão de comunicações em uma determinada rede.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-105">TAPI service providers handle the specific protocols required to perform operations such as establishing a communications session on a given network.</span></span> <span data-ttu-id="ed0f6-106">Um aplicativo de usuário final ou de servidor normalmente requer apenas informações de rede muito gerais, como o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-106">An end-user or server application normally requires only very general network information, such as address type.</span></span>

<span data-ttu-id="ed0f6-107">Alguns tipos comuns de redes:</span><span class="sxs-lookup"><span data-stu-id="ed0f6-107">Some common types of networks:</span></span>

-   <span data-ttu-id="ed0f6-108">**POTS (serviço de telefone antigo):** A voz e os dados são transmitidos em formato analógico enquanto estão no *loop local* e são transmitidos digitalmente em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-108">**POTS (Plain Old Telephone Service):** Voice and data are transmitted in analog format while in the *local loop* and are digitally transmitted elsewhere.</span></span> <span data-ttu-id="ed0f6-109">Normalmente, um tipo de mídia por chamada, um canal por linha.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-109">Typically, one media type per call, one channel per line.</span></span>
-   <span data-ttu-id="ed0f6-110">**ISDN (rede digital de serviços integrados):** Transmitido digitalmente.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-110">**ISDN (Integrated Services Digital Network):** Transmitted digitally.</span></span> <span data-ttu-id="ed0f6-111">Velocidades de até 128 Kbps em linhas da interface de taxa básica (BRI-ISDN) e muito mais altas em linhas de interface de taxa primária (PRI-ISDN).</span><span class="sxs-lookup"><span data-stu-id="ed0f6-111">Speeds of up to 128 Kbps on Basic Rate Interface (BRI-ISDN) lines and much higher on Primary Rate Interface (PRI-ISDN) lines.</span></span> <span data-ttu-id="ed0f6-112">Pelo menos três canais e até 32 canais, para transmissão simultânea e independente operada de voz e dados.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-112">At least three channels and as many as 32 channels, for simultaneous, independently operated transmission of voice and data.</span></span> <span data-ttu-id="ed0f6-113">Padrão internacional.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-113">International standard.</span></span>
-   <span data-ttu-id="ed0f6-114">**T1/E1:** Transmitido digitalmente.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-114">**T1/E1:** Transmitted digitally.</span></span> <span data-ttu-id="ed0f6-115">T1 é um link de transmissão com uma capacidade de 1,544 Mbps, normalmente usada para conectar redes entre distâncias remotas.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-115">T1 is a transmission link with a capacity of 1.544 Mbps, typically used for connecting networks across remote distances.</span></span> <span data-ttu-id="ed0f6-116">Na União Europeia, o T1 é chamado de E1.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-116">In the European Union T1 is called E1.</span></span>
-   <span data-ttu-id="ed0f6-117">**56 comutado:** Sinalização a 56 Kbps por linhas telefônicas de discagem, mas requer equipamento especial.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-117">**Switched 56:** Signaling at 56 Kbps over dial-up telephone lines, but requires special equipment.</span></span> <span data-ttu-id="ed0f6-118">Limitado a chamadas para outras instalações especialmente equipadas.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-118">Limited to calls to other specially equipped facilities.</span></span>
-   <span data-ttu-id="ed0f6-119">**Centrex:** Serviços de rede centralizados por meio de linhas telefônicas regulares e uso de equipamentos da companhia telefônica.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-119">**CENTREX:** Centralized network services through regular telephone lines and using telephone company equipment.</span></span> <span data-ttu-id="ed0f6-120">Nenhum equipamento especial é necessário.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-120">No special equipment required.</span></span>
-   <span data-ttu-id="ed0f6-121">**PBXs digitais (trocas de branches particulares) e sistemas-chave:** Voz e dados transmitidos em sistemas de telefone privado usando interfaces proprietárias.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-121">**Digital PBXs (private branch exchanges) and key systems:** Voice and data transmitted on private telephone systems using proprietary interfaces.</span></span>
-   <span data-ttu-id="ed0f6-122">**Redes IP:** Voz e dados transmitidos em redes usando o IP (Internet Protocol), como a própria Internet ou uma intranet corporativa.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-122">**IP Networks:** Voice and data transmitted on networks using the Internet Protocol (IP), such as the Internet itself or a corporate intranet.</span></span>

<span data-ttu-id="ed0f6-123">Note que esta lista não é exaustiva.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-123">Please note that this list is not exhaustive.</span></span> <span data-ttu-id="ed0f6-124">Qualquer mecanismo de transporte de rede pode ter suporte, dadas os provedores de serviço apropriados.</span><span class="sxs-lookup"><span data-stu-id="ed0f6-124">Any network transport mechanism can be supported, given appropriate service providers.</span></span>

 

 



