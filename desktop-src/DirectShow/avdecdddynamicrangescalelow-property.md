---
description: Especifica o aumento de nível baixo quando o decodificador executa o controle de intervalo dinâmico em um fluxo de áudio Dolby AC-3.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Propriedade AVDecDDDynamicRangeScaleLow (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b68b1d4376d9ba15859be943ded23458fe16d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010050"
---
# <a name="avdecdddynamicrangescalelow-property"></a><span data-ttu-id="ff22e-103">Propriedade AVDecDDDynamicRangeScaleLow</span><span class="sxs-lookup"><span data-stu-id="ff22e-103">AVDecDDDynamicRangeScaleLow property</span></span>

<span data-ttu-id="ff22e-104">Especifica o aumento de nível baixo quando o decodificador executa o controle de intervalo dinâmico em um fluxo de áudio Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="ff22e-104">Specifies the low-level boost when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="ff22e-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ff22e-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ff22e-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ff22e-106">Data type</span></span>

<span data-ttu-id="ff22e-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="ff22e-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ff22e-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="ff22e-108">Property GUID</span></span>

<span data-ttu-id="ff22e-109">**CODECAPI \_ AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="ff22e-109">**CODECAPI\_AVDecDDDynamicRangeScaleLow**</span></span>

## <a name="property-value"></a><span data-ttu-id="ff22e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ff22e-110">Property value</span></span>

<span data-ttu-id="ff22e-111">O valor dessa propriedade tem o seguinte intervalo.</span><span class="sxs-lookup"><span data-stu-id="ff22e-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="ff22e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ff22e-112">Value</span></span> | <span data-ttu-id="ff22e-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff22e-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="ff22e-114">0</span><span class="sxs-lookup"><span data-stu-id="ff22e-114">0</span></span>     | <span data-ttu-id="ff22e-115">Sem compactação de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="ff22e-115">No dynamic range compression.</span></span> <span data-ttu-id="ff22e-116">Preserve o intervalo dinâmico completo.</span><span class="sxs-lookup"><span data-stu-id="ff22e-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="ff22e-117">100</span><span class="sxs-lookup"><span data-stu-id="ff22e-117">100</span></span>   | <span data-ttu-id="ff22e-118">Aplicar compactação completa de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="ff22e-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="ff22e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff22e-119">Remarks</span></span>

<span data-ttu-id="ff22e-120">Essa propriedade aplica-se somente quando o valor da propriedade [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) é eAVDecDDOperationalMode \_ linha.</span><span class="sxs-lookup"><span data-stu-id="ff22e-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff22e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff22e-121">Requirements</span></span>



| <span data-ttu-id="ff22e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff22e-122">Requirement</span></span> | <span data-ttu-id="ff22e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ff22e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff22e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff22e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ff22e-125">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ff22e-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ff22e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff22e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ff22e-127">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ff22e-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ff22e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff22e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff22e-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff22e-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff22e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff22e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff22e-131">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="ff22e-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ff22e-132">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ff22e-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




