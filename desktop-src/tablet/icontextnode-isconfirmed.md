---
description: Recupera um valor que indica se o confirmtype passado para esse método foi definido neste IContextNode.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'Método IContextNode:: isconfirmed (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501811"
---
# <a name="icontextnodeisconfirmed-method"></a><span data-ttu-id="77b6d-103">Método IContextNode:: isconfirmed</span><span class="sxs-lookup"><span data-stu-id="77b6d-103">IContextNode::IsConfirmed method</span></span>

<span data-ttu-id="77b6d-104">Recupera um valor que indica se o confirmtype passado para esse método foi definido neste IContextNode.</span><span class="sxs-lookup"><span data-stu-id="77b6d-104">Retrieves a value that indicates whether the ConfirmationType passed in to this method has been set on this IContextNode.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b6d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77b6d-105">Syntax</span></span>


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a><span data-ttu-id="77b6d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77b6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77b6d-107">*confirmable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77b6d-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b6d-108">O tipo de confirmação que está sendo testado para.</span><span class="sxs-lookup"><span data-stu-id="77b6d-108">The confirmation type being tested for.</span></span>

</dd> <dt>

<span data-ttu-id="77b6d-109">*pfTypeConfirmed* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="77b6d-109">*pfTypeConfirmed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77b6d-110">**Variante \_ TRUE** se o tipo transmitido em confirmated tiver sido definido neste objeto [**IContextNode**](icontextnode.md) ; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="77b6d-110">**VARIANT\_TRUE** if the type passed in confirmedType has been set on this [**IContextNode**](icontextnode.md) object; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77b6d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77b6d-111">Return value</span></span>

<span data-ttu-id="77b6d-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="77b6d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77b6d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="77b6d-113">Remarks</span></span>

<span data-ttu-id="77b6d-114">Esse valor é definido pelo método [**IContextNode:: Confirm**](icontextnode-confirm.md) .</span><span class="sxs-lookup"><span data-stu-id="77b6d-114">This value is set by the [**IContextNode::Confirm**](icontextnode-confirm.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="77b6d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77b6d-115">Requirements</span></span>



| <span data-ttu-id="77b6d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="77b6d-116">Requirement</span></span> | <span data-ttu-id="77b6d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="77b6d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77b6d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77b6d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="77b6d-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="77b6d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="77b6d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77b6d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="77b6d-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="77b6d-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="77b6d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77b6d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="77b6d-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="77b6d-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="77b6d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="77b6d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77b6d-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77b6d-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="77b6d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="77b6d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b6d-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="77b6d-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="77b6d-128">**IContextNode:: confirmar**</span><span class="sxs-lookup"><span data-stu-id="77b6d-128">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="77b6d-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="77b6d-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




