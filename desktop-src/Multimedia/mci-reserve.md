---
title: MCI_RESERVE comando (mmsystem. h)
description: O comando de reserva do MCI \_ aloca espaço em disco contíguo para o espaço de trabalho da instância de driver de dispositivo para uso com a gravação subsequente. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- Multimídia do Windows de comando MCI_RESERVE
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918915"
---
# <a name="mci_reserve-command"></a><span data-ttu-id="5e853-105">Comando de reserva do MCI \_</span><span class="sxs-lookup"><span data-stu-id="5e853-105">MCI\_RESERVE command</span></span>

<span data-ttu-id="5e853-106">O comando de reserva do MCI \_ aloca espaço em disco contíguo para o espaço de trabalho da instância de driver de dispositivo para uso com a gravação subsequente.</span><span class="sxs-lookup"><span data-stu-id="5e853-106">The MCI\_RESERVE command allocates contiguous disk space for the workspace of the device driver instance for use with subsequent recording.</span></span> <span data-ttu-id="5e853-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="5e853-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="5e853-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e853-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
);
```



## <a name="parameters"></a><span data-ttu-id="5e853-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e853-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e853-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5e853-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5e853-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="5e853-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5e853-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5e853-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5e853-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="5e853-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="5e853-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5e853-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e853-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span><span class="sxs-lookup"><span data-stu-id="5e853-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span></span>
</dt> <dd>

<span data-ttu-id="5e853-116">Ponteiro para uma estrutura de [**\_ parâmetros de \_ reserva \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="5e853-116">Pointer to an [**MCI\_DGV\_RESERVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e853-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5e853-117">Return Value</span></span>

<span data-ttu-id="5e853-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="5e853-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e853-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e853-119">Remarks</span></span>

<span data-ttu-id="5e853-120">Se o espaço de trabalho contiver dados não salvos, esses dados serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="5e853-120">If the workspace contains unsaved data, this data is lost.</span></span> <span data-ttu-id="5e853-121">Se o espaço em disco não for reservado antes da gravação, o comando de [ \_ registro MCI](mci-record.md) executará uma reserva implícita com parâmetros padrão específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e853-121">If disk space is not reserved prior to recording, the [MCI\_RECORD](mci-record.md) command performs an implied reserve with device-specific default parameters.</span></span> <span data-ttu-id="5e853-122">Em algumas implementações, a reserva não é necessária e pode ser ignorada pelo driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e853-122">On some implementations, reserve is not required and might be ignored by the device driver.</span></span> <span data-ttu-id="5e853-123">Reservar espaço explicitamente proporciona a você um melhor controle sobre quando o atraso de alocação de disco ocorre, quanto espaço é alocado e onde o espaço em disco é alocado.</span><span class="sxs-lookup"><span data-stu-id="5e853-123">Explicitly reserving space gives you better control over when the delay for disk allocation occurs, how much space is allocated, and where the disk space is allocated.</span></span> <span data-ttu-id="5e853-124">A quantidade e o local do espaço em disco já reservados para esta instância de dispositivo podem ser alterados emitindo \_ novamente a reserva MCI.</span><span class="sxs-lookup"><span data-stu-id="5e853-124">The amount and location of disk space already reserved for this device instance can be changed by issuing MCI\_RESERVE again.</span></span> <span data-ttu-id="5e853-125">Qualquer espaço em disco alocado e ainda não utilizado não será desalocado até que os dados gravados sejam salvos ou até que a instância do driver de dispositivo seja fechada.</span><span class="sxs-lookup"><span data-stu-id="5e853-125">Any allocated and still unused disk space is not deallocated until any recorded data is saved or until the device driver instance is closed.</span></span>

<span data-ttu-id="5e853-126">Se o vídeo for desativado com o \_ sinalizador MCI off do comando [de \_ vídeo MCI](mci-setvideo.md) , o espaço reservado não inclui nenhum vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e853-126">If video is turned off with the MCI\_OFF flag of the [MCI\_SETVIDEO](mci-setvideo.md) command, the space reserved does not include any video.</span></span> <span data-ttu-id="5e853-127">Se o áudio for desativado com o \_ sinalizador MCI off do comando [ \_ SetAudio do MCI](mci-setaudio.md) , o espaço reservado não incluirá nenhum áudio.</span><span class="sxs-lookup"><span data-stu-id="5e853-127">If audio is turned off with the MCI\_OFF flag of the [MCI\_SETAUDIO](mci-setaudio.md) command, the space reserved does not include any audio.</span></span> <span data-ttu-id="5e853-128">Se o áudio e o vídeo estiverem desligados ou se o tamanho solicitado for zero, nenhum espaço será reservado e qualquer espaço reservado existente será desalocado.</span><span class="sxs-lookup"><span data-stu-id="5e853-128">If both audio and video are turned off or if the requested size is zero, no space is reserved and any existing reserved space is deallocated.</span></span>

<span data-ttu-id="5e853-129">Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="5e853-129">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="5e853-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_ \_ reserva de DGV MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="5e853-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI\_DGV\_RESERVE\_IN</span></span>
</dt> <dd>

<span data-ttu-id="5e853-131">O membro **lpstrPath** da estrutura identificada por *lpReserve* contém um endereço de um buffer que contém o local de um arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="5e853-131">The **lpstrPath** member of the structure identified by *lpReserve* contains an address of a buffer containing the location of a temporary file.</span></span> <span data-ttu-id="5e853-132">O buffer contém apenas a unidade e o caminho de diretório do arquivo usado para armazenar dados gravados; o nome de arquivo é especificado pelo driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e853-132">The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.</span></span> <span data-ttu-id="5e853-133">Esse arquivo temporário é excluído quando a instância do dispositivo é fechada, a menos que seja salva explicitamente.</span><span class="sxs-lookup"><span data-stu-id="5e853-133">This temporary file is deleted when the device instance is closed unless it is explicitly saved.</span></span> <span data-ttu-id="5e853-134">Se esse sinalizador for omitido, o driver de dispositivo especificará onde o espaço em disco está alocado.</span><span class="sxs-lookup"><span data-stu-id="5e853-134">If this flag is omitted, the device driver specifies where disk space is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="5e853-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>\_tamanho de \_ reserva do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="5e853-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI\_DGV\_RESERVE\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="5e853-136">O membro **dwSize** da estrutura identificada por *lpReserve* especifica a quantidade aproximada de espaço em disco a ser reservada no espaço de trabalho para gravação.</span><span class="sxs-lookup"><span data-stu-id="5e853-136">The **dwSize** member of the structure identified by *lpReserve* specifies the approximate amount of disk space to reserve in the workspace for recording.</span></span> <span data-ttu-id="5e853-137">O valor é especificado no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="5e853-137">The value is specified in the current time format.</span></span> <span data-ttu-id="5e853-138">A quantidade de espaço em disco é estimada a partir da hora solicitada e de qual formato de arquivo e algoritmo de vídeo e áudio e os valores de qualidade estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="5e853-138">The amount of disk space is estimated from the requested time and from which file format and video and audio algorithm and quality values are in effect.</span></span> <span data-ttu-id="5e853-139">Se esse sinalizador for omitido, o driver de dispositivo poderá usar um valor padrão definido por ele.</span><span class="sxs-lookup"><span data-stu-id="5e853-139">If this flag is omitted, the device driver might use a default value it defines.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e853-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e853-140">Requirements</span></span>



| <span data-ttu-id="5e853-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e853-141">Requirement</span></span> | <span data-ttu-id="5e853-142">Valor</span><span class="sxs-lookup"><span data-stu-id="5e853-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e853-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e853-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5e853-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e853-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5e853-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e853-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5e853-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e853-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5e853-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5e853-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e853-148"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e853-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e853-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e853-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e853-150">MCI</span><span class="sxs-lookup"><span data-stu-id="5e853-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5e853-151">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="5e853-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

