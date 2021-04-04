---
title: MCI_OPEN comando (mmsystem. h)
description: O \_ comando MCI abrir Inicializa um dispositivo ou arquivo. Todos os dispositivos reconhecem este comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- Multimídia do Windows de comando MCI_OPEN
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824144"
---
# <a name="mci_open-command"></a><span data-ttu-id="a525c-105">Comando de abertura do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a525c-105">MCI\_OPEN command</span></span>

<span data-ttu-id="a525c-106">O \_ comando MCI abrir Inicializa um dispositivo ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="a525c-106">The MCI\_OPEN command initializes a device or file.</span></span> <span data-ttu-id="a525c-107">Todos os dispositivos reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="a525c-107">All devices recognize this command.</span></span>

<span data-ttu-id="a525c-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a525c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
);
```



## <a name="parameters"></a><span data-ttu-id="a525c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a525c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a525c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a525c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a525c-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="a525c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a525c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a525c-113">\_Notificação MCI ou \_ espera MCI.</span><span class="sxs-lookup"><span data-stu-id="a525c-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="a525c-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a525c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a525c-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span><span class="sxs-lookup"><span data-stu-id="a525c-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span></span>
</dt> <dd>

<span data-ttu-id="a525c-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros abertos do MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a525c-116">Pointer to an [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span> <span data-ttu-id="a525c-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="a525c-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a525c-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a525c-118">Return Value</span></span>

<span data-ttu-id="a525c-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="a525c-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a525c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a525c-120">Remarks</span></span>

<span data-ttu-id="a525c-121">O \_ sinalizador de tipo Open do MCI \_ deve ser usado sempre que um dispositivo é especificado na função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a525c-121">The MCI\_OPEN\_TYPE flag must be used whenever a device is specified in the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="a525c-122">Se você abrir um dispositivo especificando uma constante do tipo de dispositivo, deverá especificar o sinalizador de \_ ID de tipo aberto MCI, \_ além do \_ tipo de abertura de MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a525c-122">If you open a device by specifying a device-type constant, you must specify the MCI\_OPEN\_TYPE\_ID flag in addition to MCI\_OPEN\_TYPE.</span></span> <span data-ttu-id="a525c-123">Para obter uma lista de constantes de tipo de dispositivo, consulte [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="a525c-123">For a list of device-type constants, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="a525c-124">Se o \_ sinalizador de compartilhamento aberto do MCI \_ não for especificado quando um dispositivo ou arquivo for aberto inicialmente, todos os \_ comandos de abertura do MCI subsequentes para o dispositivo ou arquivo falharão.</span><span class="sxs-lookup"><span data-stu-id="a525c-124">If the MCI\_OPEN\_SHAREABLE flag is not specified when a device or file is initially opened, all subsequent MCI\_OPEN commands to the device or file will fail.</span></span> <span data-ttu-id="a525c-125">Se o dispositivo ou arquivo já estiver aberto e esse sinalizador não for especificado, a chamada falhará mesmo que o primeiro comando aberto especificado por MCI seja \_ \_ compartilhável.</span><span class="sxs-lookup"><span data-stu-id="a525c-125">If the device or file is already open and this flag is not specified, the call will fail even if the first open command specified MCI\_OPEN\_SHAREABLE.</span></span> <span data-ttu-id="a525c-126">Arquivos abertos para o MCISEQ. DRV e MCIWAVE. Os dispositivos DRV não são compartilháveis.</span><span class="sxs-lookup"><span data-stu-id="a525c-126">Files opened for the MCISEQ.DRV and MCIWAVE.DRV devices are nonsharable.</span></span>

<span data-ttu-id="a525c-127">O caso é ignorado no nome do dispositivo, mas não pode haver espaços em branco à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="a525c-127">Case is ignored in the device name, but there cannot be leading or trailing blanks.</span></span>

<span data-ttu-id="a525c-128">Para usar a seleção automática de tipo (por meio das entradas no registro), atribua o nome de arquivo e a extensão de arquivos ao membro **lpstrElementName** da estrutura identificada por *lpOpen*, defina o membro **lpstrDeviceType** como **nulo** e defina o \_ sinalizador de elemento abrir do MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a525c-128">To use automatic type selection (via the entries in the registry), assign the filename and file extension to the **lpstrElementName** member of the structure identified by *lpOpen*, set the **lpstrDeviceType** member to **NULL**, and set the MCI\_OPEN\_ELEMENT flag.</span></span>

<span data-ttu-id="a525c-129">Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que oferecem suporte a MCI \_ Open:</span><span class="sxs-lookup"><span data-stu-id="a525c-129">The following additional flags apply to all devices supporting MCI\_OPEN:</span></span>

<dl> <dt>

<span data-ttu-id="a525c-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_alias de abrir MCI \_</span><span class="sxs-lookup"><span data-stu-id="a525c-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI\_OPEN\_ALIAS</span></span>
</dt> <dd>

<span data-ttu-id="a525c-131">Um alias é incluído no membro **lpstrAlias** da estrutura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="a525c-131">An alias is included in the **lpstrAlias** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ aberto \_ compartilhável</span><span class="sxs-lookup"><span data-stu-id="a525c-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI\_OPEN\_SHAREABLE</span></span>
</dt> <dd>

<span data-ttu-id="a525c-133">O dispositivo ou arquivo deve ser aberto como compartilhável.</span><span class="sxs-lookup"><span data-stu-id="a525c-133">The device or file should be opened as sharable.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>tipo de MCI \_ aberto \_</span><span class="sxs-lookup"><span data-stu-id="a525c-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI\_OPEN\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="a525c-135">Um nome de tipo de dispositivo ou constante está incluído no membro **lpstrDeviceType** da estrutura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="a525c-135">A device type name or constant is included in the **lpstrDeviceType** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ID do \_ tipo \_ Open do MCI</span><span class="sxs-lookup"><span data-stu-id="a525c-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI\_OPEN\_TYPE\_ID</span></span>
</dt> <dd>

<span data-ttu-id="a525c-137">A palavra de ordem inferior do membro **lpstrDeviceType** da estrutura identificada por *lpOpen* contém um identificador de tipo de dispositivo MCI padrão e a palavra de ordem superior, opcionalmente, contém o índice ordinal para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a525c-137">The low-order word of the **lpstrDeviceType** member of the structure identified by *lpOpen* contains a standard MCI device type identifier and the high-order word optionally contains the ordinal index for the device.</span></span> <span data-ttu-id="a525c-138">Use esse sinalizador com o \_ sinalizador de tipo aberto do MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a525c-138">Use this flag with the MCI\_OPEN\_TYPE flag.</span></span>

</dd> </dl>

<span data-ttu-id="a525c-139">Os seguintes sinalizadores adicionais se aplicam a dispositivos compostos:</span><span class="sxs-lookup"><span data-stu-id="a525c-139">The following additional flags apply to compound devices:</span></span>

<dl> <dt>

<span data-ttu-id="a525c-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>\_elemento MCI Open \_</span><span class="sxs-lookup"><span data-stu-id="a525c-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI\_OPEN\_ELEMENT</span></span>
</dt> <dd>

<span data-ttu-id="a525c-141">Um nome de arquivo é incluído no membro **lpstrElementName** da estrutura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="a525c-141">A filename is included in the **lpstrElementName** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_ID do \_ elemento de abertura do MCI \_</span><span class="sxs-lookup"><span data-stu-id="a525c-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI\_OPEN\_ELEMENT\_ID</span></span>
</dt> <dd>

<span data-ttu-id="a525c-143">O membro **lpstrElementName** da estrutura identificada por *lpOpen* é interpretado como um valor **DWORD** e tem significado interno para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a525c-143">The **lpstrElementName** member of the structure identified by *lpOpen* is interpreted as a **DWORD** value and has meaning internal to the device.</span></span> <span data-ttu-id="a525c-144">Use esse sinalizador com o \_ sinalizador de \_ elemento MCI Open.</span><span class="sxs-lookup"><span data-stu-id="a525c-144">Use this flag with the MCI\_OPEN\_ELEMENT flag.</span></span>

</dd> </dl>

<span data-ttu-id="a525c-145">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="a525c-145">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a525c-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>\_DGV MCI \_ abrir \_ noestático</span><span class="sxs-lookup"><span data-stu-id="a525c-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI\_DGV\_OPEN\_NOSTATIC</span></span>
</dt> <dd>

<span data-ttu-id="a525c-147">O dispositivo deve reduzir o número de cores estáticas (do sistema) na paleta.</span><span class="sxs-lookup"><span data-stu-id="a525c-147">The device should reduce the number of static (system) colors in the palette.</span></span> <span data-ttu-id="a525c-148">Isso aumenta o número de cores disponíveis para renderizar o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a525c-148">This increases the number of colors available for rendering the video stream.</span></span> <span data-ttu-id="a525c-149">Esse sinalizador se aplica somente a dispositivos que compartilham uma paleta com o Windows.</span><span class="sxs-lookup"><span data-stu-id="a525c-149">This flag applies only to devices that share a palette with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>DGV do MCI \_ \_ abrir \_ pai</span><span class="sxs-lookup"><span data-stu-id="a525c-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI\_DGV\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="a525c-151">O identificador de janela pai é especificado no membro **hwndParent** da estrutura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="a525c-151">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>\_DGV MCI \_ abrir \_ WS</span><span class="sxs-lookup"><span data-stu-id="a525c-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI\_DGV\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="a525c-153">Um estilo de janela é especificado no membro **dwStyle** da estrutura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="a525c-153">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ abrir \_ 16 bits</span><span class="sxs-lookup"><span data-stu-id="a525c-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI\_DGV\_OPEN\_16BIT</span></span>
</dt> <dd>

<span data-ttu-id="a525c-155">Indica uma preferência para o suporte a dispositivos MCI de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a525c-155">Indicates a preference for 16-bit MCI device support.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ abrir \_ 32 bits</span><span class="sxs-lookup"><span data-stu-id="a525c-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI\_DGV\_OPEN\_32BIT</span></span>
</dt> <dd>

<span data-ttu-id="a525c-157">Indica uma preferência para o suporte a dispositivos MCI de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a525c-157">Indicates a preference for 32-bit MCI device support.</span></span>

</dd> </dl>

<span data-ttu-id="a525c-158">Para dispositivos de vídeo digital, o parâmetro *lpOpen* aponta para uma estrutura de [**\_ \_ \_ parâmetros Open parms DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="a525c-158">For digital-video devices, the *lpOpen* parameter points to an [**MCI\_DGV\_OPEN\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) structure.</span></span>

<span data-ttu-id="a525c-159">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="a525c-159">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a525c-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>OVLY do MCI \_ \_ abrir \_ pai</span><span class="sxs-lookup"><span data-stu-id="a525c-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI\_OVLY\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="a525c-161">O identificador de janela pai é especificado no membro **hwndParent** da estrutura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="a525c-161">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="a525c-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>\_OVLY MCI \_ abrir \_ WS</span><span class="sxs-lookup"><span data-stu-id="a525c-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI\_OVLY\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="a525c-163">Um estilo de janela é especificado no membro **dwStyle** da estrutura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="a525c-163">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span> <span data-ttu-id="a525c-164">O valor **dwStyle** especifica o estilo da janela que o driver criará e exibirá se o aplicativo não fornecer um.</span><span class="sxs-lookup"><span data-stu-id="a525c-164">The **dwStyle** value specifies the style of the window that the driver will create and display if the application does not provide one.</span></span> <span data-ttu-id="a525c-165">O parâmetro Style usa um inteiro que define o estilo da janela.</span><span class="sxs-lookup"><span data-stu-id="a525c-165">The style parameter takes an integer that defines the window style.</span></span> <span data-ttu-id="a525c-166">Essas constantes são as mesmas que os estilos de janela padrão (como WS \_ -Child, WS \_ OVERLAPPEDWINDOW ou WS \_ popup).</span><span class="sxs-lookup"><span data-stu-id="a525c-166">These constants are the same as the standard window styles (such as WS\_CHILD, WS\_OVERLAPPEDWINDOW, or WS\_POPUP).</span></span>

</dd> </dl>

<span data-ttu-id="a525c-167">Para dispositivos de sobreposição de vídeo, o parâmetro *lpOpen* aponta para uma estrutura de [**\_ \_ \_ parâmetros Open parms OVLY MCI**](mci-ovly-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a525c-167">For video-overlay devices, the *lpOpen* parameter points to an [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md) structure.</span></span>

<span data-ttu-id="a525c-168">O seguinte sinalizador adicional é usado com o tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="a525c-168">The following additional flag is used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="a525c-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_ \_ buffer aberto do MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="a525c-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI\_WAVE\_OPEN\_BUFFER</span></span>
</dt> <dd>

<span data-ttu-id="a525c-170">Um comprimento de buffer é especificado no membro **dwBufferSeconds** da estrutura identificada por *lpOpen*.</span><span class="sxs-lookup"><span data-stu-id="a525c-170">A buffer length is specified in the **dwBufferSeconds** member of the structure identified by *lpOpen*.</span></span>

</dd> </dl>

<span data-ttu-id="a525c-171">Para dispositivos de formato de onda-áudio, o parâmetro *lpOpen* aponta para uma estrutura [**MCI de \_ \_ Open \_ parms de Wave**](mci-wave-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a525c-171">For waveform-audio devices, the *lpOpen* parameter points to an [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) structure.</span></span> <span data-ttu-id="a525c-172">O driver MCIWAVE requer um dispositivo de áudio de onda assíncrono.</span><span class="sxs-lookup"><span data-stu-id="a525c-172">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="a525c-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a525c-173">Requirements</span></span>



| <span data-ttu-id="a525c-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="a525c-174">Requirement</span></span> | <span data-ttu-id="a525c-175">Valor</span><span class="sxs-lookup"><span data-stu-id="a525c-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a525c-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a525c-176">Minimum supported client</span></span><br/> | <span data-ttu-id="a525c-177">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a525c-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a525c-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a525c-178">Minimum supported server</span></span><br/> | <span data-ttu-id="a525c-179">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a525c-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a525c-180">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a525c-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="a525c-181"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a525c-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a525c-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="a525c-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a525c-183">MCI</span><span class="sxs-lookup"><span data-stu-id="a525c-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a525c-184">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="a525c-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

