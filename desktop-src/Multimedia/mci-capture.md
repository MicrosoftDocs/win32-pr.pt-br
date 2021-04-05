---
title: MCI_CAPTURE comando (mmsystem. h)
description: O \_ comando de captura MCI captura o conteúdo do buffer de quadro e o armazena em um arquivo especificado. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- Multimídia do Windows de comando MCI_CAPTURE
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918760"
---
# <a name="mci_capture-command"></a><span data-ttu-id="05c1a-105">\_Comando de captura MCI</span><span class="sxs-lookup"><span data-stu-id="05c1a-105">MCI\_CAPTURE command</span></span>

<span data-ttu-id="05c1a-106">O \_ comando de captura MCI captura o conteúdo do buffer de quadro e o armazena em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="05c1a-106">The MCI\_CAPTURE command captures the contents of the frame buffer and stores it in a specified file.</span></span> <span data-ttu-id="05c1a-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="05c1a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="05c1a-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="05c1a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a><span data-ttu-id="05c1a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05c1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05c1a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="05c1a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="05c1a-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="05c1a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="05c1a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="05c1a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="05c1a-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="05c1a-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="05c1a-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="05c1a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="05c1a-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span><span class="sxs-lookup"><span data-stu-id="05c1a-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span></span>
</dt> <dd>

<span data-ttu-id="05c1a-116">Ponteiro para uma estrutura de [**\_ \_ \_ parâmetros de captura DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="05c1a-116">Pointer to an [**MCI\_DGV\_CAPTURE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05c1a-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="05c1a-117">Return Value</span></span>

<span data-ttu-id="05c1a-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="05c1a-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="05c1a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="05c1a-119">Remarks</span></span>

<span data-ttu-id="05c1a-120">Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="05c1a-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="05c1a-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>\_ \_ captura de DGV MCI \_ como</span><span class="sxs-lookup"><span data-stu-id="05c1a-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI\_DGV\_CAPTURE\_AS</span></span>
</dt> <dd>

<span data-ttu-id="05c1a-122">O membro **lpstrFileName** da estrutura identificada por *lpCapture* contém um endereço de um buffer que especifica o caminho e o nome de arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="05c1a-122">The **lpstrFileName** member of the structure identified by *lpCapture* contains an address of a buffer specifying the destination path and filename.</span></span> <span data-ttu-id="05c1a-123">(Esse sinalizador é necessário.)</span><span class="sxs-lookup"><span data-stu-id="05c1a-123">(This flag is required.)</span></span>

</dd> <dt>

<span data-ttu-id="05c1a-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_ \_ captura de DGV MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="05c1a-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI\_DGV\_CAPTURE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="05c1a-125">O membro **RC** da estrutura identificada por *lpCapture* contém um retângulo válido.</span><span class="sxs-lookup"><span data-stu-id="05c1a-125">The **rc** member of the structure identified by *lpCapture* contains a valid rectangle.</span></span> <span data-ttu-id="05c1a-126">O retângulo especifica a região retangular dentro do buffer de quadro que é recortado e salvo em disco.</span><span class="sxs-lookup"><span data-stu-id="05c1a-126">The rectangle specifies the rectangular region within the frame buffer that is cropped and saved to disk.</span></span> <span data-ttu-id="05c1a-127">Se omitido, a região cortada usa como padrão o retângulo especificado ou padronizado em um comando anterior [ \_ Put](mci-put.md) que especifica a área de origem dessa instância do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="05c1a-127">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [MCI\_PUT](mci-put.md) command that specifies the source area for this instance of the device driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05c1a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c1a-128">Requirements</span></span>



| <span data-ttu-id="05c1a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c1a-129">Requirement</span></span> | <span data-ttu-id="05c1a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="05c1a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c1a-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c1a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="05c1a-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="05c1a-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="05c1a-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c1a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="05c1a-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="05c1a-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="05c1a-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="05c1a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="05c1a-136"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05c1a-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05c1a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="05c1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c1a-138">MCI</span><span class="sxs-lookup"><span data-stu-id="05c1a-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="05c1a-139">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="05c1a-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

