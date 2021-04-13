---
title: MCI_GETDEVCAPS comando (mmsystem. h)
description: O \_ comando MCI GETDEVCAPS recupera informações estáticas sobre um dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- Multimídia do Windows de comando MCI_GETDEVCAPS
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499796"
---
# <a name="mci_getdevcaps-command"></a><span data-ttu-id="4ad96-104">\_Comando MCI GETDEVCAPS</span><span class="sxs-lookup"><span data-stu-id="4ad96-104">MCI\_GETDEVCAPS command</span></span>

<span data-ttu-id="4ad96-105">O \_ comando MCI GETDEVCAPS recupera informações estáticas sobre um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ad96-105">The MCI\_GETDEVCAPS command retrieves static information about a device.</span></span> <span data-ttu-id="4ad96-106">Todos os dispositivos reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="4ad96-106">All devices recognize this command.</span></span> <span data-ttu-id="4ad96-107">Os parâmetros e sinalizadores disponíveis para este comando dependem do dispositivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="4ad96-107">The parameters and flags available for this command depend on the selected device.</span></span> <span data-ttu-id="4ad96-108">As informações são retornadas no membro **dwReturn** da estrutura identificada por *lpCapsParms*.</span><span class="sxs-lookup"><span data-stu-id="4ad96-108">Information is returned in the **dwReturn** member of the structure identified by *lpCapsParms*.</span></span>

