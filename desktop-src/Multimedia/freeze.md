---
title: congelar comando
description: O comando Freeze congela a entrada de vídeo ou a saída de vídeo em um videocassete ou desabilita a aquisição de vídeo para o buffer de quadros. Dispositivos de vídeo digital, de sobreposição de vídeo e VCR reconhecem este comando.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- congelar multimídia do Windows de comando
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008840"
---
# <a name="freeze-command"></a><span data-ttu-id="b25dd-105">congelar comando</span><span class="sxs-lookup"><span data-stu-id="b25dd-105">freeze command</span></span>

<span data-ttu-id="b25dd-106">O comando Freeze congela a entrada de vídeo ou a saída de vídeo em um videocassete ou desabilita a aquisição de vídeo para o buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="b25dd-106">The freeze command freezes video input or video output on a VCR or disables video acquisition to the frame buffer.</span></span> <span data-ttu-id="b25dd-107">Dispositivos de vídeo digital, de sobreposição de vídeo e VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="b25dd-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="b25dd-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b25dd-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="b25dd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b25dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b25dd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b25dd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b25dd-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="b25dd-111">Identifier of an MCI device.</span></span> <span data-ttu-id="b25dd-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="b25dd-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="b25dd-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span><span class="sxs-lookup"><span data-stu-id="b25dd-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b25dd-114">Sinalizador que identifica o que congelar.</span><span class="sxs-lookup"><span data-stu-id="b25dd-114">Flag that identifies what to freeze.</span></span> <span data-ttu-id="b25dd-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **Freeze** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="b25dd-115">The following table lists device types that recognize the **freeze** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b25dd-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b25dd-116">Value</span></span></th>
<th><span data-ttu-id="b25dd-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b25dd-117">Meaning</span></span></th>
<th><span data-ttu-id="b25dd-118">Significado</span><span class="sxs-lookup"><span data-stu-id="b25dd-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b25dd-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="b25dd-119">digitalvideo</span></span></td>
<td><span data-ttu-id="b25dd-120">no <em>retângulo</em></span><span class="sxs-lookup"><span data-stu-id="b25dd-120">at <em>rectangle</em></span></span></td>
<td><span data-ttu-id="b25dd-121">exterior</span><span class="sxs-lookup"><span data-stu-id="b25dd-121">outside</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b25dd-122">overlay</span><span class="sxs-lookup"><span data-stu-id="b25dd-122">overlay</span></span></td>
<td><span data-ttu-id="b25dd-123">no <em>retângulo</em></span><span class="sxs-lookup"><span data-stu-id="b25dd-123">at <em>rectangle</em></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b25dd-124">videocassete</span><span class="sxs-lookup"><span data-stu-id="b25dd-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="b25dd-125">field</span><span class="sxs-lookup"><span data-stu-id="b25dd-125">field</span></span></li>
<li><span data-ttu-id="b25dd-126">frame</span><span class="sxs-lookup"><span data-stu-id="b25dd-126">frame</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b25dd-127">input</span><span class="sxs-lookup"><span data-stu-id="b25dd-127">input</span></span></li>
<li><span data-ttu-id="b25dd-128">output</span><span class="sxs-lookup"><span data-stu-id="b25dd-128">output</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b25dd-129">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro *lpszFreezeFlags* e seus significados.</span><span class="sxs-lookup"><span data-stu-id="b25dd-129">The following table lists the flags that can be specified in the *lpszFreezeFlags* parameter and their meanings.</span></span>



