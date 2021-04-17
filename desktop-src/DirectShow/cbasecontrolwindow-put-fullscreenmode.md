---
description: O \_ método Put fullscreenmode define o modo de tela inteira do processador.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Método de CBaseControlWindow.put_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752523"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a><span data-ttu-id="292d1-103">CBaseControlWindow. put \_ método fullscreenmode</span><span class="sxs-lookup"><span data-stu-id="292d1-103">CBaseControlWindow.put\_FullScreenMode method</span></span>

<span data-ttu-id="292d1-104">O `put_FullScreenMode` método define o modo de tela inteira do processador.</span><span class="sxs-lookup"><span data-stu-id="292d1-104">The `put_FullScreenMode` method sets the full-screen mode of the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="292d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="292d1-105">Syntax</span></span>


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="292d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="292d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="292d1-107">*Tela inteira*</span><span class="sxs-lookup"><span data-stu-id="292d1-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="292d1-108">Modo de tela inteira a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="292d1-108">Full-screen mode to apply.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="292d1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="292d1-109">Return value</span></span>

<span data-ttu-id="292d1-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="292d1-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="292d1-111">A implementação atual retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="292d1-111">The current implementation returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="292d1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="292d1-112">Remarks</span></span>

<span data-ttu-id="292d1-113">Um processador de vídeo que implementa um modo de tela inteira deve substituir essa função de membro e implementar quaisquer modos com suporte.</span><span class="sxs-lookup"><span data-stu-id="292d1-113">A video renderer that implements a full-screen mode should override this member function and implement whatever modes it supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="292d1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="292d1-114">Requirements</span></span>



| <span data-ttu-id="292d1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="292d1-115">Requirement</span></span> | <span data-ttu-id="292d1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="292d1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="292d1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="292d1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="292d1-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="292d1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="292d1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="292d1-119">Library</span></span><br/> | <dl> <span data-ttu-id="292d1-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="292d1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="292d1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="292d1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292d1-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="292d1-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




