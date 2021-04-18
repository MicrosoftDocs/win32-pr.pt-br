---
description: O método OnPaletteChange manipula as mensagens de alteração da paleta.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Método CBaseWindow. OnPaletteChange (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757707"
---
# <a name="cbasewindowonpalettechange-method"></a><span data-ttu-id="95bd1-103">Método CBaseWindow. OnPaletteChange</span><span class="sxs-lookup"><span data-stu-id="95bd1-103">CBaseWindow.OnPaletteChange method</span></span>

<span data-ttu-id="95bd1-104">O `OnPaletteChange` método manipula as mensagens de alteração da paleta.</span><span class="sxs-lookup"><span data-stu-id="95bd1-104">The `OnPaletteChange` method handles palette-change messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="95bd1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95bd1-105">Syntax</span></span>


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a><span data-ttu-id="95bd1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95bd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95bd1-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="95bd1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="95bd1-108">Identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="95bd1-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="95bd1-109">*Message*</span><span class="sxs-lookup"><span data-stu-id="95bd1-109">*Message*</span></span> 
</dt> <dd>

<span data-ttu-id="95bd1-110">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="95bd1-110">Message identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95bd1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95bd1-111">Return value</span></span>

<span data-ttu-id="95bd1-112">Retornará 0 se a mensagem tiver sido processada ou 1 se a mensagem não tiver sido processada.</span><span class="sxs-lookup"><span data-stu-id="95bd1-112">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="95bd1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="95bd1-113">Remarks</span></span>

<span data-ttu-id="95bd1-114">Esse método manipula \_ as mensagens do WM PaletteChanged e do WM \_ QUERYNEWPALETTE.</span><span class="sxs-lookup"><span data-stu-id="95bd1-114">This method handles WM\_PALETTECHANGED and WM\_QUERYNEWPALETTE messages.</span></span> <span data-ttu-id="95bd1-115">Ele chama o método [**CBaseWindow::D orealisepalette**](cbasewindow-dorealisepalette.md) para obter a nova paleta.</span><span class="sxs-lookup"><span data-stu-id="95bd1-115">It calls the [**CBaseWindow::DoRealisePalette**](cbasewindow-dorealisepalette.md) method to realize the new palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="95bd1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95bd1-116">Requirements</span></span>



| <span data-ttu-id="95bd1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="95bd1-117">Requirement</span></span> | <span data-ttu-id="95bd1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="95bd1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95bd1-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95bd1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="95bd1-120"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95bd1-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95bd1-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95bd1-121">Library</span></span><br/> | <dl> <span data-ttu-id="95bd1-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="95bd1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95bd1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="95bd1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95bd1-124">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="95bd1-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




