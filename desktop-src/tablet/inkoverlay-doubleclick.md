---
description: Evento InkOverlay. DoubleClick – ocorre quando o objeto InkCollector ou InkOverlay é clicado duas vezes.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Evento InkOverlay. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c358a6c44ccda9be9dc4d0dd1d3e81e4a983ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086824"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="0d602-103">Evento InkOverlay. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="0d602-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="0d602-104">Ocorre quando o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="0d602-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d602-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d602-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="0d602-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d602-107">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0d602-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d602-108">Se o evento deve ser cancelado para o controle pai.</span><span class="sxs-lookup"><span data-stu-id="0d602-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d602-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0d602-109">Return value</span></span>

<span data-ttu-id="0d602-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0d602-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d602-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d602-111">Remarks</span></span>

<span data-ttu-id="0d602-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEDblClick de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="0d602-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d602-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d602-113">Requirements</span></span>



| <span data-ttu-id="0d602-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d602-114">Requirement</span></span> | <span data-ttu-id="0d602-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0d602-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d602-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d602-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0d602-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0d602-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0d602-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d602-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0d602-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0d602-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0d602-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d602-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d602-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0d602-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0d602-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d602-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d602-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d602-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0d602-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0d602-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d602-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="0d602-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




