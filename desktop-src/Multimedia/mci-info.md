---
title: MCI_INFO comando (mmsystem. h)
description: O \_ comando MCI info recupera informações de cadeia de caracteres de um dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- Multimídia do Windows de comando MCI_INFO
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086232"
---
# <a name="mci_info-command"></a><span data-ttu-id="a096b-104">Comando de informações do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-104">MCI\_INFO command</span></span>

<span data-ttu-id="a096b-105">O \_ comando MCI info recupera informações de cadeia de caracteres de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a096b-105">The MCI\_INFO command retrieves string information from a device.</span></span> <span data-ttu-id="a096b-106">Todos os dispositivos reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="a096b-106">All devices recognize this command.</span></span> <span data-ttu-id="a096b-107">As informações são retornadas no membro **lpstrReturn** da estrutura identificada por *lpInfo*.</span><span class="sxs-lookup"><span data-stu-id="a096b-107">Information is returned in the **lpstrReturn** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="a096b-108">O membro **dwRetSize** especifica o tamanho do buffer para os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="a096b-108">The **dwRetSize** member specifies the buffer length for the returned data.</span></span>

<span data-ttu-id="a096b-109">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a096b-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a096b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a096b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a096b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a096b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a096b-112">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="a096b-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a096b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a096b-114">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="a096b-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="a096b-115">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a096b-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a096b-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span><span class="sxs-lookup"><span data-stu-id="a096b-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span></span>
</dt> <dd>

