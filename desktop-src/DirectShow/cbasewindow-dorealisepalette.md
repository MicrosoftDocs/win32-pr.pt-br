---
description: O método DoRealisePalette percebe a paleta atual da janela.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Método CBaseWindow. DoRealisePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755602"
---
# <a name="cbasewindowdorealisepalette-method"></a><span data-ttu-id="9a2a4-103">Método CBaseWindow. DoRealisePalette</span><span class="sxs-lookup"><span data-stu-id="9a2a4-103">CBaseWindow.DoRealisePalette method</span></span>

<span data-ttu-id="9a2a4-104">O `DoRealisePalette` método percebe a paleta atual da janela.</span><span class="sxs-lookup"><span data-stu-id="9a2a4-104">The `DoRealisePalette` method realizes the window's current palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2a4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a2a4-105">Syntax</span></span>


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a><span data-ttu-id="9a2a4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a2a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a2a4-107">*bForceBackground*</span><span class="sxs-lookup"><span data-stu-id="9a2a4-107">*bForceBackground*</span></span> 
</dt> <dd>

<span data-ttu-id="9a2a4-108">Valor booliano que especifica se a paleta é forçada a ser uma paleta de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="9a2a4-108">Boolean value that specifies whether the palette is forced to be a background palette.</span></span> <span data-ttu-id="9a2a4-109">Para obter mais informações, consulte **SelectPalette** no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="9a2a4-109">For more information, see **SelectPalette** in the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a2a4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a2a4-110">Return value</span></span>

<span data-ttu-id="9a2a4-111">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a2a4-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="9a2a4-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9a2a4-112">Return code</span></span>                                                                             | <span data-ttu-id="9a2a4-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a2a4-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="9a2a4-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="9a2a4-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9a2a4-115">Uma chamada interna para **GdiFlush** retornou um erro.</span><span class="sxs-lookup"><span data-stu-id="9a2a4-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="9a2a4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a2a4-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9a2a4-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="9a2a4-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="9a2a4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a2a4-118">Remarks</span></span>

<span data-ttu-id="9a2a4-119">O método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="9a2a4-119">The [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method calls this method.</span></span> <span data-ttu-id="9a2a4-120">Para definir uma nova paleta, chame o método [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) .</span><span class="sxs-lookup"><span data-stu-id="9a2a4-120">To set a new palette, call the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a2a4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a2a4-121">Requirements</span></span>



| <span data-ttu-id="9a2a4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a2a4-122">Requirement</span></span> | <span data-ttu-id="9a2a4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9a2a4-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2a4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a2a4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9a2a4-125"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a2a4-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a2a4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a2a4-126">Library</span></span><br/> | <dl> <span data-ttu-id="9a2a4-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9a2a4-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a2a4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a2a4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a2a4-129">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="9a2a4-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




