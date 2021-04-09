---
description: Recupera um nome de tipo legível por humanos deste IContextNode.
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'Método IContextNode:: getTypeName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090542"
---
# <a name="icontextnodegettypename-method"></a><span data-ttu-id="2ddbd-103">Método IContextNode:: getTypeName</span><span class="sxs-lookup"><span data-stu-id="2ddbd-103">IContextNode::GetTypeName method</span></span>

<span data-ttu-id="2ddbd-104">Recupera um nome de tipo legível por humanos deste [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="2ddbd-104">Retrieves a human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ddbd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ddbd-105">Syntax</span></span>


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="2ddbd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ddbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddbd-107">*pbstrContextNodeType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2ddbd-107">*pbstrContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddbd-108">Um nome de tipo legível por humanos deste [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="2ddbd-108">A human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddbd-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ddbd-109">Return value</span></span>

<span data-ttu-id="2ddbd-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2ddbd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ddbd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ddbd-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="2ddbd-112">Para evitar um vazamento de memória, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) no \* *pbstrContextNodeType* quando você não precisar mais usar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2ddbd-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrContextNodeType* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="2ddbd-113">Por exemplo, esse método define *pbstrContextNodeType* como "InkWordNode" para um nó de palavra à tinta (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="2ddbd-113">For example, this method sets *pbstrContextNodeType* to "InkWordNode" for an ink word node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddbd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ddbd-114">Requirements</span></span>



| <span data-ttu-id="2ddbd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ddbd-115">Requirement</span></span> | <span data-ttu-id="2ddbd-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2ddbd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddbd-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ddbd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ddbd-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2ddbd-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2ddbd-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ddbd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ddbd-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2ddbd-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2ddbd-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ddbd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ddbd-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2ddbd-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2ddbd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2ddbd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ddbd-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ddbd-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2ddbd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ddbd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddbd-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="2ddbd-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2ddbd-127">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="2ddbd-127">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="2ddbd-128">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="2ddbd-128">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="2ddbd-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="2ddbd-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

