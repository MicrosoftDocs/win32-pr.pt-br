---
title: comando salvar
description: O comando salvar salva um arquivo MCI. Os dispositivos de sobreposição de vídeo e Wave-Audio reconhecem este comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não dão suporte a ele.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- salvar o comando multimídia do Windows
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812900"
---
# <a name="save-command"></a><span data-ttu-id="45af0-106">comando salvar</span><span class="sxs-lookup"><span data-stu-id="45af0-106">save command</span></span>

<span data-ttu-id="45af0-107">O comando salvar salva um arquivo MCI.</span><span class="sxs-lookup"><span data-stu-id="45af0-107">The save command saves an MCI file.</span></span> <span data-ttu-id="45af0-108">Os dispositivos de sobreposição de vídeo e Wave-Audio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="45af0-108">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="45af0-109">Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não dão suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="45af0-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not support it.</span></span>

<span data-ttu-id="45af0-110">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="45af0-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="45af0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45af0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45af0-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="45af0-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="45af0-113">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="45af0-113">Identifier of an MCI device.</span></span> <span data-ttu-id="45af0-114">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="45af0-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="45af0-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span><span class="sxs-lookup"><span data-stu-id="45af0-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span></span>
</dt> <dd>

<span data-ttu-id="45af0-116">Sinalizador que especifica o nome do arquivo que está sendo salvo e, opcionalmente, sinalizadores adicionais modificando a operação de salvamento.</span><span class="sxs-lookup"><span data-stu-id="45af0-116">Flag specifying the name of the file being saved and, optionally, additional flags modifying the save operation.</span></span> <span data-ttu-id="45af0-117">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **salvar** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="45af0-117">The following table lists device types that recognize the **save** command and the flags used by each type.</span></span>



| <span data-ttu-id="45af0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="45af0-118">Value</span></span>        | <span data-ttu-id="45af0-119">Significado</span><span class="sxs-lookup"><span data-stu-id="45af0-119">Meaning</span></span>              | <span data-ttu-id="45af0-120">Significado</span><span class="sxs-lookup"><span data-stu-id="45af0-120">Meaning</span></span>               |
|--------------|----------------------|-----------------------|
| <span data-ttu-id="45af0-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="45af0-121">digitalvideo</span></span> | <span data-ttu-id="45af0-122">anular no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="45af0-122">abort at *rectangle*</span></span> | <span data-ttu-id="45af0-123">*nome do arquivo* keepreserve</span><span class="sxs-lookup"><span data-stu-id="45af0-123">*filename* keepreserve</span></span> |
| <span data-ttu-id="45af0-124">overlay</span><span class="sxs-lookup"><span data-stu-id="45af0-124">overlay</span></span>      | <span data-ttu-id="45af0-125">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="45af0-125">at *rectangle*</span></span>       | <span data-ttu-id="45af0-126">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="45af0-126">*filename*</span></span>            |
| <span data-ttu-id="45af0-127">sequenciador</span><span class="sxs-lookup"><span data-stu-id="45af0-127">sequencer</span></span>    | <span data-ttu-id="45af0-128">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="45af0-128">*filename*</span></span>           |                       |
| <span data-ttu-id="45af0-129">waveaudio</span><span class="sxs-lookup"><span data-stu-id="45af0-129">waveaudio</span></span>    | <span data-ttu-id="45af0-130">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="45af0-130">*filename*</span></span>           |                       |



 

<span data-ttu-id="45af0-131">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszFileName** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="45af0-131">The following table lists the flags that can be specified in the **lpszFilename** parameter and their meanings.</span></span>



