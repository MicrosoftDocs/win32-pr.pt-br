---
description: Ocorre quando o controle InkPicture conclui a redesenho de si mesmo.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture. pintado (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772557"
---
# <a name="inkpicturepainted-event"></a><span data-ttu-id="b8269-103">Evento InkPicture. pintado</span><span class="sxs-lookup"><span data-stu-id="b8269-103">InkPicture.Painted event</span></span>

<span data-ttu-id="b8269-104">Ocorre quando o controle [InkPicture](inkpicture-control-reference.md) conclui a redesenho de si mesmo.</span><span class="sxs-lookup"><span data-stu-id="b8269-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8269-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8269-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="b8269-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8269-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8269-107">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b8269-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8269-108">O contexto do dispositivo no qual o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b8269-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b8269-109">*Rect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b8269-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8269-110">O [**InkRectangle**](inkrectangle-class.md) que foi redesenhado.</span><span class="sxs-lookup"><span data-stu-id="b8269-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8269-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8269-111">Return value</span></span>

<span data-ttu-id="b8269-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b8269-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8269-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8269-113">Remarks</span></span>

<span data-ttu-id="b8269-114">Esse método de evento é definido nos dispinterfaces **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** com uma ID de \_ IOEPainted DISPID.</span><span class="sxs-lookup"><span data-stu-id="b8269-114">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8269-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8269-115">Requirements</span></span>



| <span data-ttu-id="b8269-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8269-116">Requirement</span></span> | <span data-ttu-id="b8269-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b8269-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8269-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8269-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8269-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b8269-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b8269-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8269-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8269-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b8269-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b8269-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8269-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8269-123"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8269-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8269-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8269-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8269-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8269-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b8269-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8269-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8269-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="b8269-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




