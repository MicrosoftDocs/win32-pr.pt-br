---
description: Especifica a compensação entre a qualidade de codificação e a velocidade. Essa propriedade é válida em todos os modos de controle de taxa.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Propriedade AVEncCommonQualityVsSpeed (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087847"
---
# <a name="avenccommonqualityvsspeed-property"></a><span data-ttu-id="7df0d-104">Propriedade AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="7df0d-104">AVEncCommonQualityVsSpeed property</span></span>

<span data-ttu-id="7df0d-105">Especifica a compensação entre a qualidade de codificação e a velocidade.</span><span class="sxs-lookup"><span data-stu-id="7df0d-105">Specifies the tradeoff between encoding quality and speed.</span></span> <span data-ttu-id="7df0d-106">Essa propriedade é válida em todos os modos de controle de taxa.</span><span class="sxs-lookup"><span data-stu-id="7df0d-106">This property is valid in all rate control modes.</span></span>

<span data-ttu-id="7df0d-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7df0d-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7df0d-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7df0d-108">Data type</span></span>

<span data-ttu-id="7df0d-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="7df0d-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7df0d-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="7df0d-110">Property GUID</span></span>

<span data-ttu-id="7df0d-111">**CODECAPI \_ AVEncCommonQualityVsSpeed**</span><span class="sxs-lookup"><span data-stu-id="7df0d-111">**CODECAPI\_AVEncCommonQualityVsSpeed**</span></span>

## <a name="property-value"></a><span data-ttu-id="7df0d-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7df0d-112">Property value</span></span>

<span data-ttu-id="7df0d-113">O valor dessa propriedade tem o seguinte intervalo.</span><span class="sxs-lookup"><span data-stu-id="7df0d-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="7df0d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7df0d-114">Value</span></span> | <span data-ttu-id="7df0d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7df0d-115">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="7df0d-116">0</span><span class="sxs-lookup"><span data-stu-id="7df0d-116">0</span></span>     | <span data-ttu-id="7df0d-117">Menor qualidade e codificação mais rápida.</span><span class="sxs-lookup"><span data-stu-id="7df0d-117">Lower quality, faster encoding.</span></span>  |
| <span data-ttu-id="7df0d-118">100</span><span class="sxs-lookup"><span data-stu-id="7df0d-118">100</span></span>   | <span data-ttu-id="7df0d-119">Maior qualidade, codificação mais lenta.</span><span class="sxs-lookup"><span data-stu-id="7df0d-119">Higher quality, slower encoding.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7df0d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df0d-120">Requirements</span></span>



| <span data-ttu-id="7df0d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df0d-121">Requirement</span></span> | <span data-ttu-id="7df0d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7df0d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7df0d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df0d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7df0d-124">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7df0d-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7df0d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df0d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7df0d-126">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7df0d-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7df0d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7df0d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7df0d-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7df0d-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df0d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7df0d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df0d-130">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="7df0d-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7df0d-131">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="7df0d-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




