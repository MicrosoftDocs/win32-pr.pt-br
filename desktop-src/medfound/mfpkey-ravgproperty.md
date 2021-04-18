---
description: Especifica a taxa média de bits, em bits por segundo, usada para codificação de 2 passagens, taxa de bits variável (VBR).
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: Propriedade MFPKEY_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791503"
---
# <a name="mfpkey_ravg-property"></a><span data-ttu-id="5f01a-103">\_Propriedade MFPKEY RAVG</span><span class="sxs-lookup"><span data-stu-id="5f01a-103">MFPKEY\_RAVG Property</span></span>

<span data-ttu-id="5f01a-104">Especifica a taxa média de bits, em bits por segundo, usada para codificação de 2 passagens, taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="5f01a-104">Specifies the average bit rate, in bits per second, used for 2-pass, variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5f01a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5f01a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5f01a-106">g \_ wszWMVCAvgBitrate</span><span class="sxs-lookup"><span data-stu-id="5f01a-106">g\_wszWMVCAvgBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="5f01a-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="5f01a-107">Data Type</span></span>

<span data-ttu-id="5f01a-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="5f01a-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="5f01a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f01a-109">Remarks</span></span>

<span data-ttu-id="5f01a-110">Em uma VBR restrita e irrestrita, esse valor é a taxa média de bits na duração do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5f01a-110">In both constrained and unconstrained VBR, this value is the average bit rate across the duration of the content.</span></span>

<span data-ttu-id="5f01a-111">Você deve definir esse valor para ambos os modos de codificação de VBR de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="5f01a-111">You must set this value for both modes of two-pass VBR encoding.</span></span> <span data-ttu-id="5f01a-112">Depois de começar a processar amostras, você não deve consultar esse valor até concluir a codificação do fluxo.</span><span class="sxs-lookup"><span data-stu-id="5f01a-112">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="5f01a-113">O codificador interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação está acima; o próximo exemplo que você processa é tratado como o início de uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="5f01a-113">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="5f01a-114">Essa propriedade também pode ser lida no final de uma sessão de codificação de VBR de 1 passagem.</span><span class="sxs-lookup"><span data-stu-id="5f01a-114">This property can also be read at the end of a 1-pass VBR encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f01a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f01a-115">Requirements</span></span>



| <span data-ttu-id="5f01a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f01a-116">Requirement</span></span> | <span data-ttu-id="5f01a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5f01a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f01a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f01a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5f01a-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5f01a-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5f01a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f01a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5f01a-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5f01a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f01a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f01a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f01a-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f01a-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f01a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f01a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f01a-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f01a-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




