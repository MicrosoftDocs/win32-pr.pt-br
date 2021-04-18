---
description: O \_ método Get BackgroundPalette recupera a paleta realizada no sinalizador de segundo plano.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Método de CBaseControlWindow.get_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749644"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a><span data-ttu-id="52372-103">CBaseControlWindow. obter \_ método BackgroundPalette</span><span class="sxs-lookup"><span data-stu-id="52372-103">CBaseControlWindow.get\_BackgroundPalette method</span></span>

<span data-ttu-id="52372-104">O `get_BackgroundPalette` método recupera a paleta realizada no sinalizador de segundo plano.</span><span class="sxs-lookup"><span data-stu-id="52372-104">The `get_BackgroundPalette` method retrieves the realized palette in the background flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="52372-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52372-105">Syntax</span></span>


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="52372-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52372-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52372-107">*pBackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="52372-107">*pBackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="52372-108">Ponteiro para um sinalizador booliano de automação (0 está desativado, 1 está ativado).</span><span class="sxs-lookup"><span data-stu-id="52372-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52372-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52372-109">Return value</span></span>

<span data-ttu-id="52372-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="52372-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52372-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="52372-111">Remarks</span></span>

<span data-ttu-id="52372-112">Essa função de membro implementa o método [**IVideoWindow:: get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) .</span><span class="sxs-lookup"><span data-stu-id="52372-112">This member function implements the [**IVideoWindow::get\_BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) method.</span></span> <span data-ttu-id="52372-113">Se um vídeo for reproduzido dentro de outro aplicativo ou documento, talvez o aplicativo queira usar sua própria paleta.</span><span class="sxs-lookup"><span data-stu-id="52372-113">If a video will be played within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="52372-114">Ele pode perguntar se o vídeo usa a paleta de primeiro plano atual em vez de sua própria definindo esse sinalizador como 1.</span><span class="sxs-lookup"><span data-stu-id="52372-114">It can ask that the video use the current foreground palette rather than its own by setting this flag to  1.</span></span> <span data-ttu-id="52372-115">Se isso for definido como 0, a janela será instalada e perceberá sua própria paleta preferida.</span><span class="sxs-lookup"><span data-stu-id="52372-115">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="52372-116">Observe que solicitar que a janela use uma paleta diferente causará severas penalidades de desempenho.</span><span class="sxs-lookup"><span data-stu-id="52372-116">Note that asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="52372-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52372-117">Requirements</span></span>



| <span data-ttu-id="52372-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="52372-118">Requirement</span></span> | <span data-ttu-id="52372-119">Valor</span><span class="sxs-lookup"><span data-stu-id="52372-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52372-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52372-120">Header</span></span><br/>  | <dl> <span data-ttu-id="52372-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52372-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="52372-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52372-122">Library</span></span><br/> | <dl> <span data-ttu-id="52372-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="52372-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52372-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="52372-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52372-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="52372-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




