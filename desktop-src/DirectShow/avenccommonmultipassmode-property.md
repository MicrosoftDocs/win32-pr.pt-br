---
description: Especifica o número de aprovações de codificação que o codificador suporta.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Propriedade AVEncCommonMultipassMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825956"
---
# <a name="avenccommonmultipassmode-property"></a><span data-ttu-id="aff91-103">Propriedade AVEncCommonMultipassMode</span><span class="sxs-lookup"><span data-stu-id="aff91-103">AVEncCommonMultipassMode property</span></span>

<span data-ttu-id="aff91-104">Especifica o número de aprovações de codificação que o codificador suporta.</span><span class="sxs-lookup"><span data-stu-id="aff91-104">Specifies the number of encoding passes that the encoder supports.</span></span>

<span data-ttu-id="aff91-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="aff91-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="aff91-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="aff91-106">Data type</span></span>

<span data-ttu-id="aff91-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="aff91-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aff91-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="aff91-108">Property GUID</span></span>

<span data-ttu-id="aff91-109">**CODECAPI \_ AVEncCommonMultipassMode**</span><span class="sxs-lookup"><span data-stu-id="aff91-109">**CODECAPI\_AVEncCommonMultipassMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="aff91-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="aff91-110">Property value</span></span>

<span data-ttu-id="aff91-111">Essa propriedade é retornada como um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="aff91-111">This property is returned as a range of values.</span></span> <span data-ttu-id="aff91-112">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="aff91-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="aff91-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aff91-113">Remarks</span></span>

<span data-ttu-id="aff91-114">A decodificação da latência é definida como a quantidade de dados que o decodificador deve armazenar em buffer.</span><span class="sxs-lookup"><span data-stu-id="aff91-114">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="aff91-115">Por exemplo, definir essa propriedade como **Variant \_ true** em um codificador de vídeo MPEG limita os tipos de estruturas GOP que o codificador pode usar.</span><span class="sxs-lookup"><span data-stu-id="aff91-115">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

<span data-ttu-id="aff91-116">Para definir a passagem de codificação atual, defina a propriedade [**AVEncCommonPassStart**](avenccommonpassstart-property.md) .</span><span class="sxs-lookup"><span data-stu-id="aff91-116">To set the current encoding pass, set the [**AVEncCommonPassStart**](avenccommonpassstart-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff91-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aff91-117">Requirements</span></span>



| <span data-ttu-id="aff91-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff91-118">Requirement</span></span> | <span data-ttu-id="aff91-119">Valor</span><span class="sxs-lookup"><span data-stu-id="aff91-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aff91-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aff91-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aff91-121">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aff91-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aff91-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aff91-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aff91-123">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aff91-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aff91-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aff91-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff91-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff91-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff91-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="aff91-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff91-127">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="aff91-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="aff91-128">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="aff91-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




