---
description: Especifica a taxa de bits de pico, em bits por segundo, usada para reprodução de taxa de bits de variável (VBR) restrita de 2 passagens.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: Propriedade MFPKEY_RMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165360"
---
# <a name="mfpkey_rmax-property"></a><span data-ttu-id="f2448-103">\_Propriedade MFPKEY RMAX</span><span class="sxs-lookup"><span data-stu-id="f2448-103">MFPKEY\_RMAX Property</span></span>

<span data-ttu-id="f2448-104">Especifica a taxa de bits de pico, em bits por segundo, usada para reprodução de taxa de bits de variável (VBR) restrita de 2 passagens.</span><span class="sxs-lookup"><span data-stu-id="f2448-104">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) playback.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f2448-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f2448-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f2448-106">g \_ wszWMVCMaxBitrate</span><span class="sxs-lookup"><span data-stu-id="f2448-106">g\_wszWMVCMaxBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="f2448-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f2448-107">Data Type</span></span>

<span data-ttu-id="f2448-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="f2448-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f2448-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="f2448-109">Default Value</span></span>

<span data-ttu-id="f2448-110">Sem padrão.</span><span class="sxs-lookup"><span data-stu-id="f2448-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2448-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2448-111">Remarks</span></span>

<span data-ttu-id="f2448-112">Esse valor representa a taxa de bits de pico para reprodução.</span><span class="sxs-lookup"><span data-stu-id="f2448-112">This value represents the peak bit rate for playback.</span></span> <span data-ttu-id="f2448-113">O valor de [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) é usado para descrever o buffer em termos dessa taxa de bits; na verdade, a VBR restrita é semelhante à taxa de bits constante (CBR) usando esse valor como a taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="f2448-113">The value of [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is used to describe the buffer in terms of this bit rate; in effect, constrained VBR is similar to constant bit rate (CBR) using this value as the bit rate.</span></span> <span data-ttu-id="f2448-114">No entanto, um fluxo de VBR restrito pode ser reproduzido em uma taxa de bits inferior, desde que o buffer seja aumentado.</span><span class="sxs-lookup"><span data-stu-id="f2448-114">However, a constrained VBR stream can be played back at a lower bit rate, as long as the buffer is increased.</span></span>

<span data-ttu-id="f2448-115">Você deve definir esse valor para codificação de VBR de duas passagens de pico restrita.</span><span class="sxs-lookup"><span data-stu-id="f2448-115">You must set this value for peak-constrained two-pass VBR encoding.</span></span> <span data-ttu-id="f2448-116">Depois de começar a processar amostras, você não deve consultar esse valor até concluir a codificação do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f2448-116">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="f2448-117">O codificador interpreta uma solicitação para esse valor como um sinal de que a sessão de codificação está acima; o próximo exemplo que você processa é tratado como o início de uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="f2448-117">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="f2448-118">Normalmente, esse valor é de duas a três vezes maior que o valor de [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="f2448-118">Typically, this value is two to three times greater than the value of [MFPKEY\_RAVG](mfpkey-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2448-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2448-119">Requirements</span></span>



| <span data-ttu-id="f2448-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2448-120">Requirement</span></span> | <span data-ttu-id="f2448-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f2448-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2448-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2448-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f2448-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2448-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f2448-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2448-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f2448-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2448-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2448-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2448-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2448-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2448-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2448-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2448-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2448-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2448-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




