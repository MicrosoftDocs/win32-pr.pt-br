---
description: Remove uma parte dos dados específicos do aplicativo.
ms.assetid: 41077c2f-39e3-4069-ac05-97f1785e37b7
title: 'Método IContextNode:: RemovePropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.RemovePropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4c2fd5924b206ee296c066a908d2a59b02019f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501810"
---
# <a name="icontextnoderemovepropertydata-method"></a><span data-ttu-id="e6a34-103">Método IContextNode:: RemovePropertyData</span><span class="sxs-lookup"><span data-stu-id="e6a34-103">IContextNode::RemovePropertyData method</span></span>

<span data-ttu-id="e6a34-104">Remove uma parte dos dados específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6a34-104">Removes a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a34-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6a34-105">Syntax</span></span>


```C++
HRESULT RemovePropertyData(
  [in] const GUID *pPropertyDataId
);
```



## <a name="parameters"></a><span data-ttu-id="e6a34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6a34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a34-107">*pPropertyDataId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6a34-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a34-108">O identificador dos dados a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="e6a34-108">The identifier of the data to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a34-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6a34-109">Return value</span></span>

<span data-ttu-id="e6a34-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e6a34-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a34-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6a34-111">Remarks</span></span>

<span data-ttu-id="e6a34-112">**E \_ INVALIDARG** será retornado se o parâmetro *pPropertyDataId* for uma das constantes de [Propriedades do nó de contexto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a34-112">**E\_INVALIDARG** is returned if the *pPropertyDataId* parameter is one of the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a34-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6a34-113">Requirements</span></span>



| <span data-ttu-id="e6a34-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a34-114">Requirement</span></span> | <span data-ttu-id="e6a34-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e6a34-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a34-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6a34-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a34-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e6a34-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e6a34-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6a34-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a34-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e6a34-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e6a34-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6a34-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a34-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e6a34-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e6a34-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e6a34-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6a34-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6a34-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e6a34-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6a34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a34-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e6a34-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e6a34-126">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e6a34-126">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="e6a34-127">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e6a34-127">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="e6a34-128">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e6a34-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="e6a34-129">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="e6a34-129">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="e6a34-130">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="e6a34-130">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="e6a34-131">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="e6a34-131">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="e6a34-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="e6a34-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




