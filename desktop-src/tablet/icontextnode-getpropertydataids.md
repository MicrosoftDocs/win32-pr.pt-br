---
description: Recupera os identificadores para os quais há dados de propriedade.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'Método IContextNode:: GetPropertyDataIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791082"
---
# <a name="icontextnodegetpropertydataids-method"></a><span data-ttu-id="6fd77-103">Método IContextNode:: GetPropertyDataIds</span><span class="sxs-lookup"><span data-stu-id="6fd77-103">IContextNode::GetPropertyDataIds method</span></span>

<span data-ttu-id="6fd77-104">Recupera os identificadores para os quais há dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6fd77-104">Retrieves the identifiers for which there is property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd77-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fd77-105">Syntax</span></span>


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a><span data-ttu-id="6fd77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fd77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd77-107">*pulGuidCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6fd77-107">*pulGuidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-108">O número de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fd77-108">The number of properties.</span></span>

</dd> <dt>

<span data-ttu-id="6fd77-109">*ppGuids* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6fd77-109">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd77-110">Os identificadores para os quais há dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6fd77-110">The identifiers for which there is property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd77-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fd77-111">Return value</span></span>

<span data-ttu-id="6fd77-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6fd77-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6fd77-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fd77-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6fd77-114">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppGuids* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="6fd77-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="6fd77-115">Esse método retorna os identificadores específicos do aplicativo para dados de propriedade que foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="6fd77-115">This method returns the application-specific identifiers for property data that has been added.</span></span> <span data-ttu-id="6fd77-116">Ele também retorna os identificadores para os dados de propriedade interna, que são descritos pelas constantes de [Propriedades do nó de contexto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd77-116">It also returns the identifiers for the internal property data, which are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd77-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fd77-117">Requirements</span></span>



| <span data-ttu-id="6fd77-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fd77-118">Requirement</span></span> | <span data-ttu-id="6fd77-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6fd77-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd77-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fd77-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd77-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6fd77-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6fd77-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fd77-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd77-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6fd77-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6fd77-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fd77-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fd77-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6fd77-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6fd77-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6fd77-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fd77-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fd77-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6fd77-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fd77-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd77-129">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="6fd77-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6fd77-130">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6fd77-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="6fd77-131">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6fd77-131">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="6fd77-132">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="6fd77-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="6fd77-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="6fd77-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

