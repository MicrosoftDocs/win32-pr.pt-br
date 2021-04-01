---
title: comando Reserve
description: O comando Reserve aloca espaço em disco contíguo para o espaço de trabalho da instância do dispositivo. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- comando de reserva de multimídia do Windows
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918012"
---
# <a name="reserve-command"></a><span data-ttu-id="d2e7b-105">comando Reserve</span><span class="sxs-lookup"><span data-stu-id="d2e7b-105">reserve command</span></span>

<span data-ttu-id="d2e7b-106">O comando Reserve aloca espaço em disco contíguo para o espaço de trabalho da instância do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-106">The reserve command allocates contiguous disk space for the device instance's workspace.</span></span> <span data-ttu-id="d2e7b-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d2e7b-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d2e7b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2e7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2e7b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d2e7b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d2e7b-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d2e7b-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d2e7b-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span><span class="sxs-lookup"><span data-stu-id="d2e7b-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span></span>
</dt> <dd>

<span data-ttu-id="d2e7b-114">Um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-114">One or more of the following flags.</span></span>



| <span data-ttu-id="d2e7b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d2e7b-115">Value</span></span>           | <span data-ttu-id="d2e7b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d2e7b-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e7b-117">no *caminho*</span><span class="sxs-lookup"><span data-stu-id="d2e7b-117">in *path*</span></span>       | <span data-ttu-id="d2e7b-118">Especifica a unidade e o caminho do diretório (mas não o nome) de um arquivo temporário usado para armazenar dados gravados.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-118">Specifies the drive and directory path (but not the name) of a temporary file used to hold recorded data.</span></span> <span data-ttu-id="d2e7b-119">O nome desse arquivo é especificado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-119">The name of this file is specified by the device.</span></span> <span data-ttu-id="d2e7b-120">O arquivo temporário é excluído quando o dispositivo é fechado.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-120">The temporary file is deleted when the device is closed.</span></span> <span data-ttu-id="d2e7b-121">Se esse sinalizador for omitido, o dispositivo especificará o local do espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-121">If this flag is omitted, the device specifies the location of the disk space.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d2e7b-122">*duração* do tamanho</span><span class="sxs-lookup"><span data-stu-id="d2e7b-122">size *duration*</span></span> | <span data-ttu-id="d2e7b-123">Especifica a quantidade aproximada de espaço em disco a ser reservada no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-123">Specifies the approximate amount of disk space to reserve in the workspace.</span></span> <span data-ttu-id="d2e7b-124">O valor *Duration* é especificado no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-124">The *duration* value is specified in the current time format.</span></span> <span data-ttu-id="d2e7b-125">O dispositivo baseia sua estimativa do espaço em disco necessário nos seguintes parâmetros: a hora solicitada, o formato de arquivo, o algoritmo de compactação de vídeo e áudio e os valores de qualidade de compactação em vigor.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-125">The device bases its estimate of the required disk space on the following parameters: the requested time, the file format, the video and audio compression algorithm, and the compression quality values in effect.</span></span> <span data-ttu-id="d2e7b-126">Se [setvideo](setvideo.md) "registro" for "desativado", o espaço será reservado somente para áudio.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-126">If [setvideo](setvideo.md) "record" is "off", then space is reserved only for audio.</span></span> <span data-ttu-id="d2e7b-127">Se [SetAudio](setaudio.md) "registro" for "desativado", o espaço será reservado somente para vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-127">If [setaudio](setaudio.md) "record" is "off", then space is reserved only for video.</span></span> <span data-ttu-id="d2e7b-128">Se ambos estiverem "desativados" ou se a *duração* for zero, nenhum espaço será reservado e qualquer espaço reservado existente será desalocado.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-128">If both are "off", or if *duration* is zero, then no space is reserved and any existing reserved space is deallocated.</span></span> <span data-ttu-id="d2e7b-129">Se esse sinalizador for omitido, o dispositivo usará um padrão definido pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-129">If this flag is omitted, the device will use a device-defined default.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d2e7b-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d2e7b-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d2e7b-131">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-131">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="d2e7b-132">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d2e7b-132">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2e7b-133">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d2e7b-133">Return Value</span></span>

<span data-ttu-id="d2e7b-134">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-134">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2e7b-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2e7b-135">Remarks</span></span>

<span data-ttu-id="d2e7b-136">Se necessário, os comandos [gravar](record.md) ou [salvar](save.md) subsequentes usam o espaço reservado por esse comando.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-136">If needed, subsequent [record](record.md) or [save](save.md) commands use the space reserved by this command.</span></span> <span data-ttu-id="d2e7b-137">Se o espaço de trabalho contiver dados não salvos, os dados serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-137">If the workspace contains unsaved data, the data is lost.</span></span> <span data-ttu-id="d2e7b-138">Alguns dispositivos não exigem reserva e os ignoram.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-138">Some devices do not require reserve and ignore it.</span></span> <span data-ttu-id="d2e7b-139">Se o espaço em disco não for reservado antes da gravação, o comando gravar executará uma reserva implícita com sinalizadores padrão específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-139">If disk space is not reserved prior to recording, the record command performs an implied reserve with device-specific default flags.</span></span> <span data-ttu-id="d2e7b-140">Use um comando de reserva explícito se desejar um melhor controle de quando ocorrer o atraso de alocação de disco, o controle de quanto espaço é alocado e o controle de onde o espaço em disco é alocado.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-140">Use an explicit reserve command if you want better control of when the delay for disk allocation occurs, control of how much space is allocated, and control of where the disk space is allocated.</span></span> <span data-ttu-id="d2e7b-141">Seu aplicativo pode alterar a quantidade e o local do espaço em disco reservado anteriormente com os comandos de reserva subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-141">Your application can change the amount and location of previously reserved disk space with subsequent reserve commands.</span></span> <span data-ttu-id="d2e7b-142">Qualquer espaço em disco alocado e ainda não utilizado não será desalocado até que os dados gravados sejam salvos ou até que a instância do dispositivo seja fechada.</span><span class="sxs-lookup"><span data-stu-id="d2e7b-142">Any allocated and still unused disk space is not deallocated until any recorded data is saved, or until the device instance is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2e7b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2e7b-143">Requirements</span></span>



| <span data-ttu-id="d2e7b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2e7b-144">Requirement</span></span> | <span data-ttu-id="d2e7b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="d2e7b-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2e7b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2e7b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e7b-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2e7b-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d2e7b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2e7b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e7b-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2e7b-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d2e7b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2e7b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e7b-151">MCI</span><span class="sxs-lookup"><span data-stu-id="d2e7b-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d2e7b-152">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="d2e7b-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d2e7b-153">gravável</span><span class="sxs-lookup"><span data-stu-id="d2e7b-153">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="d2e7b-154">salvar</span><span class="sxs-lookup"><span data-stu-id="d2e7b-154">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="d2e7b-155">SetAudio</span><span class="sxs-lookup"><span data-stu-id="d2e7b-155">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="d2e7b-156">setvideo</span><span class="sxs-lookup"><span data-stu-id="d2e7b-156">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

