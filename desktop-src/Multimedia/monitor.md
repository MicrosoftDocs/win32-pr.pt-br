---
title: comando monitorar
description: O comando monitor especifica a origem da apresentação. (A fonte de apresentação padrão é o espaço de trabalho.) Alternar a origem da apresentação alterna todos os fluxos de áudio e vídeo na origem. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- monitorar multimídia do Windows de comando
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644631"
---
# <a name="monitor-command"></a><span data-ttu-id="f1329-106">comando monitorar</span><span class="sxs-lookup"><span data-stu-id="f1329-106">monitor command</span></span>

<span data-ttu-id="f1329-107">O comando monitor especifica a origem da apresentação.</span><span class="sxs-lookup"><span data-stu-id="f1329-107">The monitor command specifies the presentation source.</span></span> <span data-ttu-id="f1329-108">(A fonte de apresentação padrão é o espaço de trabalho.) Alternar a origem da apresentação alterna todos os fluxos de áudio e vídeo na origem.</span><span class="sxs-lookup"><span data-stu-id="f1329-108">(The default presentation source is the workspace.) Switching the presentation source switches all audio and video streams in the source.</span></span> <span data-ttu-id="f1329-109">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f1329-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="f1329-110">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f1329-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f1329-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1329-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1329-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f1329-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f1329-113">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f1329-113">Identifier of an MCI device.</span></span> <span data-ttu-id="f1329-114">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="f1329-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f1329-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span><span class="sxs-lookup"><span data-stu-id="f1329-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="f1329-116">Um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1329-116">One or more of the following flags.</span></span>



| <span data-ttu-id="f1329-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f1329-117">Value</span></span>           | <span data-ttu-id="f1329-118">Significado</span><span class="sxs-lookup"><span data-stu-id="f1329-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1329-119">arquivo</span><span class="sxs-lookup"><span data-stu-id="f1329-119">file</span></span>            | <span data-ttu-id="f1329-120">Especifica que o espaço de trabalho é a fonte da apresentação.</span><span class="sxs-lookup"><span data-stu-id="f1329-120">Specifies that the workspace is the presentation source.</span></span> <span data-ttu-id="f1329-121">Essa é a origem padrão.</span><span class="sxs-lookup"><span data-stu-id="f1329-121">This is the default source.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f1329-122">input</span><span class="sxs-lookup"><span data-stu-id="f1329-122">input</span></span>           | <span data-ttu-id="f1329-123">Especifica que a entrada externa é a origem da apresentação.</span><span class="sxs-lookup"><span data-stu-id="f1329-123">Specifies that the external input is the presentation source.</span></span> <span data-ttu-id="f1329-124">Se um comando [Play](play.md) estiver em andamento, primeiro será pausado.</span><span class="sxs-lookup"><span data-stu-id="f1329-124">If a [play](play.md) command is in progress, it is first paused.</span></span> <span data-ttu-id="f1329-125">Se [setvideo](setvideo.md) for "on", esse sinalizador exibirá uma janela oculta padrão.</span><span class="sxs-lookup"><span data-stu-id="f1329-125">If [setvideo](setvideo.md) is "on", this flag displays a default hidden window.</span></span> <span data-ttu-id="f1329-126">Os dispositivos podem limitar o que outras instâncias de dispositivo podem fazer ao monitorar a entrada.</span><span class="sxs-lookup"><span data-stu-id="f1329-126">Devices might limit what other device instances can do while monitoring input.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f1329-127">*método* de método</span><span class="sxs-lookup"><span data-stu-id="f1329-127">method *method*</span></span> | <span data-ttu-id="f1329-128">Quando usado com o **Monitor** "Input", esse sinalizador seleciona o método de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f1329-128">When used with **monitor** "input", this flag selects the method of monitoring.</span></span> <span data-ttu-id="f1329-129">O *método* é "pre", "post" ou "Direct".</span><span class="sxs-lookup"><span data-stu-id="f1329-129">The *method* is either "pre", "post", or "direct".</span></span> <span data-ttu-id="f1329-130">Solicitações de monitoramento direto que o dispositivo está configurado para a qualidade de exibição ideal durante o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f1329-130">Direct monitoring requests that the device be configured for optimum display quality during monitoring.</span></span> <span data-ttu-id="f1329-131">O método de monitoramento direto pode ser incompatível com a gravação de vídeo de movimento. Pré e pós-monitoramento permitem a gravação do vídeo em movimento.</span><span class="sxs-lookup"><span data-stu-id="f1329-131">The direct monitoring method might be incompatible with motion video recording.Pre- and post-monitoring allow motion video recording.</span></span> <span data-ttu-id="f1329-132">O monitoramento prévio mostra a entrada externa antes da compactação, enquanto o pós-processamento mostra a entrada externa após a compactação.</span><span class="sxs-lookup"><span data-stu-id="f1329-132">Pre-monitoring shows the external input prior to compression, while post-monitoring shows the external input after compression.</span></span> <span data-ttu-id="f1329-133">Normalmente, diferentes métodos de monitoramento têm diferentes implicações de hardware.</span><span class="sxs-lookup"><span data-stu-id="f1329-133">Typically, different monitoring methods have different hardware implications.</span></span> <span data-ttu-id="f1329-134">O método de monitoramento padrão é selecionado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1329-134">The default monitoring method is selected by the device.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1329-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f1329-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f1329-136">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="f1329-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="f1329-137">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f1329-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1329-138">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f1329-138">Return Value</span></span>

