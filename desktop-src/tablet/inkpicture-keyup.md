---
description: Ocorre quando uma tecla é liberada enquanto o controle InkPicture tem foco.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: Evento InkPicture. KeyUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768228"
---
# <a name="inkpicturekeyup-event"></a><span data-ttu-id="885ff-103">Evento InkPicture. KeyUp</span><span class="sxs-lookup"><span data-stu-id="885ff-103">InkPicture.KeyUp event</span></span>

<span data-ttu-id="885ff-104">Ocorre quando uma tecla é liberada enquanto o controle [InkPicture](inkpicture-control-reference.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="885ff-104">Occurs when a key is released while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="885ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="885ff-105">Syntax</span></span>


```C++
void KeyUp(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="885ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="885ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="885ff-107">*KeyCode* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="885ff-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="885ff-108">O valor ASCII da chave que está sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="885ff-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="885ff-109">*Shift* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="885ff-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="885ff-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="885ff-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="885ff-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="885ff-111">Return value</span></span>

<span data-ttu-id="885ff-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="885ff-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="885ff-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="885ff-113">Remarks</span></span>

<span data-ttu-id="885ff-114">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="885ff-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="885ff-115">A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEKeyUp DISPID.</span><span class="sxs-lookup"><span data-stu-id="885ff-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="885ff-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="885ff-116">Requirements</span></span>



| <span data-ttu-id="885ff-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="885ff-117">Requirement</span></span> | <span data-ttu-id="885ff-118">Valor</span><span class="sxs-lookup"><span data-stu-id="885ff-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="885ff-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="885ff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="885ff-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="885ff-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="885ff-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="885ff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="885ff-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="885ff-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="885ff-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="885ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="885ff-124"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="885ff-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="885ff-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="885ff-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="885ff-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="885ff-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="885ff-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="885ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="885ff-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="885ff-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

