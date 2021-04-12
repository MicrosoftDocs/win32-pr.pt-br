---
description: Ocorre depois que a propriedade ModoTamanho do controle InkPicture é alterada.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Evento InkPicture. Modotamanhochanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297380"
---
# <a name="inkpicturesizemodechanged-event"></a><span data-ttu-id="e51d8-103">Evento InkPicture. Modotamanhochanged</span><span class="sxs-lookup"><span data-stu-id="e51d8-103">InkPicture.SizeModeChanged event</span></span>

<span data-ttu-id="e51d8-104">Ocorre depois que a propriedade [**ModoTamanho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) do controle [InkPicture](inkpicture-control-reference.md) é alterada.</span><span class="sxs-lookup"><span data-stu-id="e51d8-104">Occurs after the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property of the [InkPicture](inkpicture-control-reference.md) control has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e51d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e51d8-105">Syntax</span></span>


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a><span data-ttu-id="e51d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e51d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e51d8-107">*NewMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e51d8-107">*NewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e51d8-108">O novo estado do controle [InkPicture](inkpicture-control-reference.md) , com base no novo valor da propriedade [**ModoTamanho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="e51d8-108">The new state of the [InkPicture](inkpicture-control-reference.md) control, based on the new value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> <dt>

<span data-ttu-id="e51d8-109">*OldMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e51d8-109">*OldMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e51d8-110">O estado antigo do controle [InkPicture](inkpicture-control-reference.md) , com base no valor antigo da propriedade [**ModoTamanho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="e51d8-110">The old state of the [InkPicture](inkpicture-control-reference.md) control, based on the old value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e51d8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e51d8-111">Return value</span></span>

<span data-ttu-id="e51d8-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e51d8-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e51d8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e51d8-113">Remarks</span></span>

<span data-ttu-id="e51d8-114">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="e51d8-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="e51d8-115">A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPESizeModeChanged DISPID.</span><span class="sxs-lookup"><span data-stu-id="e51d8-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeModeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="e51d8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e51d8-116">Requirements</span></span>



| <span data-ttu-id="e51d8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e51d8-117">Requirement</span></span> | <span data-ttu-id="e51d8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e51d8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51d8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e51d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e51d8-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e51d8-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e51d8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e51d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e51d8-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e51d8-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e51d8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e51d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e51d8-124"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e51d8-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e51d8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e51d8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e51d8-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e51d8-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e51d8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e51d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51d8-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e51d8-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

