---
title: comando Restore
description: O comando Restore copia uma imagem ainda de um arquivo para o buffer de quadros. Esse é o inverso do comando Capture. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- comando restaurar multimídia do Windows
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d7f0f236b26e3e73807b32485442d597e93d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918013"
---
# <a name="restore-command"></a><span data-ttu-id="b07c5-106">comando Restore</span><span class="sxs-lookup"><span data-stu-id="b07c5-106">restore command</span></span>

<span data-ttu-id="b07c5-107">O comando Restore copia uma imagem ainda de um arquivo para o buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="b07c5-107">The restore command copies a still image from a file to the frame buffer.</span></span> <span data-ttu-id="b07c5-108">Esse é o inverso do comando [Capture](capture.md) .</span><span class="sxs-lookup"><span data-stu-id="b07c5-108">This is the reverse of the [capture](capture.md) command.</span></span> <span data-ttu-id="b07c5-109">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="b07c5-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="b07c5-110">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b07c5-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="b07c5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b07c5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b07c5-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b07c5-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b07c5-113">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="b07c5-113">Identifier of an MCI device.</span></span> <span data-ttu-id="b07c5-114">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="b07c5-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="b07c5-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span><span class="sxs-lookup"><span data-stu-id="b07c5-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span></span>
</dt> <dd>

<span data-ttu-id="b07c5-116">Um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b07c5-116">One or more of the following flags.</span></span>



| <span data-ttu-id="b07c5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b07c5-117">Value</span></span>           | <span data-ttu-id="b07c5-118">Significado</span><span class="sxs-lookup"><span data-stu-id="b07c5-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b07c5-119">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="b07c5-119">at *rectangle*</span></span>  | <span data-ttu-id="b07c5-120">Especifica um retângulo relativo à origem do buffer do quadro.</span><span class="sxs-lookup"><span data-stu-id="b07c5-120">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="b07c5-121">O *retângulo* é especificado como *X1 Y1 x2 y2*.</span><span class="sxs-lookup"><span data-stu-id="b07c5-121">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="b07c5-122">As coordenadas *X1 Y1* especificam o canto superior esquerdo e as coordenadas *x2 y2* especificam a largura e a altura. Se esse sinalizador não for usado, a imagem será copiada para o canto superior esquerdo do buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="b07c5-122">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.If this flag is not used, the image is copied to the upper left corner of the frame buffer.</span></span><br/> |
| <span data-ttu-id="b07c5-123">de *nome de arquivo*</span><span class="sxs-lookup"><span data-stu-id="b07c5-123">from *filename*</span></span> | <span data-ttu-id="b07c5-124">Especifica o nome de arquivo da imagem a ser relembrado.</span><span class="sxs-lookup"><span data-stu-id="b07c5-124">Specifies the image filename to recall.</span></span> <span data-ttu-id="b07c5-125">Esse sinalizador é necessário.</span><span class="sxs-lookup"><span data-stu-id="b07c5-125">This flag is required.</span></span>                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="b07c5-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="b07c5-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b07c5-127">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="b07c5-127">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="b07c5-128">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b07c5-128">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b07c5-129">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b07c5-129">Return Value</span></span>

<span data-ttu-id="b07c5-130">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="b07c5-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b07c5-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="b07c5-131">Remarks</span></span>

<span data-ttu-id="b07c5-132">Os dispositivos podem reconhecer uma variedade de formatos de imagem; um bitmap independente de dispositivo do Windows é sempre reconhecido.</span><span class="sxs-lookup"><span data-stu-id="b07c5-132">Devices can recognize a variety of image formats; a Windows device-independent bitmap is always recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="b07c5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b07c5-133">Requirements</span></span>



| <span data-ttu-id="b07c5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b07c5-134">Requirement</span></span> | <span data-ttu-id="b07c5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b07c5-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b07c5-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b07c5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b07c5-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b07c5-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b07c5-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b07c5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b07c5-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b07c5-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b07c5-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b07c5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b07c5-141">MCI</span><span class="sxs-lookup"><span data-stu-id="b07c5-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b07c5-142">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="b07c5-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="b07c5-143">captura</span><span class="sxs-lookup"><span data-stu-id="b07c5-143">capture</span></span>](capture.md)
</dt> </dl>

 

