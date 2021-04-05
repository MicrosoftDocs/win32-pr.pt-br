---
description: Ocorre quando uma tecla é pressionada enquanto o controle InkPicture tem foco.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Evento InkPicture. KeyPress (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921025"
---
# <a name="inkpicturekeypress-event"></a><span data-ttu-id="4c4d5-103">Evento InkPicture. KeyPress</span><span class="sxs-lookup"><span data-stu-id="4c4d5-103">InkPicture.KeyPress event</span></span>

<span data-ttu-id="4c4d5-104">Ocorre quando uma tecla é pressionada enquanto o controle [InkPicture](inkpicture-control-reference.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="4c4d5-104">Occurs when a key is pressed while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c4d5-105">Syntax</span></span>


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a><span data-ttu-id="4c4d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c4d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c4d5-107">*KeyAscii* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4c4d5-107">*KeyAscii* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4d5-108">O valor ASCII da chave que está sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="4c4d5-108">The ASCII value of the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c4d5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c4d5-109">Return value</span></span>

<span data-ttu-id="4c4d5-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4c4d5-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4d5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c4d5-111">Remarks</span></span>

<span data-ttu-id="4c4d5-112">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="4c4d5-112">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="4c4d5-113">A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEKeyPress DISPID.</span><span class="sxs-lookup"><span data-stu-id="4c4d5-113">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4d5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c4d5-114">Requirements</span></span>



| <span data-ttu-id="4c4d5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4d5-115">Requirement</span></span> | <span data-ttu-id="4c4d5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4c4d5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4d5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4d5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4d5-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4c4d5-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4c4d5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4d5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4d5-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c4d5-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4c4d5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c4d5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c4d5-122"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4c4d5-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4c4d5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c4d5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c4d5-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c4d5-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4c4d5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c4d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4d5-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="4c4d5-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

