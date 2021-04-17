---
description: O método setrealize especifica se a janela do percebe as paletas.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Método CBaseWindow. setrealize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789981"
---
# <a name="cbasewindowsetrealize-method"></a><span data-ttu-id="cc850-103">Método CBaseWindow. setrealde</span><span class="sxs-lookup"><span data-stu-id="cc850-103">CBaseWindow.SetRealize method</span></span>

<span data-ttu-id="cc850-104">O `SetRealize` método especifica se a janela do percebe as paletas.</span><span class="sxs-lookup"><span data-stu-id="cc850-104">The `SetRealize` method specifies whether the window realizes palettes.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc850-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc850-105">Syntax</span></span>


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a><span data-ttu-id="cc850-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc850-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc850-107">*bRealize*</span><span class="sxs-lookup"><span data-stu-id="cc850-107">*bRealize*</span></span> 
</dt> <dd>

<span data-ttu-id="cc850-108">Valor booliano que especifica se as paletas devem ser concretizadas.</span><span class="sxs-lookup"><span data-stu-id="cc850-108">Boolean value that specifies whether to realize palettes.</span></span> <span data-ttu-id="cc850-109">Se **for true**, o método [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) perceberá paletas.</span><span class="sxs-lookup"><span data-stu-id="cc850-109">If **TRUE**, the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method realizes palettes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc850-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc850-110">Return value</span></span>

<span data-ttu-id="cc850-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cc850-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc850-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc850-112">Remarks</span></span>

<span data-ttu-id="cc850-113">Por padrão, o método **SetPalette** percebe a paleta especificada.</span><span class="sxs-lookup"><span data-stu-id="cc850-113">By default, the **SetPalette** method realizes the specified palette.</span></span> <span data-ttu-id="cc850-114">Chame esse método para alterar o comportamento padrão, de modo que as paletas sejam selecionadas, mas não realizadas.</span><span class="sxs-lookup"><span data-stu-id="cc850-114">Call this method to change the default behavior, so that palettes are selected but not realized.</span></span> <span data-ttu-id="cc850-115">Esse método define a variável de membro [**CBaseWindow:: m \_ bNoRealize**](cbasewindow-m-bnorealize.md) .</span><span class="sxs-lookup"><span data-stu-id="cc850-115">This method sets the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc850-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc850-116">Requirements</span></span>



| <span data-ttu-id="cc850-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc850-117">Requirement</span></span> | <span data-ttu-id="cc850-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cc850-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc850-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc850-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cc850-120"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc850-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc850-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc850-121">Library</span></span><br/> | <dl> <span data-ttu-id="cc850-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cc850-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc850-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc850-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc850-124">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="cc850-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




