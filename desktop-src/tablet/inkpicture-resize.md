---
description: Ocorre quando o controle InkPicture é redimensionado (quando os valores de propriedade Width e/ou Height são alterados).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: Evento InkPicture. Resize (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011480"
---
# <a name="inkpictureresize-event"></a><span data-ttu-id="d07c6-103">Evento InkPicture. Resize</span><span class="sxs-lookup"><span data-stu-id="d07c6-103">InkPicture.Resize event</span></span>

<span data-ttu-id="d07c6-104">Ocorre quando o controle [InkPicture](inkpicture-control-reference.md) é redimensionado (quando os valores de propriedade Width e/ou Height são alterados).</span><span class="sxs-lookup"><span data-stu-id="d07c6-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is resized (when the Width and/or Height property values change).</span></span>

## <a name="syntax"></a><span data-ttu-id="d07c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d07c6-105">Syntax</span></span>


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="d07c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d07c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d07c6-107">*Mantida*</span><span class="sxs-lookup"><span data-stu-id="d07c6-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="d07c6-108">O número de pixels do lado esquerdo da janela que contém o controle para o lado esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="d07c6-108">The number of pixels from the left side of the window that contains the control to the left side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d07c6-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="d07c6-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="d07c6-110">O número de pixels da parte superior da janela que contém o controle até a parte superior do controle.</span><span class="sxs-lookup"><span data-stu-id="d07c6-110">The number of pixels from the top of the window that contains the control to the top of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d07c6-111">*Certo*</span><span class="sxs-lookup"><span data-stu-id="d07c6-111">*Right*</span></span> 
</dt> <dd>

<span data-ttu-id="d07c6-112">O número de pixels do lado esquerdo da janela que contém o controle do lado direito do controle.</span><span class="sxs-lookup"><span data-stu-id="d07c6-112">The number of pixels from the left side of the window that contains the control to the right side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d07c6-113">*Inferior*</span><span class="sxs-lookup"><span data-stu-id="d07c6-113">*Bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="d07c6-114">O número de pixels da parte superior da janela que contém o controle até a parte inferior do controle.</span><span class="sxs-lookup"><span data-stu-id="d07c6-114">The number of pixels from the top of the window that contains the control to the bottom of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d07c6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d07c6-115">Return value</span></span>

<span data-ttu-id="d07c6-116">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d07c6-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d07c6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d07c6-117">Remarks</span></span>

<span data-ttu-id="d07c6-118">A nova largura do controle em pixels será igual à diferença entre os parâmetros *direito* e *esquerdo* .</span><span class="sxs-lookup"><span data-stu-id="d07c6-118">The new width of the control in pixels will be equal to the difference between the *Right* and *Left* parameters.</span></span> <span data-ttu-id="d07c6-119">Da mesma forma, a nova altura será igual à diferença entre *inferior* e *superior*.</span><span class="sxs-lookup"><span data-stu-id="d07c6-119">Likewise, the new height will be equal to the difference between *Bottom* and *Top*.</span></span>

<span data-ttu-id="d07c6-120">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="d07c6-120">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="d07c6-121">A interface **\_ IInkPictureEvents** implementa a interface IDispatch com um identificador de **\_ IPEResize DISPID**.</span><span class="sxs-lookup"><span data-stu-id="d07c6-121">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEResize**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d07c6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d07c6-122">Requirements</span></span>



| <span data-ttu-id="d07c6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d07c6-123">Requirement</span></span> | <span data-ttu-id="d07c6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d07c6-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07c6-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d07c6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d07c6-126">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d07c6-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d07c6-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d07c6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d07c6-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d07c6-128">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d07c6-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d07c6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d07c6-130"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d07c6-130"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d07c6-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d07c6-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d07c6-132"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d07c6-132"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d07c6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d07c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d07c6-134">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d07c6-134">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




