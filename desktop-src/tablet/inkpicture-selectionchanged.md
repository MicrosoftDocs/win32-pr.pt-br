---
description: Ocorre quando a seleção de tinta no controle InkPicture é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: Evento InkPicture. SelectionChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14594efe4e5ecda64167ec9a0e075fc60d8e9a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753669"
---
# <a name="inkpictureselectionchanged-event"></a><span data-ttu-id="cedfe-103">Evento InkPicture. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="cedfe-103">InkPicture.SelectionChanged event</span></span>

<span data-ttu-id="cedfe-104">Ocorre quando a seleção de tinta no controle [InkPicture](inkpicture-control-reference.md) é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="cedfe-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="cedfe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cedfe-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="cedfe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cedfe-106">Parameters</span></span>

<span data-ttu-id="cedfe-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cedfe-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cedfe-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cedfe-108">Return value</span></span>

<span data-ttu-id="cedfe-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cedfe-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cedfe-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cedfe-110">Remarks</span></span>

<span data-ttu-id="cedfe-111">Para obter mais detalhes sobre esse evento, consulte o evento [**SelectionChanged**](inkoverlay-selectionchanged.md) do objeto [**InkOverlay**](inkoverlay-class.md) , que tem a mesma funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="cedfe-111">For further details about this event, refer to the [**InkOverlay**](inkoverlay-class.md) object's [**SelectionChanged**](inkoverlay-selectionchanged.md) event, which has the same functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="cedfe-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cedfe-112">Requirements</span></span>



| <span data-ttu-id="cedfe-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cedfe-113">Requirement</span></span> | <span data-ttu-id="cedfe-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cedfe-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cedfe-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cedfe-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cedfe-116">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cedfe-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cedfe-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cedfe-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cedfe-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cedfe-118">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="cedfe-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cedfe-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cedfe-120"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cedfe-120"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cedfe-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cedfe-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="cedfe-122"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cedfe-122"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="cedfe-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cedfe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cedfe-124">InkPicture</span><span class="sxs-lookup"><span data-stu-id="cedfe-124">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="cedfe-125">[**Controle de propriedade de seleção \[ InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="cedfe-125">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

 