<span data-ttu-id="a096b-117">Ponteiro para uma estrutura de [**\_ \_ parâmetros de informações MCI**](mci-info-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a096b-117">Pointer to an [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure.</span></span> <span data-ttu-id="a096b-118">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="a096b-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a096b-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a096b-119">Return Value</span></span>

<span data-ttu-id="a096b-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="a096b-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a096b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="a096b-121">Remarks</span></span>

<span data-ttu-id="a096b-122">O seguinte sinalizador padrão adicional e específico de comando se aplica a todos os dispositivos que dão suporte a informações de MCI \_ :</span><span class="sxs-lookup"><span data-stu-id="a096b-122">The following additional standard and command-specific flag applies to all devices supporting MCI\_INFO:</span></span>

<dl> <dt>

<span data-ttu-id="a096b-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_produto de informações do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI\_INFO\_PRODUCT</span></span>
</dt> <dd>

<span data-ttu-id="a096b-124">Obtém uma descrição do hardware associado a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a096b-124">Obtains a description of the hardware associated with a device.</span></span> <span data-ttu-id="a096b-125">Os dispositivos devem fornecer uma descrição que identifique o driver e o hardware usados.</span><span class="sxs-lookup"><span data-stu-id="a096b-125">Devices should supply a description that identifies both the driver and the hardware used.</span></span>

</dd> </dl>

<span data-ttu-id="a096b-126">Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **cdaudio** :</span><span class="sxs-lookup"><span data-stu-id="a096b-126">The following additional flags apply to the **cdaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a096b-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>identidade de mídia do MCI \_ info \_ \_</span><span class="sxs-lookup"><span data-stu-id="a096b-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI\_INFO\_MEDIA\_IDENTITY</span></span>
</dt> <dd>

<span data-ttu-id="a096b-128">Produz um identificador exclusivo para o CD de áudio atualmente carregado no Player que está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="a096b-128">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span> <span data-ttu-id="a096b-129">Esse sinalizador retorna uma cadeia de 16 dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="a096b-129">This flag returns a string of 16 hexadecimal digits.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>informações do MCI \_ \_ mídia \_ UPC</span><span class="sxs-lookup"><span data-stu-id="a096b-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI\_INFO\_MEDIA\_UPC</span></span>
</dt> <dd>

<span data-ttu-id="a096b-131">Produz o código do produto universal (UPC) que é codificado em um CD de áudio.</span><span class="sxs-lookup"><span data-stu-id="a096b-131">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="a096b-132">O UPC é uma cadeia de caracteres de dígitos.</span><span class="sxs-lookup"><span data-stu-id="a096b-132">The UPC is a string of digits.</span></span> <span data-ttu-id="a096b-133">Ele pode não estar disponível para todos os CDs.</span><span class="sxs-lookup"><span data-stu-id="a096b-133">It might not be available for all CDs.</span></span>

</dd> </dl>

<span data-ttu-id="a096b-134">Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="a096b-134">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a096b-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>\_item de \_ informações do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI\_DGV\_INFO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="a096b-136">Uma constante que indica as informações desejadas é incluída no membro **dwItem** da estrutura identificada por *lpInfo*.</span><span class="sxs-lookup"><span data-stu-id="a096b-136">A constant indicating the information desired is included in the **dwItem** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="a096b-137">As seguintes constantes são definidas para dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="a096b-137">The following constants are defined for digital-video devices:</span></span>

</dd> <dt>

<span data-ttu-id="a096b-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ informações de \_ áudio \_ alg</span><span class="sxs-lookup"><span data-stu-id="a096b-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI\_DGV\_INFO\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="a096b-139">Retorna o nome do algoritmo de compactação de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-139">Returns the name for the current audio compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>qualidade de áudio do MCI \_ DGV \_ info \_ \_</span><span class="sxs-lookup"><span data-stu-id="a096b-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI\_DGV\_INFO\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="a096b-141">Retorna o nome do descritor de qualidade de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-141">Returns the name for the current audio quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>informações do MCI \_ DGV \_ ainda em \_ \_ alg</span><span class="sxs-lookup"><span data-stu-id="a096b-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI\_DGV\_INFO\_STILL\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="a096b-143">Retorna o nome do algoritmo de compactação de imagem ainda atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-143">Returns the name for the current still image compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>informações do MCI \_ DGV \_ \_ ainda \_ qualidade</span><span class="sxs-lookup"><span data-stu-id="a096b-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI\_DGV\_INFO\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="a096b-145">Retorna o nome do descritor de qualidade da imagem atual ainda.</span><span class="sxs-lookup"><span data-stu-id="a096b-145">Returns the name for the current still image quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>\_uso de \_ informações do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI\_DGV\_INFO\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="a096b-147">Retorna uma cadeia de caracteres que descreve as restrições de uso que podem ser impostas pelo proprietário do Visual ou dos dados audíveis no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a096b-147">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audible data in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>vídeo de informações do MCI \_ DGV \_ \_ \_ alg</span><span class="sxs-lookup"><span data-stu-id="a096b-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI\_DGV\_INFO\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="a096b-149">Retorna o nome do algoritmo de compactação de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-149">Returns the name for the current video compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>\_qualidade de \_ vídeo de informações de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="a096b-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI\_DGV\_INFO\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="a096b-151">Retorna o nome do descritor de qualidade de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-151">Returns the name for the current video quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_versão de informações do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="a096b-153">Retorna o nível de versão do driver de dispositivo e do hardware.</span><span class="sxs-lookup"><span data-stu-id="a096b-153">Returns the release level of the device driver and hardware.</span></span> <span data-ttu-id="a096b-154">Os desenvolvedores de drivers de dispositivo devem documentar a sintaxe da cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="a096b-154">Device driver developers must document the syntax of the returned string.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>\_texto de \_ informações do DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI\_DGV\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="a096b-156">Obtém a legenda da janela.</span><span class="sxs-lookup"><span data-stu-id="a096b-156">Obtains the window caption.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_arquivo de informações do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="a096b-158">Obtém o caminho e o nome do último arquivo especificado com o comando [MCI \_ Open](mci-open.md) ou [MCI \_ Load](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="a096b-158">Obtains the path and filename of the last file specified with the [MCI\_OPEN](mci-open.md) or [MCI\_LOAD](mci-load.md) command.</span></span> <span data-ttu-id="a096b-159">Se um arquivo não tiver sido especificado, o dispositivo retornará uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="a096b-159">If a file has not been specified, the device returns a null-terminated string.</span></span> <span data-ttu-id="a096b-160">Esse sinalizador tem suporte apenas em dispositivos que retornam **true** para o MCI \_ GETDEVCAPS \_ usa o \_ sinalizador de arquivos do comando [ \_ GETDEVCAPS do MCI](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="a096b-160">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

<span data-ttu-id="a096b-161">Para dispositivos de vídeo digital, o *lpInfo* aponta para uma estrutura de parâmetros de [**informações de \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="a096b-161">For digital-video devices, *lpInfo* points to an [**MCI\_DGV\_INFO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) structure.</span></span>

<span data-ttu-id="a096b-162">Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **Sequencer** :</span><span class="sxs-lookup"><span data-stu-id="a096b-162">The following additional flags apply to the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a096b-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>informações de MCI \_ \_ direitos autorais</span><span class="sxs-lookup"><span data-stu-id="a096b-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI\_INFO\_COPYRIGHT</span></span>
</dt> <dd>

<span data-ttu-id="a096b-164">Obtém o aviso de direitos autorais do arquivo MIDI do evento meta de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="a096b-164">Obtains the MIDI file copyright notice from the copyright meta event.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_arquivo de informações do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="a096b-166">Obtém o FileName do arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-166">Obtains the filename of the current file.</span></span> <span data-ttu-id="a096b-167">Esse sinalizador tem suporte apenas em dispositivos que retornam **true** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o \_ GETDEVCAPS MCI que usa o \_ \_ sinalizador arquivos.</span><span class="sxs-lookup"><span data-stu-id="a096b-167">This flag is supported only by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>\_nome da informação MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI\_INFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="a096b-169">Obtém o nome da sequência do evento meta de nome de sequência/faixa.</span><span class="sxs-lookup"><span data-stu-id="a096b-169">Obtains the sequence name from the sequence/track name meta event.</span></span>

</dd> </dl>

<span data-ttu-id="a096b-170">O seguinte sinalizador adicional se aplica ao tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="a096b-170">The following additional flag applies to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a096b-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_versão de \_ informações do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI\_VCR\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="a096b-172">Define o membro **lpstrReturn** da estrutura de [**parâmetros de \_ informações \_ do MCI**](mci-info-parms.md) para apontar para o número de versão.</span><span class="sxs-lookup"><span data-stu-id="a096b-172">Sets **lpstrReturn** member of the [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure to point to the version number.</span></span> <span data-ttu-id="a096b-173">Também define o membro **dwRetSize** igual ao comprimento da cadeia de caracteres apontada para.</span><span class="sxs-lookup"><span data-stu-id="a096b-173">Also sets the **dwRetSize** member equal to the length of the string pointed to.</span></span>

</dd> </dl>

<span data-ttu-id="a096b-174">Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="a096b-174">The following additional flags apply to the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a096b-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_arquivo de informações do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="a096b-176">Obtém o FileName do arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-176">Obtains the filename of the current file.</span></span> <span data-ttu-id="a096b-177">Esse sinalizador tem suporte apenas em dispositivos que retornam **true** para o MCI \_ GETDEVCAPS \_ usa o \_ sinalizador de arquivos do comando [ \_ GETDEVCAPS do MCI](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="a096b-177">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>\_texto de \_ informações do OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI\_OVLY\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="a096b-179">Obtém a legenda da janela associada ao dispositivo de sobreposição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a096b-179">Obtains the caption of the window associated with the video-overlay device.</span></span>

</dd> </dl>

<span data-ttu-id="a096b-180">Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="a096b-180">The following additional flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a096b-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_arquivo de informações do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="a096b-182">Obtém o FileName do arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-182">Obtains the filename of the current file.</span></span> <span data-ttu-id="a096b-183">Esse sinalizador tem suporte de dispositivos que retornam **true** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o \_ GETDEVCAPS MCI \_ usando o \_ sinalizador arquivos.</span><span class="sxs-lookup"><span data-stu-id="a096b-183">This flag is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="a096b-185">Obtém o nome do produto da entrada atual.</span><span class="sxs-lookup"><span data-stu-id="a096b-185">Obtains the product name of the current input.</span></span>

</dd> <dt>

<span data-ttu-id="a096b-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_saída de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="a096b-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="a096b-187">Obtém o nome do produto da saída atual e seu valor é específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a096b-187">Obtains the product name of the current output and its value is device specific.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a096b-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a096b-188">Requirements</span></span>



| <span data-ttu-id="a096b-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="a096b-189">Requirement</span></span> | <span data-ttu-id="a096b-190">Valor</span><span class="sxs-lookup"><span data-stu-id="a096b-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a096b-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a096b-191">Minimum supported client</span></span><br/> | <span data-ttu-id="a096b-192">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a096b-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a096b-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a096b-193">Minimum supported server</span></span><br/> | <span data-ttu-id="a096b-194">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a096b-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a096b-195">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a096b-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="a096b-196"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a096b-196"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a096b-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="a096b-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a096b-198">MCI</span><span class="sxs-lookup"><span data-stu-id="a096b-198">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a096b-199">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="a096b-199">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

