---
description: Habilita o modo de baixa latência em um codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Propriedade CODECAPI_AVLowLatencyMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826900"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="5b5cd-103">\_Propriedade CODECAPI AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="5b5cd-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="5b5cd-104">Habilita o modo de baixa latência em um codec.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b5cd-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5b5cd-105">Data type</span></span>

<span data-ttu-id="5b5cd-106">**ULONG** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="5b5cd-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5b5cd-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="5b5cd-107">Property GUID</span></span>

<span data-ttu-id="5b5cd-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="5b5cd-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="5b5cd-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5b5cd-109">Property value</span></span>

<span data-ttu-id="5b5cd-110">Se o valor for diferente de zero, o modo de baixa latência será habilitado.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="5b5cd-111">Se o valor for zero, o modo de baixa latência será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b5cd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b5cd-112">Remarks</span></span>

<span data-ttu-id="5b5cd-113">Essa propriedade se aplica a codificadores e decodificadores.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="5b5cd-114">O modo de baixa latência é útil para comunicações em tempo real ou captura dinâmica, quando a latência deve ser minimizada.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="5b5cd-115">No entanto, o modo de baixa latência também pode reduzir a codificação ou a qualidade da codificação.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="5b5cd-116">Espera-se que o codificador não adicione nenhum atraso de exemplo devido à reordenação do quadro no processo de codificação, e um exemplo de entrada deve produzir um exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="5b5cd-117">B fatias/quadros podem estar presentes desde que não introduzam nenhuma reordenação de quadro no codificador.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

> [!WARNING] 
> <span data-ttu-id="5b5cd-118">Na implementação atual, o decodificador Media Foundation H. 264 usa o tipo **VT_UI4** para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-118">In the current implementation, the Media Foundation H.264 decoder uses the type **VT_UI4** for this property.</span></span> <span data-ttu-id="5b5cd-119">Todas as outras implementações, incluindo o codificador H. 264, usam o tipo **VT_BOOL**.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-119">All other implementations, including the H.264 encoder, use the type **VT_BOOL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5cd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5cd-120">Requirements</span></span>



| <span data-ttu-id="5b5cd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5cd-121">Requirement</span></span> | <span data-ttu-id="5b5cd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5b5cd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5cd-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5cd-124">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5b5cd-124">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="5b5cd-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5cd-126">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5b5cd-126">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5b5cd-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5b5cd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5cd-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cd-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5cd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b5cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5cd-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b5cd-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5b5cd-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="5b5cd-131">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

