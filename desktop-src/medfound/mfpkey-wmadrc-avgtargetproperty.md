---
description: Especifica o nível de volume médio desejado de conteúdo de áudio de saída.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: Propriedade MFPKEY_WMADRC_AVGTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165299"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a><span data-ttu-id="d57ca-103">\_Propriedade MFPKEY WMADRC \_ AVGTARGET</span><span class="sxs-lookup"><span data-stu-id="d57ca-103">MFPKEY\_WMADRC\_AVGTARGET Property</span></span>

<span data-ttu-id="d57ca-104">Especifica o nível de volume médio desejado de conteúdo de áudio de saída.</span><span class="sxs-lookup"><span data-stu-id="d57ca-104">Specifies the desired average volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d57ca-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d57ca-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d57ca-106">g \_ wszWMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="d57ca-106">g\_wszWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="d57ca-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d57ca-107">Data Type</span></span>

<span data-ttu-id="d57ca-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="d57ca-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d57ca-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="d57ca-109">Default Value</span></span>

<span data-ttu-id="d57ca-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="d57ca-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57ca-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d57ca-111">Remarks</span></span>

<span data-ttu-id="d57ca-112">Você pode definir esse valor no decodificador para a finalidade do controle de intervalo dinâmico, mas terá efeito somente se a propriedade [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) for definida.</span><span class="sxs-lookup"><span data-stu-id="d57ca-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

> [!Note]  
> <span data-ttu-id="d57ca-113">Não é recomendável definir o valor de destino médio.</span><span class="sxs-lookup"><span data-stu-id="d57ca-113">Setting the average target value is not recommended.</span></span> <span data-ttu-id="d57ca-114">O ajuste do valor médio não afeta a diferença entre sons altos e suaves.</span><span class="sxs-lookup"><span data-stu-id="d57ca-114">Adjusting the average value does not affect the difference between loud and soft sounds.</span></span> <span data-ttu-id="d57ca-115">Em vez disso, ele corta ou aumenta o volume médio geral que pode causar distorção indesejável durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="d57ca-115">Instead, it cuts or boosts the overall average volume which may cause undesirable distortion during playback.</span></span>

 

<span data-ttu-id="d57ca-116">Se você solicitar o controle de intervalo dinâmico do decodificador quando essa propriedade não for definida, o codec calculará um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="d57ca-116">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="d57ca-117">Use as propriedades [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) e [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular os valores apropriados para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d57ca-117">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d57ca-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d57ca-118">Requirements</span></span>



| <span data-ttu-id="d57ca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d57ca-119">Requirement</span></span> | <span data-ttu-id="d57ca-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d57ca-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d57ca-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d57ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d57ca-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d57ca-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d57ca-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d57ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d57ca-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d57ca-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d57ca-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d57ca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57ca-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57ca-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d57ca-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d57ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57ca-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d57ca-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




