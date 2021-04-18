---
description: O método OnReceiveMessage manipula mensagens de janela.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Método CBaseWindow. OnReceiveMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752089"
---
# <a name="cbasewindowonreceivemessage-method"></a><span data-ttu-id="6ee6d-103">Método CBaseWindow. OnReceiveMessage</span><span class="sxs-lookup"><span data-stu-id="6ee6d-103">CBaseWindow.OnReceiveMessage method</span></span>

<span data-ttu-id="6ee6d-104">O `OnReceiveMessage` método manipula mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="6ee6d-104">The `OnReceiveMessage` method handles window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee6d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ee6d-105">Syntax</span></span>


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="6ee6d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ee6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee6d-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6ee6d-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee6d-108">Identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="6ee6d-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="6ee6d-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="6ee6d-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee6d-110">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6ee6d-110">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6ee6d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ee6d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee6d-112">Primeiro parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6ee6d-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6ee6d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ee6d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ee6d-114">Segundo parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6ee6d-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee6d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ee6d-115">Return value</span></span>

<span data-ttu-id="6ee6d-116">Retornará 0 se a mensagem tiver sido processada ou 1 se a mensagem não tiver sido processada.</span><span class="sxs-lookup"><span data-stu-id="6ee6d-116">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ee6d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ee6d-117">Remarks</span></span>

<span data-ttu-id="6ee6d-118">A classe base manipula as seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="6ee6d-118">The base class handles the following messages:</span></span>

-   <span data-ttu-id="6ee6d-119">fechar o WM \_</span><span class="sxs-lookup"><span data-stu-id="6ee6d-119">WM\_CLOSE</span></span>
-   <span data-ttu-id="6ee6d-120">movimentação do WM \_</span><span class="sxs-lookup"><span data-stu-id="6ee6d-120">WM\_MOVE</span></span>
-   <span data-ttu-id="6ee6d-121">paleta do WMchanged \_</span><span class="sxs-lookup"><span data-stu-id="6ee6d-121">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="6ee6d-122">QUERYNEWPALETTE do WM \_</span><span class="sxs-lookup"><span data-stu-id="6ee6d-122">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="6ee6d-123">tamanho do WM \_</span><span class="sxs-lookup"><span data-stu-id="6ee6d-123">WM\_SIZE</span></span>
-   <span data-ttu-id="6ee6d-124">SYSCOLORCHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="6ee6d-124">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="6ee6d-125">Uma classe derivada pode substituir esse método para lidar com outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="6ee6d-125">A derived class can override this method to handle other messages.</span></span> <span data-ttu-id="6ee6d-126">A classe derivada deve chamar o método de classe base para manipular todas as mensagens que a classe derivada ignora.</span><span class="sxs-lookup"><span data-stu-id="6ee6d-126">The derived class should call the base class method to handle any messages that the derived class ignores.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee6d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ee6d-127">Requirements</span></span>



| <span data-ttu-id="6ee6d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee6d-128">Requirement</span></span> | <span data-ttu-id="6ee6d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee6d-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee6d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ee6d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6ee6d-131"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ee6d-131"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ee6d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ee6d-132">Library</span></span><br/> | <dl> <span data-ttu-id="6ee6d-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6ee6d-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee6d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ee6d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee6d-135">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="6ee6d-135">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




