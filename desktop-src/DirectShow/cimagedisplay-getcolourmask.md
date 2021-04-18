---
description: O método GetColourMask recupera as máscaras de cores para o formato de exibição atual.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Método CImageDisplay. GetColourMask (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778502"
---
# <a name="cimagedisplaygetcolourmask-method"></a><span data-ttu-id="78960-103">Método CImageDisplay. GetColourMask</span><span class="sxs-lookup"><span data-stu-id="78960-103">CImageDisplay.GetColourMask method</span></span>

<span data-ttu-id="78960-104">O `GetColourMask` método recupera as máscaras de cores para o formato de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="78960-104">The `GetColourMask` method retrieves the color masks for the current display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="78960-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78960-105">Syntax</span></span>


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a><span data-ttu-id="78960-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78960-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78960-107">*pMaskRed*</span><span class="sxs-lookup"><span data-stu-id="78960-107">*pMaskRed*</span></span> 
</dt> <dd>

<span data-ttu-id="78960-108">Ponteiro para uma variável que recebe a máscara de componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="78960-108">Pointer to a variable that receives the red-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="78960-109">*pMaskGreen*</span><span class="sxs-lookup"><span data-stu-id="78960-109">*pMaskGreen*</span></span> 
</dt> <dd>

<span data-ttu-id="78960-110">Ponteiro para uma variável que recebe a máscara de componente verde.</span><span class="sxs-lookup"><span data-stu-id="78960-110">Pointer to a variable that receives the green-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="78960-111">*pMaskBlue*</span><span class="sxs-lookup"><span data-stu-id="78960-111">*pMaskBlue*</span></span> 
</dt> <dd>

<span data-ttu-id="78960-112">Ponteiro para uma variável que recebe a máscara de componente azul.</span><span class="sxs-lookup"><span data-stu-id="78960-112">Pointer to a variable that receives the blue-component mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78960-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78960-113">Return value</span></span>

<span data-ttu-id="78960-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="78960-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="78960-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78960-115">Requirements</span></span>



| <span data-ttu-id="78960-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="78960-116">Requirement</span></span> | <span data-ttu-id="78960-117">Valor</span><span class="sxs-lookup"><span data-stu-id="78960-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78960-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78960-118">Header</span></span><br/>  | <dl> <span data-ttu-id="78960-119"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78960-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78960-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78960-120">Library</span></span><br/> | <dl> <span data-ttu-id="78960-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="78960-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78960-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="78960-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78960-123">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="78960-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




