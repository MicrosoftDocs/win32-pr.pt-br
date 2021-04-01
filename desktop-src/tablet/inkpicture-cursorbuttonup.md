---
description: Ocorre quando o InkCollector detecta um botão de cursor que está ativo.
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: Evento InkPicture. CursorButtonUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6dbee586b3179f35593c95c2d62109a379c3216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829693"
---
# <a name="inkpicturecursorbuttonup-event"></a><span data-ttu-id="7c949-103">Evento InkPicture. CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="7c949-103">InkPicture.CursorButtonUp event</span></span>

<span data-ttu-id="7c949-104">Ocorre quando o [**InkCollector**](inkcollector-class.md) detecta um botão de cursor que está ativo.</span><span class="sxs-lookup"><span data-stu-id="7c949-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c949-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c949-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="7c949-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c949-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c949-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c949-108">O objeto da [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorButtonUp** .</span><span class="sxs-lookup"><span data-stu-id="7c949-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="7c949-109">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c949-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c949-110">O botão que foi lançado.</span><span class="sxs-lookup"><span data-stu-id="7c949-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c949-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c949-111">Return value</span></span>

<span data-ttu-id="7c949-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7c949-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c949-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c949-113">Remarks</span></span>

<span data-ttu-id="7c949-114">Um botão em uma dica de caneta fica ativo quando o usuário conclui um traço e levanta a caneta do digitalizador.</span><span class="sxs-lookup"><span data-stu-id="7c949-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="7c949-115">Um botão em um cilindro fica ativo quando o botão não é pressionado.</span><span class="sxs-lookup"><span data-stu-id="7c949-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="7c949-116">Ao liberar o botão direito do mouse, você realmente recebe dois eventos **CursorButtonUp** -um para o botão direito e outro para o botão esquerdo para cima.</span><span class="sxs-lookup"><span data-stu-id="7c949-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="7c949-117">Esse método de evento é definido nos dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** com uma ID de ICECursorButtonUp DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="7c949-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c949-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c949-118">Requirements</span></span>



| <span data-ttu-id="7c949-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c949-119">Requirement</span></span> | <span data-ttu-id="7c949-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7c949-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c949-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c949-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c949-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7c949-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7c949-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c949-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c949-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7c949-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7c949-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c949-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c949-126"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7c949-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7c949-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c949-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c949-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c949-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7c949-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c949-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c949-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="7c949-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7c949-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="7c949-131">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="7c949-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="7c949-132">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="7c949-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="7c949-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="7c949-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="7c949-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




