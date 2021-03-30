---
title: Mensagem de WM_CAP_SET_MCI_DEVICE (VFW. h)
description: A \_ mensagem do dispositivo MCI do conjunto de Cap do WM \_ \_ \_ especifica o nome do dispositivo de vídeo MCI a ser usado para capturar dados. Você pode enviar essa mensagem explicitamente ou usando a macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_MCI_DEVICE
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644288"
---
# <a name="wm_cap_set_mci_device-message"></a><span data-ttu-id="7e97d-105">\_Mensagem do \_ \_ dispositivo MCI do conjunto de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="7e97d-105">WM\_CAP\_SET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="7e97d-106">A mensagem do **\_ \_ \_ \_ dispositivo MCI do conjunto de Cap do WM** especifica o nome do dispositivo de vídeo MCI a ser usado para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="7e97d-106">The **WM\_CAP\_SET\_MCI\_DEVICE** message specifies the name of the MCI video device to be used to capture data.</span></span> <span data-ttu-id="7e97d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .</span><span class="sxs-lookup"><span data-stu-id="7e97d-107">You can send this message explicitly or by using the [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) macro.</span></span>


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="7e97d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e97d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e97d-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="7e97d-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="7e97d-110">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e97d-110">Pointer to a null-terminated string containing the name of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e97d-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7e97d-111">Return Value</span></span>

<span data-ttu-id="7e97d-112">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7e97d-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e97d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e97d-113">Remarks</span></span>

<span data-ttu-id="7e97d-114">Essa mensagem armazena o nome do dispositivo MCI em uma estrutura interna.</span><span class="sxs-lookup"><span data-stu-id="7e97d-114">This message stores the MCI device name in an internal structure.</span></span> <span data-ttu-id="7e97d-115">Ele não abre nem acessa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e97d-115">It does not open or access the device.</span></span> <span data-ttu-id="7e97d-116">O nome do dispositivo padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7e97d-116">The default device name is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e97d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e97d-117">Requirements</span></span>



| <span data-ttu-id="7e97d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e97d-118">Requirement</span></span> | <span data-ttu-id="7e97d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7e97d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7e97d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e97d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7e97d-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7e97d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7e97d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e97d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7e97d-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7e97d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7e97d-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7e97d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e97d-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e97d-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e97d-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7e97d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e97d-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7e97d-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7e97d-128">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7e97d-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





