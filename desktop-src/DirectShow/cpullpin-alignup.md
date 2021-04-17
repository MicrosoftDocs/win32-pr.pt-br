---
description: O método AlignUp Arredonda um valor para cima até um limite de alinhamento especificado. Observação removida no Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Método CPullPin. AlignUp (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789958"
---
# <a name="cpullpinalignup-method"></a><span data-ttu-id="0bf0a-104">Método CPullPin. AlignUp</span><span class="sxs-lookup"><span data-stu-id="0bf0a-104">CPullPin.AlignUp method</span></span>

<span data-ttu-id="0bf0a-105">O método **AlignUp** Arredonda um valor para cima até um limite de alinhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="0bf0a-105">The **AlignUp** method rounds a value up to a specified alignment boundary.</span></span>

> [!Note]  
> <span data-ttu-id="0bf0a-106">Removido do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0bf0a-106">Removed in Windows 7.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0bf0a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bf0a-107">Syntax</span></span>


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="0bf0a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bf0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf0a-109">*precisa*</span><span class="sxs-lookup"><span data-stu-id="0bf0a-109">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf0a-110">Especifica o número a ser alinhado.</span><span class="sxs-lookup"><span data-stu-id="0bf0a-110">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="0bf0a-111">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="0bf0a-111">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf0a-112">Especifica o limite de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="0bf0a-112">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bf0a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bf0a-113">Return value</span></span>

<span data-ttu-id="0bf0a-114">Retorna o resultado alinhado.</span><span class="sxs-lookup"><span data-stu-id="0bf0a-114">Returns the aligned result.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bf0a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bf0a-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0bf0a-116">Esse método pode causar estouro numérico se *ll* + (*LALIGN* -1) estouros.</span><span class="sxs-lookup"><span data-stu-id="0bf0a-116">This method can cause numeric overflow if *ll* + (*lAlign* - 1) overflows.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0bf0a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bf0a-117">Requirements</span></span>



| <span data-ttu-id="0bf0a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bf0a-118">Requirement</span></span> | <span data-ttu-id="0bf0a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0bf0a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf0a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bf0a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0bf0a-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bf0a-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="0bf0a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bf0a-122">Library</span></span><br/> | <dl> <span data-ttu-id="0bf0a-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0bf0a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf0a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bf0a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf0a-125">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="0bf0a-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




