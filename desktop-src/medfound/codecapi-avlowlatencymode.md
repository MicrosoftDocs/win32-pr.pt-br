---
description: Habilita o modo de baixa latência em um codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Propriedade CODECAPI_AVLowLatencyMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781162"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="00df6-103">\_Propriedade CODECAPI AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="00df6-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="00df6-104">Habilita o modo de baixa latência em um codec.</span><span class="sxs-lookup"><span data-stu-id="00df6-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="00df6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="00df6-105">Data type</span></span>

<span data-ttu-id="00df6-106">**ULONG** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="00df6-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="00df6-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="00df6-107">Property GUID</span></span>

<span data-ttu-id="00df6-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="00df6-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="00df6-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="00df6-109">Property value</span></span>

<span data-ttu-id="00df6-110">Se o valor for diferente de zero, o modo de baixa latência será habilitado.</span><span class="sxs-lookup"><span data-stu-id="00df6-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="00df6-111">Se o valor for zero, o modo de baixa latência será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="00df6-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="00df6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="00df6-112">Remarks</span></span>

<span data-ttu-id="00df6-113">Essa propriedade se aplica a codificadores e decodificadores.</span><span class="sxs-lookup"><span data-stu-id="00df6-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="00df6-114">O modo de baixa latência é útil para comunicações em tempo real ou captura dinâmica, quando a latência deve ser minimizada.</span><span class="sxs-lookup"><span data-stu-id="00df6-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="00df6-115">No entanto, o modo de baixa latência também pode reduzir a codificação ou a qualidade da codificação.</span><span class="sxs-lookup"><span data-stu-id="00df6-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="00df6-116">Espera-se que o codificador não adicione nenhum atraso de exemplo devido à reordenação do quadro no processo de codificação, e um exemplo de entrada deve produzir um exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="00df6-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="00df6-117">B fatias/quadros podem estar presentes desde que não introduzam nenhuma reordenação de quadro no codificador.</span><span class="sxs-lookup"><span data-stu-id="00df6-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="00df6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00df6-118">Requirements</span></span>



| <span data-ttu-id="00df6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00df6-119">Requirement</span></span> | <span data-ttu-id="00df6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="00df6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00df6-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00df6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00df6-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="00df6-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="00df6-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00df6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00df6-124">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="00df6-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="00df6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00df6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00df6-126"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="00df6-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00df6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="00df6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00df6-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00df6-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="00df6-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="00df6-129">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

