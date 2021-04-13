---
description: Especifica o nível de qualidade para codificação.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Propriedade AVEncCommonQuality (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456822"
---
# <a name="avenccommonquality-property"></a><span data-ttu-id="1287b-103">Propriedade AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="1287b-103">AVEncCommonQuality property</span></span>

<span data-ttu-id="1287b-104">Especifica o nível de qualidade para codificação.</span><span class="sxs-lookup"><span data-stu-id="1287b-104">Specifies the quality level for encoding.</span></span>

<span data-ttu-id="1287b-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1287b-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="1287b-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1287b-106">Data type</span></span>

<span data-ttu-id="1287b-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="1287b-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1287b-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="1287b-108">Property GUID</span></span>

<span data-ttu-id="1287b-109">**CODECAPI \_ AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="1287b-109">**CODECAPI\_AVEncCommonQuality**</span></span>

## <a name="property-value"></a><span data-ttu-id="1287b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1287b-110">Property value</span></span>

<span data-ttu-id="1287b-111">O valor dessa propriedade tem o seguinte intervalo.</span><span class="sxs-lookup"><span data-stu-id="1287b-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="1287b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="1287b-112">Value</span></span> | <span data-ttu-id="1287b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1287b-113">Description</span></span>                           |
|-------|---------------------------------------|
| <span data-ttu-id="1287b-114">0</span><span class="sxs-lookup"><span data-stu-id="1287b-114">0</span></span>     | <span data-ttu-id="1287b-115">Qualidade mínima, tamanho de saída menor.</span><span class="sxs-lookup"><span data-stu-id="1287b-115">Minimum quality, smaller output size.</span></span> |
| <span data-ttu-id="1287b-116">100</span><span class="sxs-lookup"><span data-stu-id="1287b-116">100</span></span>   | <span data-ttu-id="1287b-117">Qualidade máxima, tamanho de saída maior.</span><span class="sxs-lookup"><span data-stu-id="1287b-117">Maximum quality, larger output size.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="1287b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1287b-118">Remarks</span></span>

<span data-ttu-id="1287b-119">Essa propriedade controla o nível de qualidade quando o codificador não está usando uma taxa de bits restrita.</span><span class="sxs-lookup"><span data-stu-id="1287b-119">This property controls the quality level when the encoder is not using a constrained bit rate.</span></span> <span data-ttu-id="1287b-120">A propriedade [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) determina se a taxa de bits está restrita.</span><span class="sxs-lookup"><span data-stu-id="1287b-120">The [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) property determines whether the bit rate is constrained.</span></span>

## <a name="requirements"></a><span data-ttu-id="1287b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1287b-121">Requirements</span></span>



| <span data-ttu-id="1287b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1287b-122">Requirement</span></span> | <span data-ttu-id="1287b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1287b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1287b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1287b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1287b-125">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1287b-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1287b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1287b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1287b-127">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1287b-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1287b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1287b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1287b-129"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1287b-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1287b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1287b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1287b-131">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="1287b-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="1287b-132">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="1287b-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




