---
title: descongelar comando
description: O comando descongelar reabilita a aquisição de vídeo para o buffer de quadro após ele ter sido desabilitado pelo comando Freeze. Dispositivos digitais de vídeo, VCR e de sobreposição de vídeo reconhecem este comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- descongelar multimídia do Windows de comando
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645164"
---
# <a name="unfreeze-command"></a><span data-ttu-id="3dcaf-105">descongelar comando</span><span class="sxs-lookup"><span data-stu-id="3dcaf-105">unfreeze command</span></span>

<span data-ttu-id="3dcaf-106">O comando descongelar reabilita a aquisição de vídeo para o buffer de quadro após ele ter sido desabilitado pelo comando [Freeze](freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="3dcaf-106">The unfreeze command reenables video acquisition to the frame buffer after it has been disabled by the [freeze](freeze.md) command.</span></span> <span data-ttu-id="3dcaf-107">Dispositivos digitais de vídeo, VCR e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="3dcaf-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3dcaf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dcaf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dcaf-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="3dcaf-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3dcaf-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-111">Identifier of an MCI device.</span></span> <span data-ttu-id="3dcaf-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="3dcaf-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="3dcaf-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="3dcaf-114">Sinalizador para reabilitar a aquisição de vídeo para o buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-114">Flag for reenabling video acquisition to the frame buffer.</span></span> <span data-ttu-id="3dcaf-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **descongelar** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-115">The following table lists device types that recognize the **unfreeze** command and the flags used by each type.</span></span>



| <span data-ttu-id="3dcaf-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3dcaf-116">Value</span></span>        | <span data-ttu-id="3dcaf-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3dcaf-117">Meaning</span></span>        |
|--------------|----------------|
| <span data-ttu-id="3dcaf-118">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="3dcaf-118">digitalvideo</span></span> | <span data-ttu-id="3dcaf-119">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="3dcaf-119">at *rectangle*</span></span> |
| <span data-ttu-id="3dcaf-120">overlay</span><span class="sxs-lookup"><span data-stu-id="3dcaf-120">overlay</span></span>      | <span data-ttu-id="3dcaf-121">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="3dcaf-121">at *rectangle*</span></span> |
| <span data-ttu-id="3dcaf-122">videocassete</span><span class="sxs-lookup"><span data-stu-id="3dcaf-122">vcr</span></span>          | <span data-ttu-id="3dcaf-123">saída de entrada</span><span class="sxs-lookup"><span data-stu-id="3dcaf-123">input output</span></span>   |



 

<span data-ttu-id="3dcaf-124">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszUnfreeze** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-124">The following table lists the flags that can be specified in the **lpszUnfreeze** parameter and their meanings.</span></span>



| <span data-ttu-id="3dcaf-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3dcaf-125">Value</span></span>          | <span data-ttu-id="3dcaf-126">Significado</span><span class="sxs-lookup"><span data-stu-id="3dcaf-126">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcaf-127">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="3dcaf-127">at *rectangle*</span></span> | <span data-ttu-id="3dcaf-128">Especifica a região que terá a aquisição de vídeo reativada.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-128">Specifies the region that will have video acquisition reenabled.</span></span> <span data-ttu-id="3dcaf-129">O retângulo é relativo à origem do buffer de vídeo e é especificado como *X1 Y1 x2 y2*.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-129">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="3dcaf-130">As coordenadas *X1 Y1* especificam o canto superior esquerdo do retângulo, e as coordenadas *x2 y2* especificam a largura e a altura.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-130">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="3dcaf-131">input</span><span class="sxs-lookup"><span data-stu-id="3dcaf-131">input</span></span>          | <span data-ttu-id="3dcaf-132">Descongele a imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-132">Unfreeze the input image.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3dcaf-133">output</span><span class="sxs-lookup"><span data-stu-id="3dcaf-133">output</span></span>         | <span data-ttu-id="3dcaf-134">Descongele a imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-134">Unfreeze the output image.</span></span> <span data-ttu-id="3dcaf-135">Se nem "Input" nem "output" for fornecido, "output" será assumido.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-135">If neither "input" nor "output" is given, "output" is assumed.</span></span>                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="3dcaf-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3dcaf-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3dcaf-137">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-137">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="3dcaf-138">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-138">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="3dcaf-139">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3dcaf-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dcaf-140">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3dcaf-140">Return Value</span></span>

<span data-ttu-id="3dcaf-141">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="3dcaf-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3dcaf-142">Examples</span></span>

<span data-ttu-id="3dcaf-143">O comando a seguir destrava uma região do buffer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3dcaf-143">The following command unfreezes a region of the video buffer.</span></span>

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a><span data-ttu-id="3dcaf-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dcaf-144">Requirements</span></span>



| <span data-ttu-id="3dcaf-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dcaf-145">Requirement</span></span> | <span data-ttu-id="3dcaf-146">Valor</span><span class="sxs-lookup"><span data-stu-id="3dcaf-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3dcaf-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dcaf-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3dcaf-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3dcaf-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3dcaf-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dcaf-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3dcaf-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3dcaf-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3dcaf-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dcaf-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dcaf-152">MCI</span><span class="sxs-lookup"><span data-stu-id="3dcaf-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3dcaf-153">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="3dcaf-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="3dcaf-154">Trave</span><span class="sxs-lookup"><span data-stu-id="3dcaf-154">freeze</span></span>](freeze.md)
</dt> </dl>

 

