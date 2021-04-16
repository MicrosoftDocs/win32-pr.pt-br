---
description: O método SetWindowForeground move a janela de vídeo para o primeiro plano e, opcionalmente, dá o foco.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Método CBaseControlWindow. SetWindowForeground (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752521"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a><span data-ttu-id="59f8d-103">Método CBaseControlWindow. SetWindowForeground</span><span class="sxs-lookup"><span data-stu-id="59f8d-103">CBaseControlWindow.SetWindowForeground method</span></span>

<span data-ttu-id="59f8d-104">O `SetWindowForeground` método move a janela de vídeo para o primeiro plano e, opcionalmente, dá o foco.</span><span class="sxs-lookup"><span data-stu-id="59f8d-104">The `SetWindowForeground` method moves the video window to the foreground and optionally gives it focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f8d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59f8d-105">Syntax</span></span>


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a><span data-ttu-id="59f8d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59f8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f8d-107">*Foco*</span><span class="sxs-lookup"><span data-stu-id="59f8d-107">*Focus*</span></span> 
</dt> <dd>

<span data-ttu-id="59f8d-108">Valor que especifica se a janela de vídeo receberá o foco.</span><span class="sxs-lookup"><span data-stu-id="59f8d-108">Value that specifies whether the video window will get focus.</span></span> <span data-ttu-id="59f8d-109">Um valor de 1 dá ao foco da janela e 0 não.</span><span class="sxs-lookup"><span data-stu-id="59f8d-109">A value of  1 gives the window focus and 0 does not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59f8d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59f8d-110">Return value</span></span>

<span data-ttu-id="59f8d-111">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="59f8d-111">Returns one of the following values.</span></span>



| <span data-ttu-id="59f8d-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="59f8d-112">Return code</span></span>                                                                                           | <span data-ttu-id="59f8d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="59f8d-113">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59f8d-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="59f8d-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="59f8d-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="59f8d-115">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="59f8d-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="59f8d-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="59f8d-117">O foco não é igual a 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="59f8d-117">Focus doesn't equal  1 or 0.</span></span><br/>                                   |
| <dl> <span data-ttu-id="59f8d-118"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="59f8d-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="59f8d-119">O filtro atual não está conectado a um grafo de filtro completo.</span><span class="sxs-lookup"><span data-stu-id="59f8d-119">The current filter isn't connected to a complete filter graph.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59f8d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59f8d-120">Requirements</span></span>



| <span data-ttu-id="59f8d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="59f8d-121">Requirement</span></span> | <span data-ttu-id="59f8d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="59f8d-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f8d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59f8d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="59f8d-124"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59f8d-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59f8d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59f8d-125">Library</span></span><br/> | <dl> <span data-ttu-id="59f8d-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="59f8d-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59f8d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="59f8d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f8d-128">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="59f8d-128">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




