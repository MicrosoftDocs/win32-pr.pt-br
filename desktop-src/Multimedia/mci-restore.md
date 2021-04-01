---
title: MCI_RESTORE comando (mmsystem. h)
description: O \_ comando MCI Restore copia um bitmap de um arquivo para o buffer de quadros. Dispositivos de vídeo digital reconhecem este comando. Esse comando executa a ação oposta do comando de \_ captura MCI.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- Multimídia do Windows de comando MCI_RESTORE
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644977"
---
# <a name="mci_restore-command"></a><span data-ttu-id="737f1-106">\_Comando de restauração MCI</span><span class="sxs-lookup"><span data-stu-id="737f1-106">MCI\_RESTORE command</span></span>

<span data-ttu-id="737f1-107">O \_ comando MCI Restore copia um bitmap de um arquivo para o buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="737f1-107">The MCI\_RESTORE command copies a bitmap from a file to the frame buffer.</span></span> <span data-ttu-id="737f1-108">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="737f1-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="737f1-109">Esse comando executa a ação oposta do comando [de \_ captura MCI](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="737f1-109">This command performs the opposite action of the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

<span data-ttu-id="737f1-110">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="737f1-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
);
```



## <a name="parameters"></a><span data-ttu-id="737f1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="737f1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737f1-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="737f1-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="737f1-113">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="737f1-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="737f1-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="737f1-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="737f1-115">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="737f1-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="737f1-116">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="737f1-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="737f1-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span><span class="sxs-lookup"><span data-stu-id="737f1-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span></span>
</dt> <dd>

<span data-ttu-id="737f1-118">Ponteiro para uma estrutura de [**\_ \_ \_ parâmetros de restauração DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="737f1-118">Pointer to an [**MCI\_DGV\_RESTORE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737f1-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="737f1-119">Return Value</span></span>

<span data-ttu-id="737f1-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="737f1-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="737f1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="737f1-121">Remarks</span></span>

<span data-ttu-id="737f1-122">A implementação pode reconhecer uma variedade de formatos de imagem, mas um DIB (bitmap independente de dispositivo) do Windows é sempre aceito.</span><span class="sxs-lookup"><span data-stu-id="737f1-122">The implementation can recognize a variety of image formats, but a Windows device-independent bitmap (DIB) is always accepted.</span></span>

<span data-ttu-id="737f1-123">Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="737f1-123">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="737f1-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_restaurar DGV \_ MCI \_ de</span><span class="sxs-lookup"><span data-stu-id="737f1-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI\_DGV\_RESTORE\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="737f1-125">O membro **lpstrFileName** da estrutura identificada por *lpRestore* contém um endereço de um buffer que contém o nome de arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="737f1-125">The **lpstrFileName** member of the structure identified by *lpRestore* contains an address of a buffer containing the source filename.</span></span> <span data-ttu-id="737f1-126">O nome do arquivo é necessário.</span><span class="sxs-lookup"><span data-stu-id="737f1-126">The filename is required.</span></span>

</dd> <dt>

<span data-ttu-id="737f1-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>restauração do MCI \_ DGV \_ \_ em</span><span class="sxs-lookup"><span data-stu-id="737f1-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI\_DGV\_RESTORE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="737f1-128">O membro **RC** da estrutura identificada por *lpRestore* contém um retângulo válido.</span><span class="sxs-lookup"><span data-stu-id="737f1-128">The **rc** member of the structure identified by *lpRestore* contains a valid rectangle.</span></span> <span data-ttu-id="737f1-129">O retângulo especifica uma região do buffer de quadro em relação à sua origem.</span><span class="sxs-lookup"><span data-stu-id="737f1-129">The rectangle specifies a region of the frame buffer relative to its origin.</span></span> <span data-ttu-id="737f1-130">O primeiro par de coordenadas especifica o canto superior esquerdo do retângulo; o segundo par especifica a largura e a altura.</span><span class="sxs-lookup"><span data-stu-id="737f1-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="737f1-131">Se esse sinalizador não for especificado, a imagem será copiada para o canto superior esquerdo do buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="737f1-131">If this flag is not specified, the image is copied to the upper left corner of the frame buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="737f1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="737f1-132">Requirements</span></span>



| <span data-ttu-id="737f1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="737f1-133">Requirement</span></span> | <span data-ttu-id="737f1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="737f1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="737f1-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="737f1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="737f1-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="737f1-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="737f1-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="737f1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="737f1-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="737f1-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="737f1-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="737f1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="737f1-140"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="737f1-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="737f1-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="737f1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737f1-142">MCI</span><span class="sxs-lookup"><span data-stu-id="737f1-142">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="737f1-143">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="737f1-143">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

