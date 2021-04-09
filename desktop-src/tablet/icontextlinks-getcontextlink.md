---
description: Recupera o IContextLink no índice especificado.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'Método IContextLinks:: GetContextLink (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090551"
---
# <a name="icontextlinksgetcontextlink-method"></a><span data-ttu-id="abc71-103">Método IContextLinks:: GetContextLink</span><span class="sxs-lookup"><span data-stu-id="abc71-103">IContextLinks::GetContextLink method</span></span>

<span data-ttu-id="abc71-104">Recupera o [**IContextLink**](icontextlink.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="abc71-104">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc71-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abc71-105">Syntax</span></span>


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a><span data-ttu-id="abc71-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abc71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc71-107">*ulIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abc71-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abc71-108">O índice de base zero do objeto [**IContextLink**](icontextlink.md) a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="abc71-108">The zero-based index of the [**IContextLink**](icontextlink.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="abc71-109">*ppContextLink* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abc71-109">*ppContextLink* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abc71-110">Um ponteiro para o objeto [**IContextLink**](icontextlink.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="abc71-110">A pointer to the [**IContextLink**](icontextlink.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abc71-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abc71-111">Return value</span></span>

<span data-ttu-id="abc71-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="abc71-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abc71-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="abc71-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="abc71-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextLink* quando você não precisar mais usar o link de contexto.</span><span class="sxs-lookup"><span data-stu-id="abc71-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLink* when you no longer need to use the context link.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="abc71-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abc71-115">Requirements</span></span>



| <span data-ttu-id="abc71-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="abc71-116">Requirement</span></span> | <span data-ttu-id="abc71-117">Valor</span><span class="sxs-lookup"><span data-stu-id="abc71-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc71-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abc71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="abc71-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="abc71-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="abc71-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abc71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="abc71-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="abc71-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="abc71-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="abc71-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="abc71-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="abc71-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="abc71-124">DLL</span><span class="sxs-lookup"><span data-stu-id="abc71-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abc71-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abc71-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="abc71-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="abc71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc71-127">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="abc71-127">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="abc71-128">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="abc71-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="abc71-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="abc71-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

