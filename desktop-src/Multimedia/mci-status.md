---
title: MCI_STATUS comando (mmsystem. h)
description: O \_ comando status do MCI recupera informações sobre um dispositivo MCI. Todos os dispositivos reconhecem este comando. As informações são retornadas no membro dwReturn da estrutura identificada pelo parâmetro lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- Multimídia do Windows de comando MCI_STATUS
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "104297787"
---
# <a name="mci_status-command"></a><span data-ttu-id="4c142-106">Comando de status do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-106">MCI\_STATUS command</span></span>

> [!NOTE]
> <span data-ttu-id="4c142-107">Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.</span><span class="sxs-lookup"><span data-stu-id="4c142-107">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="4c142-108">Neste documento, há referências à palavra ' escravo '.</span><span class="sxs-lookup"><span data-stu-id="4c142-108">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="4c142-109">O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.</span><span class="sxs-lookup"><span data-stu-id="4c142-109">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="4c142-110">Essa palavra-chave é usada, pois é atualmente a palavra usada nos comandos.</span><span class="sxs-lookup"><span data-stu-id="4c142-110">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="4c142-111">Para fins de consistência, este documento contém esta palavra.</span><span class="sxs-lookup"><span data-stu-id="4c142-111">For consistency, this document contains this word.</span></span> <span data-ttu-id="4c142-112">Quando esta palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.</span><span class="sxs-lookup"><span data-stu-id="4c142-112">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="4c142-113">O \_ comando status do MCI recupera informações sobre um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="4c142-113">The MCI\_STATUS command retrieves information about an MCI device.</span></span> <span data-ttu-id="4c142-114">Todos os dispositivos reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="4c142-114">All devices recognize this command.</span></span> <span data-ttu-id="4c142-115">As informações são retornadas no membro **dwReturn** da estrutura identificada pelo parâmetro *lpStatus* .</span><span class="sxs-lookup"><span data-stu-id="4c142-115">Information is returned in the **dwReturn** member of the structure identified by the *lpStatus* parameter.</span></span>

<span data-ttu-id="4c142-116">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c142-116">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a><span data-ttu-id="4c142-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c142-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c142-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4c142-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4c142-119">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="4c142-119">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4c142-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4c142-121">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="4c142-121">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="4c142-122">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4c142-122">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c142-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span><span class="sxs-lookup"><span data-stu-id="4c142-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span></span>
</dt> <dd>

