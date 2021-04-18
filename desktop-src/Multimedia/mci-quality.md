---
title: MCI_QUALITY comando (mmsystem. h)
description: O comando de qualidade do MCI \_ define um nível de qualidade personalizado para compactação de dados de áudio, vídeo ou ainda imagem. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- Multimídia do Windows de comando MCI_QUALITY
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369214"
---
# <a name="mci_quality-command"></a><span data-ttu-id="636f9-105">\_Comando de qualidade MCI</span><span class="sxs-lookup"><span data-stu-id="636f9-105">MCI\_QUALITY command</span></span>

<span data-ttu-id="636f9-106">O comando de qualidade do MCI \_ define um nível de qualidade personalizado para compactação de dados de áudio, vídeo ou ainda imagem.</span><span class="sxs-lookup"><span data-stu-id="636f9-106">The MCI\_QUALITY command defines a custom quality level for audio, video, or still image data compression.</span></span> <span data-ttu-id="636f9-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="636f9-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="636f9-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="636f9-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
);
```



## <a name="parameters"></a><span data-ttu-id="636f9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="636f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="636f9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="636f9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="636f9-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="636f9-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="636f9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="636f9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="636f9-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="636f9-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="636f9-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="636f9-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="636f9-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span><span class="sxs-lookup"><span data-stu-id="636f9-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span></span>
</dt> <dd>

<span data-ttu-id="636f9-116">Ponteiro para uma estrutura de [**\_ \_ \_ parâmetros de qualidade DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="636f9-116">Pointer to an [**MCI\_DGV\_QUALITY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="636f9-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="636f9-117">Return Value</span></span>

<span data-ttu-id="636f9-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="636f9-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="636f9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="636f9-119">Remarks</span></span>

<span data-ttu-id="636f9-120">O nome definido para esse nível de qualidade pode ser usado ao definir o áudio, o vídeo ou ainda a qualidade com os comandos [MCI \_ SetAudio](mci-setaudio.md) e [MCI \_ setvideo](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="636f9-120">The name defined for this quality level can be used when setting the audio, video, or still quality with the [MCI\_SETAUDIO](mci-setaudio.md) and [MCI\_SETVIDEO](mci-setvideo.md) commands.</span></span>

<span data-ttu-id="636f9-121">Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="636f9-121">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="636f9-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>\_alg qualidade do MCI \_</span><span class="sxs-lookup"><span data-stu-id="636f9-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI\_QUALITY\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="636f9-123">O membro **lpstrAlgorithm** da estrutura identificada por *lpQuality* contém um endereço de um buffer que contém o nome do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="636f9-123">The **lpstrAlgorithm** member of the structure identified by *lpQuality* contains an address of a buffer containing the name of the algorithm.</span></span> <span data-ttu-id="636f9-124">Esse algoritmo deve ser suportado pelo driver de dispositivo e deve ser compatível com o descritor de áudio, ainda ou vídeo que é usado.</span><span class="sxs-lookup"><span data-stu-id="636f9-124">This algorithm must be supported by the device driver, and must be compatible with the audio, still, or video descriptor that is used.</span></span> <span data-ttu-id="636f9-125">Se esse sinalizador for omitido, o algoritmo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="636f9-125">If this flag is omitted, the current algorithm is used.</span></span>

</dd> <dt>

<span data-ttu-id="636f9-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_caixa de diálogo qualidade do MCI \_</span><span class="sxs-lookup"><span data-stu-id="636f9-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI\_QUALITY\_DIALOG</span></span>
</dt> <dd>

<span data-ttu-id="636f9-127">O driver de dispositivo deve exibir uma caixa de diálogo para especificar o nível de qualidade.</span><span class="sxs-lookup"><span data-stu-id="636f9-127">The device driver should display a dialog box for specifying the quality level.</span></span> <span data-ttu-id="636f9-128">A caixa de diálogo tem campos específicos de algoritmo usados internamente pelo driver de dispositivo para criar uma estrutura que descreve um nível de qualidade específico.</span><span class="sxs-lookup"><span data-stu-id="636f9-128">The dialog box has algorithm-specific fields used internally by the device driver to create a structure describing a specific quality level.</span></span>

</dd> <dt>

<span data-ttu-id="636f9-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_alça de qualidade do MCI \_</span><span class="sxs-lookup"><span data-stu-id="636f9-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI\_QUALITY\_HANDLE</span></span>
</dt> <dd>

<span data-ttu-id="636f9-130">O membro **dwHandle** da estrutura identificada por *lpQuality* contém um identificador para uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="636f9-130">The **dwHandle** member of the structure identified by *lpQuality* contains a handle to a structure.</span></span> <span data-ttu-id="636f9-131">A estrutura contém dados específicos de algoritmos que descrevem o nível de qualidade específico.</span><span class="sxs-lookup"><span data-stu-id="636f9-131">The structure contains algorithmic-specific data describing the specific quality level.</span></span> <span data-ttu-id="636f9-132">O formato das estruturas para os algoritmos depende do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="636f9-132">The format of the structures for the algorithms is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="636f9-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_item de qualidade MCI \_</span><span class="sxs-lookup"><span data-stu-id="636f9-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI\_QUALITY\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="636f9-134">Uma constante indicando que o tipo de algoritmo está incluído no membro **dwItem** da estrutura identificada por *lpQuality*.</span><span class="sxs-lookup"><span data-stu-id="636f9-134">A constant indicating the type of algorithm is included in the **dwItem** member of the structure identified by *lpQuality*.</span></span>

</dd> <dt>

<span data-ttu-id="636f9-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_nome da qualidade do MCI \_</span><span class="sxs-lookup"><span data-stu-id="636f9-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI\_QUALITY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="636f9-136">O membro **lpstrname** da estrutura identificada por *lpQuality* contém um endereço de um buffer que contém o descritor de qualidade.</span><span class="sxs-lookup"><span data-stu-id="636f9-136">The **lpstrName** member of the structure identified by *lpQuality* contains an address of a buffer containing the quality descriptor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="636f9-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="636f9-137">Requirements</span></span>



| <span data-ttu-id="636f9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="636f9-138">Requirement</span></span> | <span data-ttu-id="636f9-139">Valor</span><span class="sxs-lookup"><span data-stu-id="636f9-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="636f9-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="636f9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="636f9-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="636f9-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="636f9-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="636f9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="636f9-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="636f9-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="636f9-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="636f9-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="636f9-145"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="636f9-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="636f9-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="636f9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636f9-147">MCI</span><span class="sxs-lookup"><span data-stu-id="636f9-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="636f9-148">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="636f9-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

