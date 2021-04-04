---
title: Mensagem de MM_MCINOTIFY (mmsystem. h)
description: A \_ mensagem mm MCINOTIFY notifica um aplicativo de que um dispositivo MCI concluiu uma operação. Os dispositivos MCI enviam essa mensagem somente quando o \_ sinalizador de notificação MCI é usado.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- Multimídia do Windows de mensagem MM_MCINOTIFY
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085899"
---
# <a name="mm_mcinotify-message"></a><span data-ttu-id="8c219-105">\_Mensagem mm MCINOTIFY</span><span class="sxs-lookup"><span data-stu-id="8c219-105">MM\_MCINOTIFY message</span></span>

<span data-ttu-id="8c219-106">A mensagem **mm \_ MCINOTIFY** notifica um aplicativo de que um dispositivo MCI concluiu uma operação.</span><span class="sxs-lookup"><span data-stu-id="8c219-106">The **MM\_MCINOTIFY** message notifies an application that an MCI device has completed an operation.</span></span> <span data-ttu-id="8c219-107">Os dispositivos MCI enviam essa mensagem somente quando o \_ sinalizador de notificação MCI é usado.</span><span class="sxs-lookup"><span data-stu-id="8c219-107">MCI devices send this message only when the MCI\_NOTIFY flag is used.</span></span>


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a><span data-ttu-id="8c219-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c219-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c219-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="8c219-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8c219-110">Motivo da notificação.</span><span class="sxs-lookup"><span data-stu-id="8c219-110">Reason for the notification.</span></span> <span data-ttu-id="8c219-111">Os seguintes valores são definidos:</span><span class="sxs-lookup"><span data-stu-id="8c219-111">The following values are defined:</span></span>



| <span data-ttu-id="8c219-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c219-112">Requirement</span></span> | <span data-ttu-id="8c219-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8c219-113">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c219-114">\_notificação MCI \_ anulada</span><span class="sxs-lookup"><span data-stu-id="8c219-114">MCI\_NOTIFY\_ABORTED</span></span>    | <span data-ttu-id="8c219-115">O dispositivo recebeu um comando que impediu que as condições atuais para iniciar a função de retorno de chamada fossem atendidas.</span><span class="sxs-lookup"><span data-stu-id="8c219-115">The device received a command that prevented the current conditions for initiating the callback function from being met.</span></span> <span data-ttu-id="8c219-116">Se um novo comando interromper o comando atual e ele também solicitar notificação, o dispositivo enviará essa mensagem somente e não a \_ notificação MCI será \_ substituída</span><span class="sxs-lookup"><span data-stu-id="8c219-116">If a new command interrupts the current command and it also requests notification, the device sends this message only and not MCI\_NOTIFY\_SUPERSEDED</span></span> |
| <span data-ttu-id="8c219-117">\_falha na notificação do MCI \_</span><span class="sxs-lookup"><span data-stu-id="8c219-117">MCI\_NOTIFY\_FAILURE</span></span>    | <span data-ttu-id="8c219-118">Ocorreu um erro de dispositivo enquanto o dispositivo estava executando o comando.</span><span class="sxs-lookup"><span data-stu-id="8c219-118">A device error occurred while the device was executing the command.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="8c219-119">\_notificação MCI \_ bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="8c219-119">MCI\_NOTIFY\_SUCCESSFUL</span></span> | <span data-ttu-id="8c219-120">As condições que iniciam a função de retorno de chamada foram atendidas.</span><span class="sxs-lookup"><span data-stu-id="8c219-120">The conditions initiating the callback function have been met.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="8c219-121">\_notificação MCI \_ substituída</span><span class="sxs-lookup"><span data-stu-id="8c219-121">MCI\_NOTIFY\_SUPERSEDED</span></span> | <span data-ttu-id="8c219-122">O dispositivo recebeu outro comando com o sinalizador "notificar" definido e as condições atuais para iniciar a função de retorno de chamada foram substituídas.</span><span class="sxs-lookup"><span data-stu-id="8c219-122">The device received another command with the "notify" flag set and the current conditions for initiating the callback function have been superseded.</span></span>                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="8c219-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span><span class="sxs-lookup"><span data-stu-id="8c219-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span></span>
</dt> <dd>

<span data-ttu-id="8c219-124">Identificador do dispositivo que inicia a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8c219-124">Identifier of the device initiating the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c219-125">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8c219-125">Return Value</span></span>

<span data-ttu-id="8c219-126">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="8c219-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c219-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c219-127">Remarks</span></span>

<span data-ttu-id="8c219-128">Para obter mais informações sobre o \_ sinalizador de notificação MCI, consulte [o sinalizador notificar](the-notify-flag.md).</span><span class="sxs-lookup"><span data-stu-id="8c219-128">For more information about the MCI\_NOTIFY flag, see [The Notify Flag](the-notify-flag.md).</span></span>