<span data-ttu-id="4c142-124">Ponteiro para uma estrutura de [**\_ \_ parâmetros de status MCI**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-124">Pointer to an [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure.</span></span> <span data-ttu-id="4c142-125">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="4c142-125">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c142-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4c142-126">Return Value</span></span>

<span data-ttu-id="4c142-127">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="4c142-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c142-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c142-128">Remarks</span></span>

<span data-ttu-id="4c142-129">Os seguintes sinalizadores padrão adicionais e específicos de comando se aplicam a todos os dispositivos que dão suporte ao status do MCI \_ :</span><span class="sxs-lookup"><span data-stu-id="4c142-129">The following additional standard and command-specific flags apply to all devices supporting MCI\_STATUS:</span></span>

<dl> <dt>

<span data-ttu-id="4c142-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_item de status MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI\_STATUS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="4c142-131">Especifica que o membro **dwItem** da estrutura identificada por *lpStatus* contém uma constante especificando qual item de status obter.</span><span class="sxs-lookup"><span data-stu-id="4c142-131">Specifies that the **dwItem** member of the structure identified by *lpStatus* contains a constant specifying which status item to obtain.</span></span> <span data-ttu-id="4c142-132">As constantes a seguir definem qual item de status deve ser retornado no membro **dwReturn** da estrutura:</span><span class="sxs-lookup"><span data-stu-id="4c142-132">The following constants define which status item to return in the **dwReturn** member of the structure:</span></span>

<span data-ttu-id="4c142-133">\_ \_ rastreamento atual do status do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-133">MCI\_STATUS\_CURRENT\_TRACK</span></span>

<span data-ttu-id="4c142-134">O membro **dwReturn** é definido como o número de faixa atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-134">The **dwReturn** member is set to the current track number.</span></span> <span data-ttu-id="4c142-135">O MCI usa números de faixa contínuos.</span><span class="sxs-lookup"><span data-stu-id="4c142-135">MCI uses continuous track numbers.</span></span>

<span data-ttu-id="4c142-136">\_comprimento do status MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-136">MCI\_STATUS\_LENGTH</span></span>

<span data-ttu-id="4c142-137">O membro **dwReturn** é definido como o comprimento total da mídia.</span><span class="sxs-lookup"><span data-stu-id="4c142-137">The **dwReturn** member is set to the total media length.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modo de status MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-139">O membro **dwReturn** é definido como o modo atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c142-139">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="4c142-140">Os modos incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4c142-140">The modes include the following:</span></span>

-   <span data-ttu-id="4c142-141">\_modo MCI \_ não \_ está pronto</span><span class="sxs-lookup"><span data-stu-id="4c142-141">MCI\_MODE\_NOT\_READY</span></span>
-   <span data-ttu-id="4c142-142">\_pausa no modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-142">MCI\_MODE\_PAUSE</span></span>
-   <span data-ttu-id="4c142-143">\_reprodução do modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-143">MCI\_MODE\_PLAY</span></span>
-   <span data-ttu-id="4c142-144">\_parada do modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-144">MCI\_MODE\_STOP</span></span>
-   <span data-ttu-id="4c142-145">\_modo MCI \_ aberto</span><span class="sxs-lookup"><span data-stu-id="4c142-145">MCI\_MODE\_OPEN</span></span>
-   <span data-ttu-id="4c142-146">\_registro do modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-146">MCI\_MODE\_RECORD</span></span>
-   <span data-ttu-id="4c142-147">\_modo MCI \_ Seek</span><span class="sxs-lookup"><span data-stu-id="4c142-147">MCI\_MODE\_SEEK</span></span>

</dd> <dt>

<span data-ttu-id="4c142-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_status \_ do MCI número \_ de \_ faixas</span><span class="sxs-lookup"><span data-stu-id="4c142-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI\_STATUS\_NUMBER\_OF\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="4c142-149">O membro **dwReturn** é definido como o número total de faixas reproduzidas.</span><span class="sxs-lookup"><span data-stu-id="4c142-149">The **dwReturn** member is set to the total number of playable tracks.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>\_posição do status do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI\_STATUS\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="4c142-151">O membro **dwReturn** é definido como a posição atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-151">The **dwReturn** member is set to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>STATUS do MCI \_ \_ pronto</span><span class="sxs-lookup"><span data-stu-id="4c142-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI\_STATUS\_READY</span></span>
</dt> <dd>

<span data-ttu-id="4c142-153">O membro **dwReturn** será definido como **true** se o dispositivo estiver pronto; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-153">The **dwReturn** member is set to **TRUE** if the device is ready; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>\_formato de \_ tempo de status do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI\_STATUS\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-155">O membro **dwReturn** é definido como o formato de hora atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c142-155">The **dwReturn** member is set to the current time format of the device.</span></span> <span data-ttu-id="4c142-156">Os formatos de hora incluem:</span><span class="sxs-lookup"><span data-stu-id="4c142-156">The time formats include:</span></span>

-   <span data-ttu-id="4c142-157">\_bytes de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-157">MCI\_FORMAT\_BYTES</span></span>
-   <span data-ttu-id="4c142-158">\_quadros de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-158">MCI\_FORMAT\_FRAMES</span></span>
-   <span data-ttu-id="4c142-159">\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="4c142-159">MCI\_FORMAT\_HMS</span></span>
-   <span data-ttu-id="4c142-160">\_milissegundos do formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-160">MCI\_FORMAT\_MILLISECONDS</span></span>
-   <span data-ttu-id="4c142-161">\_formato MCI \_ MSF</span><span class="sxs-lookup"><span data-stu-id="4c142-161">MCI\_FORMAT\_MSF</span></span>
-   <span data-ttu-id="4c142-162">\_exemplos de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-162">MCI\_FORMAT\_SAMPLES</span></span>
-   <span data-ttu-id="4c142-163">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="4c142-163">MCI\_FORMAT\_TMSF</span></span>

</dd> <dt>

<span data-ttu-id="4c142-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>\_início do status do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI\_STATUS\_START</span></span>
</dt> <dd>

<span data-ttu-id="4c142-165">Obtém a posição inicial da mídia.</span><span class="sxs-lookup"><span data-stu-id="4c142-165">Obtains the starting position of the media.</span></span> <span data-ttu-id="4c142-166">Para obter a posição inicial, combine esse sinalizador com \_ o item de status MCI \_ e defina o membro **dwItem** da estrutura identificada por *lpStatus* para a posição do \_ status MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="4c142-166">To get the starting position, combine this flag with MCI\_STATUS\_ITEM and set the **dwItem** member of the structure identified by *lpStatus* to MCI\_STATUS\_POSITION.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>\_faixa MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="4c142-168">Indica que um parâmetro de faixa de status está incluído no membro **dwTrack** da estrutura identificada por *lpStatus*.</span><span class="sxs-lookup"><span data-stu-id="4c142-168">Indicates a status track parameter is included in the **dwTrack** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="4c142-169">Você deve usar esse sinalizador com a posição do status do MCI ou com as \_ \_ constantes de comprimento do status do MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4c142-169">You must use this flag with the MCI\_STATUS\_POSITION or MCI\_STATUS\_LENGTH constants.</span></span> <span data-ttu-id="4c142-170">Quando usado com a \_ \_ posição do status MCI, \_ a faixa MCI Obtém a posição inicial da faixa especificada. Quando usado com o \_ \_ comprimento do status MCI, \_ a faixa MCI Obtém o comprimento da faixa especificada. O MCI usa números de faixa contínuos.</span><span class="sxs-lookup"><span data-stu-id="4c142-170">When used with MCI\_STATUS\_POSITION, MCI\_TRACK obtains the starting position of the specified track. When used with MCI\_STATUS\_LENGTH, MCI\_TRACK obtains the length of the specified track. MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="4c142-171">Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **cdaudio** .</span><span class="sxs-lookup"><span data-stu-id="4c142-171">The following additional flags are used with the **cdaudio** device type.</span></span> <span data-ttu-id="4c142-172">Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c142-172">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="4c142-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_faixa de \_ tipo de status \_ \_ do MCI CDA</span><span class="sxs-lookup"><span data-stu-id="4c142-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI\_CDA\_STATUS\_TYPE\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="4c142-174">O membro **dwReturn** é definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4c142-174">The **dwReturn** member is set to one of the following values:</span></span>

-   <span data-ttu-id="4c142-175">áudio de controle do MCI \_ CDA \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-175">MCI\_CDA\_TRACK\_AUDIO</span></span>
-   <span data-ttu-id="4c142-176">\_ \_ outro controle do MCI CDA \_</span><span class="sxs-lookup"><span data-stu-id="4c142-176">MCI\_CDA\_TRACK\_OTHER</span></span>

<span data-ttu-id="4c142-177">Para usar esse sinalizador, o \_ sinalizador de faixa MCI deve ser definido e o membro **dwTrack** da estrutura identificada por *lpStatus* deve conter um número de faixa válido.</span><span class="sxs-lookup"><span data-stu-id="4c142-177">To use this flag, the MCI\_TRACK flag must be set, and the **dwTrack** member of the structure identified by *lpStatus* must contain a valid track number.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="4c142-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-179">O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-179">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="4c142-180">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="4c142-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="4c142-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>espaço em disco de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI\_DGV\_STATUS\_DISKSPACE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-182">O membro **lpstrDrive** da estrutura identificada por *lpStatus* especifica uma unidade de disco ou, em algumas implementações, um caminho.</span><span class="sxs-lookup"><span data-stu-id="4c142-182">The **lpstrDrive** member of the structure identified by *lpStatus* specifies a disk drive or, in some implementations, a path.</span></span> <span data-ttu-id="4c142-183">O \_ comando status do MCI retorna a quantidade aproximada de espaço em disco que pode ser obtida pelo comando de [ \_ reserva do MCI](mci-reserve.md) no membro **dwReturn** da estrutura identificada por *lpStatus*.</span><span class="sxs-lookup"><span data-stu-id="4c142-183">The MCI\_STATUS command returns the approximate amount of disk space that could be obtained by the [MCI\_RESERVE](mci-reserve.md) command in the **dwReturn** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="4c142-184">O espaço em disco é medido em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-184">The disk space is measured in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_entrada de \_ status MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="4c142-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI\_DGV\_STATUS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-186">A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* se aplica à entrada.</span><span class="sxs-lookup"><span data-stu-id="4c142-186">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the input.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>\_status do DGV MCI \_ \_ restante</span><span class="sxs-lookup"><span data-stu-id="4c142-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI\_DGV\_STATUS\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-188">A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* se aplica ao canal de áudio à esquerda.</span><span class="sxs-lookup"><span data-stu-id="4c142-188">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>STATUS de DGV do MCI \_ \_ \_ nominal</span><span class="sxs-lookup"><span data-stu-id="4c142-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI\_DGV\_STATUS\_NOMINAL</span></span>
</dt> <dd>

<span data-ttu-id="4c142-190">A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* solicita o valor nominal em vez do valor atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-190">The constant specified by the **dwItem** member of the structure identified by *lpStatus* requests the nominal value rather than the current value.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>\_saída de \_ status de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI\_DGV\_STATUS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-192">A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* se aplica à saída.</span><span class="sxs-lookup"><span data-stu-id="4c142-192">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the output.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>\_registro de \_ status do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI\_DGV\_STATUS\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-194">A taxa de quadros retornada para o \_ sinalizador de taxa de quadros do status do MCI DGV \_ \_ \_ é a taxa usada para compactação.</span><span class="sxs-lookup"><span data-stu-id="4c142-194">The frame rate returned for the MCI\_DGV\_STATUS\_FRAME\_RATE flag is the rate used for compression.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>referência de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI\_DGV\_STATUS\_REFERENCE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-196">O membro **dwReturn** da estrutura identificada por *lpStatus* retorna a imagem de quadro chave mais próxima que precede o quadro especificado no membro **dwReference** .</span><span class="sxs-lookup"><span data-stu-id="4c142-196">The **dwReturn** member of the structure identified by *lpStatus* returns the nearest key-frame image that precedes the frame specified in the **dwReference** member.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>\_status de DGV MCI \_ \_ direito</span><span class="sxs-lookup"><span data-stu-id="4c142-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI\_DGV\_STATUS\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-198">A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* se aplica ao canal de áudio correto.</span><span class="sxs-lookup"><span data-stu-id="4c142-198">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the right audio channel.</span></span>

</dd> </dl>

<span data-ttu-id="4c142-199">As constantes a seguir são usadas com o tipo de dispositivo **DigitalVideo** no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c142-199">The following constants are used with the **digitalvideo** device type in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="4c142-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>\_ \_ \_ quebras de áudio de status \_ do MCI avi</span><span class="sxs-lookup"><span data-stu-id="4c142-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI\_AVI\_STATUS\_AUDIO\_BREAKS</span></span>
</dt> <dd>

<span data-ttu-id="4c142-201">O membro **dwReturn** retorna o número de vezes que a parte de áudio da última sequência AVI se quebrou.</span><span class="sxs-lookup"><span data-stu-id="4c142-201">The **dwReturn** member returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="4c142-202">O sistema conta uma quebra de áudio sempre que tenta gravar dados de áudio no driver de dispositivo e descobre que o driver já reproduziu todos os dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4c142-202">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="4c142-203">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="4c142-203">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>quadros de status do MCI \_ AVI \_ \_ \_ ignorados</span><span class="sxs-lookup"><span data-stu-id="4c142-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI\_AVI\_STATUS\_FRAMES\_SKIPPED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-205">O membro **dwReturn** retorna o número de quadros que não foram desenhados quando a última sequência AVI foi reproduzida.</span><span class="sxs-lookup"><span data-stu-id="4c142-205">The **dwReturn** member returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="4c142-206">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="4c142-206">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>\_velocidade da \_ \_ última \_ reprodução \_ do status do MCI avi</span><span class="sxs-lookup"><span data-stu-id="4c142-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI\_AVI\_STATUS\_LAST\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-208">O membro **dwReturn** retorna um valor que representa a precisão da hora de execução real da última sequência AVI correspondente ao tempo de execução de destino.</span><span class="sxs-lookup"><span data-stu-id="4c142-208">The **dwReturn** member returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="4c142-209">O valor 1000 indica que a hora de destino e a hora real foram as mesmas.</span><span class="sxs-lookup"><span data-stu-id="4c142-209">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="4c142-210">Um valor de 2000, por exemplo, indicaria que a sequência AVI levou duas vezes mais tempo que deveria ter.</span><span class="sxs-lookup"><span data-stu-id="4c142-210">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="4c142-211">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="4c142-211">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>áudio de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI\_DGV\_STATUS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="4c142-213">O membro **dwReturn** retorna \_ o MCI ou o MCI, \_ dependendo da opção de áudio de conjunto MCI mais recente \_ \_ para o comando [ \_ set do MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-213">The **dwReturn** member returns MCI\_ON or MCI\_OFF depending on the most recent MCI\_SET\_AUDIO option for the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="4c142-214">Ele retornará \_ o MCI em se um ou ambos os alto-falantes estiverem habilitados e o MCI não estiver em \_ contrário.</span><span class="sxs-lookup"><span data-stu-id="4c142-214">It returns MCI\_ON if either or both speakers are enabled, and MCI\_OFF otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_entrada de \_ áudio de status MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI\_DGV\_STATUS\_AUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-216">O membro **dwReturn** retorna o nível de áudio instantâneo aproximado do sinal de áudio analógico.</span><span class="sxs-lookup"><span data-stu-id="4c142-216">The **dwReturn** member returns the approximate instantaneous audio level of the analog audio signal.</span></span> <span data-ttu-id="4c142-217">Um valor maior que 1000 implica que há distorção de recorte.</span><span class="sxs-lookup"><span data-stu-id="4c142-217">A value greater than 1000 implies there is clipping distortion.</span></span> <span data-ttu-id="4c142-218">Alguns dispositivos podem determinar esse valor somente durante a gravação de áudio.</span><span class="sxs-lookup"><span data-stu-id="4c142-218">Some devices can determine this value only while recording audio.</span></span> <span data-ttu-id="4c142-219">Esse valor de status não tem o comando **MCI \_ set** ou [MCI \_ SetAudio](mci-setaudio.md) associado.</span><span class="sxs-lookup"><span data-stu-id="4c142-219">This status value has no associated **MCI\_SET** or [MCI\_SETAUDIO](mci-setaudio.md) command.</span></span> <span data-ttu-id="4c142-220">Esse valor está relacionado a, mas normalizado de forma diferente do, o nível de status de onda MCI do comando Wave-Audio \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4c142-220">This value is related to, but normalized differently from, the waveform-audio command MCI\_WAVE\_STATUS\_LEVEL.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_registro de \_ áudio de status MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI\_DGV\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-222">O membro **dwReturn** retorna \_ o MCI ativado ou \_ o MCI, refletindo o estado definido pelo \_ \_ \_ sinalizador de gravação do DGV do MCI do comando do **MCI \_ SetAudio** .</span><span class="sxs-lookup"><span data-stu-id="4c142-222">The **dwReturn** member returns MCI\_ON or MCI\_OFF reflecting the state set by the MCI\_DGV\_SETAUDIO\_RECORD flag of the **MCI\_SETAUDIO** command.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_fonte de \_ áudio de status MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI\_DGV\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-224">O membro **dwReturn** retorna a fonte do digitalizador de áudio atual:</span><span class="sxs-lookup"><span data-stu-id="4c142-224">The **dwReturn** member returns the current audio digitizer source:</span></span>

</dd> <dt>

<span data-ttu-id="4c142-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>\_média de DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI\_DGV\_SETAUDIO\_AVERAGE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-226">Especifica a média dos canais de áudio esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="4c142-226">Specifies the average of the left and right audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ setáudio \_ esquerdo</span><span class="sxs-lookup"><span data-stu-id="4c142-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-228">Especifica o canal de áudio à esquerda.</span><span class="sxs-lookup"><span data-stu-id="4c142-228">Specifies the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>\_DGV de \_ som \_ do MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-230">Especifica o canal de áudio correto.</span><span class="sxs-lookup"><span data-stu-id="4c142-230">Specifies the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>\_estéreo de \_ áudio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI\_DGV\_SETAUDIO\_STEREO</span></span>
</dt> <dd>

<span data-ttu-id="4c142-232">Especifica o estéreo.</span><span class="sxs-lookup"><span data-stu-id="4c142-232">Specifies stereo.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_fluxo de \_ áudio de status MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI\_DGV\_STATUS\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="4c142-234">O membro **dwReturn** retorna o número de fluxo de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-234">The **dwReturn** member returns the current audio-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>AVGBYTESPERSEC de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI\_DGV\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="4c142-236">O membro **dwReturn** retorna o número médio de bytes por segundo usados para gravação.</span><span class="sxs-lookup"><span data-stu-id="4c142-236">The **dwReturn** member returns the average number of bytes per second used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>STATUS do MCI \_ DGV \_ \_ Bass</span><span class="sxs-lookup"><span data-stu-id="4c142-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI\_DGV\_STATUS\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="4c142-238">O membro **dwReturn** retorna o nível de sons de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-238">The **dwReturn** member returns the current audio bass level.</span></span> <span data-ttu-id="4c142-239">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-239">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>BITSPERPEL de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI\_DGV\_STATUS\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="4c142-241">O membro **dwReturn** retorna o número de bits por pixel usado para salvar dados capturados ou gravados.</span><span class="sxs-lookup"><span data-stu-id="4c142-241">The **dwReturn** member returns the number of bits per pixel used for saving captured or recorded data.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>BITSPERSAMPLE de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI\_DGV\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-243">O membro **dwReturn** retorna o número de bits por amostra que o dispositivo usa para gravação.</span><span class="sxs-lookup"><span data-stu-id="4c142-243">The **dwReturn** member returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="4c142-244">Isso se aplica somente a dispositivos que dão suporte ao formato PCM.</span><span class="sxs-lookup"><span data-stu-id="4c142-244">This applies only to devices supporting the PCM format.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>BLOCKALIGN de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI\_DGV\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="4c142-246">O membro **dwReturn** retorna o alinhamento dos blocos de dados em relação ao início da onda de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c142-246">The **dwReturn** member returns the alignment of data blocks relative to the start of the input waveform.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>brilho do status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI\_DGV\_STATUS\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="4c142-248">O membro **dwReturn** retorna o nível de brilho do vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-248">The **dwReturn** member returns the current video brightness level.</span></span> <span data-ttu-id="4c142-249">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-249">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>cor de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI\_DGV\_STATUS\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="4c142-251">O membro **dwReturn** retorna o nível de cor atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-251">The **dwReturn** member returns the current color level.</span></span> <span data-ttu-id="4c142-252">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-252">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>\_contraste de \_ status do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI\_DGV\_STATUS\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="4c142-254">O membro **dwReturn** retorna o nível de contraste atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-254">The **dwReturn** member returns the current contrast level.</span></span> <span data-ttu-id="4c142-255">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-255">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>\_formato de fileDGV de \_ status do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI\_DGV\_STATUS\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-257">O membro **dwReturn** retorna o formato de arquivo atual para gravação ou salvamento.</span><span class="sxs-lookup"><span data-stu-id="4c142-257">The **dwReturn** member returns the current file format for recording or saving.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_modo de \_ arquivo de status DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI\_DGV\_STATUS\_FILE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-259">O membro **dwReturn** retorna o estado da operação de arquivo:</span><span class="sxs-lookup"><span data-stu-id="4c142-259">The **dwReturn** member returns the state of the file operation:</span></span>

<span data-ttu-id="4c142-260">\_edição do \_ modo de arquivo MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-260">MCI\_DGV\_FILE\_MODE\_EDITING</span></span>

<span data-ttu-id="4c142-261">Retornado durante operações de recortar, copiar, excluir, colar e desfazer.</span><span class="sxs-lookup"><span data-stu-id="4c142-261">Returned during cut, copy, delete, paste, and undo operations.</span></span>

<span data-ttu-id="4c142-262">\_modo de \_ arquivo DGV MCI \_ \_ ocioso</span><span class="sxs-lookup"><span data-stu-id="4c142-262">MCI\_DGV\_FILE\_MODE\_IDLE</span></span>

<span data-ttu-id="4c142-263">Retornado quando o arquivo está pronto para a próxima operação.</span><span class="sxs-lookup"><span data-stu-id="4c142-263">Returned when the file is ready for the next operation.</span></span>

<span data-ttu-id="4c142-264">\_carregamento do \_ modo de arquivo DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-264">MCI\_DGV\_FILE\_MODE\_LOADING</span></span>

<span data-ttu-id="4c142-265">Retornado enquanto o arquivo está sendo carregado.</span><span class="sxs-lookup"><span data-stu-id="4c142-265">Returned while the file is being loaded.</span></span>

<span data-ttu-id="4c142-266">\_salvamento do \_ modo de arquivo DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-266">MCI\_DGV\_FILE\_MODE\_SAVING</span></span>

<span data-ttu-id="4c142-267">Retornado enquanto o arquivo está sendo salvo.</span><span class="sxs-lookup"><span data-stu-id="4c142-267">Returned while the file is being saved.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_conclusão do \_ arquivo de status DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI\_DGV\_STATUS\_FILE\_COMPLETION</span></span>
</dt> <dd>

<span data-ttu-id="4c142-269">O membro **dwReturn** retorna a porcentagem estimada em que uma operação de carregamento, gravação, captura, recorte, cópia, exclusão, colagem ou desfazer foi progredida.</span><span class="sxs-lookup"><span data-stu-id="4c142-269">The **dwReturn** member returns the estimated percentage a load, save, capture, cut, copy, delete, paste, or undo operation has progressed.</span></span> <span data-ttu-id="4c142-270">(Os aplicativos podem usar isso para fornecer um indicador visual de progresso.) Não há suporte para esse sinalizador em todos os dispositivos de vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="4c142-270">(Applications can use this to provide a visual indicator of progress.) This flag is not supported by all digital-video devices.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>\_ \_ encaminhamento de status DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI\_DGV\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-272">O membro **dwReturn** retornará **true** se a direção do dispositivo estiver encaminhada ou o dispositivo não estiver sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="4c142-272">The **dwReturn** member returns **TRUE** if the device direction is forward or the device is not playing.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_taxa de \_ quadros de status \_ \_ do MCI DGV</span><span class="sxs-lookup"><span data-stu-id="4c142-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI\_DGV\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-274">O membro **dwReturn** deve ser usado com o \_ status de DGV do MCI \_ \_ nominal, \_ \_ o registro de status do MCI DGV \_ ou ambos.</span><span class="sxs-lookup"><span data-stu-id="4c142-274">The **dwReturn** member must be used with MCI\_DGV\_STATUS\_NOMINAL, MCI\_DGV\_STATUS\_RECORD, or both.</span></span> <span data-ttu-id="4c142-275">Quando usado com o \_ registro de status MCI DGV \_ \_ , a taxa de quadros atual usada para gravação é retornada.</span><span class="sxs-lookup"><span data-stu-id="4c142-275">When used with MCI\_DGV\_STATUS\_RECORD, the current frame rate used for recording is returned.</span></span> <span data-ttu-id="4c142-276">Quando usado com \_ \_ o registro de status MCI DGV \_ e \_ status de DGV MCI \_ \_ nominal, a taxa de quadros nominal associada ao sinal de vídeo de entrada é retornada.</span><span class="sxs-lookup"><span data-stu-id="4c142-276">When used with both MCI\_DGV\_STATUS\_RECORD and MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the input video signal is returned.</span></span> <span data-ttu-id="4c142-277">Quando usado com \_ o status de DGV do MCI \_ \_ nominal, a taxa de quadros nominal associada ao arquivo é retornada.</span><span class="sxs-lookup"><span data-stu-id="4c142-277">When used with MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the file is returned.</span></span> <span data-ttu-id="4c142-278">Em todos os casos, as unidades estão em quadros por segundo multiplicadas por 1000.</span><span class="sxs-lookup"><span data-stu-id="4c142-278">In all cases the units are in frames per second multiplied by 1000.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>DGV do status do MCI \_ \_ \_ gama</span><span class="sxs-lookup"><span data-stu-id="4c142-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI\_DGV\_STATUS\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="4c142-280">O membro **dwReturn** retorna o valor de gama atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-280">The **dwReturn** member returns the current gamma value.</span></span> <span data-ttu-id="4c142-281">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-281">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>HPAL de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI\_DGV\_STATUS\_HPAL</span></span>
</dt> <dd>

<span data-ttu-id="4c142-283">O membro **dwReturn** retorna o valor decimal ASCII para o identificador de paleta atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-283">The **dwReturn** member returns the ASCII decimal value for the current palette handle.</span></span> <span data-ttu-id="4c142-284">O identificador está contido na palavra de ordem inferior do valor retornado.</span><span class="sxs-lookup"><span data-stu-id="4c142-284">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_HWND de \_ status \_ DGV do MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI\_DGV\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="4c142-286">O membro **dwReturn** retorna o valor decimal ASCII para o identificador de janela explícito ou padrão atual associado a esta instância de driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c142-286">The **dwReturn** member returns the ASCII decimal value for the current explicit or default window handle associated with this device driver instance.</span></span> <span data-ttu-id="4c142-287">O identificador está contido na palavra de ordem inferior do valor retornado.</span><span class="sxs-lookup"><span data-stu-id="4c142-287">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>\_cor da \_ chave de status \_ \_ do MCI DGV</span><span class="sxs-lookup"><span data-stu-id="4c142-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI\_DGV\_STATUS\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="4c142-289">O membro **dwReturn** retorna o valor de cor de chave atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-289">The **dwReturn** member returns the current key-color value.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>\_índice de \_ chave de status MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI\_DGV\_STATUS\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="4c142-291">O membro **dwReturn** retorna o valor de índice de chave atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-291">The **dwReturn** member returns the current key-index value.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_Monitor de \_ status do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI\_DGV\_STATUS\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="4c142-293">O membro **dwReturn** retorna uma constante que indica a origem da apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-293">The **dwReturn** member returns a constant indicating the source of the current presentation.</span></span> <span data-ttu-id="4c142-294">As seguintes constantes são definidas:</span><span class="sxs-lookup"><span data-stu-id="4c142-294">The following constants are defined:</span></span>

<span data-ttu-id="4c142-295">\_arquivo de \_ Monitor de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-295">MCI\_DGV\_MONITOR\_FILE</span></span>

<span data-ttu-id="4c142-296">Um arquivo é a origem.</span><span class="sxs-lookup"><span data-stu-id="4c142-296">A file is the source.</span></span>

<span data-ttu-id="4c142-297">\_entrada do \_ Monitor de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-297">MCI\_DGV\_MONITOR\_INPUT</span></span>

<span data-ttu-id="4c142-298">A entrada é a origem.</span><span class="sxs-lookup"><span data-stu-id="4c142-298">The input is the source.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_método de \_ Monitor de status DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI\_DGV\_STATUS\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-300">O membro **dwReturn** retorna uma constante indicando o método usado para o monitoramento de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c142-300">The **dwReturn** member returns a constant indicating the method used for input monitoring.</span></span> <span data-ttu-id="4c142-301">As seguintes constantes são definidas:</span><span class="sxs-lookup"><span data-stu-id="4c142-301">The following constants are defined:</span></span>

<span data-ttu-id="4c142-302">\_método MCI \_ DGV \_ direto</span><span class="sxs-lookup"><span data-stu-id="4c142-302">MCI\_DGV\_METHOD\_DIRECT</span></span>

<span data-ttu-id="4c142-303">Monitoramento de entrada direto.</span><span class="sxs-lookup"><span data-stu-id="4c142-303">Direct input monitoring.</span></span>

<span data-ttu-id="4c142-304">\_post do \_ método MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="4c142-304">MCI\_DGV\_METHOD\_POST</span></span>

<span data-ttu-id="4c142-305">Monitoramento de pós-entrada.</span><span class="sxs-lookup"><span data-stu-id="4c142-305">Post-input monitoring.</span></span>

<span data-ttu-id="4c142-306">\_método MCI \_ DGV \_ pre</span><span class="sxs-lookup"><span data-stu-id="4c142-306">MCI\_DGV\_METHOD\_PRE</span></span>

<span data-ttu-id="4c142-307">Monitoramento de pré-entrada.</span><span class="sxs-lookup"><span data-stu-id="4c142-307">Pre-input monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_modo de \_ pausa de status \_ \_ do MCI DGV</span><span class="sxs-lookup"><span data-stu-id="4c142-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI\_DGV\_STATUS\_PAUSE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-309">O membro **dwReturn** retorna o \_ modo MCI \_ Play se o dispositivo foi pausado durante a reprodução e \_ retorna \_ o registro do modo MCI se o dispositivo foi pausado durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="4c142-309">The **dwReturn** member returns MCI\_MODE\_PLAY if the device was paused while playing and returns MCI\_MODE\_RECORD if the device was paused while recording.</span></span> <span data-ttu-id="4c142-310">O comando retornará MCIERR \_ \_ função não aplicável como um erro retornado se o dispositivo não estiver em pausa.</span><span class="sxs-lookup"><span data-stu-id="4c142-310">The command returns MCIERR\_NONAPPLICABLE\_FUNCTION as an error return if the device is not paused.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>SAMPLESPERSECOND de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI\_DGV\_STATUS\_SAMPLESPERSECOND</span></span>
</dt> <dd>

<span data-ttu-id="4c142-312">O membro **dwReturn** retorna o número de amostras por segundo registradas.</span><span class="sxs-lookup"><span data-stu-id="4c142-312">The **dwReturn** member returns the number of samples per second recorded.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>STATUS do MCI \_ DGV \_ \_ Seek \_ exactly</span><span class="sxs-lookup"><span data-stu-id="4c142-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI\_DGV\_STATUS\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="4c142-314">O membro **dwReturn** retorna **true** ou **false** indicando se o formato de busca exata está definido ou não.</span><span class="sxs-lookup"><span data-stu-id="4c142-314">The **dwReturn** member returns **TRUE** or **FALSE** indicating whether or not the seek exactly format is set.</span></span> <span data-ttu-id="4c142-315">(Os aplicativos podem definir esse formato usando o comando [MCI \_ set](mci-set.md) com o \_ sinalizador MCI DGV \_ set \_ Seek \_ Exact.)</span><span class="sxs-lookup"><span data-stu-id="4c142-315">(Applications can set this format by using the [MCI\_SET](mci-set.md) command with the MCI\_DGV\_SET\_SEEK\_EXACTLY flag.)</span></span>

</dd> <dt>

<span data-ttu-id="4c142-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_nitidez do \_ status do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI\_DGV\_STATUS\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="4c142-317">O membro **dwReturn** retorna o nível de nitidez atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-317">The **dwReturn** member returns the current sharpness level.</span></span> <span data-ttu-id="4c142-318">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-318">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>\_tamanho do \_ status do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI\_DGV\_STATUS\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-320">O membro **dwReturn** retorna a duração de reprodução aproximada dos dados compactados que o espaço de trabalho reservado irá manter.</span><span class="sxs-lookup"><span data-stu-id="4c142-320">The **dwReturn** member returns the approximate playback duration of compressed data that the reserved workspace will hold.</span></span> <span data-ttu-id="4c142-321">As unidades de duração estão no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-321">The duration units are in the current time format.</span></span> <span data-ttu-id="4c142-322">Ele retornará zero se não houver espaço reservado em disco.</span><span class="sxs-lookup"><span data-stu-id="4c142-322">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="4c142-323">O tamanho retornado é aproximado, pois o espaço em disco preciso para dados compactados não pode, em geral, ser previsto até que os dados tenham sido compactados.</span><span class="sxs-lookup"><span data-stu-id="4c142-323">The size returned is approximate since the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>STATUS do MCI \_ DGV \_ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="4c142-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI\_DGV\_STATUS\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-325">O membro **dwReturn** retorna o código de tempo SMPTE associado à posição atual no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4c142-325">The **dwReturn** member returns the SMPTE time code associated with the current position in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>\_velocidade de \_ status do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI\_DGV\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-327">O membro **dwReturn** retorna a velocidade de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-327">The **dwReturn** member returns the current playback speed.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>o \_ status do MCI DGV \_ ainda é \_ \_ FileFormat</span><span class="sxs-lookup"><span data-stu-id="4c142-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI\_DGV\_STATUS\_STILL\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-329">O membro **dwReturn** retorna o formato de arquivo atual para o comando de [ \_ captura MCI](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-329">The **dwReturn** member returns the current file format for the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_tonalidade de \_ status MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="4c142-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI\_DGV\_STATUS\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-331">O membro **dwReturn** retorna o nível de tonalidade de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-331">The **dwReturn** member returns the current video tint level.</span></span> <span data-ttu-id="4c142-332">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-332">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>STATUS do MCI \_ DGV \_ \_ agudo</span><span class="sxs-lookup"><span data-stu-id="4c142-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI\_DGV\_STATUS\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-334">O membro **dwReturn** retorna o nível de agudos de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-334">The **dwReturn** member returns the current audio treble level.</span></span> <span data-ttu-id="4c142-335">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-335">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>\_status de DGV MCI \_ \_ não salvo</span><span class="sxs-lookup"><span data-stu-id="4c142-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI\_DGV\_STATUS\_UNSAVED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-337">O membro **dwReturn** retornará **true** se houver dados gravados no espaço de trabalho que podem ser perdidos como resultado de um [ \_ fechamento MCI](mci-close.md), [ \_ carregamento de MCI](mci-load.md), [ \_ registro MCI](mci-record.md), [ \_ reserva de MCI](mci-reserve.md), [ \_ recorte de MCI](mci-cut.md), [ \_ exclusão](mci-delete.md)de MCI ou comando de [ \_ colar MCI](mci-paste.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-337">The **dwReturn** member returns **TRUE** if there is recorded data in the workspace that might be lost as a result of a [MCI\_CLOSE](mci-close.md), [MCI\_LOAD](mci-load.md), [MCI\_RECORD](mci-record.md), [MCI\_RESERVE](mci-reserve.md), [MCI\_CUT](mci-cut.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="4c142-338">Caso contrário, o membro retornará **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-338">The member returns **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>vídeo de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI\_DGV\_STATUS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="4c142-340">O membro **dwReturn** retornará o MCI se o \_ vídeo estiver habilitado ou o MCI \_ desativado se estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4c142-340">The **dwReturn** member returns MCI\_ON if video is enabled or MCI\_OFF if it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_registro de \_ vídeo de status \_ \_ do MCI DGV</span><span class="sxs-lookup"><span data-stu-id="4c142-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI\_DGV\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-342">O membro **dwReturn** retorna \_ o MCI ativado ou o MCI \_ desativado, refletindo o estado definido \_ pelo \_ \_ sinalizador de gravação do DGV do MCI do comando do [MCI \_](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-342">The **dwReturn** member returns MCI\_ON or MCI\_OFF, reflecting the state set by the MCI\_DGV\_SETVIDEO\_RECORD flag of the [MCI\_SETVIDEO](mci-setvideo.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_fonte de \_ vídeo de status MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI\_DGV\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-344">O membro **dwReturn** retorna uma constante que indica o tipo de fonte de vídeo definido pelo \_ sinalizador de origem do DGV \_ do MCI \_ do comando do **MCI \_ setvideo** .</span><span class="sxs-lookup"><span data-stu-id="4c142-344">The **dwReturn** member returns a constant indicating the type of video source set by the MCI\_DGV\_SETVIDEO\_SOURCE flag of the **MCI\_SETVIDEO** command.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>\_número de \_ \_ src de vídeo de status DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI\_DGV\_STATUS\_VIDEO\_SRC\_NUM</span></span>
</dt> <dd>

<span data-ttu-id="4c142-346">O membro **dwReturn** retorna o número dentro do seu tipo da fonte de entrada de vídeo ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="4c142-346">The **dwReturn** member returns the number within its type of the video-input source currently active.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_fluxo de \_ vídeo de status \_ \_ do MCI DGV</span><span class="sxs-lookup"><span data-stu-id="4c142-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI\_DGV\_STATUS\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="4c142-348">O membro **dwReturn** retorna o número de fluxo de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-348">The **dwReturn** member returns the current video-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>VOLUME de status do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI\_DGV\_STATUS\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="4c142-350">O membro **dwReturn** retorna a média do volume para os alto-falantes esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="4c142-350">The **dwReturn** member returns the average of the volume to the left and right speakers.</span></span> <span data-ttu-id="4c142-351">Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.</span><span class="sxs-lookup"><span data-stu-id="4c142-351">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>janela de status do MCI \_ DGV \_ \_ \_ visível</span><span class="sxs-lookup"><span data-stu-id="4c142-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI\_DGV\_STATUS\_WINDOW\_VISIBLE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-353">O membro **dwReturn** retornará **true** se a janela não estiver oculta.</span><span class="sxs-lookup"><span data-stu-id="4c142-353">The **dwReturn** member returns **TRUE** if the window is not hidden.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>janela de status do MCI \_ DGV \_ \_ \_ minimizada</span><span class="sxs-lookup"><span data-stu-id="4c142-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI\_DGV\_STATUS\_WINDOW\_MINIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-355">O membro **dwReturn** retornará **true** se a janela for minimizada.</span><span class="sxs-lookup"><span data-stu-id="4c142-355">The **dwReturn** member returns **TRUE** if the window is minimized.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>janela de status do MCI \_ DGV \_ \_ \_ maximizada</span><span class="sxs-lookup"><span data-stu-id="4c142-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI\_DGV\_STATUS\_WINDOW\_MAXIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-357">O membro **dwReturn** retornará **true** se a janela for maximizada.</span><span class="sxs-lookup"><span data-stu-id="4c142-357">The **dwReturn** member returns **TRUE** if the window is maximized.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="4c142-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-359">O membro **dwReturn** retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="4c142-359">The **dwReturn** member returns **TRUE**.</span></span>

</dd> </dl>

<span data-ttu-id="4c142-360">Para dispositivos de vídeo digital, o parâmetro *lpStatus* aponta para uma estrutura de [**\_ \_ \_ parâmetros de status DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="4c142-360">For digital-video devices, the *lpStatus* parameter points to an [**MCI\_DGV\_STATUS\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) structure.</span></span>

<span data-ttu-id="4c142-361">Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **Sequencer** .</span><span class="sxs-lookup"><span data-stu-id="4c142-361">The following additional flags are used with the **sequencer** device type.</span></span> <span data-ttu-id="4c142-362">Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c142-362">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="4c142-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>\_DIVTYPE de \_ status de Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI\_SEQ\_STATUS\_DIVTYPE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-364">O membro **dwReturn** é definido como um dos seguintes valores indicando o tipo de divisão atual de uma sequência:</span><span class="sxs-lookup"><span data-stu-id="4c142-364">The **dwReturn** member is set to one of the following values indicating the current division type of a sequence:</span></span>

-   <span data-ttu-id="4c142-365">MCI \_ Seq \_ div \_ PPQN</span><span class="sxs-lookup"><span data-stu-id="4c142-365">MCI\_SEQ\_DIV\_PPQN</span></span>
-   <span data-ttu-id="4c142-366">MCI \_ Seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="4c142-366">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>
-   <span data-ttu-id="4c142-367">MCI \_ Seq \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="4c142-367">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>
-   <span data-ttu-id="4c142-368">MCI \_ Seq \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="4c142-368">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>
-   <span data-ttu-id="4c142-369">MCI \_ Seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="4c142-369">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span>

</dd> <dt>

<span data-ttu-id="4c142-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_mestre de \_ status de Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI\_SEQ\_STATUS\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="4c142-371">O membro **dwReturn** é definido como o tipo de sincronização usado para a operação mestre.</span><span class="sxs-lookup"><span data-stu-id="4c142-371">The **dwReturn** member is set to the synchronization type used for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>\_deslocamento de \_ status de Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI\_SEQ\_STATUS\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="4c142-373">O membro **dwReturn** é definido como o deslocamento SMPTE atual de uma sequência.</span><span class="sxs-lookup"><span data-stu-id="4c142-373">The **dwReturn** member is set to the current SMPTE offset of a sequence.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>porta de status do MCI \_ Seq \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI\_SEQ\_STATUS\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-375">O membro **dwReturn** é definido como o identificador do dispositivo MIDI para a porta atual usada pela sequência.</span><span class="sxs-lookup"><span data-stu-id="4c142-375">The **dwReturn** member is set to the MIDI device identifier for the current port used by the sequence.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>\_auxiliar Seq de \_ status \_ do MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI\_SEQ\_STATUS\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-377">O membro **dwReturn** é definido como o tipo de sincronização usado para a operação subordinada.</span><span class="sxs-lookup"><span data-stu-id="4c142-377">The **dwReturn** member is set to the synchronization type used for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>\_tempo de \_ status de Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI\_SEQ\_STATUS\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="4c142-379">O membro **dwReturn** é definido como o tempo atual de uma sequência MIDI em batidas por minuto para arquivos PPQN ou quadros por segundo para arquivos SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4c142-379">The **dwReturn** member is set to the current tempo of a MIDI sequence in beats per minute for PPQN files, or frames per second for SMPTE files.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="4c142-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-381">O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-381">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="4c142-382">Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **VCR** .</span><span class="sxs-lookup"><span data-stu-id="4c142-382">The following additional flags are used with the **vcr** device type.</span></span> <span data-ttu-id="4c142-383">Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c142-383">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="4c142-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="4c142-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-385">O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-385">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_registro de \_ montagem do status do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI\_VCR\_STATUS\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-387">O membro **dwReturn** será definido como **true** se o modo de montagem estiver on; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-387">The **dwReturn** member is set to **TRUE** if assemble mode is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_Monitor de \_ áudio de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="4c142-389">O membro **dwReturn** é definido como uma constante, indicando o tipo de monitor de áudio selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4c142-389">The **dwReturn** member is set to a constant, indicating the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_número do \_ \_ Monitor de \_ áudio \_ MCI de status do VCR</span><span class="sxs-lookup"><span data-stu-id="4c142-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="4c142-391">O membro **dwReturn** é definido como o número do tipo de monitor de áudio selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4c142-391">The **dwReturn** member is set to the number of the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_registro de \_ áudio de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI\_VCR\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-393">O membro **dwReturn** será definido como **true** se o áudio for gravado quando o próximo comando de registro for fornecido; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-393">The **dwReturn** member is set to **TRUE** if audio will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="4c142-394">Se você especificar a \_ faixa MCI no parâmetro *dwFlags* deste comando, **dwTrack** conterá a faixa à qual essa consulta se aplica.</span><span class="sxs-lookup"><span data-stu-id="4c142-394">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_fonte de \_ áudio de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-396">O membro **dwReturn** é definido como uma constante, indicando o tipo de fonte de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-396">The **dwReturn** member is set to a constant, indicating the current audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>\_número de \_ \_ fonte de \_ áudio \_ MCI de status do VCR</span><span class="sxs-lookup"><span data-stu-id="4c142-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="4c142-398">O membro **dwReturn** é definido como o número do tipo de fonte de áudio selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4c142-398">The **dwReturn** member is set to the number of the currently selected audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>\_relógio de \_ status do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI\_VCR\_STATUS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="4c142-400">O membro **dwReturn** é definido como o valor do relógio atual, em incrementos de clock totais.</span><span class="sxs-lookup"><span data-stu-id="4c142-400">The **dwReturn** member is set to the current clock value, in total clock increments.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>\_ID do \_ relógio de status do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI\_VCR\_STATUS\_CLOCK\_ID</span></span>
</dt> <dd>

<span data-ttu-id="4c142-402">O membro **dwReturn** é definido como um número que descreve exclusivamente o relógio em uso.</span><span class="sxs-lookup"><span data-stu-id="4c142-402">The **dwReturn** member is set to a number which uniquely describes the clock in use.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>\_formato do \_ contador de status do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI\_VCR\_STATUS\_COUNTER\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-404">O membro **dwReturn** é definido como uma constante que descreve o formato do contador atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-404">The **dwReturn** member is set to a constant describing the current counter format.</span></span> <span data-ttu-id="4c142-405">Para obter mais informações, consulte o \_ \_ \_ sinalizador de formato de tempo do MCI set do comando do [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-405">For more information, see the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_resolução do \_ contador de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI\_VCR\_STATUS\_COUNTER\_RESOLUTION</span></span>
</dt> <dd>

<span data-ttu-id="4c142-407">O membro **dwReturn** é definido como uma constante que descreve a resolução do contador e é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4c142-407">The **dwReturn** member is set to a constant describing the resolution of the counter, and is one of the following values:</span></span>

-   <span data-ttu-id="4c142-408">\_ \_ \_ \_ Quadros de resolução do contador de VCR MCI: o contador tem resolução de quadros.</span><span class="sxs-lookup"><span data-stu-id="4c142-408">MCI\_VCR\_COUNTER\_RES\_FRAMES: Counter has resolution of frames.</span></span>
-   <span data-ttu-id="4c142-409">\_ \_ \_ Segundos de res do contador de videocassete MCI: o \_ contador tem a resolução de segundos.</span><span class="sxs-lookup"><span data-stu-id="4c142-409">MCI\_VCR\_COUNTER\_RES\_SECONDS: Counter has resolution of seconds.</span></span>
-   <span data-ttu-id="4c142-410">\_Valor do \_ contador de status do VCR MCI \_ \_ : o membro **dwReturn** é definido como a leitura do contador atual, no formato de tempo do contador atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-410">MCI\_VCR\_STATUS\_COUNTER\_VALUE: The **dwReturn** member is set to the current counter reading, in the current counter-time format.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_taxa de \_ quadros de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI\_VCR\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-412">O membro **dwReturn** é definido como a taxa de quadros nativa atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c142-412">The **dwReturn** member is set to the current native frame rate of the device.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_índice de \_ status de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI\_VCR\_STATUS\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="4c142-414">O membro **dwReturn** é definido como uma constante, descrevendo o conteúdo atual da exibição na tela e é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4c142-414">The **dwReturn** member is set to a constant, describing the current contents of the on-screen display, and is one of the following:</span></span>

-   <span data-ttu-id="4c142-415">\_contador de \_ índice de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-415">MCI\_VCR\_INDEX\_COUNTER</span></span>
-   <span data-ttu-id="4c142-416">\_data do \_ índice de VCR do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-416">MCI\_VCR\_INDEX\_DATE</span></span>
-   <span data-ttu-id="4c142-417">\_tempo de \_ índice de VCR do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-417">MCI\_VCR\_INDEX\_TIME</span></span>
-   <span data-ttu-id="4c142-418">código de meio do \_ índice de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-418">MCI\_VCR\_INDEX\_TIMECODE</span></span>

</dd> <dt>

<span data-ttu-id="4c142-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ \_ índice de status de VCR MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="4c142-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI\_VCR\_STATUS\_INDEX\_ON</span></span>
</dt> <dd>

<span data-ttu-id="4c142-420">O membro **dwReturn** será definido como **true** se a exibição na tela estiver on; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-420">The **dwReturn** member is set to **TRUE** if the on-screen display is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_tipo de \_ mídia de status do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI\_VCR\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-422">O membro **dwReturn** é definido como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4c142-422">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="4c142-423">Mídia de VCR MCI com \_ \_ \_ 8mm</span><span class="sxs-lookup"><span data-stu-id="4c142-423">MCI\_VCR\_MEDIA\_8MM</span></span>
-   <span data-ttu-id="4c142-424">\_Mídia VCR \_ MCI \_ Hi8</span><span class="sxs-lookup"><span data-stu-id="4c142-424">MCI\_VCR\_MEDIA\_HI8</span></span>
-   <span data-ttu-id="4c142-425">\_VHS de \_ mídia \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-425">MCI\_VCR\_MEDIA\_VHS</span></span>
-   <span data-ttu-id="4c142-426">\_mídia VCR \_ MCI \_ SVHS</span><span class="sxs-lookup"><span data-stu-id="4c142-426">MCI\_VCR\_MEDIA\_SVHS</span></span>
-   <span data-ttu-id="4c142-427">mídia de VCR do MCI \_ \_ \_ beta</span><span class="sxs-lookup"><span data-stu-id="4c142-427">MCI\_VCR\_MEDIA\_BETA</span></span>
-   <span data-ttu-id="4c142-428">\_mídia VCR \_ MCI \_ EDBETA</span><span class="sxs-lookup"><span data-stu-id="4c142-428">MCI\_VCR\_MEDIA\_EDBETA</span></span>
-   <span data-ttu-id="4c142-429">\_mídia de VCR MCI \_ \_ diferente</span><span class="sxs-lookup"><span data-stu-id="4c142-429">MCI\_VCR\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="4c142-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_número de \_ status do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI\_VCR\_STATUS\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="4c142-431">O membro **dwNumber** é definido como o número do sintonizador lógico quando você usa esse sinalizador com o \_ sinalizador de canal do \_ sintonizador de status do VCR MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4c142-431">The **dwNumber** member is set to the logical-tuner number when you use this flag with the MCI\_VCR\_STATUS\_TUNER\_CHANNEL flag.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ status do VCR \_ MCI \_ número \_ de \_ faixas de áudio</span><span class="sxs-lookup"><span data-stu-id="4c142-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_AUDIO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="4c142-433">O membro **dwReturn** é definido como o número de faixas de áudio que são selecionáveis de forma independente.</span><span class="sxs-lookup"><span data-stu-id="4c142-433">The **dwReturn** member is set to the number of audio tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ status do VCR \_ MCI \_ número \_ de \_ faixas de vídeo</span><span class="sxs-lookup"><span data-stu-id="4c142-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_VIDEO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="4c142-435">O membro **dwReturn** é definido como o número de faixas de vídeo que são selecionáveis de forma independente.</span><span class="sxs-lookup"><span data-stu-id="4c142-435">The **dwReturn** member is set to the number of video tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>\_ \_ \_ tempo limite de pausa de status de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI\_VCR\_STATUS\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-437">O membro **dwReturn** é definido como a duração máxima, em milissegundos, de um comando PAUSE.</span><span class="sxs-lookup"><span data-stu-id="4c142-437">The **dwReturn** member is set to the maximum duration, in milliseconds, of a pause command.</span></span> <span data-ttu-id="4c142-438">O valor de retorno de zero indica que nenhum tempo limite ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="4c142-438">The return value of zero indicates that no time-out will occur.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>\_formato de \_ reprodução de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI\_VCR\_STATUS\_PLAY\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-440">O membro **dwReturn** é definido como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4c142-440">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="4c142-441">\_EP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-441">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="4c142-442">\_formato de videocassete MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="4c142-442">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="4c142-443">\_ \_ outro formato de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-443">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="4c142-444">\_SP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-444">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="4c142-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_duração de \_ redistribuição de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI\_VCR\_STATUS\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="4c142-446">O membro **dwReturn** é definido como o tamanho da fita de vídeo que será reproduzida após o ponto em que foi interrompido, no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-446">The **dwReturn** member is set to the length of the videotape that will play after the spot at which it was stopped, in the current time format.</span></span> <span data-ttu-id="4c142-447">Isso é necessário para desposicionar o transporte de fita do VCR de um comando parar ou pausar.</span><span class="sxs-lookup"><span data-stu-id="4c142-447">This is needed to brake the VCR tape transport from a stop or pause command.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>\_ \_ \_ ativação de status de VCR MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="4c142-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI\_VCR\_STATUS\_POWER\_ON</span></span>
</dt> <dd>

<span data-ttu-id="4c142-449">O membro **dwReturn** será definido como **true** se a energia estiver ativada; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-449">The **dwReturn** member is set to **TRUE** if the power is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_duração da \_ preversão do status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI\_VCR\_STATUS\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="4c142-451">O membro **dwReturn** é definido como o tamanho da fita de vídeo que será reproduzida antes do ponto em que ele foi iniciado, no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-451">The **dwReturn** member is set to the length of the videotape that will play before the spot at which it was started, in the current time format.</span></span> <span data-ttu-id="4c142-452">Isso é necessário para estabilizar a saída do VCR.</span><span class="sxs-lookup"><span data-stu-id="4c142-452">This is needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_formato de \_ registro de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI\_VCR\_STATUS\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-454">O membro **dwReturn** é definido como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4c142-454">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="4c142-455">\_EP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-455">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="4c142-456">\_formato de videocassete MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="4c142-456">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="4c142-457">\_ \_ outro formato de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-457">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="4c142-458">\_SP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-458">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="4c142-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_velocidade de \_ status do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI\_VCR\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-460">O membro **dwReturn** é definido como a velocidade atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-460">The **dwReturn** member is set to the current speed.</span></span> <span data-ttu-id="4c142-461">Para obter mais informações, consulte o \_ \_ \_ sinalizador de velocidade do conjunto de VCR MCI do comando [ \_ set do MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-461">For more information, see the MCI\_VCR\_SET\_SPEED flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>\_modo de \_ tempo de status do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI\_VCR\_STATUS\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-463">O membro **dwReturn** é definido como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4c142-463">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="4c142-464">\_contador de \_ tempo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-464">MCI\_VCR\_TIME\_COUNTER</span></span>
-   <span data-ttu-id="4c142-465">\_detecção de \_ tempo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-465">MCI\_VCR\_TIME\_DETECT</span></span>
-   <span data-ttu-id="4c142-466">tempo de vida de \_ hora do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-466">MCI\_VCR\_TIME\_TIMECODE</span></span>

<span data-ttu-id="4c142-467">Para obter mais informações, consulte o \_ \_ \_ \_ sinalizador de modo de tempo de conjunto de VCR MCI do comando [ \_ set do MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-467">For more information, see the MCI\_VCR\_SET\_TIME\_MODE flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>\_tipo de \_ tempo de status do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI\_VCR\_STATUS\_TIME\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-469">O membro **dwReturn** é definido como uma constante que descreve o tipo de hora atual em uso (usado por [Play](play.md), [Record](record.md), [Seek](seek.md)e assim por diante) e é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4c142-469">The **dwReturn** member is set to a constant describing the current time type in use (used by [play](play.md), [record](record.md), [seek](seek.md), and so on), and is one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="4c142-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_contador de \_ tempo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="4c142-471">O contador está em uso.</span><span class="sxs-lookup"><span data-stu-id="4c142-471">Counter is in use.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>tempo de vida de \_ hora do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-473">O código de pafica em uso.</span><span class="sxs-lookup"><span data-stu-id="4c142-473">Timecode is in use.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>\_código de status de VCR MCI \_ \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="4c142-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI\_VCR\_STATUS\_TIMECODE\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-475">O membro **dwReturn** será definido como **true** se o código de tempo estiver presente na posição atual no conteúdo; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-475">The **dwReturn** member is set to **TRUE** if timecode is present at the current position in the content; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_registro de \_ código de status do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI\_VCR\_STATUS\_TIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-477">O membro **dwReturn** será definido como **true** se o código de code for registrado quando o próximo comando de registro for atribuído; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-477">The **dwReturn** member is set to **TRUE** if the timecode will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>\_tipo de \_ código de status de VCR do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI\_VCR\_STATUS\_TIMECODE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-479">O membro **dwReturn** é definido como uma constante, descrevendo o tipo de código de erro que é diretamente suportado pelo dispositivo e é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4c142-479">The **dwReturn** member is set to a constant, describing the type of timecode that is directly supported by the device, and is one of the following:</span></span>

-   <span data-ttu-id="4c142-480">\_Tipo de código de paficação de videocassete MCI \_ \_ \_ None: este dispositivo não usa um código de um.</span><span class="sxs-lookup"><span data-stu-id="4c142-480">MCI\_VCR\_TIMECODE\_TYPE\_NONE: This device does not use a timecode.</span></span>
-   <span data-ttu-id="4c142-481">\_ \_ Tipo de código de erro de VCR MCI \_ \_ outro: este dispositivo usa um código de erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="4c142-481">MCI\_VCR\_TIMECODE\_TYPE\_OTHER: This device uses an unspecified timecode.</span></span>
-   <span data-ttu-id="4c142-482">\_Tipo de \_ código de pausar VCR MCI \_ \_ : este dispositivo usa o código de pausando SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4c142-482">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE: This device uses SMPTE timecode.</span></span>
-   <span data-ttu-id="4c142-483">Tipo de código de caso de \_ VCR MCI \_ \_ \_ \_ drop ignore: este dispositivo usa o código de recurso de descarte SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4c142-483">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE\_DROP: This device uses SMPTE drop timecode.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_canal de \_ \_ sintonização de status de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI\_VCR\_STATUS\_TUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="4c142-485">O membro **dwReturn** é definido como o número do canal atual.</span><span class="sxs-lookup"><span data-stu-id="4c142-485">The **dwReturn** member is set to the current channel number.</span></span> <span data-ttu-id="4c142-486">Se você especificar \_ \_ \_ o número de status do VCR MCI no parâmetro *dwFlags* deste comando, **dwNumber** conterá o número do sintonizador lógico ao qual esse comando se aplica.</span><span class="sxs-lookup"><span data-stu-id="4c142-486">If you specify MCI\_VCR\_STATUS\_NUMBER in the *dwFlags* parameter of this command, **dwNumber** contains the logical-tuner number this command applies to.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_Monitor de \_ vídeo de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="4c142-488">O membro **dwReturn** é definido como uma constante, indicando o tipo de monitor de vídeo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4c142-488">The **dwReturn** member is set to a constant, indicating the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_número do \_ Monitor de vídeo do status do VCR MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="4c142-490">O membro **dwReturn** é definido como o número do tipo de monitor de vídeo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4c142-490">The **dwReturn** member is set to the number of the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_registro de \_ vídeo de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI\_VCR\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-492">O membro **dwReturn** será definido como **true** se o vídeo for gravado quando o próximo comando de registro for fornecido; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-492">The **dwReturn** member is set to **TRUE** if video will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="4c142-493">Se você especificar a \_ faixa MCI no parâmetro *dwFlags* deste comando, **dwTrack** conterá a faixa à qual essa consulta se aplica.</span><span class="sxs-lookup"><span data-stu-id="4c142-493">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_fonte de \_ vídeo de status de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-495">O membro **dwReturn** é definido como uma constante que indica o tipo de fonte de vídeo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4c142-495">The **dwReturn** member is set to a constant indicating the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_número de \_ fonte do vídeo de status do VCR MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="4c142-497">O membro **dwReturn** é definido como o número do tipo de fonte de vídeo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4c142-497">The **dwReturn** member is set to the number of the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>\_status do VCR MCI \_ \_ \_ protegido contra gravação</span><span class="sxs-lookup"><span data-stu-id="4c142-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI\_VCR\_STATUS\_WRITE\_PROTECTED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-499">O membro **dwReturn** será definido como **true** se a mídia estiver protegida contra gravação; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-499">The **dwReturn** member is set to **TRUE** if the media is write-protected; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="4c142-500">Para dispositivos VCR, o parâmetro *lpStatus* aponta para uma estrutura de parâmetros de [**status de \_ VCR \_ \_ MCI**](mci-vcr-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-500">For VCR devices, the *lpStatus* parameter points to an [**MCI\_VCR\_STATUS\_PARMS**](mci-vcr-status-parms.md) structure.</span></span>

<span data-ttu-id="4c142-501">Usar o \_ sinalizador de \_ comprimento do status MCI para determinar o comprimento da mídia sempre retorna 2 horas para dispositivos VCR, a menos que o comprimento tenha sido explicitamente alterado usando o comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="4c142-501">Using the MCI\_STATUS\_LENGTH flag to determine the length of the media always returns 2 hours for VCR devices, unless the length has been explicitly changed using the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="4c142-502">Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo de **sobreposição** .</span><span class="sxs-lookup"><span data-stu-id="4c142-502">The following additional flags are used with the **overlay** device type.</span></span> <span data-ttu-id="4c142-503">Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c142-503">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="4c142-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_HWND de \_ status \_ OVLY do MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI\_OVLY\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="4c142-505">O membro **dwReturn** é definido como o identificador da janela associada ao dispositivo de sobreposição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4c142-505">The **dwReturn** member is set to the handle of the window associated with the video-overlay device.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_Stretch de \_ status de OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI\_OVLY\_STATUS\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="4c142-507">O membro **dwReturn** será definido como **true** se o alargamento estiver habilitado; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-507">The **dwReturn** member is set to **TRUE** if stretching is enabled; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="4c142-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-509">O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-509">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="4c142-510">Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **VIDEODISC** .</span><span class="sxs-lookup"><span data-stu-id="4c142-510">The following additional flags are used with the **videodisc** device type.</span></span> <span data-ttu-id="4c142-511">Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c142-511">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="4c142-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente</span><span class="sxs-lookup"><span data-stu-id="4c142-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-513">O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-513">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modo de status MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-515">O membro **dwReturn** é definido como o modo atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c142-515">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="4c142-516">Os dispositivos VIDEODISC podem retornar a \_ constante de estacionamento do modo de VD do MCI \_ \_ , além das constantes que qualquer dispositivo pode retornar, conforme documentado com o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c142-516">Videodisc devices can return the MCI\_VD\_MODE\_PARK constant, in addition to the constants any device can return, as documented with the *dwFlags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_tamanho do \_ disco de status de VD do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI\_VD\_STATUS\_DISC\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-518">O membro **dwReturn** é definido como o tamanho do disco carregado em polegadas (8 ou 12).</span><span class="sxs-lookup"><span data-stu-id="4c142-518">The **dwReturn** member is set to the size of the loaded disc in inches (8 or 12).</span></span>

</dd> <dt>

<span data-ttu-id="4c142-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>\_avanço do \_ status de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI\_VD\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="4c142-520">O membro **dwReturn** é definido como **true** se estiver tocando; caso contrário, será definido como **false** .</span><span class="sxs-lookup"><span data-stu-id="4c142-520">The **dwReturn** member is set to **TRUE** if playing forward; it is set to **FALSE** otherwise.</span></span>

<span data-ttu-id="4c142-521">O dispositivo MCI VIDEODISC não dá suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="4c142-521">The MCI videodisc device does not support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_tipo de \_ mídia de status de VD do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c142-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI\_VD\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-523">O membro **dwReturn** é definido como o tipo de mídia da mídia inserida.</span><span class="sxs-lookup"><span data-stu-id="4c142-523">The **dwReturn** member is set to the media type of the inserted media.</span></span> <span data-ttu-id="4c142-524">Os seguintes tipos de mídia podem ser retornados:</span><span class="sxs-lookup"><span data-stu-id="4c142-524">The following media types can be returned:</span></span>

<span data-ttu-id="4c142-525">\_cav de \_ mídia de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-525">MCI\_VD\_MEDIA\_CAV</span></span>

<span data-ttu-id="4c142-526">\_CLV de \_ mídia de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-526">MCI\_VD\_MEDIA\_CLV</span></span>

<span data-ttu-id="4c142-527">mídia de VD do MCI \_ \_ \_ diferente</span><span class="sxs-lookup"><span data-stu-id="4c142-527">MCI\_VD\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="4c142-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>\_ \_ lado do status de VD \_ do MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI\_VD\_STATUS\_SIDE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-529">O membro **dwReturn** é definido como 1 ou 2 para indicar qual lado do disco está carregado.</span><span class="sxs-lookup"><span data-stu-id="4c142-529">The **dwReturn** member is set to 1 or 2 to indicate which side of the disc is loaded.</span></span> <span data-ttu-id="4c142-530">Nem todos os dispositivos VIDEODISC dão suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="4c142-530">Not all videodisc devices support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>\_velocidade de \_ status de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI\_VD\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="4c142-532">O membro **dwReturn** é definido como a velocidade de reprodução em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="4c142-532">The **dwReturn** member is set to the play speed in frames per second.</span></span> <span data-ttu-id="4c142-533">O MCIPIONR. O driver de dispositivo DRV retorna MCIERR \_ função sem suporte \_ .</span><span class="sxs-lookup"><span data-stu-id="4c142-533">The MCIPIONR.DRV device driver returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> </dl>

<span data-ttu-id="4c142-534">Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="4c142-534">The following additional flags are used with the **waveaudio** device type.</span></span> <span data-ttu-id="4c142-535">Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="4c142-535">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="4c142-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>\_FORMATTAG Wave \_ MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI\_WAVE\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="4c142-537">O membro **dwReturn** é definido como a marca de formato atual usada para reproduzir, gravar e salvar.</span><span class="sxs-lookup"><span data-stu-id="4c142-537">The **dwReturn** member is set to the current format tag used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-539">O membro **dwReturn** é definido como o dispositivo de entrada de onda usado para gravação.</span><span class="sxs-lookup"><span data-stu-id="4c142-539">The **dwReturn** member is set to the wave input device used for recording.</span></span> <span data-ttu-id="4c142-540">Se nenhum dispositivo estiver em uso e nenhum dispositivo tiver sido explicitamente definido, o retorno de erro será MCIERR \_ Wave \_ INPUTUNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="4c142-540">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_INPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_saída de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="4c142-542">O membro **dwReturn** é definido como o dispositivo de saída de onda usado para reprodução.</span><span class="sxs-lookup"><span data-stu-id="4c142-542">The **dwReturn** member is set to the wave output device used for playing.</span></span> <span data-ttu-id="4c142-543">Se nenhum dispositivo estiver em uso e nenhum dispositivo tiver sido explicitamente definido, o retorno de erro será MCIERR \_ Wave \_ OUTPUTUNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="4c142-543">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_OUTPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>\_AVGBYTESPERSEC de \_ status de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI\_WAVE\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="4c142-545">O membro **dwReturn** é definido para os bytes atuais por segundo usados para reprodução, gravação e salvamento.</span><span class="sxs-lookup"><span data-stu-id="4c142-545">The **dwReturn** member is set to the current bytes per second used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>\_BITSPERSAMPLE de \_ status de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI\_WAVE\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="4c142-547">O membro **dwReturn** é definido para os bits atuais por amostra usados para reproduzir, gravar e salvar dados formatados PCM.</span><span class="sxs-lookup"><span data-stu-id="4c142-547">The **dwReturn** member is set to the current bits per sample used for playing, recording, and saving PCM formatted data.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>\_BLOCKALIGN de \_ status de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI\_WAVE\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="4c142-549">O membro **dwReturn** é definido como o alinhamento de bloco atual usado para reproduzir, gravar e salvar.</span><span class="sxs-lookup"><span data-stu-id="4c142-549">The **dwReturn** member is set to the current block alignment used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_canais de \_ status de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI\_WAVE\_STATUS\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="4c142-551">O membro **dwReturn** é definido como a contagem de canais atual usada para reproduzir, gravar e salvar.</span><span class="sxs-lookup"><span data-stu-id="4c142-551">The **dwReturn** member is set to the current channel count used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>\_nível de \_ status de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI\_WAVE\_STATUS\_LEVEL</span></span>
</dt> <dd>

<span data-ttu-id="4c142-553">O membro **dwReturn** é definido como o registro atual ou o nível de reprodução dos dados formatados do PCM.</span><span class="sxs-lookup"><span data-stu-id="4c142-553">The **dwReturn** member is set to the current record or playback level of PCM formatted data.</span></span> <span data-ttu-id="4c142-554">O valor é retornado como um valor de 8 ou 16 bits, dependendo do tamanho de amostra usado.</span><span class="sxs-lookup"><span data-stu-id="4c142-554">The value is returned as an 8- or 16-bit value, depending on the sample size used.</span></span> <span data-ttu-id="4c142-555">O nível de canal direito ou mono é retornado na palavra de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="4c142-555">The right or mono channel level is returned in the low-order word.</span></span> <span data-ttu-id="4c142-556">O nível de canal esquerdo é retornado na palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="4c142-556">The left channel level is returned in the high-order word.</span></span>

</dd> <dt>

<span data-ttu-id="4c142-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>\_SAMPLESPERSEC de \_ status de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI\_WAVE\_STATUS\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="4c142-558">O membro **dwReturn** é definido para os exemplos atuais por segundo usados para reproduzir, gravar e salvar.</span><span class="sxs-lookup"><span data-stu-id="4c142-558">The **dwReturn** member is set to the current samples per second used for playing, recording, and saving.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c142-559">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c142-559">Requirements</span></span>



| <span data-ttu-id="4c142-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c142-560">Requirement</span></span> | <span data-ttu-id="4c142-561">Valor</span><span class="sxs-lookup"><span data-stu-id="4c142-561">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c142-562">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c142-562">Minimum supported client</span></span><br/> | <span data-ttu-id="4c142-563">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c142-563">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4c142-564">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c142-564">Minimum supported server</span></span><br/> | <span data-ttu-id="4c142-565">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c142-565">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4c142-566">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4c142-566">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c142-567"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c142-567"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c142-568">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c142-568">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c142-569">MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-569">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4c142-570">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-570">MCI Commands</span></span>](mci-commands.md)
</dt> <dt>

[<span data-ttu-id="4c142-571">recorte de MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-571">MCI\_CUT</span></span>](mci-cut.md)
</dt> <dt>

[<span data-ttu-id="4c142-572">exclusão de MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-572">MCI\_DELETE</span></span>](mci-delete.md)
</dt> <dt>

[<span data-ttu-id="4c142-573">\_colar MCI</span><span class="sxs-lookup"><span data-stu-id="4c142-573">MCI\_PASTE</span></span>](mci-paste.md)
</dt> <dt>

[<span data-ttu-id="4c142-574">Reserva de MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-574">MCI\_RESERVE</span></span>](mci-reserve.md)
</dt> <dt>

[<span data-ttu-id="4c142-575">conjunto de MCI \_</span><span class="sxs-lookup"><span data-stu-id="4c142-575">MCI\_SET</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="4c142-576">reproduzir</span><span class="sxs-lookup"><span data-stu-id="4c142-576">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="4c142-577">gravável</span><span class="sxs-lookup"><span data-stu-id="4c142-577">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="4c142-578">Procure</span><span class="sxs-lookup"><span data-stu-id="4c142-578">seek</span></span>](seek.md)
</dt> </dl>

 

