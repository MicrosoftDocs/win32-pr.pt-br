---
description: O \_ método Put BackgroundPalette define um sinalizador para obter a paleta em segundo plano.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Método de CBaseControlWindow.put_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750686"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a><span data-ttu-id="09cd4-103">Método CBaseControlWindow. put \_ BackgroundPalette</span><span class="sxs-lookup"><span data-stu-id="09cd4-103">CBaseControlWindow.put\_BackgroundPalette method</span></span>

<span data-ttu-id="09cd4-104">O `put_BackgroundPalette` método define um sinalizador para obter a paleta em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="09cd4-104">The `put_BackgroundPalette` method sets a flag to realize the palette in the background.</span></span>

## <a name="syntax"></a><span data-ttu-id="09cd4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09cd4-105">Syntax</span></span>


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="09cd4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09cd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09cd4-107">*BackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="09cd4-107">*BackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="09cd4-108">Sinalizador booliano de automação (0 está desativado, 1 está ativado).</span><span class="sxs-lookup"><span data-stu-id="09cd4-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09cd4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09cd4-109">Return value</span></span>

<span data-ttu-id="09cd4-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09cd4-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09cd4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="09cd4-111">Remarks</span></span>

<span data-ttu-id="09cd4-112">Para reproduzir um vídeo dentro de outro aplicativo ou documento, o aplicativo pode querer usar sua própria paleta.</span><span class="sxs-lookup"><span data-stu-id="09cd4-112">To play a video within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="09cd4-113">Ele pode perguntar se o vídeo usa a paleta de primeiro plano atual, em vez de sua própria, como a paleta de plano de fundo, definindo esse sinalizador como 1.</span><span class="sxs-lookup"><span data-stu-id="09cd4-113">It can ask that the video use the current foreground palette rather than its own as the background palette by setting this flag to  1.</span></span> <span data-ttu-id="09cd4-114">Se isso for definido como 0, a janela será instalada e perceberá sua própria paleta preferida.</span><span class="sxs-lookup"><span data-stu-id="09cd4-114">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="09cd4-115">Pedir que a janela use uma paleta diferente causará severas penalidades de desempenho.</span><span class="sxs-lookup"><span data-stu-id="09cd4-115">Asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="09cd4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09cd4-116">Requirements</span></span>



| <span data-ttu-id="09cd4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="09cd4-117">Requirement</span></span> | <span data-ttu-id="09cd4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="09cd4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09cd4-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09cd4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="09cd4-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09cd4-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09cd4-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09cd4-121">Library</span></span><br/> | <dl> <span data-ttu-id="09cd4-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="09cd4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09cd4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="09cd4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09cd4-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="09cd4-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