| <span data-ttu-id="b25dd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b25dd-130">Value</span></span>          | <span data-ttu-id="b25dd-131">Significado</span><span class="sxs-lookup"><span data-stu-id="b25dd-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b25dd-132">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="b25dd-132">at *rectangle*</span></span> | <span data-ttu-id="b25dd-133">Especifica a região que será congelada.</span><span class="sxs-lookup"><span data-stu-id="b25dd-133">Specifies the region that will be frozen.</span></span> <span data-ttu-id="b25dd-134">Para dispositivos de sobreposição de vídeo, essa região terá a aquisição de vídeo desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b25dd-134">For video-overlay devices, this region will have video acquisition disabled.</span></span> <span data-ttu-id="b25dd-135">Para dispositivos de vídeo digital, os pixels dentro do retângulo terão seu bit de máscara de bloqueio ativado (a menos que o sinalizador "externo" seja especificado).</span><span class="sxs-lookup"><span data-stu-id="b25dd-135">For digital-video devices, the pixels within the rectangle will have their lock mask bit turned on (unless the "outside" flag is specified).</span></span> <span data-ttu-id="b25dd-136">O retângulo é relativo à origem do buffer de vídeo e é especificado como *X1 Y1 x2 y2*.</span><span class="sxs-lookup"><span data-stu-id="b25dd-136">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="b25dd-137">As coordenadas *X1 Y1* especificam o canto superior esquerdo do retângulo, e as coordenadas *x2 y2* especificam a largura e a altura.</span><span class="sxs-lookup"><span data-stu-id="b25dd-137">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="b25dd-138">field</span><span class="sxs-lookup"><span data-stu-id="b25dd-138">field</span></span>          | <span data-ttu-id="b25dd-139">Congela o primeiro campo.</span><span class="sxs-lookup"><span data-stu-id="b25dd-139">Freezes the first field.</span></span> <span data-ttu-id="b25dd-140">O campo é assumido por padrão (se nenhum quadro nem campo for especificado).</span><span class="sxs-lookup"><span data-stu-id="b25dd-140">Field is assumed by default (if neither frame nor field is specified).</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b25dd-141">frame</span><span class="sxs-lookup"><span data-stu-id="b25dd-141">frame</span></span>          | <span data-ttu-id="b25dd-142">Congela o quadro inteiro, exibindo os dois campos.</span><span class="sxs-lookup"><span data-stu-id="b25dd-142">Freezes the entire frame, displaying both fields.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b25dd-143">input</span><span class="sxs-lookup"><span data-stu-id="b25dd-143">input</span></span>          | <span data-ttu-id="b25dd-144">Congela o quadro atual da imagem de entrada, se está em pausa ou em execução.</span><span class="sxs-lookup"><span data-stu-id="b25dd-144">Freezes the current frame of the input image, whether it is paused or running.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b25dd-145">output</span><span class="sxs-lookup"><span data-stu-id="b25dd-145">output</span></span>         | <span data-ttu-id="b25dd-146">Congela o quadro atual da saída do VCR.</span><span class="sxs-lookup"><span data-stu-id="b25dd-146">Freezes the current frame of the output from the VCR.</span></span> <span data-ttu-id="b25dd-147">Se o VCR estiver sendo executado quando congelar for emitido, o quadro atual será congelado e o VCR será pausado.</span><span class="sxs-lookup"><span data-stu-id="b25dd-147">If the VCR is playing when freeze is issued, the current frame is frozen and the VCR is paused.</span></span> <span data-ttu-id="b25dd-148">Se o VCR estiver em pausa quando esse comando for emitido, o quadro atual será congelado.</span><span class="sxs-lookup"><span data-stu-id="b25dd-148">If the VCR is paused when this command is issued, the current frame is frozen.</span></span> <span data-ttu-id="b25dd-149">A imagem congelada permanece no dispositivo de saída até que um comando de [descongelamento](unfreeze.md) seja emitido.</span><span class="sxs-lookup"><span data-stu-id="b25dd-149">The frozen image remains on the output device until an [unfreeze](unfreeze.md) command is issued.</span></span> <span data-ttu-id="b25dd-150">Se nem "Input" nem "output" for especificado, "output" será assumido.</span><span class="sxs-lookup"><span data-stu-id="b25dd-150">If neither "input" nor "output" is specified, "output" is assumed.</span></span>                                                                                    |
| <span data-ttu-id="b25dd-151">exterior</span><span class="sxs-lookup"><span data-stu-id="b25dd-151">outside</span></span>        | <span data-ttu-id="b25dd-152">Indica que a área fora da região especificada usando o sinalizador "at" está congelada.</span><span class="sxs-lookup"><span data-stu-id="b25dd-152">Indicates that the area outside the region specified using the "at" flag is frozen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="b25dd-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="b25dd-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b25dd-154">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="b25dd-154">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="b25dd-155">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="b25dd-155">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="b25dd-156">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b25dd-156">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b25dd-157">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b25dd-157">Return Value</span></span>

<span data-ttu-id="b25dd-158">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="b25dd-158">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b25dd-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="b25dd-159">Remarks</span></span>

<span data-ttu-id="b25dd-160">Quando usado com dispositivos VCR, esse comando destina-se a cartões de captura de quadros.</span><span class="sxs-lookup"><span data-stu-id="b25dd-160">When used with VCR devices, this command is intended for frame-grabbing cards.</span></span>

<span data-ttu-id="b25dd-161">Para especificar regiões de aquisição irregular com o sinalizador "at", use uma série de comandos congelar e [descongelar](unfreeze.md) .</span><span class="sxs-lookup"><span data-stu-id="b25dd-161">To specify irregular acquisition regions with the "at" flag, use a series of freeze and [unfreeze](unfreeze.md) commands.</span></span> <span data-ttu-id="b25dd-162">Alguns dispositivos de sobreposição de vídeo limitam a complexidade da região de aquisição.</span><span class="sxs-lookup"><span data-stu-id="b25dd-162">Some video-overlay devices limit the complexity of the acquisition region.</span></span>

<span data-ttu-id="b25dd-163">Esse comando só terá suporte se uma chamada para o comando [Capability](capability.md) com o sinalizador "pode congelar" retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="b25dd-163">This command is supported only if a call to the [capability](capability.md) command with the "can freeze" flag returns **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="b25dd-164">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b25dd-164">Examples</span></span>

<span data-ttu-id="b25dd-165">O comando a seguir desabilita a aquisição de vídeo em um quadrado de 100 pixels no canto superior esquerdo do buffer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b25dd-165">The following command disables video acquisition in a 100-pixel square at the upper left corner of the video buffer.</span></span>

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a><span data-ttu-id="b25dd-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b25dd-166">Requirements</span></span>



| <span data-ttu-id="b25dd-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="b25dd-167">Requirement</span></span> | <span data-ttu-id="b25dd-168">Valor</span><span class="sxs-lookup"><span data-stu-id="b25dd-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b25dd-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b25dd-169">Minimum supported client</span></span><br/> | <span data-ttu-id="b25dd-170">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b25dd-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b25dd-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b25dd-171">Minimum supported server</span></span><br/> | <span data-ttu-id="b25dd-172">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b25dd-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b25dd-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="b25dd-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25dd-174">MCI</span><span class="sxs-lookup"><span data-stu-id="b25dd-174">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b25dd-175">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="b25dd-175">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="b25dd-176">capability</span><span class="sxs-lookup"><span data-stu-id="b25dd-176">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="b25dd-177">descongelar</span><span class="sxs-lookup"><span data-stu-id="b25dd-177">unfreeze</span></span>](unfreeze.md)
</dt> </dl>

 

