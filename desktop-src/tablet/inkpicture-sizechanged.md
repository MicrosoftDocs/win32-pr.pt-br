---
description: Ocorre depois que o controle InkPicture é redimensionado, especificamente, depois que o valor da propriedade Width ou Height é alterado.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture. SizeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922649"
---
# <a name="inkpicturesizechanged-event"></a><span data-ttu-id="60bbf-103">Evento InkPicture. SizeChanged</span><span class="sxs-lookup"><span data-stu-id="60bbf-103">InkPicture.SizeChanged event</span></span>

<span data-ttu-id="60bbf-104">Ocorre depois que o controle [InkPicture](inkpicture-control-reference.md) é redimensionado, especificamente, depois que o valor da propriedade [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) ou [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) é alterado.</span><span class="sxs-lookup"><span data-stu-id="60bbf-104">Occurs after the [InkPicture](inkpicture-control-reference.md) control has been resized, specifically, after the [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) or [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) property value changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="60bbf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60bbf-105">Syntax</span></span>


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="60bbf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60bbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60bbf-107">*À esquerda* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60bbf-107">*Left* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60bbf-108">A coordenada x do lado esquerdo do controle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="60bbf-108">The x-coordinate of the left side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="60bbf-109">*Superior* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60bbf-109">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60bbf-110">A coordenada y da parte superior do controle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="60bbf-110">The y-coordinate of the top of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="60bbf-111">*À direita* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60bbf-111">*Right* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60bbf-112">A coordenada x do lado direito do controle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="60bbf-112">The x-coordinate of the right side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="60bbf-113">*Parte inferior* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60bbf-113">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60bbf-114">A coordenada y da parte inferior do controle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="60bbf-114">The y-coordinate of the bottom of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60bbf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60bbf-115">Return value</span></span>

<span data-ttu-id="60bbf-116">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="60bbf-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60bbf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="60bbf-117">Remarks</span></span>

<span data-ttu-id="60bbf-118">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="60bbf-118">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="60bbf-119">A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPESizeChanged DISPID.</span><span class="sxs-lookup"><span data-stu-id="60bbf-119">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="60bbf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60bbf-120">Requirements</span></span>



| <span data-ttu-id="60bbf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="60bbf-121">Requirement</span></span> | <span data-ttu-id="60bbf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="60bbf-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60bbf-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60bbf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="60bbf-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="60bbf-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="60bbf-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60bbf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="60bbf-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="60bbf-126">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="60bbf-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60bbf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="60bbf-128"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="60bbf-128"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="60bbf-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60bbf-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="60bbf-130"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60bbf-130"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="60bbf-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="60bbf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60bbf-132">InkPicture</span><span class="sxs-lookup"><span data-stu-id="60bbf-132">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

