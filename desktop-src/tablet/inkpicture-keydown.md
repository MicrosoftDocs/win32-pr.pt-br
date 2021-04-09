---
description: Ocorre quando uma tecla é pressionada e na posição para baixo enquanto o controle InkPicture tem foco.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: Evento InkPicture. KeyDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011822"
---
# <a name="inkpicturekeydown-event"></a><span data-ttu-id="4655d-103">Evento InkPicture. KeyDown</span><span class="sxs-lookup"><span data-stu-id="4655d-103">InkPicture.KeyDown event</span></span>

<span data-ttu-id="4655d-104">Ocorre quando uma tecla é pressionada e na posição para baixo enquanto o controle [InkPicture](inkpicture-control-reference.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="4655d-104">Occurs when a key is pressed and in the down position while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="4655d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4655d-105">Syntax</span></span>


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="4655d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4655d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4655d-107">*KeyCode* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4655d-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4655d-108">O valor ASCII da chave que está sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="4655d-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="4655d-109">*Shift* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4655d-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4655d-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="4655d-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4655d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4655d-111">Return value</span></span>

<span data-ttu-id="4655d-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4655d-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4655d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4655d-113">Remarks</span></span>

<span data-ttu-id="4655d-114">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="4655d-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="4655d-115">A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEKeyDown DISPID.</span><span class="sxs-lookup"><span data-stu-id="4655d-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="4655d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4655d-116">Requirements</span></span>



| <span data-ttu-id="4655d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4655d-117">Requirement</span></span> | <span data-ttu-id="4655d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4655d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4655d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4655d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4655d-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4655d-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4655d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4655d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4655d-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4655d-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4655d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4655d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4655d-124"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4655d-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4655d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4655d-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4655d-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4655d-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4655d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4655d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4655d-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="4655d-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

