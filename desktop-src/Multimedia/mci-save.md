---
title: MCI_SAVE comando (mmsystem. h)
description: O comando de salvamento do MCI \_ salva o arquivo atual.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- Multimídia do Windows de comando MCI_SAVE
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454805"
---
# <a name="mci_save-command"></a><span data-ttu-id="88e4f-104">Comando de salvamento do MCI \_</span><span class="sxs-lookup"><span data-stu-id="88e4f-104">MCI\_SAVE command</span></span>

<span data-ttu-id="88e4f-105">O comando de salvamento do MCI \_ salva o arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="88e4f-105">The MCI\_SAVE command saves the current file.</span></span> <span data-ttu-id="88e4f-106">Dispositivos que modificam arquivos não devem destruir a cópia original até receberem a mensagem de salvamento.</span><span class="sxs-lookup"><span data-stu-id="88e4f-106">Devices that modify files should not destroy the original copy until they receive the save message.</span></span> <span data-ttu-id="88e4f-107">Os dispositivos de sobreposição de vídeo e Wave-Audio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="88e4f-107">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="88e4f-108">Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.</span><span class="sxs-lookup"><span data-stu-id="88e4f-108">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="88e4f-109">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="88e4f-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
);
```



## <a name="parameters"></a><span data-ttu-id="88e4f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88e4f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88e4f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="88e4f-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="88e4f-112">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="88e4f-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="88e4f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="88e4f-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="88e4f-114">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="88e4f-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="88e4f-115">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="88e4f-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="88e4f-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span><span class="sxs-lookup"><span data-stu-id="88e4f-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span></span>
</dt> <dd>

<span data-ttu-id="88e4f-117">Ponteiro para uma estrutura de [**\_ \_ parâmetros de salvamento MCI**](mci-save-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="88e4f-117">Pointer to an [**MCI\_SAVE\_PARMS**](mci-save-parms.md) structure.</span></span> <span data-ttu-id="88e4f-118">(Dispositivos com parâmetros adicionais podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="88e4f-118">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88e4f-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="88e4f-119">Return Value</span></span>

<span data-ttu-id="88e4f-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="88e4f-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="88e4f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="88e4f-121">Remarks</span></span>

<span data-ttu-id="88e4f-122">Esse comando tem suporte em dispositivos que retornam **true** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o \_ GETDEVCAPS MCI que \_ pode \_ salvar o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="88e4f-122">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_SAVE flag.</span></span>

<span data-ttu-id="88e4f-123">O seguinte sinalizador adicional se aplica a todos os dispositivos que dão suporte ao [ \_ salvamento de MCI](/windows):</span><span class="sxs-lookup"><span data-stu-id="88e4f-123">The following additional flag applies to all devices supporting [MCI\_SAVE](/windows):</span></span>

<dl> <dt>

<span data-ttu-id="88e4f-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_arquivo de salvamento de MCI \_</span><span class="sxs-lookup"><span data-stu-id="88e4f-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI\_SAVE\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="88e4f-125">O membro **lpFileName** da estrutura identificada por *lpSave* contém um endereço de um buffer que contém o nome de arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="88e4f-125">The **lpfilename** member of the structure identified by *lpSave* contains an address of a buffer containing the destination filename.</span></span>

</dd> </dl>

<span data-ttu-id="88e4f-126">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="88e4f-126">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="88e4f-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="88e4f-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="88e4f-128">O membro **RC** da estrutura identificada por *lpSave* contém um retângulo válido.</span><span class="sxs-lookup"><span data-stu-id="88e4f-128">The **rc** member of the structure identified by *lpSave* contains a valid rectangle.</span></span> <span data-ttu-id="88e4f-129">O retângulo especifica uma região do buffer de quadro que será salva no arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="88e4f-129">The rectangle specifies a region of the frame buffer that will be saved to the specified file.</span></span> <span data-ttu-id="88e4f-130">O primeiro par de coordenadas especifica o canto superior esquerdo do retângulo; o segundo par especifica a largura e a altura.</span><span class="sxs-lookup"><span data-stu-id="88e4f-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="88e4f-131">Dispositivos de vídeo digital devem usar o comando [MCI \_ Capture](mci-capture.md) para capturar o conteúdo do buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="88e4f-131">Digital-video devices must use the [MCI\_CAPTURE](mci-capture.md) command to capture the contents of the frame buffer.</span></span> <span data-ttu-id="88e4f-132">(Os dispositivos de sobreposição de vídeo também devem usar o MCI \_ CAPTURA.) Esse sinalizador é para compatibilidade com o conjunto de comandos de sobreposição de vídeo MCI existente.</span><span class="sxs-lookup"><span data-stu-id="88e4f-132">(Video-overlay devices should also use MCI\_CAPTURE.) This flag is for compatibility with the existing MCI video-overlay command set.</span></span>

</dd> <dt>

<span data-ttu-id="88e4f-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_ \_ anular salvamento de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="88e4f-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI\_DGV\_SAVE\_ABORT</span></span>
</dt> <dd>

<span data-ttu-id="88e4f-134">Interrompe uma operação de salvamento em andamento.</span><span class="sxs-lookup"><span data-stu-id="88e4f-134">Stops a save operation in progress.</span></span> <span data-ttu-id="88e4f-135">Esse deve ser o único sinalizador presente.</span><span class="sxs-lookup"><span data-stu-id="88e4f-135">This must be the only flag present.</span></span>

</dd> <dt>

<span data-ttu-id="88e4f-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ Salvar \_ KEEPRESERVE</span><span class="sxs-lookup"><span data-stu-id="88e4f-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI\_DGV\_SAVE\_KEEPRESERVE</span></span>
</dt> <dd>

<span data-ttu-id="88e4f-137">O espaço em disco não utilizado saiu do comando [de \_ reserva do MCI](mci-reserve.md) original não é desalocado.</span><span class="sxs-lookup"><span data-stu-id="88e4f-137">Unused disk space left over from the original [MCI\_RESERVE](mci-reserve.md) command is not deallocated.</span></span>

</dd> </dl>

<span data-ttu-id="88e4f-138">Para dispositivos de vídeo digital, o parâmetro *lpSave* aponta para uma estrutura de parâmetros de [**salvamento de \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="88e4f-138">For digital-video devices, the *lpSave* parameter points to an [**MCI\_DGV\_SAVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) structure.</span></span>

<span data-ttu-id="88e4f-139">O seguinte sinalizador adicional é usado com o tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="88e4f-139">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="88e4f-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="88e4f-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="88e4f-141">O membro **RC** da estrutura identificada por *lpSave* contém um retângulo de exibição válido que indica a área do buffer de vídeo a ser salva.</span><span class="sxs-lookup"><span data-stu-id="88e4f-141">The **rc** member of the structure identified by *lpSave* contains a valid display rectangle indicating the area of the video buffer to save.</span></span>

</dd> </dl>

<span data-ttu-id="88e4f-142">Para dispositivos de sobreposição de vídeo, o parâmetro *lpSave* aponta para uma estrutura de [**parâmetros de \_ \_ salvamento \_ de OVLY MCI**](/previous-versions//dd743447(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="88e4f-142">For video-overlay devices, the *lpSave* parameter points to an [**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e4f-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88e4f-143">Requirements</span></span>



| <span data-ttu-id="88e4f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="88e4f-144">Requirement</span></span> | <span data-ttu-id="88e4f-145">Valor</span><span class="sxs-lookup"><span data-stu-id="88e4f-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e4f-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88e4f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="88e4f-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88e4f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="88e4f-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88e4f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="88e4f-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88e4f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="88e4f-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="88e4f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="88e4f-151"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88e4f-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e4f-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="88e4f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e4f-153">MCI</span><span class="sxs-lookup"><span data-stu-id="88e4f-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="88e4f-154">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="88e4f-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

