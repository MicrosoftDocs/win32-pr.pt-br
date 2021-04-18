---
description: O método CompleteConnect notifica a janela de que o pino de entrada do renderizador foi conectado.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Método CBaseWindow. CompleteConnect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770106"
---
# <a name="cbasewindowcompleteconnect-method"></a><span data-ttu-id="f5ec8-103">Método CBaseWindow. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="f5ec8-103">CBaseWindow.CompleteConnect method</span></span>

<span data-ttu-id="f5ec8-104">O `CompleteConnect` método notifica a janela que o pino de entrada do renderizador foi conectado.</span><span class="sxs-lookup"><span data-stu-id="f5ec8-104">The `CompleteConnect` method notifies the window that the renderer's input pin has been connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ec8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5ec8-105">Syntax</span></span>


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a><span data-ttu-id="f5ec8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5ec8-106">Parameters</span></span>

<span data-ttu-id="f5ec8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f5ec8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5ec8-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5ec8-108">Return value</span></span>

<span data-ttu-id="f5ec8-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f5ec8-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5ec8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5ec8-110">Remarks</span></span>

<span data-ttu-id="f5ec8-111">Esse método redefine o sinalizador de ativação da janela ([**CBaseWindow:: m \_ bActivated**](cbasewindow-m-bactivated.md)) como **false**.</span><span class="sxs-lookup"><span data-stu-id="f5ec8-111">This method resets the window activation flag ([**CBaseWindow::m\_bActivated**](cbasewindow-m-bactivated.md)) to **FALSE**.</span></span> <span data-ttu-id="f5ec8-112">Quando um processador de vídeo conclui uma conexão de PIN, ele pode chamar o método [**CBaseWindow:: ActivateWindow**](cbasewindow-activatewindow.md) para definir o tamanho e a posição da janela.</span><span class="sxs-lookup"><span data-stu-id="f5ec8-112">When a video renderer completes a pin connection, it might call the [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) method to set the window's size and position.</span></span> <span data-ttu-id="f5ec8-113">Para forçar o **ActivateWindow** a recalcular esses atributos, primeiro chame o `CompleteConnect` método.</span><span class="sxs-lookup"><span data-stu-id="f5ec8-113">To force **ActivateWindow** to recalculate these attributes, first call the `CompleteConnect` method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ec8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5ec8-114">Requirements</span></span>



| <span data-ttu-id="f5ec8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ec8-115">Requirement</span></span> | <span data-ttu-id="f5ec8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f5ec8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ec8-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5ec8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f5ec8-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5ec8-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5ec8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5ec8-119">Library</span></span><br/> | <dl> <span data-ttu-id="f5ec8-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f5ec8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ec8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5ec8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ec8-122">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="f5ec8-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




