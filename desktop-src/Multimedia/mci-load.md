---
title: MCI_LOAD comando (mmsystem. h)
description: O comando de carregamento do MCI \_ carrega um arquivo. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- Multimídia do Windows de comando MCI_LOAD
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917974"
---
# <a name="mci_load-command"></a><span data-ttu-id="330a7-105">Comando de carregamento do MCI \_</span><span class="sxs-lookup"><span data-stu-id="330a7-105">MCI\_LOAD command</span></span>

<span data-ttu-id="330a7-106">O comando de carregamento do MCI \_ carrega um arquivo.</span><span class="sxs-lookup"><span data-stu-id="330a7-106">The MCI\_LOAD command loads a file.</span></span> <span data-ttu-id="330a7-107">Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="330a7-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="330a7-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="330a7-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
);
```



## <a name="parameters"></a><span data-ttu-id="330a7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="330a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="330a7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="330a7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="330a7-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="330a7-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="330a7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="330a7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="330a7-113">\_Notificação MCI, \_ espera MCI ou, para dispositivos de vídeo digital, teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="330a7-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="330a7-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="330a7-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="330a7-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span><span class="sxs-lookup"><span data-stu-id="330a7-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span></span>
</dt> <dd>

<span data-ttu-id="330a7-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros de carga MCI**](mci-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="330a7-116">Pointer to an [**MCI\_LOAD\_PARMS**](mci-load-parms.md) structure.</span></span> <span data-ttu-id="330a7-117">(Dispositivos com parâmetros adicionais podem substituir essa estrutura por uma estrutura específica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="330a7-117">(Devices with additional parameters might replace this structure with a device-specific structure.</span></span> <span data-ttu-id="330a7-118">Para dispositivos de vídeo digital, o parâmetro **lpLoad** aponta para uma estrutura de [**\_ \_ \_ parâmetros de carga DGV MCI**](/previous-versions//dd743391(v=vs.85)) .)</span><span class="sxs-lookup"><span data-stu-id="330a7-118">For digital-video devices, the **lpLoad** parameter points to an [**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85)) structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="330a7-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="330a7-119">Return Value</span></span>

<span data-ttu-id="330a7-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="330a7-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="330a7-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="330a7-121">Remarks</span></span>

<span data-ttu-id="330a7-122">O seguinte sinalizador adicional se aplica a todos os dispositivos que dão suporte à \_ carga MCI:</span><span class="sxs-lookup"><span data-stu-id="330a7-122">The following additional flag applies to all devices supporting MCI\_LOAD:</span></span>

<dl> <dt>

<span data-ttu-id="330a7-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_arquivo de carregamento MCI \_</span><span class="sxs-lookup"><span data-stu-id="330a7-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI\_LOAD\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="330a7-124">O membro **lpFileName** da estrutura identificada por *lpLoad* contém um endereço de um buffer que contém o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="330a7-124">The **lpfilename** member of the structure identified by *lpLoad* contains an address of a buffer containing the filename.</span></span>

</dd> </dl>

<span data-ttu-id="330a7-125">O seguinte sinalizador adicional é usado com o tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="330a7-125">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="330a7-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="330a7-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="330a7-127">O membro **RC** da estrutura identificada por *lpLoad* contém um retângulo de exibição válido que identifica a área do buffer de vídeo a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="330a7-127">The **rc** member of the structure identified by *lpLoad* contains a valid display rectangle that identifies the area of the video buffer to update.</span></span>

</dd> </dl>

<span data-ttu-id="330a7-128">Para dispositivos de sobreposição de vídeo, o parâmetro *lpLoad* aponta para uma estrutura de [**\_ \_ \_ parâmetros de carga OVLY MCI**](mci-ovly-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="330a7-128">For video-overlay devices, the *lpLoad* parameter points to an [**MCI\_OVLY\_LOAD\_PARMS**](mci-ovly-load-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="330a7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="330a7-129">Requirements</span></span>



| <span data-ttu-id="330a7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="330a7-130">Requirement</span></span> | <span data-ttu-id="330a7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="330a7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="330a7-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="330a7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="330a7-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="330a7-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="330a7-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="330a7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="330a7-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="330a7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="330a7-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="330a7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="330a7-137"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="330a7-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="330a7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="330a7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330a7-139">MCI</span><span class="sxs-lookup"><span data-stu-id="330a7-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="330a7-140">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="330a7-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

