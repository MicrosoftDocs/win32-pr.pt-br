---
description: O \_ método Get fullscreenmode recupera o modo de tela inteira atual.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Método de CBaseControlWindow.get_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787429"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a><span data-ttu-id="750dc-103">Método CBaseControlWindow. get \_ fullscreenmode</span><span class="sxs-lookup"><span data-stu-id="750dc-103">CBaseControlWindow.get\_FullScreenMode method</span></span>

<span data-ttu-id="750dc-104">O `get_FullScreenMode` método recupera o modo de tela inteira atual.</span><span class="sxs-lookup"><span data-stu-id="750dc-104">The `get_FullScreenMode` method retrieves the current full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="750dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="750dc-105">Syntax</span></span>


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="750dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="750dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750dc-107">*Tela inteira*</span><span class="sxs-lookup"><span data-stu-id="750dc-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="750dc-108">Ponteiro para o modo de tela inteira atual.</span><span class="sxs-lookup"><span data-stu-id="750dc-108">Pointer to the current full-screen mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750dc-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="750dc-109">Return value</span></span>

<span data-ttu-id="750dc-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="750dc-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="750dc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="750dc-111">Remarks</span></span>

<span data-ttu-id="750dc-112">Essa função de membro retorna E \_ NOTIMPL por padrão.</span><span class="sxs-lookup"><span data-stu-id="750dc-112">This member function returns E\_NOTIMPL by default.</span></span> <span data-ttu-id="750dc-113">Isso informa ao distribuidor de plug-in do [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) que esse processador não implementa um processador de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="750dc-113">This informs the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor that this renderer does not implement a full-screen renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="750dc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="750dc-114">Requirements</span></span>



| <span data-ttu-id="750dc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="750dc-115">Requirement</span></span> | <span data-ttu-id="750dc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="750dc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="750dc-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="750dc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="750dc-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="750dc-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="750dc-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="750dc-119">Library</span></span><br/> | <dl> <span data-ttu-id="750dc-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="750dc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="750dc-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="750dc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750dc-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="750dc-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