| <span data-ttu-id="45af0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="45af0-132">Value</span></span>          | <span data-ttu-id="45af0-133">Significado</span><span class="sxs-lookup"><span data-stu-id="45af0-133">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45af0-134">abort</span><span class="sxs-lookup"><span data-stu-id="45af0-134">abort</span></span>          | <span data-ttu-id="45af0-135">Interrompe uma operação de **salvamento** em andamento.</span><span class="sxs-lookup"><span data-stu-id="45af0-135">Stops a **save** operation in progress.</span></span> <span data-ttu-id="45af0-136">Se usado, deve ser o único item presente.</span><span class="sxs-lookup"><span data-stu-id="45af0-136">If used, this must be the only item present.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="45af0-137">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="45af0-137">at *rectangle*</span></span> | <span data-ttu-id="45af0-138">Especifica um retângulo relativo à origem do buffer do quadro.</span><span class="sxs-lookup"><span data-stu-id="45af0-138">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="45af0-139">O *retângulo* é especificado como *X1 Y1 x2 y2*.</span><span class="sxs-lookup"><span data-stu-id="45af0-139">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="45af0-140">As coordenadas *X1 Y1* especificam o canto superior esquerdo e as coordenadas *x2 y2* especificam a largura e a altura. Para dispositivos de vídeo digital, o comando de [captura](capture.md) é usado para capturar o conteúdo do buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="45af0-140">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.For digital-video devices, the [capture](capture.md) command is used to capture the contents of the frame buffer.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="45af0-141">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="45af0-141">*filename*</span></span>     | <span data-ttu-id="45af0-142">Especifica o nome de arquivo a ser atribuído ao arquivos de dados.</span><span class="sxs-lookup"><span data-stu-id="45af0-142">Specifies the filename to assign to the data file.</span></span> <span data-ttu-id="45af0-143">Se um caminho não for especificado, o arquivo será colocado no disco e no diretório especificado anteriormente no comando [reserva](reserve.md) explícita ou implícita.</span><span class="sxs-lookup"><span data-stu-id="45af0-143">If a path is not specified, the file will be placed on the disk and in the directory previously specified on the explicit or implicit [reserve](reserve.md) command.</span></span> <span data-ttu-id="45af0-144">Se a **reserva** não tiver sido emitida, a unidade e o diretório padrão serão os associados à tarefa do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="45af0-144">If **reserve** has not been issued, the default drive and directory are those associated with the application's task.</span></span> <span data-ttu-id="45af0-145">Se um caminho for especificado, o dispositivo poderá exigir que ele esteja na unidade de disco especificada pela **reserva** explícita ou implícita.</span><span class="sxs-lookup"><span data-stu-id="45af0-145">If a path is specified, the device might require it to be on the disk drive specified by the explicit or implicit **reserve**.</span></span> <span data-ttu-id="45af0-146">Esse sinalizador é necessário.</span><span class="sxs-lookup"><span data-stu-id="45af0-146">This flag is required.</span></span> |
| <span data-ttu-id="45af0-147">keepreserve</span><span class="sxs-lookup"><span data-stu-id="45af0-147">keepreserve</span></span>    | <span data-ttu-id="45af0-148">Especifica que o espaço em disco não utilizado restante do comando de **reserva** original não é desalocado.</span><span class="sxs-lookup"><span data-stu-id="45af0-148">Specifies that unused disk space left over from the original **reserve** command is not deallocated.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="45af0-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="45af0-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="45af0-150">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="45af0-150">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="45af0-151">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="45af0-151">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="45af0-152">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="45af0-152">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45af0-153">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="45af0-153">Return Value</span></span>

<span data-ttu-id="45af0-154">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="45af0-154">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="45af0-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="45af0-155">Remarks</span></span>

<span data-ttu-id="45af0-156">A variável *filename* será necessária se o dispositivo tiver sido aberto usando o identificador de dispositivo "novo".</span><span class="sxs-lookup"><span data-stu-id="45af0-156">The *filename* variable is required if the device was opened using the "new" device identifier.</span></span>

## <a name="examples"></a><span data-ttu-id="45af0-157">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45af0-157">Examples</span></span>

<span data-ttu-id="45af0-158">O comando a seguir salva todo o buffer de vídeo em um arquivo chamado VCAPFILE. TGA.</span><span class="sxs-lookup"><span data-stu-id="45af0-158">The following command saves the entire video buffer to a file named VCAPFILE.TGA.</span></span>

``` syntax
save vboard c:\vcap\vcapfile.tga
```

## <a name="requirements"></a><span data-ttu-id="45af0-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45af0-159">Requirements</span></span>



| <span data-ttu-id="45af0-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="45af0-160">Requirement</span></span> | <span data-ttu-id="45af0-161">Valor</span><span class="sxs-lookup"><span data-stu-id="45af0-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="45af0-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45af0-162">Minimum supported client</span></span><br/> | <span data-ttu-id="45af0-163">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45af0-163">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="45af0-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45af0-164">Minimum supported server</span></span><br/> | <span data-ttu-id="45af0-165">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45af0-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="45af0-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="45af0-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45af0-167">MCI</span><span class="sxs-lookup"><span data-stu-id="45af0-167">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="45af0-168">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="45af0-168">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="45af0-169">captura</span><span class="sxs-lookup"><span data-stu-id="45af0-169">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="45af0-170">reservado</span><span class="sxs-lookup"><span data-stu-id="45af0-170">reserve</span></span>](reserve.md)
</dt> </dl>

 

