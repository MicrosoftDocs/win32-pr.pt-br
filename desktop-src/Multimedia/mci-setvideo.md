---
title: MCI_SETVIDEO comando (mmsystem. h)
description: O \_ comando AddVideo do MCI define os valores associados à reprodução de vídeo. Os dispositivos de vídeo digital e VCR reconhecem este comando.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- Multimídia do Windows de comando MCI_SETVIDEO
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455201"
---
# <a name="mci_setvideo-command"></a><span data-ttu-id="f53a5-105">Comando do vídeo do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-105">MCI\_SETVIDEO command</span></span>

<span data-ttu-id="f53a5-106">O \_ comando AddVideo do MCI define os valores associados à reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-106">The MCI\_SETVIDEO command sets values associated with video playback.</span></span> <span data-ttu-id="f53a5-107">Os dispositivos de vídeo digital e VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f53a5-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="f53a5-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f53a5-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
);
```



## <a name="parameters"></a><span data-ttu-id="f53a5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f53a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f53a5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f53a5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="f53a5-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f53a5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-113">**MCI \_ NOTIFICAÇÃO**, **\_ espera do MCI** ou **\_ teste MCI**.</span><span class="sxs-lookup"><span data-stu-id="f53a5-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or **MCI\_TEST**.</span></span> <span data-ttu-id="f53a5-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f53a5-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span><span class="sxs-lookup"><span data-stu-id="f53a5-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f53a5-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="f53a5-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="f53a5-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f53a5-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f53a5-118">Return Value</span></span>

<span data-ttu-id="f53a5-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f53a5-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f53a5-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f53a5-120">Remarks</span></span>

<span data-ttu-id="f53a5-121">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo "DigitalVideo":</span><span class="sxs-lookup"><span data-stu-id="f53a5-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="f53a5-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>\_DGV de \_ vídeo do \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f53a5-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI\_DGV\_SETVIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-123">O membro **lpstrAlgorithm** da estrutura identificada por *lpSetVideo* contém um endereço de um buffer que contém o nome de um algoritmo de compactação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-123">The **lpstrAlgorithm** member of the structure identified by *lpSetVideo* contains an address of a buffer containing the name of a video compression algorithm.</span></span> <span data-ttu-id="f53a5-124">O algoritmo de compactação é usado por comandos de [ \_ gravação MCI](mci-record.md) ou de [ \_ reserva de MCI](mci-reserve.md) subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f53a5-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="f53a5-125">Os algoritmos disponíveis são dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-125">The available algorithms are device dependent.</span></span>

<span data-ttu-id="f53a5-126">Se o algoritmo especificado for incompatível com o formato de arquivo atual, o formato de arquivo será alterado para o formato padrão do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-126">If the specified algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>\_DGV de \_ relógio de setvideo do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI\_DGV\_SETVIDEO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-128">Quando usado com **o \_ DGV de \_ vídeo \_ MCI**, indica que o tempo é especificado em milissegundos e é o tempo absoluto.</span><span class="sxs-lookup"><span data-stu-id="f53a5-128">When used with **MCI\_DGV\_SETVIDEO\_OVER**, indicates time is specified in milliseconds and is absolute time.</span></span> <span data-ttu-id="f53a5-129">(Esse tempo não está em etapa com a reprodução do espaço de trabalho.)</span><span class="sxs-lookup"><span data-stu-id="f53a5-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_entrada do DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI\_DGV\_SETVIDEO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-131">Modifica o **\_ \_ \_ brilho do DGV MCI**, a **\_ \_ \_ cor do DGV do MCI**, o MCI DGV setvideo **\_ \_ \_ contraste**, **o \_ MCI DGV \_ setvideo \_ gama**, a **\_ \_ \_ nitidez do MCI DGV** ou a **\_ \_ \_ tonalidade de vídeo** do MCI DGV para que ele afete o sinal de entrada e modifique o que é registrado.</span><span class="sxs-lookup"><span data-stu-id="f53a5-131">Modifies the **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="f53a5-132">Se possível, esse é o padrão ao monitorar a entrada.</span><span class="sxs-lookup"><span data-stu-id="f53a5-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_item de DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI\_DGV\_SETVIDEO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-134">Uma constante de vídeo é especificada no membro **dwItem** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-134">A video constant is specified in the **dwItem** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-135">A constante identifica o valor que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="f53a5-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="f53a5-136">Você pode especificar as seguintes constantes com este sinalizador:</span><span class="sxs-lookup"><span data-stu-id="f53a5-136">You can specify the following constants with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>\_procedimento de \_ desenho de vídeo do AVI do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI\_AVI\_SETVIDEO\_DRAW\_PROCEDURE</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-138">Um novo endereço de procedimento de desenho é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-138">A new drawing procedure address is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-139">Você pode especificar um novo procedimento de desenho somente quando o dispositivo estiver ocioso.</span><span class="sxs-lookup"><span data-stu-id="f53a5-139">You can specify a new drawing procedure only when the device is idle.</span></span> <span data-ttu-id="f53a5-140">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="f53a5-140">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="f53a5-141">Não há nenhum equivalente a esse sinalizador na interface de comando de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f53a5-141">There is no equivalent to this flag in the string command interface.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_cor da \_ paleta de vídeo do AVI do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-143">Uma nova cor de paleta é especificada nos membros **dwOver** e **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-143">A new palette color is specified in the **dwOver** and **dwValue** members of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-144">O membro **dwOver** especifica o índice da paleta da cor a ser alterada e o membro **dwValue** especifica a nova cor, como um valor RGB.</span><span class="sxs-lookup"><span data-stu-id="f53a5-144">The **dwOver** member specifies the palette index of the color to be changed and the **dwValue** member specifies the new color, as an RGB value.</span></span> <span data-ttu-id="f53a5-145">Você também deve especificar os sinalizadores de **\_ \_ \_ valor** do MCI **\_ DGV \_ \_** e do MCI DGV com o **\_ \_ \_ Item** de vídeo MCI DGV ao usar essa constante.</span><span class="sxs-lookup"><span data-stu-id="f53a5-145">You must also specify the **MCI\_DGV\_SETVIDEO\_OVER** and **MCI\_DGV\_SETVIDEO\_VALUE** flags with **MCI\_DGV\_SETVIDEO\_ITEM** when you use this constant.</span></span> <span data-ttu-id="f53a5-146">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="f53a5-146">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_meio- \_ Tom da \_ paleta de vídeo do AVI do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_HALFTONE</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-148">Indica que a paleta de meio-tom deve ser usada, em vez da paleta padrão.</span><span class="sxs-lookup"><span data-stu-id="f53a5-148">Indicates that the halftone palette should be used, instead of the default palette.</span></span> <span data-ttu-id="f53a5-149">Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="f53a5-149">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>\_BITSPERPEL DGV \_ do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI\_DGV\_SETVIDEO\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-151">O número de bits por pixel é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-151">The number of bits per pixel is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-152">O número de bits por pixel é usado para salvar dados capturados ou gravados</span><span class="sxs-lookup"><span data-stu-id="f53a5-152">The number of bits per pixel is used for saving captured or recorded data</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>\_brilho do DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI\_DGV\_SETVIDEO\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-154">O nível de brilho do vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-154">The video brightness level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_cor do DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI\_DGV\_SETVIDEO\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-156">O nível de saturação da cor do vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-156">The video color saturation level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>\_contraste de DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI\_DGV\_SETVIDEO\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-158">O nível de contraste do vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-158">The video contrast level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_taxa de \_ quadros do \_ DGV do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI\_DGV\_SETVIDEO\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-160">Uma taxa de quadros é especificada no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-160">A frame rate is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-161">A taxa é especificada em unidades de quadros por segundo, em vez de 1000.</span><span class="sxs-lookup"><span data-stu-id="f53a5-161">The rate is specified in units of frames per second times 1000.</span></span> <span data-ttu-id="f53a5-162">Por exemplo, 29,97 quadros por segundo é especificado como 29970.</span><span class="sxs-lookup"><span data-stu-id="f53a5-162">For example, 29.97 frames per second is specified as 29970.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>\_gama de DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI\_DGV\_SETVIDEO\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-164">Um valor de expoente de correção gama é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-164">A gamma correction exponent value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-165">A correção gama ajusta o mapeamento entre a intensidade codificada na fonte da apresentação e o brilho exibido.</span><span class="sxs-lookup"><span data-stu-id="f53a5-165">Gamma correction adjusts the mapping between the intensity encoded in the presentation source and the displayed brightness.</span></span> <span data-ttu-id="f53a5-166">O valor é o expoente multiplicado por 1000.</span><span class="sxs-lookup"><span data-stu-id="f53a5-166">The value is the exponent multiplied by 1000.</span></span> <span data-ttu-id="f53a5-167">Por exemplo, 2200 indica um expoente de 2,2.</span><span class="sxs-lookup"><span data-stu-id="f53a5-167">For example, 2200 indicates an exponent of 2.2.</span></span> <span data-ttu-id="f53a5-168">Um valor de 1000 indica um expoente de 1, que não se aplica a nenhuma correção de gama.</span><span class="sxs-lookup"><span data-stu-id="f53a5-168">A value of 1000 indicates an exponent of 1, which applies no gamma correction.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>\_cor da \_ chave do \_ DGV do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI\_DGV\_SETVIDEO\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-170">Uma cor de chave é especificada no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-170">A key color is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-171">A cor da chave é um valor RGB.</span><span class="sxs-lookup"><span data-stu-id="f53a5-171">The key color is an RGB value.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_índice de \_ chave do \_ DGV do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI\_DGV\_SETVIDEO\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-173">Um valor de índice de chave é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-173">A key index value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-174">O parâmetro de índice é um índice de paleta física.</span><span class="sxs-lookup"><span data-stu-id="f53a5-174">The index parameter is a physical palette index.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>\_PALHANDLE DGV \_ do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI\_DGV\_SETVIDEO\_PALHANDLE</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-176">Um identificador de paleta é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-176">A palette handle is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-177">O identificador da paleta está contido na palavra de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="f53a5-177">The palette handle is contained in the low-order word.</span></span> <span data-ttu-id="f53a5-178">Os dispositivos de vídeo digital não devem liberar a paleta passada com esse comando.</span><span class="sxs-lookup"><span data-stu-id="f53a5-178">Digital-video devices should not free the palette passed with this command.</span></span> <span data-ttu-id="f53a5-179">Os aplicativos devem liberá-lo depois que fecharem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-179">Applications should free it after they close the device.</span></span> <span data-ttu-id="f53a5-180">Esse sinalizador tem suporte apenas em dispositivos que usam paletas.</span><span class="sxs-lookup"><span data-stu-id="f53a5-180">This flag is supported only by devices that use palettes.</span></span> <span data-ttu-id="f53a5-181">Se esse identificador de paleta especificado for zero, a paleta padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="f53a5-181">If this specified palette handle is zero, then the default palette is used.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_nitidez do DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI\_DGV\_SETVIDEO\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-183">Um valor de nitidez de vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-183">A video sharpness value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>\_fonte de \_ vídeo MCI \_ DGV</span><span class="sxs-lookup"><span data-stu-id="f53a5-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI\_DGV\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-185">Uma constante especificando a origem da entrada de vídeo é especificada no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-185">A constant specifying the source of the video input is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-186">As seguintes constantes são definidas:</span><span class="sxs-lookup"><span data-stu-id="f53a5-186">The following constants are defined:</span></span>

-   <span data-ttu-id="f53a5-187">**MCI \_ DGV de \_ vídeo \_ src \_ NTSC**: televisão NTSC.</span><span class="sxs-lookup"><span data-stu-id="f53a5-187">**MCI\_DGV\_SETVIDEO\_SRC\_NTSC**: NTSC television.</span></span>
-   <span data-ttu-id="f53a5-188">DGV de vídeo do MCI \_ PAL- \_ Video \_ src \_ : PAL televisão.</span><span class="sxs-lookup"><span data-stu-id="f53a5-188">MCI\_DGV\_SETVIDEO\_SRC\_PAL: PAL television.</span></span>
-   <span data-ttu-id="f53a5-189">Vídeo do MCI \_ DGV do \_ vídeo \_ src \_ RGB: RGB.</span><span class="sxs-lookup"><span data-stu-id="f53a5-189">MCI\_DGV\_SETVIDEO\_SRC\_RGB: RGB video.</span></span>
-   <span data-ttu-id="f53a5-190">DGV secam do MCI de \_ \_ vídeo \_ \_ : SECAM televisão.</span><span class="sxs-lookup"><span data-stu-id="f53a5-190">MCI\_DGV\_SETVIDEO\_SRC\_SECAM: SECAM television.</span></span>
-   <span data-ttu-id="f53a5-191">\_DGV \_ de SVIDEO do MCI de vídeo \_ \_ : S-Video.</span><span class="sxs-lookup"><span data-stu-id="f53a5-191">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO: S-Video.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_fluxo de DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI\_DGV\_SETVIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-193">Um fluxo de vídeo é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-193">A video stream is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-194">O valor inteiro especifica o fluxo de vídeo reproduzido do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f53a5-194">The integer value specifies the video stream played back from the workspace.</span></span> <span data-ttu-id="f53a5-195">Se o fluxo não for especificado e o formato de arquivo não definir um fluxo padrão, o primeiro fluxo de vídeo intercalado fisicamente será reproduzido.</span><span class="sxs-lookup"><span data-stu-id="f53a5-195">If the stream is not specified and the file format does not define a default stream, the first physically interleaved video stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_tonalidade do DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI\_DGV\_SETVIDEO\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-197">Um valor de tonalidade de vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-197">A video tint value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-198">Normalmente, esse ajuste é modelado após o controle de tonalidade de muitos conjuntos de televisão de cor, com 250 definido como verde, 750 definido como vermelho e 0 (ou 1000) definido como azul.</span><span class="sxs-lookup"><span data-stu-id="f53a5-198">Typically, this adjustment is modeled after the tint control of many color television sets, with 250 defined as green, 750 defined as red, and 0 (or 1000) defined as blue.</span></span> <span data-ttu-id="f53a5-199">O valor nominal é sempre 500.</span><span class="sxs-lookup"><span data-stu-id="f53a5-199">The nominal value is always 500.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_saída do DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI\_DGV\_SETVIDEO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-201">O **\_ DGV de \_ \_ brilho do MCI**, **a \_ \_ \_ cor do vídeo MCI DGV**, o MCI DGV setvideo **\_ \_ \_ contraste**, o **MCI \_ DGV \_ setvideo \_ gama**, a **\_ \_ \_ nitidez do MCI DGV** ou o sinalizador de **\_ \_ \_ tonalidade do vídeo MCI DGV** é modificado para que ele afete apenas o sinal exibido e não o que é registrado.</span><span class="sxs-lookup"><span data-stu-id="f53a5-201">The **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** flag is modified so that it affects only the displayed signal and not what is recorded.</span></span> <span data-ttu-id="f53a5-202">Se possível, esse é o padrão ao monitorar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-202">If possible, this is the default when monitoring a file.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>\_DGV de \_ vídeo MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI\_DGV\_SETVIDEO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-204">Um parâmetro de comprimento de transição está incluído no membro **dwOver** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-204">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-205">O comprimento da transição especifica quanto tempo (no formato de hora atual) deve ser necessário para fazer uma alteração.</span><span class="sxs-lookup"><span data-stu-id="f53a5-205">The transition length specifies how long (in the current time format) it should take to make a change.</span></span> <span data-ttu-id="f53a5-206">Se esse sinalizador não for usado, a alteração ocorrerá imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f53a5-206">If this flag is not used, the change occurs immediately.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>\_qualidade de \_ vídeo DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f53a5-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI\_DGV\_SETVIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-208">O membro **lpstrQuality** da estrutura identificada por *lpSetVideo* contém um endereço de um buffer que descreve a qualidade do vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-208">The **lpstrQuality** member of the structure identified by *lpSetVideo* contains an address of a buffer describing the video quality.</span></span> <span data-ttu-id="f53a5-209">Uma cadeia de texto no buffer especifica as características do algoritmo de compactação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-209">A text-string in the buffer specifies the characteristics of the video compression algorithm.</span></span>

<span data-ttu-id="f53a5-210">O sinalizador de **\_ \_ \_ alg DGV do MCI de vídeo** pode ser usado para selecionar um descritor de qualidade para o algoritmo especificado.</span><span class="sxs-lookup"><span data-stu-id="f53a5-210">The **MCI\_DGV\_SETVIDEO\_ALG** flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="f53a5-211">Se esse sinalizador for omitido, o algoritmo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="f53a5-211">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="f53a5-212">Os algoritmos e os nomes de descritores disponíveis dependem do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-212">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="f53a5-213">Cada dispositivo fornece documentação para os algoritmos disponíveis e uma descrição dos nomes de descritores aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="f53a5-213">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="f53a5-214">O comando de [ \_ qualidade do MCI](mci-quality.md) pode definir nomes de descritores adicionais.</span><span class="sxs-lookup"><span data-stu-id="f53a5-214">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span> <span data-ttu-id="f53a5-215">Todos os dispositivos dão suporte aos descritores "Low", "Medium" e "High".</span><span class="sxs-lookup"><span data-stu-id="f53a5-215">All devices support the descriptors "low", "medium", and "high".</span></span> <span data-ttu-id="f53a5-216">O padrão é específico do driver.</span><span class="sxs-lookup"><span data-stu-id="f53a5-216">The default is driver specific.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>\_registro do DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI\_DGV\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-218">Especifica se a gravação inclui ou exclui dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-218">Specifies whether recording includes or excludes video data.</span></span> <span data-ttu-id="f53a5-219">Quando combinado com o **MCI \_ definido \_ como ativado**, os dados de vídeo são registrados.</span><span class="sxs-lookup"><span data-stu-id="f53a5-219">When combined with **MCI\_SET\_ON**, video data is recorded.</span></span> <span data-ttu-id="f53a5-220">Quando combinado com **o \_ MCI \_ definido**, os dados de vídeo são excluídos.</span><span class="sxs-lookup"><span data-stu-id="f53a5-220">When combined with **MCI\_SET\_OFF**, video data is excluded.</span></span> <span data-ttu-id="f53a5-221">O padrão inclui dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-221">The default includes video data.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>\_ \_ \_ número src de DGV do \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f53a5-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI\_DGV\_SETVIDEO\_SRC\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-223">Um número para a fonte de vídeo é especificado no membro **dwSourceNumber** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-223">A number for the video source is specified in the **dwSourceNumber** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-224">Se houver mais de uma entrada do tipo especificado pelo **\_ \_ \_ valor de DGV do MCI**, o valor selecionará a entrada.</span><span class="sxs-lookup"><span data-stu-id="f53a5-224">If there is more than one input of the type specified by **MCI\_DGV\_SETVIDEO\_VALUE**, the value selects the input.</span></span> <span data-ttu-id="f53a5-225">Esse sinalizador deve sempre ser usado com **a \_ \_ \_ fonte de vídeo MCI DGV**.</span><span class="sxs-lookup"><span data-stu-id="f53a5-225">This flag must always be used with **MCI\_DGV\_SETVIDEO\_SOURCE**.</span></span> <span data-ttu-id="f53a5-226">Se **o \_ \_ \_ valor de DGV do MCI** for omitido, no entanto, o número de origem especificado indicará a origem absoluta a ser usada conforme especificado no comando da [ \_ lista de MCI](mci-list.md) .</span><span class="sxs-lookup"><span data-stu-id="f53a5-226">If **MCI\_DGV\_SETVIDEO\_VALUE** is omitted, however, the specified source number indicates the absolute source to use as specified in the [MCI\_LIST](mci-list.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>o \_ DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI\_DGV\_SETVIDEO\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-228">O nome do algoritmo ou o valor de qualidade especificado se aplica às imagens do ainda.</span><span class="sxs-lookup"><span data-stu-id="f53a5-228">The algorithm name or quality value specified applies to still images.</span></span>

<span data-ttu-id="f53a5-229">Cada driver de dispositivo deve dar suporte a um algoritmo de "nenhum", o que significa que não há compactação.</span><span class="sxs-lookup"><span data-stu-id="f53a5-229">Every device driver must support an algorithm of "none", which means no compression.</span></span> <span data-ttu-id="f53a5-230">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="f53a5-230">This is the default.</span></span> <span data-ttu-id="f53a5-231">Nesse caso, os dispositivos de vídeo digital salvam imagens ainda como bitmaps independentes de dispositivo (DIBs) RGB.</span><span class="sxs-lookup"><span data-stu-id="f53a5-231">In this case, digital-video devices save still images as RGB device-independent bitmaps (DIBs).</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_valor do DGV do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI\_DGV\_SETVIDEO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-233">Um valor é incluído no membro **dwValue** da estrutura identificada por *lpSetVideo*.</span><span class="sxs-lookup"><span data-stu-id="f53a5-233">A value is included in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="f53a5-234">O significado do valor é especificado pelo sinalizador de **\_ \_ \_ item de vídeo DGV MCI** .</span><span class="sxs-lookup"><span data-stu-id="f53a5-234">The meaning of the value is specified by the **MCI\_DGV\_SETVIDEO\_ITEM** flag.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado</span><span class="sxs-lookup"><span data-stu-id="f53a5-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-236">Desabilita a saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-236">Disables video output.</span></span> <span data-ttu-id="f53a5-237">Para dispositivos de vídeo digital, desabilitar o vídeo define os pixels no retângulo de destino definido pelo comando [MCI \_ Put](mci-put.md) (ou seu padrão, a região cliente da janela atual) para uma cor sólida, mas não tem efeito sobre o buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="f53a5-237">For digital-video devices, disabling video sets the pixels in the destination rectangle defined by the [MCI\_PUT](mci-put.md) command (or its default, the client region of the current window) to a solid color, but it has no effect on the frame buffer.</span></span> <span data-ttu-id="f53a5-238">Você pode ocultar a janela com o comando de [ \_ janela MCI](mci-window.md) , se desejado.</span><span class="sxs-lookup"><span data-stu-id="f53a5-238">You can hide the window with the [MCI\_WINDOW](mci-window.md) command if desired.</span></span> <span data-ttu-id="f53a5-239">A origem do vídeo, seja o espaço de trabalho ou uma entrada externa, pode continuar armazenando novas imagens no buffer de quadros, mas elas não são exibidas até que o vídeo seja habilitado.</span><span class="sxs-lookup"><span data-stu-id="f53a5-239">The source of video, whether it's the workspace or an external input, might continue to store new images in the frame buffer, but they are not displayed until the video is enabled.</span></span> <span data-ttu-id="f53a5-240">Embora os aplicativos devam usar o \_ comando AUTOVIDEO MCI para controlar essa função, os dispositivos de vídeo digital ainda devem dar suporte a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="f53a5-240">While applications should use the MCI\_SETVIDEO command to control this function, digital-video devices must still support this flag.</span></span> <span data-ttu-id="f53a5-241">O valor padrão após um Open é on.</span><span class="sxs-lookup"><span data-stu-id="f53a5-241">The default value after an open is on.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em</span><span class="sxs-lookup"><span data-stu-id="f53a5-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-243">Habilita a saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f53a5-243">Enables video output.</span></span>

</dd> </dl>

<span data-ttu-id="f53a5-244">Para dispositivos de vídeo digital, o parâmetro *lpSetVideo* aponta para uma estrutura de [**\_ \_ \_ parâmetros de vídeo DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="f53a5-244">For digital-video devices, the *lpSetVideo* parameter points to an [**MCI\_DGV\_SETVIDEO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) structure.</span></span>

<span data-ttu-id="f53a5-245">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo "VCR":</span><span class="sxs-lookup"><span data-stu-id="f53a5-245">The following additional flags are used with the "vcr" device type:</span></span>

<dl> <dt>

<span data-ttu-id="f53a5-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_registro de \_ vídeo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI\_VCR\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-247">Define a gravação de vídeo como ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="f53a5-247">Sets the video recording to on or off.</span></span> <span data-ttu-id="f53a5-248">Usado em conjunto com um dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="f53a5-248">Used in conjunction with one of following flags:</span></span>

-   <span data-ttu-id="f53a5-249">**MCI \_ DEFINIDO \_ em**.</span><span class="sxs-lookup"><span data-stu-id="f53a5-249">**MCI\_SET\_ON**.</span></span> <span data-ttu-id="f53a5-250">Gravação de vídeo ativada.</span><span class="sxs-lookup"><span data-stu-id="f53a5-250">Video recording on.</span></span>
-   <span data-ttu-id="f53a5-251">**MCI \_ definido como \_ desativado**.</span><span class="sxs-lookup"><span data-stu-id="f53a5-251">**MCI\_SET\_OFF**.</span></span> <span data-ttu-id="f53a5-252">Gravação de vídeo desativada.</span><span class="sxs-lookup"><span data-stu-id="f53a5-252">Video recording off.</span></span> <span data-ttu-id="f53a5-253">Pode ser necessário primeiro desativar a gravação de montagem (usando o comando [MCI \_ set](mci-set.md) com o conjunto de **VCR MCI Definir sinalizador de \_ \_ \_ \_ registro de montagem** definido como desativado) antes que a gravação de vídeo possa ser desativada.</span><span class="sxs-lookup"><span data-stu-id="f53a5-253">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the **MCI\_VCR\_SET\_ASSEMBLE\_RECORD** flag set to off) before the video recording can be turned off.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>\_faixa MCI</span><span class="sxs-lookup"><span data-stu-id="f53a5-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-255">O membro **dwTrack** da estrutura identificada por *lpSetVideo* especifica qual faixa é afetada pelo comando.</span><span class="sxs-lookup"><span data-stu-id="f53a5-255">The **dwTrack** member of the structure identified by *lpSetVideo* specifies which track is affected by the command.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_fonte de \_ vídeo do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI\_VCR\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-257">Define a fonte de vídeo e deve ser usada com a marca de **\_ vídeo do VCR MCI \_ \_ para** sinalizar.</span><span class="sxs-lookup"><span data-stu-id="f53a5-257">Sets the video source, and must be used with the **MCI\_VCR\_SETVIDEO\_TO** flag.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_Monitor de \_ vídeo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f53a5-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI\_VCR\_SETVIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-259">Define o monitor de fonte de vídeo e deve ser usado com o conjunto de \_ vídeos do VCR MCI \_ \_ para sinalizar.</span><span class="sxs-lookup"><span data-stu-id="f53a5-259">Sets the video source monitor, and must be used with the MCI\_VCR\_SETVIDEO\_TO flag.</span></span>

</dd> <dt>

<span data-ttu-id="f53a5-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>\_vídeo de VCR do MCI \_ \_ para</span><span class="sxs-lookup"><span data-stu-id="f53a5-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI\_VCR\_SETVIDEO\_TO</span></span>
</dt> <dd>

<span data-ttu-id="f53a5-261">O membro **dwTo** da estrutura identificada por *lpSetVideo* contém uma das seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="f53a5-261">The **dwTo** member of the structure identified by *lpSetVideo* contains one of the following constants:</span></span>

<dl> <dd><span data-ttu-id="f53a5-262">**\_ \_ \_ sintonizador de tipo de src VCR do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f53a5-262">**MCI\_VCR\_SRC\_TYPE\_TUNER**</span></span></dd> <dd><span data-ttu-id="f53a5-263">**\_linha de \_ tipo de src VCR \_ MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f53a5-263">**MCI\_VCR\_SRC\_TYPE\_LINE**</span></span></dd> <dd><span data-ttu-id="f53a5-264">**\_tipo de \_ src do VCR \_ do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f53a5-264">**MCI\_VCR\_SRC\_TYPE\_AUX**</span></span></dd> <dd><span data-ttu-id="f53a5-265">**\_tipo de src VCR do MCI \_ \_ \_ genérico**</span><span class="sxs-lookup"><span data-stu-id="f53a5-265">**MCI\_VCR\_SRC\_TYPE\_GENERIC**</span></span></dd> <dd><span data-ttu-id="f53a5-266">**\_tipo de src de vídeo MCI \_ \_ \_ sem áudio**</span><span class="sxs-lookup"><span data-stu-id="f53a5-266">**MCI\_VCR\_SRC\_TYPE\_MUTE**</span></span></dd> <dd><span data-ttu-id="f53a5-267">**\_saída do \_ tipo de src VCR \_ MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f53a5-267">**MCI\_VCR\_SRC\_TYPE\_OUTPUT**</span></span></dd> <dd><span data-ttu-id="f53a5-268">**\_tipo de src VCR do MCI \_ \_ \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="f53a5-268">**MCI\_VCR\_SRC\_TYPE\_RGB**</span></span></dd> <dd><span data-ttu-id="f53a5-269">**\_número de \_ vídeo do VCR MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f53a5-269">**MCI\_VCR\_SETVIDEO\_NUMBER**</span></span></dd> </dl>

<span data-ttu-id="f53a5-270">O membro **dwNumber** da estrutura identificada por *lpSetVideo* contém a entrada de vídeo (do tipo especificado no membro **dwTo** ) a ser usado.</span><span class="sxs-lookup"><span data-stu-id="f53a5-270">The **dwNumber** member of the structure identified by *lpSetVideo* contains the video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

<span data-ttu-id="f53a5-271">Para dispositivos VCR, o parâmetro *lpSetVideo* aponta para uma estrutura de parâmetros de [**vídeo do \_ VCR \_ \_ MCI**](mci-vcr-setvideo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f53a5-271">For VCR devices, the *lpSetVideo* parameter points to an [**MCI\_VCR\_SETVIDEO\_PARMS**](mci-vcr-setvideo-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53a5-272">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f53a5-272">Requirements</span></span>



| <span data-ttu-id="f53a5-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="f53a5-273">Requirement</span></span> | <span data-ttu-id="f53a5-274">Valor</span><span class="sxs-lookup"><span data-stu-id="f53a5-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f53a5-275">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f53a5-275">Minimum supported client</span></span><br/> | <span data-ttu-id="f53a5-276">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f53a5-276">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f53a5-277">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f53a5-277">Minimum supported server</span></span><br/> | <span data-ttu-id="f53a5-278">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f53a5-278">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f53a5-279">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f53a5-279">Header</span></span><br/>                   | <dl> <span data-ttu-id="f53a5-280"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f53a5-280"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f53a5-281">Confira também</span><span class="sxs-lookup"><span data-stu-id="f53a5-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53a5-282">MCI</span><span class="sxs-lookup"><span data-stu-id="f53a5-282">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f53a5-283">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f53a5-283">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