<span data-ttu-id="8c219-129">Um dispositivo retorna o sinalizador de notificação MCI com \_ \_ êxito com **mm \_ MCINOTIFY** quando a ação de um comando é concluída.</span><span class="sxs-lookup"><span data-stu-id="8c219-129">A device returns the MCI\_NOTIFY\_SUCCESSFUL flag with **MM\_MCINOTIFY** when the action for a command finishes.</span></span> <span data-ttu-id="8c219-130">Por exemplo, um dispositivo de áudio de CD usa esse sinalizador para notificação para o comando [**Play**](play.md) ( [**\_ reprodução MCI**](mci-play.md)) quando o dispositivo termina de ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="8c219-130">For example, a CD audio device uses this flag for notification for the [**play**](play.md) ( [**MCI\_PLAY**](mci-play.md)) command when the device finishes playing.</span></span> <span data-ttu-id="8c219-131">O comando **Play** é bem-sucedido somente quando atinge a posição final especificada ou atinge o final da mídia.</span><span class="sxs-lookup"><span data-stu-id="8c219-131">The **play** command is successful only when it reaches the specified end position or reaches the end of the media.</span></span> <span data-ttu-id="8c219-132">Da mesma forma, os comandos [**Seek**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) e [**Record**](record.md) ( [**\_ registro MCI**](mci-record.md)) não retornam \_ \_ a notificação de MCI com êxito até atingirem a posição final especificada ou atingirem o final da mídia.</span><span class="sxs-lookup"><span data-stu-id="8c219-132">Similarly, the [**seek**](seek.md) ( [**MCI\_SEEK**](mci-seek.md)) and [**record**](record.md) ( [**MCI\_RECORD**](mci-record.md)) commands do not return MCI\_NOTIFY\_SUCCESSFUL until they reach the specified end position or reach the end of the media.</span></span>

<span data-ttu-id="8c219-133">Um dispositivo retorna o \_ sinalizador de notificação MCI \_ abortado com **mm \_ MCINOTIFY** somente quando recebe um comando que impede que ele atenda às condições de notificação.</span><span class="sxs-lookup"><span data-stu-id="8c219-133">A device returns the MCI\_NOTIFY\_ABORTED flag with **MM\_MCINOTIFY** only when it receives a command that prevents it from meeting the notification conditions.</span></span> <span data-ttu-id="8c219-134">Por exemplo, o comando [**Play**](play.md) não anulará a notificação para um comando de **reprodução** anterior, desde que o novo comando não altere a direção da reprodução nem altere a posição final.</span><span class="sxs-lookup"><span data-stu-id="8c219-134">For example, the [**play**](play.md) command would not abort notification for a previous **play** command provided that the new command does not change the play direction or change the ending position.</span></span> <span data-ttu-id="8c219-135">Os comandos de [**busca**](seek.md) e [**registro**](record.md) se comportam da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="8c219-135">The [**seek**](seek.md) and [**record**](record.md) commands behave similarly.</span></span> <span data-ttu-id="8c219-136">O MCI também não envia \_ uma notificação MCI \_ abortada quando a reprodução ou a gravação é pausada com o comando [**Pause**](pause.md) ( [**MCI \_ Pause**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="8c219-136">MCI also does not send MCI\_NOTIFY\_ABORTED when playback or recording is paused with the [**pause**](pause.md) ( [**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="8c219-137">Enviar o comando [**retomar**](resume.md) ( [**MCI \_ resume**](mci-resume.md)) permite que eles continuem a atender às condições de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8c219-137">Sending the [**resume**](resume.md) ( [**MCI\_RESUME**](mci-resume.md)) command allows them to continue to meet the callback conditions.</span></span>

<span data-ttu-id="8c219-138">Quando o aplicativo solicitar uma notificação para um comando, verifique o retorno de erro das funções [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8c219-138">When your application requests notification for a command, check the error return of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) functions.</span></span> <span data-ttu-id="8c219-139">Se essas funções encontrarem um erro e retornarem um valor diferente de zero, o MCI não definirá a notificação para o comando.</span><span class="sxs-lookup"><span data-stu-id="8c219-139">If these functions encounter an error and return a nonzero value, MCI will not set notification for the command.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c219-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c219-140">Requirements</span></span>



| <span data-ttu-id="8c219-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c219-141">Requirement</span></span> | <span data-ttu-id="8c219-142">Valor</span><span class="sxs-lookup"><span data-stu-id="8c219-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c219-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c219-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8c219-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c219-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c219-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c219-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8c219-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c219-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c219-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8c219-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c219-148"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c219-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c219-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c219-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c219-150">MCI</span><span class="sxs-lookup"><span data-stu-id="8c219-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8c219-151">Mensagens MCI</span><span class="sxs-lookup"><span data-stu-id="8c219-151">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="8c219-152">**temporariamente**</span><span class="sxs-lookup"><span data-stu-id="8c219-152">**pause**</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="8c219-153">**reproduzir**</span><span class="sxs-lookup"><span data-stu-id="8c219-153">**play**</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="8c219-154">**gravável**</span><span class="sxs-lookup"><span data-stu-id="8c219-154">**record**</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="8c219-155">**Volte**</span><span class="sxs-lookup"><span data-stu-id="8c219-155">**resume**</span></span>](resume.md)
</dt> <dt>

[<span data-ttu-id="8c219-156">**Procure**</span><span class="sxs-lookup"><span data-stu-id="8c219-156">**seek**</span></span>](seek.md)
</dt> </dl>

 

