---
description: Determina se o objeto IContextNode contém dados armazenados no identificador especificado.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'Método IContextNode:: ContainsPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461158"
---
# <a name="icontextnodecontainspropertydata-method"></a><span data-ttu-id="23663-103">Método IContextNode:: ContainsPropertyData</span><span class="sxs-lookup"><span data-stu-id="23663-103">IContextNode::ContainsPropertyData method</span></span>

<span data-ttu-id="23663-104">Determina se o objeto [**IContextNode**](icontextnode.md) contém dados armazenados no identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="23663-104">Determines whether the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="23663-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23663-105">Syntax</span></span>


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a><span data-ttu-id="23663-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23663-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23663-107">*pPropertyDataId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23663-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23663-108">O identificador dos dados.</span><span class="sxs-lookup"><span data-stu-id="23663-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="23663-109">*pbContains* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="23663-109">*pbContains* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23663-110">**Variante \_ TRUE** se o objeto [**IContextNode**](icontextnode.md) contiver dados armazenados sob o identificador especificado; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="23663-110">**VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23663-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23663-111">Return value</span></span>

<span data-ttu-id="23663-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="23663-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23663-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="23663-113">Remarks</span></span>

<span data-ttu-id="23663-114">Além dos dados específicos do aplicativo, você também pode usar esse método para determinar se esse [**IContextNode**](icontextnode.md) contém outros dados internos (consulte [Propriedades de dica de análise](analysis-hint-properties.md) e propriedades de nó de [contexto](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="23663-114">In addition to application-specific data, you can also use this method to determine whether this [**IContextNode**](icontextnode.md) contains other internal data (see [Analysis Hint Properties](analysis-hint-properties.md) and [Context Node Properties](context-node-properties.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="23663-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23663-115">Requirements</span></span>



| <span data-ttu-id="23663-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="23663-116">Requirement</span></span> | <span data-ttu-id="23663-117">Valor</span><span class="sxs-lookup"><span data-stu-id="23663-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23663-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23663-118">Minimum supported client</span></span><br/> | <span data-ttu-id="23663-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="23663-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="23663-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23663-120">Minimum supported server</span></span><br/> | <span data-ttu-id="23663-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="23663-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="23663-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23663-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="23663-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="23663-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="23663-124">DLL</span><span class="sxs-lookup"><span data-stu-id="23663-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23663-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23663-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="23663-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="23663-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23663-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="23663-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="23663-128">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="23663-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="23663-129">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="23663-129">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="23663-130">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="23663-130">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="23663-131">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="23663-131">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="23663-132">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="23663-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="23663-133">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="23663-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="23663-134">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="23663-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




