---
description: Ocorre quando a seleção de tinta no controle InkPicture está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Evento InkPicture. SelectionChanging (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837024"
---
# <a name="inkpictureselectionchanging-event"></a><span data-ttu-id="eec8f-103">Evento InkPicture. SelectionChanging</span><span class="sxs-lookup"><span data-stu-id="eec8f-103">InkPicture.SelectionChanging event</span></span>

<span data-ttu-id="eec8f-104">Ocorre quando a seleção de tinta no controle [InkPicture](inkpicture-control-reference.md) está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="eec8f-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eec8f-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="eec8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eec8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec8f-107">*NewSelection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec8f-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec8f-108">A nova coleção de [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está sendo selecionada.</span><span class="sxs-lookup"><span data-stu-id="eec8f-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec8f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eec8f-109">Return value</span></span>

<span data-ttu-id="eec8f-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="eec8f-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec8f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="eec8f-111">Remarks</span></span>

<span data-ttu-id="eec8f-112">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOESelectionChanging.</span><span class="sxs-lookup"><span data-stu-id="eec8f-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec8f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eec8f-113">Requirements</span></span>



| <span data-ttu-id="eec8f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec8f-114">Requirement</span></span> | <span data-ttu-id="eec8f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eec8f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec8f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eec8f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eec8f-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="eec8f-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="eec8f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eec8f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eec8f-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eec8f-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="eec8f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eec8f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec8f-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eec8f-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eec8f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eec8f-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="eec8f-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eec8f-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="eec8f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="eec8f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec8f-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="eec8f-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="eec8f-126">[**Controle de propriedade de seleção \[ InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="eec8f-126">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

