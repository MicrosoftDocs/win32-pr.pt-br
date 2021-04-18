---
description: Especifica o número de passagens de codificação concluídas. Essa propriedade aplica-se somente à codificação de várias passagens.
ms.assetid: 19286f26-96f1-429c-9d6a-5e9b98597cd2
title: Propriedade AVEncStatCommonCompletedPasses (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2927e501963d450cbc08106e7860dfbfd2d7d98a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105753189"
---
# <a name="avencstatcommoncompletedpasses-property"></a><span data-ttu-id="f281f-104">Propriedade AVEncStatCommonCompletedPasses</span><span class="sxs-lookup"><span data-stu-id="f281f-104">AVEncStatCommonCompletedPasses property</span></span>

<span data-ttu-id="f281f-105">Especifica o número de passagens de codificação concluídas.</span><span class="sxs-lookup"><span data-stu-id="f281f-105">Specifies the number of completed encoding passes.</span></span> <span data-ttu-id="f281f-106">Essa propriedade aplica-se somente à codificação de várias passagens.</span><span class="sxs-lookup"><span data-stu-id="f281f-106">This property applies only to multi-pass encoding.</span></span>

<span data-ttu-id="f281f-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f281f-107">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="f281f-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f281f-108">Data type</span></span>

<span data-ttu-id="f281f-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="f281f-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f281f-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="f281f-110">Property GUID</span></span>

<span data-ttu-id="f281f-111">**CODECAPI \_ AVEncStatCommonCompletedPasses**</span><span class="sxs-lookup"><span data-stu-id="f281f-111">**CODECAPI\_AVEncStatCommonCompletedPasses**</span></span>

## <a name="property-value"></a><span data-ttu-id="f281f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f281f-112">Property value</span></span>

<span data-ttu-id="f281f-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="f281f-113">This property has a linear range of values.</span></span> <span data-ttu-id="f281f-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="f281f-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="f281f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f281f-115">Requirements</span></span>



| <span data-ttu-id="f281f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f281f-116">Requirement</span></span> | <span data-ttu-id="f281f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f281f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f281f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f281f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f281f-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f281f-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f281f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f281f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f281f-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f281f-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f281f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f281f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f281f-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f281f-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f281f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f281f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f281f-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="f281f-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f281f-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="f281f-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




