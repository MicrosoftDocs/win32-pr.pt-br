---
description: Ocorre quando o objeto InkCollector ou InkOverlay é clicado duas vezes.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Evento InkOverlay. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4baddc89e309b7d64ba2294827b58956b3e6c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171168"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="ca309-103">Evento InkOverlay. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="ca309-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="ca309-104">Ocorre quando o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="ca309-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca309-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca309-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ca309-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca309-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca309-107">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ca309-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca309-108">Se o evento deve ser cancelado para o controle pai.</span><span class="sxs-lookup"><span data-stu-id="ca309-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca309-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca309-109">Return value</span></span>

<span data-ttu-id="ca309-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ca309-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca309-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca309-111">Remarks</span></span>

<span data-ttu-id="ca309-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEDblClick de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="ca309-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca309-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca309-113">Requirements</span></span>



| <span data-ttu-id="ca309-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca309-114">Requirement</span></span> | <span data-ttu-id="ca309-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ca309-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca309-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca309-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ca309-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ca309-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ca309-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca309-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ca309-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ca309-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ca309-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca309-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca309-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ca309-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ca309-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca309-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca309-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca309-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ca309-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca309-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca309-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="ca309-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




