---
description: Enviando comandos COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Enviando comandos COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778426"
---
# <a name="sending-copp-commands"></a><span data-ttu-id="366d9-103">Enviando comandos COPP</span><span class="sxs-lookup"><span data-stu-id="366d9-103">Sending COPP Commands</span></span>

<span data-ttu-id="366d9-104">Para enviar um comando de COPP (protocolo de proteção de saída) certificado, preencha uma estrutura [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="366d9-104">To send a Certified Output Protection Protocol (COPP) command, fill in an [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) structure as follows:</span></span>

-   <span data-ttu-id="366d9-105">**guidCommandID**.</span><span class="sxs-lookup"><span data-stu-id="366d9-105">**guidCommandID**.</span></span> <span data-ttu-id="366d9-106">O GUID que identifica o comando.</span><span class="sxs-lookup"><span data-stu-id="366d9-106">The GUID that identifies the command.</span></span> <span data-ttu-id="366d9-107">Consulte a referência de comando COPP.</span><span class="sxs-lookup"><span data-stu-id="366d9-107">See the COPP Command Reference.</span></span>
-   <span data-ttu-id="366d9-108">**dwSequence**.</span><span class="sxs-lookup"><span data-stu-id="366d9-108">**dwSequence**.</span></span> <span data-ttu-id="366d9-109">O número de sequência do comando.</span><span class="sxs-lookup"><span data-stu-id="366d9-109">The command sequence number.</span></span> <span data-ttu-id="366d9-110">Incrementar esse valor após cada comando.</span><span class="sxs-lookup"><span data-stu-id="366d9-110">Increment this value after each command.</span></span> <span data-ttu-id="366d9-111">(Esse valor é mostrado como **uCommandSeq** no [início de uma sessão Copp](initiating-a-copp-session.md).)</span><span class="sxs-lookup"><span data-stu-id="366d9-111">(This value is shown as **uCommandSeq** in [Initiating a COPP Session](initiating-a-copp-session.md).)</span></span>
-   <span data-ttu-id="366d9-112">**cbSizeData**.</span><span class="sxs-lookup"><span data-stu-id="366d9-112">**cbSizeData**.</span></span> <span data-ttu-id="366d9-113">O tamanho, em bytes, de todos os dados necessários para o comando.</span><span class="sxs-lookup"><span data-stu-id="366d9-113">The size, in bytes, of any data needed for the command.</span></span>
-   <span data-ttu-id="366d9-114">**CommandData**.</span><span class="sxs-lookup"><span data-stu-id="366d9-114">**CommandData**.</span></span> <span data-ttu-id="366d9-115">Dados para o comando.</span><span class="sxs-lookup"><span data-stu-id="366d9-115">Data for the command.</span></span>

<span data-ttu-id="366d9-116">Depois de preencher esses dados, calcule o MAC para o comando:</span><span class="sxs-lookup"><span data-stu-id="366d9-116">After you have filled in this data, calculate the MAC for the command:</span></span>

1.  <span data-ttu-id="366d9-117">Calcule a marca OMAC-1 para o bloco de dados que aparece após o membro **macKDI** da estrutura **AMCOPPCommand** .</span><span class="sxs-lookup"><span data-stu-id="366d9-117">Calculate the OMAC-1 tag for the block of data that appears after the **macKDI** member of the **AMCOPPCommand** structure.</span></span>
2.  <span data-ttu-id="366d9-118">Copie esse valor para o membro **macKDI** da estrutura.</span><span class="sxs-lookup"><span data-stu-id="366d9-118">Copy this value into the **macKDI** member of the structure.</span></span>

<span data-ttu-id="366d9-119">Agora, passe a estrutura para o método [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .</span><span class="sxs-lookup"><span data-stu-id="366d9-119">Now pass the structure to the [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="366d9-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="366d9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="366d9-121">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="366d9-121">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



