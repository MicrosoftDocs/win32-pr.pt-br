---
title: comando de sinal
description: O comando Signal identifica uma posição especificada no espaço de trabalho enviando o aplicativo uma \_ mensagem mm MCISIGNAL. Dispositivos de vídeo digital reconhecem este comando. O MCIAVI dá suporte a apenas um sinal ativo por vez.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- Multimídia do Windows de comando de sinal
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779613"
---
# <a name="signal-command"></a><span data-ttu-id="fb3f3-106">comando de sinal</span><span class="sxs-lookup"><span data-stu-id="fb3f3-106">signal command</span></span>

<span data-ttu-id="fb3f3-107">O comando Signal identifica uma posição especificada no espaço de trabalho enviando o aplicativo uma mensagem [mm \_ MCISIGNAL](mm-mcisignal.md) .</span><span class="sxs-lookup"><span data-stu-id="fb3f3-107">The signal command identifies a specified position in the workspace by sending the application an [MM\_MCISIGNAL](mm-mcisignal.md) message.</span></span> <span data-ttu-id="fb3f3-108">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="fb3f3-109">O MCIAVI dá suporte a apenas um sinal ativo por vez.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="fb3f3-110">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="fb3f3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb3f3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3f3-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="fb3f3-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="fb3f3-113">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-113">Identifier of an MCI device.</span></span> <span data-ttu-id="fb3f3-114">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="fb3f3-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span><span class="sxs-lookup"><span data-stu-id="fb3f3-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fb3f3-116">Um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-116">One of the following flags.</span></span>



| <span data-ttu-id="fb3f3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fb3f3-117">Value</span></span>            | <span data-ttu-id="fb3f3-118">Significado</span><span class="sxs-lookup"><span data-stu-id="fb3f3-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3f3-119">na posição</span><span class="sxs-lookup"><span data-stu-id="fb3f3-119">at position</span></span>      | <span data-ttu-id="fb3f3-120">Especifica o quadro para invocar um sinal.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-120">Specifies the frame to invoke a signal.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="fb3f3-121">cancel</span><span class="sxs-lookup"><span data-stu-id="fb3f3-121">cancel</span></span>           | <span data-ttu-id="fb3f3-122">Remove os sinais do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-122">Removes signals from the workspace.</span></span> <span data-ttu-id="fb3f3-123">Um sinal individual é especificado usando o sinalizador "uservalue".</span><span class="sxs-lookup"><span data-stu-id="fb3f3-123">An individual signal is specified by using the "uservalue" flag.</span></span> <span data-ttu-id="fb3f3-124">Se o sinalizador "uservalue" não for especificado com o uso de "Cancel", o dispositivo cancelará todos os sinais.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-124">If the "uservalue" flag is not specified by using "cancel", the device cancels all signals.</span></span> <span data-ttu-id="fb3f3-125">O sinalizador "Cancelar" é incompatível com os sinalizadores "at", "todos" e "posição de retorno".</span><span class="sxs-lookup"><span data-stu-id="fb3f3-125">The "cancel" flag is incompatible with the "at", "every", and "return position" flags.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="fb3f3-126">cada *intervalo*</span><span class="sxs-lookup"><span data-stu-id="fb3f3-126">every *interval*</span></span> | <span data-ttu-id="fb3f3-127">Especifica o período dos sinais.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-127">Specifies the period of the signals.</span></span> <span data-ttu-id="fb3f3-128">O valor do *intervalo* é especificado no formato de hora atual. Se usado com a *posição*"at", os sinais são colocados em todo o espaço de trabalho com uma marca de sinal colocada na *posição*.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-128">The *interval* value is specified in the current time format.If used with "at" *position*, signals are placed throughout the workspace with one signal mark placed at *position*.</span></span><br/> <span data-ttu-id="fb3f3-129">Sem o sinalizador "at", os sinais são colocados em todo o espaço de trabalho com um sinal na posição atual.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-129">Without the "at" flag, signals are placed throughout the workspace with one signal at the current position.</span></span><br/> <span data-ttu-id="fb3f3-130">Se esse sinalizador for omitido, somente a posição indicada pelo sinalizador "at" será marcada.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-130">If this flag is omitted, only the position indicated by the "at" flag is marked.</span></span><br/> <span data-ttu-id="fb3f3-131">Se o valor do *intervalo* for menor que a frequência mínima com suporte de um dispositivo, ele usará seu valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-131">If the *interval* value is less than the minimum frequency supported by a device, it will use its minimum value.</span></span><br/> |
| <span data-ttu-id="fb3f3-132">posição de retorno</span><span class="sxs-lookup"><span data-stu-id="fb3f3-132">return position</span></span>  | <span data-ttu-id="fb3f3-133">Indica que o dispositivo deve enviar o valor de posição em vez do identificador "uservalue" na mensagem de sinalização.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-133">Indicates the device should send the position value instead of the "uservalue" identifier in the signaling message.</span></span> <span data-ttu-id="fb3f3-134">O identificador "uservalue" ainda pode ser usado para cancelar ou redefinir as marcas de sinalização.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-134">The "uservalue" identifier can still be used to cancel or to redefine the signal marks.</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fb3f3-135">*ID* de uservalue</span><span class="sxs-lookup"><span data-stu-id="fb3f3-135">uservalue *id*</span></span>   | <span data-ttu-id="fb3f3-136">Especifica um identificador que é relatado de volta com a mensagem de sinalização.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-136">Specifies an identifier that is reported back with the signaling message.</span></span> <span data-ttu-id="fb3f3-137">Esse identificador atua como um identificador que pode ser usado com outros comandos de **sinal** para fazer referência a essa configuração de **sinal** .</span><span class="sxs-lookup"><span data-stu-id="fb3f3-137">This identifier acts as an identifier that can be used with other **signal** commands to reference this **signal** setting.</span></span> <span data-ttu-id="fb3f3-138">Se omitido, o valor padrão será zero.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-138">If omitted, the default value is zero.</span></span>                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="fb3f3-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="fb3f3-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fb3f3-140">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-140">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="fb3f3-141">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fb3f3-141">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3f3-142">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fb3f3-142">Return Value</span></span>

<span data-ttu-id="fb3f3-143">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-143">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb3f3-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb3f3-144">Remarks</span></span>

<span data-ttu-id="fb3f3-145">O identificador de janela usado para notificação de mensagens de conclusão de comando também é usado para sinalização.</span><span class="sxs-lookup"><span data-stu-id="fb3f3-145">The window handle used for notification of command completion messages is also used for signaling.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3f3-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb3f3-146">Requirements</span></span>



| <span data-ttu-id="fb3f3-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb3f3-147">Requirement</span></span> | <span data-ttu-id="fb3f3-148">Valor</span><span class="sxs-lookup"><span data-stu-id="fb3f3-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fb3f3-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb3f3-149">Minimum supported client</span></span><br/> | <span data-ttu-id="fb3f3-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fb3f3-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fb3f3-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb3f3-151">Minimum supported server</span></span><br/> | <span data-ttu-id="fb3f3-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fb3f3-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fb3f3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb3f3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3f3-154">MCI</span><span class="sxs-lookup"><span data-stu-id="fb3f3-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fb3f3-155">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="fb3f3-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="fb3f3-156">\_MCISIGNAL mm</span><span class="sxs-lookup"><span data-stu-id="fb3f3-156">MM\_MCISIGNAL</span></span>](mm-mcisignal.md)
</dt> </dl>

 

