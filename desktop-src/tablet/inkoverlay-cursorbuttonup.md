---
description: Ocorre quando o InkCollector detecta um botão de cursor que está ativo.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Evento InkOverlay. CursorButtonUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8315f2cf87589bb24e5fb3c6ac6fd7128df426e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297384"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="bf76c-103">Evento InkOverlay. CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="bf76c-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="bf76c-104">Ocorre quando o [**InkCollector**](inkcollector-class.md) detecta um botão de cursor que está ativo.</span><span class="sxs-lookup"><span data-stu-id="bf76c-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf76c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf76c-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="bf76c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf76c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf76c-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf76c-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf76c-108">O objeto da [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**CursorButtonUp**](inkcollector-cursorbuttonup.md) .</span><span class="sxs-lookup"><span data-stu-id="bf76c-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="bf76c-109">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bf76c-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf76c-110">O botão que foi lançado.</span><span class="sxs-lookup"><span data-stu-id="bf76c-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf76c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf76c-111">Return value</span></span>

<span data-ttu-id="bf76c-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bf76c-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf76c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf76c-113">Remarks</span></span>

<span data-ttu-id="bf76c-114">Um botão em uma dica de caneta fica ativo quando o usuário conclui um traço e levanta a caneta do digitalizador.</span><span class="sxs-lookup"><span data-stu-id="bf76c-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="bf76c-115">Um botão em um cilindro fica ativo quando o botão não é pressionado.</span><span class="sxs-lookup"><span data-stu-id="bf76c-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="bf76c-116">Ao liberar o botão direito do mouse, você realmente recebe dois eventos [**CursorButtonUp**](inkcollector-cursorbuttonup.md) -um para o botão direito e outro para o botão esquerdo para cima.</span><span class="sxs-lookup"><span data-stu-id="bf76c-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="bf76c-117">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICECursorButtonUp de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="bf76c-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf76c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf76c-118">Requirements</span></span>



| <span data-ttu-id="bf76c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf76c-119">Requirement</span></span> | <span data-ttu-id="bf76c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bf76c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf76c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf76c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bf76c-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bf76c-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bf76c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf76c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bf76c-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bf76c-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="bf76c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf76c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf76c-126"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bf76c-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bf76c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf76c-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf76c-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf76c-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bf76c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf76c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf76c-130">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="bf76c-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="bf76c-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="bf76c-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="bf76c-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="bf76c-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="bf76c-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="bf76c-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="bf76c-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="bf76c-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




