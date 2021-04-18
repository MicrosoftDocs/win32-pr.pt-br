---
description: Especifica o nível máximo de volume desejado de conteúdo de áudio de saída.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: Propriedade MFPKEY_WMADRC_PEAKTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807222"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a><span data-ttu-id="32445-103">\_Propriedade MFPKEY WMADRC \_ PEAKTARGET</span><span class="sxs-lookup"><span data-stu-id="32445-103">MFPKEY\_WMADRC\_PEAKTARGET Property</span></span>

<span data-ttu-id="32445-104">Especifica o nível máximo de volume desejado de conteúdo de áudio de saída.</span><span class="sxs-lookup"><span data-stu-id="32445-104">Specifies the desired maximum volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="32445-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="32445-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="32445-106">g \_ wszWMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="32445-106">g\_wszWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="32445-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="32445-107">Data Type</span></span>

<span data-ttu-id="32445-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="32445-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="32445-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="32445-109">Default Value</span></span>

<span data-ttu-id="32445-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="32445-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="32445-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="32445-111">Remarks</span></span>

<span data-ttu-id="32445-112">Você pode definir esse valor no decodificador para a finalidade do controle de intervalo dinâmico, mas terá efeito somente se a propriedade [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) for definida.</span><span class="sxs-lookup"><span data-stu-id="32445-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="32445-113">Se você solicitar o controle de intervalo dinâmico do decodificador quando essa propriedade não for definida, o codec calculará um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="32445-113">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="32445-114">Use as propriedades [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular os valores apropriados para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="32445-114">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

<span data-ttu-id="32445-115">Para obter mais informações sobre o controle de intervalo dinâmico, consulte o artigo da Web [recursos de codec do Windows Media Audio Professional](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="32445-115">For more information on dynamic range control, see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="32445-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32445-116">Requirements</span></span>



| <span data-ttu-id="32445-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="32445-117">Requirement</span></span> | <span data-ttu-id="32445-118">Valor</span><span class="sxs-lookup"><span data-stu-id="32445-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32445-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32445-119">Minimum supported client</span></span><br/> | <span data-ttu-id="32445-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="32445-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="32445-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32445-121">Minimum supported server</span></span><br/> | <span data-ttu-id="32445-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32445-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32445-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32445-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="32445-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="32445-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32445-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="32445-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32445-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32445-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