<span data-ttu-id="f1329-139">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f1329-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1329-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1329-140">Remarks</span></span>

<span data-ttu-id="f1329-141">A origem da apresentação alterna automaticamente para o espaço de trabalho após uma [reprodução](play.md), [etapa](step.md), [Pausar](pause.md), [indicação](cue.md) de "saída" ou comando de [busca](seek.md) .</span><span class="sxs-lookup"><span data-stu-id="f1329-141">The presentation source automatically switches to the workspace after a [play](play.md), [step](step.md), [pause](pause.md), [cue](cue.md) "output", or [seek](seek.md) command.</span></span> <span data-ttu-id="f1329-142">O comando [gravar](record.md) não alterna automaticamente as fontes de apresentação, o que dá ao aplicativo a opção de não mostrar o vídeo enquanto ele está sendo gravado.</span><span class="sxs-lookup"><span data-stu-id="f1329-142">The [record](record.md) command does not automatically switch presentation sources, which gives your application the option of not showing video while it is being recorded.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1329-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1329-143">Requirements</span></span>



| <span data-ttu-id="f1329-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1329-144">Requirement</span></span> | <span data-ttu-id="f1329-145">Valor</span><span class="sxs-lookup"><span data-stu-id="f1329-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f1329-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1329-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f1329-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1329-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1329-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1329-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f1329-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1329-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f1329-150">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f1329-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1329-151">MCI</span><span class="sxs-lookup"><span data-stu-id="f1329-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f1329-152">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="f1329-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="f1329-153">advertência</span><span class="sxs-lookup"><span data-stu-id="f1329-153">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="f1329-154">pause</span><span class="sxs-lookup"><span data-stu-id="f1329-154">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="f1329-155">reproduzir</span><span class="sxs-lookup"><span data-stu-id="f1329-155">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="f1329-156">gravável</span><span class="sxs-lookup"><span data-stu-id="f1329-156">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="f1329-157">Procure</span><span class="sxs-lookup"><span data-stu-id="f1329-157">seek</span></span>](seek.md)
</dt> <dt>

[<span data-ttu-id="f1329-158">etapa</span><span class="sxs-lookup"><span data-stu-id="f1329-158">step</span></span>](step.md)
</dt> </dl>

 

