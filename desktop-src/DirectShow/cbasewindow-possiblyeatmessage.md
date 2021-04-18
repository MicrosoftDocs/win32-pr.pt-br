---
description: O método PossiblyEatMessage permite que uma classe derivada encaminhe mensagens para outra janela.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Método CBaseWindow. PossiblyEatMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751694"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a><span data-ttu-id="6c7ca-103">Método CBaseWindow. PossiblyEatMessage</span><span class="sxs-lookup"><span data-stu-id="6c7ca-103">CBaseWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="6c7ca-104">O `PossiblyEatMessage` método permite que uma classe derivada encaminhe mensagens para outra janela.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-104">The `PossiblyEatMessage` method enables a derived class to forward messages to another window.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c7ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c7ca-105">Syntax</span></span>


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="6c7ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c7ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c7ca-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="6c7ca-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6c7ca-108">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-108">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6c7ca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c7ca-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c7ca-110">Primeiro parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6c7ca-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c7ca-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c7ca-112">Segundo parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c7ca-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c7ca-113">Return value</span></span>

<span data-ttu-id="6c7ca-114">Retorna **true** se a mensagem foi encaminhada ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-114">Returns **TRUE** if the message was forwarded, or **FALSE** otherwise.</span></span> <span data-ttu-id="6c7ca-115">A classe base retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-115">The base class returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c7ca-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c7ca-116">Remarks</span></span>

<span data-ttu-id="6c7ca-117">Antes que o método [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) manipule uma mensagem, ele chama `PossiblyEatMessage` .</span><span class="sxs-lookup"><span data-stu-id="6c7ca-117">Before the [**CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) method handles a message, it calls `PossiblyEatMessage`.</span></span> <span data-ttu-id="6c7ca-118">Se `PossiblyEatMessage` retornar **true**, **OnReceiveMessage** ignorará a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-118">If `PossiblyEatMessage` returns **TRUE**, **OnReceiveMessage** ignores the message.</span></span> <span data-ttu-id="6c7ca-119">Uma classe derivada pode substituir `PossiblyEatMessage` para que ela encaminhe algumas mensagens para uma janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-119">A derived class can override `PossiblyEatMessage` so that it forwards some messages to an owner window.</span></span> <span data-ttu-id="6c7ca-120">Por exemplo, a classe [**CBaseControlWindow**](cbasecontrolwindow.md) , que deriva de **CBaseWindow**, encaminha mensagens de teclado e mouse.</span><span class="sxs-lookup"><span data-stu-id="6c7ca-120">For example, the [**CBaseControlWindow**](cbasecontrolwindow.md) class, which derives from **CBaseWindow**, forwards keyboard and mouse messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c7ca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c7ca-121">Requirements</span></span>



| <span data-ttu-id="6c7ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c7ca-122">Requirement</span></span> | <span data-ttu-id="6c7ca-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6c7ca-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7ca-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c7ca-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6c7ca-125"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ca-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c7ca-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c7ca-126">Library</span></span><br/> | <dl> <span data-ttu-id="6c7ca-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ca-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c7ca-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c7ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c7ca-129">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="6c7ca-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




