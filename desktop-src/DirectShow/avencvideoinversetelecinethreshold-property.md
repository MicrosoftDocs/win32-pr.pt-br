---
description: Define o limite no qual o codificador considera um campo de vídeo redundante.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propriedade AVEncVideoInverseTelecineThreshold (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645689"
---
# <a name="avencvideoinversetelecinethreshold-property"></a><span data-ttu-id="a755b-103">Propriedade AVEncVideoInverseTelecineThreshold</span><span class="sxs-lookup"><span data-stu-id="a755b-103">AVEncVideoInverseTelecineThreshold property</span></span>

<span data-ttu-id="a755b-104">Define o limite no qual o codificador considera um campo de vídeo redundante.</span><span class="sxs-lookup"><span data-stu-id="a755b-104">Sets the threshold at which the encoder considers a video field redundant.</span></span>

<span data-ttu-id="a755b-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a755b-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a755b-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a755b-106">Data type</span></span>

<span data-ttu-id="a755b-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a755b-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a755b-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="a755b-108">Property GUID</span></span>

<span data-ttu-id="a755b-109">**CODECAPI \_ AVEncVideoInverseTelecineThreshold**</span><span class="sxs-lookup"><span data-stu-id="a755b-109">**CODECAPI\_AVEncVideoInverseTelecineThreshold**</span></span>

## <a name="property-value"></a><span data-ttu-id="a755b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a755b-110">Property value</span></span>

<span data-ttu-id="a755b-111">O valor dessa propriedade tem o seguinte intervalo.</span><span class="sxs-lookup"><span data-stu-id="a755b-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="a755b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a755b-112">Value</span></span> | <span data-ttu-id="a755b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="a755b-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="a755b-114">0</span><span class="sxs-lookup"><span data-stu-id="a755b-114">0</span></span>     | <span data-ttu-id="a755b-115">É menos provável que o codificador considere os campos de vídeo redundantes.</span><span class="sxs-lookup"><span data-stu-id="a755b-115">The encoder is less likely to consider video fields redundant.</span></span> |
| <span data-ttu-id="a755b-116">100</span><span class="sxs-lookup"><span data-stu-id="a755b-116">100</span></span>   | <span data-ttu-id="a755b-117">É mais provável que o codificador considere os campos de vídeo redundantes.</span><span class="sxs-lookup"><span data-stu-id="a755b-117">The encoder is more likely to consider video fields redundant.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a755b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a755b-118">Remarks</span></span>

<span data-ttu-id="a755b-119">Defina essa propriedade se o codificador estiver executando um telecineon inverso com uma fonte de vídeo analógica.</span><span class="sxs-lookup"><span data-stu-id="a755b-119">Set this property if the encoder is performing inverse telecine with an analog video source.</span></span>

## <a name="requirements"></a><span data-ttu-id="a755b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a755b-120">Requirements</span></span>



| <span data-ttu-id="a755b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a755b-121">Requirement</span></span> | <span data-ttu-id="a755b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a755b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a755b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a755b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a755b-124">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a755b-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a755b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a755b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a755b-126">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a755b-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a755b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a755b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a755b-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a755b-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a755b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a755b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a755b-130">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="a755b-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a755b-131">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a755b-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




