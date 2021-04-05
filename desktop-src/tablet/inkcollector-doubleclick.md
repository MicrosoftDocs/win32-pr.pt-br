---
description: Ocorre quando o objeto InkCollector ou InkOverlay é clicado duas vezes.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Evento InkCollector. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17faa459e207cd8891a13cf90f587b277d404772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826877"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="15511-103">Evento InkCollector. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="15511-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="15511-104">Ocorre quando o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="15511-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="15511-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15511-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="15511-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15511-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15511-107">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="15511-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="15511-108">**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="15511-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15511-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15511-109">Return value</span></span>

<span data-ttu-id="15511-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="15511-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15511-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="15511-111">Remarks</span></span>

<span data-ttu-id="15511-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEDblClick de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="15511-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="15511-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15511-113">Requirements</span></span>



| <span data-ttu-id="15511-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="15511-114">Requirement</span></span> | <span data-ttu-id="15511-115">Valor</span><span class="sxs-lookup"><span data-stu-id="15511-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15511-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15511-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15511-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="15511-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="15511-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15511-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15511-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="15511-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="15511-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15511-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="15511-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="15511-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="15511-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15511-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="15511-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15511-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="15511-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="15511-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15511-125">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="15511-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