<span data-ttu-id="4ad96-109">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ad96-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a><span data-ttu-id="4ad96-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ad96-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ad96-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4ad96-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-112">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="4ad96-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4ad96-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-114">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="4ad96-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="4ad96-115">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4ad96-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span><span class="sxs-lookup"><span data-stu-id="4ad96-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-117">Ponteiro para uma estrutura de [**\_ \_ parâmetros MCI do GETDEVCAPS**](mci-getdevcaps-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad96-117">Pointer to an [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ad96-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4ad96-118">Return Value</span></span>

<span data-ttu-id="4ad96-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="4ad96-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ad96-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ad96-120">Remarks</span></span>

<span data-ttu-id="4ad96-121">Os seguintes sinalizadores padrão adicionais e específicos de comando se aplicam a todos os dispositivos que dão suporte a \_ GETDEVCAPS MCI:</span><span class="sxs-lookup"><span data-stu-id="4ad96-121">The following additional standard and command-specific flags apply to all devices supporting MCI\_GETDEVCAPS:</span></span>

<dl> <dt>

<span data-ttu-id="4ad96-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_dispositivo de \_ composição MCI GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI\_GETDEVCAPS\_COMPOUND\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-123">O membro **dwReturn** será definido como **true** se o dispositivo usar o armazenamento de dados que deve ser aberto e fechado explicitamente; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4ad96-123">The **dwReturn** member is set to **TRUE** if the device uses data storage that must be explicitly opened and closed; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_tipo de \_ dispositivo MCI GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI\_GETDEVCAPS\_DEVICE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-125">O membro **dwReturn** é definido como um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="4ad96-125">The **dwReturn** member is set to one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>o MCI \_ GETDEVCAPS \_ tem \_ áudio</span><span class="sxs-lookup"><span data-stu-id="4ad96-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI\_GETDEVCAPS\_HAS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-127">O membro **dwReturn** será definido como **true** se o dispositivo tiver a saída de áudio; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4ad96-127">The **dwReturn** member is set to **TRUE** if the device has audio output; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ tem \_ vídeo</span><span class="sxs-lookup"><span data-stu-id="4ad96-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI\_GETDEVCAPS\_HAS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-129">O membro **dwReturn** será definido como **true** se o dispositivo tiver saída de vídeo; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4ad96-129">The **dwReturn** member is set to **TRUE** if the device has video output; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="4ad96-130">Por exemplo, o membro é definido como **true** para dispositivos que dão suporte ao conjunto de comandos VIDEODISC.</span><span class="sxs-lookup"><span data-stu-id="4ad96-130">For example, the member is set to **TRUE** for devices that support the videodisc command set.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_Item GETDEVCAPS \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ad96-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI\_GETDEVCAPS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-132">Especifica que o membro **dwItem** da estrutura [**do \_ GETDEVCAPS \_ parms do MCI**](mci-getdevcaps-parms.md) contém uma das seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="4ad96-132">Specifies that the **dwItem** member of the [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure contains one of the following constants:</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>o MCI \_ GETDEVCAPS \_ pode \_ ejetar</span><span class="sxs-lookup"><span data-stu-id="4ad96-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI\_GETDEVCAPS\_CAN\_EJECT</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-134">O membro **dwReturn** será definido como **true** se o dispositivo puder ejetar a mídia; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-134">The **dwReturn** member is set to **TRUE** if the device can eject the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>o MCI \_ GETDEVCAPS \_ pode \_ reproduzir</span><span class="sxs-lookup"><span data-stu-id="4ad96-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI\_GETDEVCAPS\_CAN\_PLAY</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-136">O membro **dwReturn** será definido como **true** se o dispositivo puder reproduzir a mídia; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-136">The **dwReturn** member is set to **TRUE** if the device can play the media; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="4ad96-137">Se um dispositivo especificar **true**, ele implica que o dispositivo dá suporte aos comandos MCI [ \_ Pause](mci-pause.md) e [MCI \_ Stop](mci-stop.md) , bem como ao comando de [ \_ reprodução MCI](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad96-137">If a device specifies **TRUE**, it implies the device supports the [MCI\_PAUSE](mci-pause.md) and [MCI\_STOP](mci-stop.md) commands as well as the [MCI\_PLAY](mci-play.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>o MCI \_ GETDEVCAPS \_ pode \_ gravar</span><span class="sxs-lookup"><span data-stu-id="4ad96-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI\_GETDEVCAPS\_CAN\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-139">O membro **dwReturn** será definido como **true** se o dispositivo der suporte à gravação; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-139">The **dwReturn** member is set to **TRUE** if the device supports recording; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="4ad96-140">Se um dispositivo especificar **true**, ele implica que o dispositivo dá suporte aos \_ comandos MCI Pause e MCI \_ Stop, bem como ao comando de [ \_ registro MCI](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad96-140">If a device specifies **TRUE**, it implies the device supports the MCI\_PAUSE and MCI\_STOP commands as well as the [MCI\_RECORD](mci-record.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>o MCI \_ GETDEVCAPS \_ pode \_ salvar</span><span class="sxs-lookup"><span data-stu-id="4ad96-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI\_GETDEVCAPS\_CAN\_SAVE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-142">O membro **dwReturn** será definido como **true** se o dispositivo puder salvar um arquivo; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-142">The **dwReturn** member is set to **TRUE** if the device can save a file; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>o MCI \_ GETDEVCAPS \_ usa \_ arquivos</span><span class="sxs-lookup"><span data-stu-id="4ad96-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI\_GETDEVCAPS\_USES\_FILES</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-144">O membro **dwReturn** será definido como **true** se o dispositivo exigir um nome de arquivo; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4ad96-144">The **dwReturn** member is set to **TRUE** if the device requires a filename; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="4ad96-145">Somente dispositivos compostos usam arquivos.</span><span class="sxs-lookup"><span data-stu-id="4ad96-145">Only compound devices use files.</span></span>

</dd> </dl>

<span data-ttu-id="4ad96-146">Os sinalizadores a seguir podem ser especificados no membro **dwItem** do [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="4ad96-146">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="4ad96-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ congelar</span><span class="sxs-lookup"><span data-stu-id="4ad96-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-148">O membro **dwReturn** será definido como **true** se o dispositivo puder congelar quadros; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-148">The **dwReturn** member is set to **TRUE** if the device can freeze frames; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ Bloquear</span><span class="sxs-lookup"><span data-stu-id="4ad96-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-150">O membro **dwReturn** será definido como **true** se o dispositivo puder ser bloqueado; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-150">The **dwReturn** member is set to **TRUE** if the device can lock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ reverter</span><span class="sxs-lookup"><span data-stu-id="4ad96-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-152">O membro **dwReturn** será definido como **true** se o dispositivo puder reproduzir em ordem inversa; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-152">The **dwReturn** member is set to **TRUE** if the device can play in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ pode \_ Str \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STR\_IN</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-154">O membro **dwReturn** será definido como **true** se o dispositivo puder ampliar a entrada; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-154">The **dwReturn** member is set to **TRUE** if the device can stretch input; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ alongar</span><span class="sxs-lookup"><span data-stu-id="4ad96-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-156">O membro **dwReturn** será definido como **true** se o dispositivo puder alongar uma imagem; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-156">The **dwReturn** member is set to **TRUE** if the device can stretch an image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ testar</span><span class="sxs-lookup"><span data-stu-id="4ad96-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-158">O membro **dwReturn** será definido como **true** se o dispositivo puder executar testes; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-158">The **dwReturn** member is set to **TRUE** if the device can perform tests; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ \_ ainda</span><span class="sxs-lookup"><span data-stu-id="4ad96-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI\_DGV\_GETDEVCAPS\_HAS\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-160">O membro **dwReturn** será definido como **true** se o dispositivo puder exibir imagens ainda; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-160">The **dwReturn** member is set to **TRUE** if the device can display still images; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ Max \_ Windows</span><span class="sxs-lookup"><span data-stu-id="4ad96-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI\_DGV\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-162">O membro **dwReturn** é definido como o número máximo de janelas que o dispositivo pode manipular simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="4ad96-162">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>\_ \_ taxa máxima de GETDEVCAPS DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MAXIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-164">O membro **dwReturn** é definido como a taxa máxima de reprodução para o dispositivo, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ad96-164">The **dwReturn** member is set to the maximum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>\_ \_ taxa mínima de GETDEVCAPS DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MINIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-166">O membro **dwReturn** é definido como a taxa de execução mínima para o dispositivo, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ad96-166">The **dwReturn** member is set to the minimum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ paletas MCI DGV GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI\_DGV\_GETDEVCAPS\_PALETTES</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-168">O membro **dwReturn** será definido como **true** se o dispositivo puder retornar um identificador de paleta; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-168">The **dwReturn** member is set to **TRUE** if the device can return a palette handle; otherwise, it is set to **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="4ad96-169">Os sinalizadores a seguir podem ser especificados no membro **dwItem** dos [**\_ \_ parâmetros MCI GETDEVCAPS**](mci-getdevcaps-parms.md) para o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="4ad96-169">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="4ad96-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>\_taxa de \_ \_ incremento do relógio do GETDEVCAPS MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI\_GETDEVCAPS\_CLOCK\_INCREMENT\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-171">O membro **dwReturn** é definido como o número de incrementos por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ad96-171">The **dwReturn** member is set to the number of increments per second.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ detectar \_ comprimento</span><span class="sxs-lookup"><span data-stu-id="4ad96-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_DETECT\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-173">O membro **dwReturn** será definido como **true** se o dispositivo for capaz de detectar o tamanho da mídia; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-173">The **dwReturn** member is set to **TRUE** if the device is capable of detecting the length of the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ congelar</span><span class="sxs-lookup"><span data-stu-id="4ad96-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-175">O membro **dwReturn** será definido como **true** se o dispositivo for capaz de congelar a imagem de saída; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-175">The **dwReturn** member is set to **TRUE** if the device is capable of freezing the output image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ monitorar \_ fontes</span><span class="sxs-lookup"><span data-stu-id="4ad96-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_MONITOR\_SOURCES</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-177">O membro **dwReturn** será definido como **true** se o dispositivo for capaz de monitorar fontes; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-177">The **dwReturn** member is set to **TRUE** if the device is capable of monitoring sources; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode ser \_ prevertido</span><span class="sxs-lookup"><span data-stu-id="4ad96-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-179">O membro **dwReturn** será definido como **true** se o dispositivo puder ser prevertido; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-179">The **dwReturn** member is set to **TRUE** if the device is capable of preroll; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode ser \_ visualizado</span><span class="sxs-lookup"><span data-stu-id="4ad96-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREVIEW</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-181">O membro **dwReturn** será definido como **true** se o dispositivo for capaz de visualizações; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-181">The **dwReturn** member is set to **TRUE** if the device is capable of previews; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ reverter</span><span class="sxs-lookup"><span data-stu-id="4ad96-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-183">O membro **dwReturn** será definido como **true** se o dispositivo for capaz de reproduzir em ordem inversa; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-183">The **dwReturn** member is set to **TRUE** if the device is capable of playing in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ testar</span><span class="sxs-lookup"><span data-stu-id="4ad96-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-185">O membro **dwReturn** será definido como **true** se o dispositivo for capaz de testar; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-185">The **dwReturn** member is set to **TRUE** if the device is capable of testing; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ tem \_ relógio</span><span class="sxs-lookup"><span data-stu-id="4ad96-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-187">O membro **dwReturn** será definido como **true** se o dispositivo der suporte a um relógio externo; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-187">The **dwReturn** member is set to **TRUE** if the device supports an external clock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>o \_ GETDEVCAPS de videocassete do MCI \_ tem um \_ \_ código de meio</span><span class="sxs-lookup"><span data-stu-id="4ad96-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-189">O membro **dwReturn** será definido como **true** se o dispositivo tiver a capacidade de código de paficação ou se esse recurso for desconhecido; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-189">The **dwReturn** member is set to **TRUE** if device has timecode capability or if this capability is unknown; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_ \_ \_ número \_ de marcas do GETDEVCAPS do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI\_VCR\_GETDEVCAPS\_NUMBER\_OF\_MARKS</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-191">O membro **dwReturn** é definido como o número de marcas (99).</span><span class="sxs-lookup"><span data-stu-id="4ad96-191">The **dwReturn** member is set to the number of marks (99).</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>\_precisão de \_ busca do GETDEVCAPS VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI\_VCR\_GETDEVCAPS\_SEEK\_ACCURACY</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-193">O membro **dwReturn** é definido como a precisão de busca do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ad96-193">The **dwReturn** member is set to the seek accuracy of the device.</span></span>

</dd> </dl>

<span data-ttu-id="4ad96-194">Os sinalizadores a seguir podem ser especificados no membro **dwItem** dos [**\_ \_ parâmetros MCI GETDEVCAPS**](mci-getdevcaps-parms.md) para o tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="4ad96-194">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="4ad96-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>\_GETDEVCAPS MCI \_ OVLY \_ pode \_ congelar</span><span class="sxs-lookup"><span data-stu-id="4ad96-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-196">O membro **dwReturn** será definido como **true** se o dispositivo puder congelar a imagem; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-196">The **dwReturn** member is set to **TRUE** if the device can freeze the image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>\_GETDEVCAPS MCI \_ OVLY \_ pode \_ alongar</span><span class="sxs-lookup"><span data-stu-id="4ad96-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-198">O membro **dwReturn** será definido como **true** se o dispositivo puder alongar a imagem para preencher o quadro; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-198">The **dwReturn** member is set to **TRUE** if the device can stretch the image to fill the frame; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ Max \_ Windows</span><span class="sxs-lookup"><span data-stu-id="4ad96-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI\_OVLY\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-200">O membro **dwReturn** é definido como o número máximo de janelas que o dispositivo pode manipular simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="4ad96-200">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> </dl>

<span data-ttu-id="4ad96-201">Os sinalizadores a seguir podem ser especificados no membro **dwItem** do [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para o tipo de dispositivo **VIDEODISC** :</span><span class="sxs-lookup"><span data-stu-id="4ad96-201">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="4ad96-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>o MCI de \_ VD \_ GETDEVCAPS \_ pode \_ reverter</span><span class="sxs-lookup"><span data-stu-id="4ad96-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI\_VD\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-203">O membro **dwReturn** será definido como **true** se o player do VIDEODISC puder reproduzir em ordem inversa; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="4ad96-203">The **dwReturn** member is set to **TRUE** if the videodisc player can play in reverse; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="4ad96-204">Alguns jogadores podem reproduzir discos CLV em discos inversos e CAV.</span><span class="sxs-lookup"><span data-stu-id="4ad96-204">Some players can play CLV discs in reverse as well as CAV discs.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>\_cav de VD \_ GETDEVCAPS \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ad96-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI\_VD\_GETDEVCAPS\_CAV</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-206">Quando combinado com outros itens, especifica que as informações de retorno se aplicam ao formato CAV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="4ad96-206">When combined with other items, specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="4ad96-207">Esse será o padrão se nenhum VIDEODISC for inserido.</span><span class="sxs-lookup"><span data-stu-id="4ad96-207">This is the default if no videodisc is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>\_CLV de VD \_ GETDEVCAPS \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4ad96-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI\_VD\_GETDEVCAPS\_CLV</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-209">Quando combinado com outros itens, especifica que as informações de retorno se aplicam ao formato CLV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="4ad96-209">When combined with other items, specifies that the return information applies to CLV format videodiscs.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ \_ taxa rápida de VD GETDEVCAPS do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI\_VD\_GETDEVCAPS\_FAST\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-211">O membro **dwReturn** é definido como a taxa de reprodução rápida padrão em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ad96-211">The **dwReturn** member is set to the standard fast play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>\_ \_ \_ taxa normal de VD GETDEVCAPS do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI\_VD\_GETDEVCAPS\_NORMAL\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-213">O membro **dwReturn** é definido como a taxa de reprodução normal em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ad96-213">The **dwReturn** member is set to the normal play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>\_ \_ taxa lenta de GETDEVCAPS de VD do \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI\_VD\_GETDEVCAPS\_SLOW\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-215">O membro **dwReturn** é definido como a taxa de reprodução lenta padrão em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ad96-215">The **dwReturn** member is set to the standard slow play rate in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="4ad96-216">Os sinalizadores a seguir podem ser especificados no membro **dwItem** do [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para o tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="4ad96-216">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="4ad96-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_ \_ entrada GETDEVCAPS do Wave MCI \_</span><span class="sxs-lookup"><span data-stu-id="4ad96-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI\_WAVE\_GETDEVCAPS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-218">O membro **dwReturn** é definido como o número total de dispositivos de entrada de onda (gravação).</span><span class="sxs-lookup"><span data-stu-id="4ad96-218">The **dwReturn** member is set to the total number of waveform input (recording) devices.</span></span>

</dd> <dt>

<span data-ttu-id="4ad96-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>\_saída do \_ GETDEVCAPS \_ Wave MCI</span><span class="sxs-lookup"><span data-stu-id="4ad96-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI\_WAVE\_GETDEVCAPS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="4ad96-220">O membro **dwReturn** é definido como o número total de dispositivos de saída de onda (reprodução).</span><span class="sxs-lookup"><span data-stu-id="4ad96-220">The **dwReturn** member is set to the total number of waveform output (playback) devices.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ad96-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ad96-221">Requirements</span></span>



| <span data-ttu-id="4ad96-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ad96-222">Requirement</span></span> | <span data-ttu-id="4ad96-223">Valor</span><span class="sxs-lookup"><span data-stu-id="4ad96-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad96-224">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ad96-224">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad96-225">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ad96-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4ad96-226">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ad96-226">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad96-227">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ad96-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4ad96-228">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4ad96-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ad96-229"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ad96-229"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ad96-230">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ad96-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad96-231">MCI</span><span class="sxs-lookup"><span data-stu-id="4ad96-231">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4ad96-232">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="4ad96-232">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

