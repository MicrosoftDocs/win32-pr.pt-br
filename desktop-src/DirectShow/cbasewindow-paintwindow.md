---
description: O método PaintWindow faz com que a janela seja repintada.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Método CBaseWindow. PaintWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752707"
---
# <a name="cbasewindowpaintwindow-method"></a><span data-ttu-id="80acf-103">Método CBaseWindow. PaintWindow</span><span class="sxs-lookup"><span data-stu-id="80acf-103">CBaseWindow.PaintWindow method</span></span>

<span data-ttu-id="80acf-104">O `PaintWindow` método faz com que a janela seja repintada.</span><span class="sxs-lookup"><span data-stu-id="80acf-104">The `PaintWindow` method causes the window to be repainted.</span></span>

## <a name="syntax"></a><span data-ttu-id="80acf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80acf-105">Syntax</span></span>


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a><span data-ttu-id="80acf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80acf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80acf-107">*bErase*</span><span class="sxs-lookup"><span data-stu-id="80acf-107">*bErase*</span></span> 
</dt> <dd>

<span data-ttu-id="80acf-108">Valor booliano que especifica se o plano de fundo é apagado.</span><span class="sxs-lookup"><span data-stu-id="80acf-108">Boolean value that specifies whether the background is erased.</span></span> <span data-ttu-id="80acf-109">Se o valor for **true**, o plano de fundo será apagado.</span><span class="sxs-lookup"><span data-stu-id="80acf-109">If the value is **TRUE**, the background is erased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80acf-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80acf-110">Return value</span></span>

<span data-ttu-id="80acf-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="80acf-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80acf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="80acf-112">Remarks</span></span>

<span data-ttu-id="80acf-113">Esse método gera uma mensagem de pintura do WM \_ invalidando a área inteira do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="80acf-113">This method generates a WM\_PAINT message by invalidating the window's entire client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="80acf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80acf-114">Requirements</span></span>



| <span data-ttu-id="80acf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="80acf-115">Requirement</span></span> | <span data-ttu-id="80acf-116">Valor</span><span class="sxs-lookup"><span data-stu-id="80acf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80acf-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80acf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="80acf-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80acf-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80acf-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80acf-119">Library</span></span><br/> | <dl> <span data-ttu-id="80acf-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="80acf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80acf-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="80acf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80acf-122">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="80acf-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




