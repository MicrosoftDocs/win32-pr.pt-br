---
description: Especifica a compensação entre o movimento e as imagens ainda. Essa propriedade aplica-se somente ao modo de controle de taxa de bits constante (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Propriedade AVEncVideoCBRMotionTradeoff (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920014"
---
# <a name="avencvideocbrmotiontradeoff-property"></a><span data-ttu-id="652f5-104">Propriedade AVEncVideoCBRMotionTradeoff</span><span class="sxs-lookup"><span data-stu-id="652f5-104">AVEncVideoCBRMotionTradeoff property</span></span>

<span data-ttu-id="652f5-105">Especifica a compensação entre o movimento e as imagens ainda.</span><span class="sxs-lookup"><span data-stu-id="652f5-105">Specifies the tradeoff between motion and still images.</span></span> <span data-ttu-id="652f5-106">Essa propriedade aplica-se somente ao modo de controle de taxa de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="652f5-106">This property applies only to constant bit rate (CBR) control mode.</span></span>

<span data-ttu-id="652f5-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="652f5-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="652f5-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="652f5-108">Data type</span></span>

<span data-ttu-id="652f5-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="652f5-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="652f5-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="652f5-110">Property GUID</span></span>

<span data-ttu-id="652f5-111">**CODECAPI \_ AVEncVideoCBRMotionTradeoff**</span><span class="sxs-lookup"><span data-stu-id="652f5-111">**CODECAPI\_AVEncVideoCBRMotionTradeoff**</span></span>

## <a name="property-value"></a><span data-ttu-id="652f5-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="652f5-112">Property value</span></span>

<span data-ttu-id="652f5-113">O valor dessa propriedade tem o seguinte intervalo.</span><span class="sxs-lookup"><span data-stu-id="652f5-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="652f5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="652f5-114">Value</span></span> | <span data-ttu-id="652f5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="652f5-115">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="652f5-116">0</span><span class="sxs-lookup"><span data-stu-id="652f5-116">0</span></span>     | <span data-ttu-id="652f5-117">Otimizar para imagens ainda</span><span class="sxs-lookup"><span data-stu-id="652f5-117">Optimize for still images</span></span> |
| <span data-ttu-id="652f5-118">100</span><span class="sxs-lookup"><span data-stu-id="652f5-118">100</span></span>   | <span data-ttu-id="652f5-119">Otimizar para movimento.</span><span class="sxs-lookup"><span data-stu-id="652f5-119">Optimize for motion.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="652f5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="652f5-120">Requirements</span></span>



| <span data-ttu-id="652f5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="652f5-121">Requirement</span></span> | <span data-ttu-id="652f5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="652f5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="652f5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="652f5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="652f5-124">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="652f5-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="652f5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="652f5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="652f5-126">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="652f5-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="652f5-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="652f5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="652f5-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="652f5-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="652f5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="652f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="652f5-130">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="652f5-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="652f5-131">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="652f5-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




