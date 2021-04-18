---
title: MCI_LIST comando (mmsystem. h)
description: O \_ comando lista de MCI Obtém informações sobre o número e os tipos de entradas disponíveis para o dispositivo. Os dispositivos de vídeo digital e VCR reconhecem este comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- Multimídia do Windows de comando MCI_LIST
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499794"
---
# <a name="mci_list-command"></a><span data-ttu-id="1cc4a-105">Comando de lista de MCI \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-105">MCI\_LIST command</span></span>

<span data-ttu-id="1cc4a-106">O \_ comando lista de MCI Obtém informações sobre o número e os tipos de entradas disponíveis para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-106">The MCI\_LIST command obtains information about the number and types of inputs available to the device.</span></span> <span data-ttu-id="1cc4a-107">Os dispositivos de vídeo digital e VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="1cc4a-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
);
```



## <a name="parameters"></a><span data-ttu-id="1cc4a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cc4a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc4a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1cc4a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1cc4a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="1cc4a-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="1cc4a-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1cc4a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span><span class="sxs-lookup"><span data-stu-id="1cc4a-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc4a-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="1cc4a-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="1cc4a-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc4a-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1cc4a-118">Return Value</span></span>

<span data-ttu-id="1cc4a-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc4a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cc4a-120">Remarks</span></span>

<span data-ttu-id="1cc4a-121">Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="1cc4a-121">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1cc4a-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>DGV do MCI \_ \_ lista \_ alg</span><span class="sxs-lookup"><span data-stu-id="1cc4a-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI\_DGV\_LIST\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-123">O membro **lpstrAlgorithm** da estrutura identificada por *lpList* contém um endereço de um buffer que contém o nome de um algoritmo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-123">The **lpstrAlgorithm** member of the structure identified by *lpList* contains an address of a buffer containing the name of an algorithm.</span></span> <span data-ttu-id="1cc4a-124">O nome é usado para recuperar os tipos de descritores de qualidade associados a um algoritmo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-124">The name is used to retrieve the types of quality descriptors associated with an algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>\_contagem de \_ lista de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI\_DGV\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-126">Retorna o número de opções do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-126">Returns the number of options of the specified type.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_item de \_ lista de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI\_DGV\_LIST\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-128">Uma constante indicando que o tipo de lista está incluído no membro **dwItem** da estrutura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-128">A constant indicating the list type is included in the **dwItem** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="1cc4a-129">Esse sinalizador é necessário.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-129">This flag is required.</span></span> <span data-ttu-id="1cc4a-130">Use uma das seguintes constantes para indicar o tipo de lista:</span><span class="sxs-lookup"><span data-stu-id="1cc4a-130">Use one of the following constants to indicate the list type:</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>DGV do MCI da \_ \_ lista de \_ áudio \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI\_DGV\_LIST\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-132">O comando deve recuperar os nomes dos algoritmos de áudio.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-132">The command should retrieve names of audio algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>\_qualidade de \_ áudio da lista de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI\_DGV\_LIST\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-134">O comando deve recuperar os níveis de qualidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-134">The command should retrieve audio quality levels.</span></span> <span data-ttu-id="1cc4a-135">Os níveis retornados são associados ao algoritmo referenciado pelo membro **lpstrAlgorithm** da estrutura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-135">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="1cc4a-136">Se esse membro for especificado usando a cadeia de caracteres "Current", as qualidades associadas ao algoritmo atual serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-136">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_fluxo de \_ áudio da lista de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI\_DGV\_LIST\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-138">O comando deve recuperar os nomes dos fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-138">The command should retrieve names of audio streams.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>\_lista de DGV MCI \_ \_ ainda \_ Al</span><span class="sxs-lookup"><span data-stu-id="1cc4a-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI\_DGV\_LIST\_STILL\_AL</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-140">O comando deve recuperar os nomes dos algoritmos ainda.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-140">The command should retrieve names of still algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>a \_ qualidade da lista de DGV MCI é \_ \_ ainda \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI\_DGV\_LIST\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-142">O comando deve recuperar os níveis de qualidade.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-142">The command should retrieve quality levels.</span></span> <span data-ttu-id="1cc4a-143">Os níveis retornados são associados ao algoritmo referenciado pelo membro **lpstrAlgorithm** da estrutura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-143">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="1cc4a-144">Se esse membro for especificado usando a cadeia de caracteres "Current", as qualidades associadas ao algoritmo atual serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-144">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>\_ \_ \_ vídeo alg da lista de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI\_DGV\_LIST\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-146">O comando deve recuperar os nomes dos algoritmos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-146">The command should retrieve names of video algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_qualidade de \_ vídeo da lista de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI\_DGV\_LIST\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-148">O comando deve recuperar os níveis de qualidade do vídeo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-148">The command should retrieve video quality levels.</span></span> <span data-ttu-id="1cc4a-149">Os níveis retornados são associados ao algoritmo referenciado pelo membro **lpstrAlgorithm** da estrutura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-149">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="1cc4a-150">Se esse membro for especificado usando a cadeia de caracteres "Current", as qualidades associadas ao algoritmo atual serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-150">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_fonte de \_ vídeo da lista de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI\_DGV\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-152">O comando deve retornar informações sobre as fontes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-152">The command should return information about the video sources.</span></span> <span data-ttu-id="1cc4a-153">Quando usado com \_ \_ a contagem de lista de DGV MCI \_ , o comando retorna o número de fontes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-153">When used with MCI\_DGV\_LIST\_COUNT, the command returns the number of video sources.</span></span> <span data-ttu-id="1cc4a-154">Quando usado com \_ \_ \_ o número da lista MCI DGV, o comando retorna o tipo de uma fonte de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-154">When used with MCI\_DGV\_LIST\_NUMBER, the command returns the type of a video source.</span></span> <span data-ttu-id="1cc4a-155">O MCI define os seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="1cc4a-155">MCI defines the following types:</span></span>

-   <span data-ttu-id="1cc4a-156">\_src DGV de vídeo de MCI \_ \_ \_ genérico</span><span class="sxs-lookup"><span data-stu-id="1cc4a-156">MCI\_DGV\_SETVIDEO\_SRC\_GENERIC</span></span>
-   <span data-ttu-id="1cc4a-157">NTSC DGV do MCI de \_ \_ vídeo \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-157">MCI\_DGV\_SETVIDEO\_SRC\_NTSC</span></span>
-   <span data-ttu-id="1cc4a-158">\_PAL DGV de \_ vídeo \_ do \_ MCI</span><span class="sxs-lookup"><span data-stu-id="1cc4a-158">MCI\_DGV\_SETVIDEO\_SRC\_PAL</span></span>
-   <span data-ttu-id="1cc4a-159">\_DGV de \_ vídeo MCI \_ \_ RGB</span><span class="sxs-lookup"><span data-stu-id="1cc4a-159">MCI\_DGV\_SETVIDEO\_SRC\_RGB</span></span>
-   <span data-ttu-id="1cc4a-160">SECAM de DGV do MCI de \_ \_ vídeo \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-160">MCI\_DGV\_SETVIDEO\_SRC\_SECAM</span></span>
-   <span data-ttu-id="1cc4a-161">SVIDEO de DGV do MCI de \_ \_ vídeo \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-161">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO</span></span>

<span data-ttu-id="1cc4a-162">Pode haver mais de uma fonte de cada tipo retornada.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-162">There might be more than one source of each type returned.</span></span> <span data-ttu-id="1cc4a-163">O tipo de origem genérico é usado quando mais de um tipo de sinal é permitido para esse conector.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-163">The generic source type is used when more then one type of signal is allowed for that connector.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_fluxo de \_ vídeo da lista de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI\_DGV\_LIST\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-165">O comando deve recuperar os nomes dos fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-165">The command should retrieve names of video streams.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_número da \_ lista de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI\_DGV\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-167">Um índice é especificado no membro **dwNumber** da estrutura identificada por *lpList*.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-167">An index is specified in the **dwNumber** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="1cc4a-168">O índice deve ser um inteiro entre 1 e o valor retornado para o \_ sinalizador de contagem de lista de DGV MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1cc4a-168">The index must be an integer between 1 and the value returned for the MCI\_DGV\_LIST\_COUNT flag.</span></span>

</dd> </dl>

<span data-ttu-id="1cc4a-169">Para dispositivos de vídeo digital, o *lpList* aponta para uma estrutura de parâmetros de [**lista de \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="1cc4a-169">For digital-video devices, *lpList* points to an [**MCI\_DGV\_LIST\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) structure.</span></span>

<span data-ttu-id="1cc4a-170">Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="1cc4a-170">The following additional flags apply to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1cc4a-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_fonte de \_ áudio da lista de VIDEOCASSETEs MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI\_VCR\_LIST\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-172">Listar entradas de áudio ou tipos.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-172">List audio inputs or types.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>\_contagem de lista de videocassetes MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI\_VCR\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-174">Define o membro **dwReturn** da estrutura identificada por *lpList* para o número total de entradas de vídeo ou áudio.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-174">Sets the **dwReturn** member of the structure identified by *lpList* to the total number of video or audio inputs.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>\_número da lista de videocassetes MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI\_VCR\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-176">Define o membro **dwReturn** da estrutura identificada por *lpList* para o tipo da entrada de vídeo ou áudio especificada pelo membro **dwNumber** .</span><span class="sxs-lookup"><span data-stu-id="1cc4a-176">Sets the **dwReturn** member of the structure identified by *lpList* to the type of the video or audio input specified by the **dwNumber** member.</span></span>

</dd> <dt>

<span data-ttu-id="1cc4a-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_fonte de \_ vídeo da lista de VIDEOCASSETEs MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI\_VCR\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="1cc4a-178">Listar entradas ou tipos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-178">List video inputs or types.</span></span>

</dd> </dl>

<span data-ttu-id="1cc4a-179">Para dispositivos VCR, o *lpList* aponta para uma estrutura de parâmetros de [**\_ \_ lista \_ de videocassetes MCI**](mci-vcr-list-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc4a-179">For VCR devices, *lpList* points to an [**MCI\_VCR\_LIST\_PARMS**](mci-vcr-list-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc4a-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc4a-180">Requirements</span></span>



| <span data-ttu-id="1cc4a-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc4a-181">Requirement</span></span> | <span data-ttu-id="1cc4a-182">Valor</span><span class="sxs-lookup"><span data-stu-id="1cc4a-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc4a-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cc4a-183">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc4a-184">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1cc4a-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1cc4a-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cc4a-185">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc4a-186">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1cc4a-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1cc4a-187">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1cc4a-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc4a-188"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cc4a-188"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc4a-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cc4a-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc4a-190">MCI</span><span class="sxs-lookup"><span data-stu-id="1cc4a-190">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1cc4a-191">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="1cc4a-191">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

