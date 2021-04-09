---
description: Ocorre quando um cursor entra no intervalo de detecção física (proximidade) do contexto do Tablet.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: Evento InkOverlay. CursorInRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65745e93bfb7351f7e1fa6d01965ce7a271bc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922484"
---
# <a name="inkoverlaycursorinrange-event"></a><span data-ttu-id="f4ef7-103">Evento InkOverlay. CursorInRange</span><span class="sxs-lookup"><span data-stu-id="f4ef7-103">InkOverlay.CursorInRange event</span></span>

<span data-ttu-id="f4ef7-104">Ocorre quando um cursor entra no intervalo de detecção física (proximidade) do contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="f4ef7-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ef7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4ef7-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="f4ef7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4ef7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ef7-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4ef7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ef7-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ef7-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="f4ef7-109">*NewCursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4ef7-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ef7-110">Se esta é a primeira vez que esse coletor de tinta entrou em contato com o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ef7-110">Whether this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="f4ef7-111">*Botõesstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4ef7-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ef7-112">O estado dos botões para o cursor que gerou o evento [**CursorInRange**](inkcollector-cursorinrange.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ef7-112">The state of the buttons for the cursor that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

<span data-ttu-id="f4ef7-113">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="f4ef7-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ef7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4ef7-114">Return value</span></span>

<span data-ttu-id="f4ef7-115">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f4ef7-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ef7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4ef7-116">Remarks</span></span>

<span data-ttu-id="f4ef7-117">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICECursorInRange de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="f4ef7-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="f4ef7-118">O evento [**CursorInRange**](inkcollector-cursorinrange.md) é disparado mesmo quando estiver no modo de seleção ou apagamento, não apenas quando estiver no modo de tinta.</span><span class="sxs-lookup"><span data-stu-id="f4ef7-118">The [**CursorInRange**](inkcollector-cursorinrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="f4ef7-119">Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="f4ef7-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="f4ef7-120">A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="f4ef7-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ef7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4ef7-121">Requirements</span></span>



| <span data-ttu-id="f4ef7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4ef7-122">Requirement</span></span> | <span data-ttu-id="f4ef7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f4ef7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ef7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ef7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ef7-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f4ef7-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f4ef7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ef7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ef7-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f4ef7-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f4ef7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4ef7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4ef7-129"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f4ef7-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f4ef7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4ef7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4ef7-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ef7-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f4ef7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4ef7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ef7-133">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="f4ef7-133">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f4ef7-134">**Evento CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="f4ef7-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="f4ef7-135">**Enumeração InkCursorButtonState**</span><span class="sxs-lookup"><span data-stu-id="f4ef7-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="f4ef7-136">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="f4ef7-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




