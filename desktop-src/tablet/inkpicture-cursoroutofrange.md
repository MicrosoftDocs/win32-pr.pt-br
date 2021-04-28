---
description: Evento InkPicture. CursorOutOfRange – ocorre quando o cursor sai do intervalo de detecção física (proximidade) do contexto do Tablet.
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: Evento InkPicture. CursorOutOfRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d80584eafb7f1e5222316507f08bd73efb12fae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086564"
---
# <a name="inkpicturecursoroutofrange-event"></a><span data-ttu-id="65ef7-103">Evento InkPicture. CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="65ef7-103">InkPicture.CursorOutOfRange event</span></span>

<span data-ttu-id="65ef7-104">Ocorre quando o cursor sai do intervalo de detecção física (proximidade) do contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="65ef7-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ef7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65ef7-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="65ef7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65ef7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ef7-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65ef7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ef7-108">O objeto da [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="65ef7-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ef7-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="65ef7-109">Return value</span></span>

<span data-ttu-id="65ef7-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="65ef7-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ef7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="65ef7-111">Remarks</span></span>

<span data-ttu-id="65ef7-112">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICECursorOutOfRange de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="65ef7-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="65ef7-113">O evento **CursorOutOfRange** é disparado mesmo quando estiver no modo de seleção ou apagamento, não apenas quando estiver no modo de tinta.</span><span class="sxs-lookup"><span data-stu-id="65ef7-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="65ef7-114">Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="65ef7-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="65ef7-115">A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="65ef7-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ef7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65ef7-116">Requirements</span></span>



| <span data-ttu-id="65ef7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65ef7-117">Requirement</span></span> | <span data-ttu-id="65ef7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="65ef7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ef7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65ef7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65ef7-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="65ef7-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="65ef7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65ef7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65ef7-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="65ef7-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="65ef7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65ef7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ef7-124"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="65ef7-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="65ef7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65ef7-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="65ef7-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65ef7-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="65ef7-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="65ef7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ef7-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="65ef7-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="65ef7-129">**Evento CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="65ef7-129">**CursorInRange Event**</span></span>](inkpicture-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="65ef7-130">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="65ef7-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




