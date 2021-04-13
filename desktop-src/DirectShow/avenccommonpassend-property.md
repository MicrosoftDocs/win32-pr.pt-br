---
description: Interrompe a passagem de codificação atual ou consulta se a passagem de codificação atual é a última.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propriedade AVEncCommonPassEnd (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456823"
---
# <a name="avenccommonpassend-property"></a><span data-ttu-id="fd711-103">Propriedade AVEncCommonPassEnd</span><span class="sxs-lookup"><span data-stu-id="fd711-103">AVEncCommonPassEnd property</span></span>

<span data-ttu-id="fd711-104">Interrompe a passagem de codificação atual ou consulta se a passagem de codificação atual é a última.</span><span class="sxs-lookup"><span data-stu-id="fd711-104">Stops the current encoding pass, or queries whether the current encoding pass is the last one.</span></span>

<span data-ttu-id="fd711-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fd711-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd711-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fd711-106">Data type</span></span>

<span data-ttu-id="fd711-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="fd711-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fd711-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="fd711-108">Property GUID</span></span>

<span data-ttu-id="fd711-109">**CODECAPI \_ AVEncCommonPassEnd**</span><span class="sxs-lookup"><span data-stu-id="fd711-109">**CODECAPI\_AVEncCommonPassEnd**</span></span>

## <a name="remarks"></a><span data-ttu-id="fd711-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd711-110">Remarks</span></span>

<span data-ttu-id="fd711-111">Definir essa propriedade como **Variant \_ true** finaliza a passagem de codificação atual.</span><span class="sxs-lookup"><span data-stu-id="fd711-111">Setting this property to **VARIANT\_TRUE** ends the current encoding pass.</span></span> <span data-ttu-id="fd711-112">A definição dessa propriedade como **variante \_ false** encerra a codificação de passagem.</span><span class="sxs-lookup"><span data-stu-id="fd711-112">Setting this property to **VARIANT\_FALSE** terminates multipass encoding.</span></span>

<span data-ttu-id="fd711-113">A leitura desta propriedade consulta se a passagem de codificação atual é a última.</span><span class="sxs-lookup"><span data-stu-id="fd711-113">Reading this property queries whether the current encoding pass is the last one.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd711-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd711-114">Requirements</span></span>



| <span data-ttu-id="fd711-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd711-115">Requirement</span></span> | <span data-ttu-id="fd711-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fd711-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd711-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd711-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd711-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fd711-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fd711-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd711-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd711-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fd711-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fd711-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd711-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd711-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd711-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd711-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd711-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd711-124">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="fd711-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fd711-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fd711-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




