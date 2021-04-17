---
title: Mensagem de WM_CAP_GET_MCI_DEVICE (VFW. h)
description: A mensagem do dispositivo do WM \_ Cap \_ Get \_ MCI \_ recupera o nome de um dispositivo MCI definido anteriormente com \_ a \_ \_ mensagem do dispositivo MCI de conjunto de Cap do WM \_ . Você pode enviar essa mensagem explicitamente ou usando a macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_MCI_DEVICE
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454598"
---
# <a name="wm_cap_get_mci_device-message"></a><span data-ttu-id="e5b96-105">\_Mensagem do \_ \_ dispositivo MCI da obtenção do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="e5b96-105">WM\_CAP\_GET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="e5b96-106">A mensagem do **dispositivo do WM \_ Cap \_ Get \_ MCI \_** recupera o nome de um dispositivo MCI definido anteriormente com a mensagem do [**\_ \_ \_ \_ dispositivo MCI de conjunto de Cap do WM**](wm-cap-set-mci-device.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b96-106">The **WM\_CAP\_GET\_MCI\_DEVICE** message retrieves the name of an MCI device previously set with the [**WM\_CAP\_SET\_MCI\_DEVICE**](wm-cap-set-mci-device.md) message.</span></span> <span data-ttu-id="e5b96-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="e5b96-107">You can send this message explicitly or by using the [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) macro.</span></span>


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="e5b96-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5b96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b96-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="e5b96-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="e5b96-110">Comprimento, em bytes, do buffer referenciado por **szName**.</span><span class="sxs-lookup"><span data-stu-id="e5b96-110">Length, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="e5b96-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="e5b96-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="e5b96-112">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e5b96-112">Pointer to a null-terminated string that contains the MCI device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b96-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e5b96-113">Return Value</span></span>

<span data-ttu-id="e5b96-114">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e5b96-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b96-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5b96-115">Requirements</span></span>



| <span data-ttu-id="e5b96-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b96-116">Requirement</span></span> | <span data-ttu-id="e5b96-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e5b96-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e5b96-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5b96-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b96-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5b96-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e5b96-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5b96-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b96-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5b96-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e5b96-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e5b96-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5b96-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b96-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b96-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5b96-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b96-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="e5b96-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e5b96-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="e5b96-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





