---
description: Ocorre quando a classe InkCollector detecta um botão de cursor que está inoperante.
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Evento InkCollector. CursorButtonDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3994782d1266af5060bad28dd2221fe1ba18874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296309"
---
# <a name="inkcollectorcursorbuttondown-event"></a><span data-ttu-id="e6d08-103">Evento InkCollector. CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="e6d08-103">InkCollector.CursorButtonDown event</span></span>

<span data-ttu-id="e6d08-104">Ocorre quando a [**classe InkCollector**](inkcollector-class.md) detecta um botão de cursor que está inoperante.</span><span class="sxs-lookup"><span data-stu-id="e6d08-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6d08-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="e6d08-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6d08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d08-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6d08-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d08-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorButtonDown** .</span><span class="sxs-lookup"><span data-stu-id="e6d08-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="e6d08-109">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6d08-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d08-110">O botão que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="e6d08-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d08-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6d08-111">Return value</span></span>

<span data-ttu-id="e6d08-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e6d08-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6d08-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6d08-113">Remarks</span></span>

<span data-ttu-id="e6d08-114">Um botão em uma dica de caneta fica inoperante quando o usuário abaixa a caneta para o digitalizador e começa a rastrear um traço.</span><span class="sxs-lookup"><span data-stu-id="e6d08-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="e6d08-115">Um botão em um cilindro fica inativo quando o botão é pressionado.</span><span class="sxs-lookup"><span data-stu-id="e6d08-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="e6d08-116">Quando você pressiona o botão direito do mouse, você realmente recebe dois eventos **CursorButtonDown** – um para o botão direito pressionado e outro para o botão esquerdo pressionado.</span><span class="sxs-lookup"><span data-stu-id="e6d08-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="e6d08-117">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICECursorButtonDown de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="e6d08-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d08-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6d08-118">Requirements</span></span>



| <span data-ttu-id="e6d08-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d08-119">Requirement</span></span> | <span data-ttu-id="e6d08-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e6d08-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d08-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6d08-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d08-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e6d08-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e6d08-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6d08-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d08-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e6d08-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e6d08-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6d08-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6d08-126"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e6d08-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e6d08-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6d08-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6d08-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6d08-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e6d08-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6d08-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d08-130">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="e6d08-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="e6d08-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="e6d08-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="e6d08-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="e6d08-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="e6d08-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="e6d08-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="e6d08-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="e6d08-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




