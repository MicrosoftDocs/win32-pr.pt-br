---
title: Mensagem de WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: A \_ \_ mensagem obter Caps do driver do WM Cap \_ \_ retorna os recursos de hardware do driver de captura atualmente conectados a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_GET_CAPS
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499768"
---
# <a name="wm_cap_driver_get_caps-message"></a><span data-ttu-id="7b86e-105">\_Mensagem de \_ obtenção do driver \_ \_ do WM Cap</span><span class="sxs-lookup"><span data-stu-id="7b86e-105">WM\_CAP\_DRIVER\_GET\_CAPS message</span></span>

<span data-ttu-id="7b86e-106">A **mensagem \_ \_ \_ obter \_ Caps do driver do WM Cap** retorna os recursos de hardware do driver de captura atualmente conectados a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="7b86e-106">The **WM\_CAP\_DRIVER\_GET\_CAPS** message returns the hardware capabilities of the capture driver currently connected to a capture window.</span></span> <span data-ttu-id="7b86e-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .</span><span class="sxs-lookup"><span data-stu-id="7b86e-107">You can send this message explicitly or by using the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a><span data-ttu-id="7b86e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b86e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b86e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="7b86e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="7b86e-110">Tamanho, em bytes, da estrutura referenciada por **s**.</span><span class="sxs-lookup"><span data-stu-id="7b86e-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="7b86e-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span><span class="sxs-lookup"><span data-stu-id="7b86e-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span></span>
</dt> <dd>

<span data-ttu-id="7b86e-112">Ponteiro para a estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) para conter os recursos de hardware.</span><span class="sxs-lookup"><span data-stu-id="7b86e-112">Pointer to the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure to contain the hardware capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b86e-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7b86e-113">Return Value</span></span>

<span data-ttu-id="7b86e-114">Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="7b86e-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b86e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b86e-115">Remarks</span></span>

<span data-ttu-id="7b86e-116">Os recursos retornados em [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) são constantes para um determinado driver de captura.</span><span class="sxs-lookup"><span data-stu-id="7b86e-116">The capabilities returned in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) are constant for a given capture driver.</span></span> <span data-ttu-id="7b86e-117">Os aplicativos precisam recuperar essas informações uma vez quando o driver de captura é conectado primeiro a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="7b86e-117">Applications need to retrieve this information once when the capture driver is first connected to a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b86e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b86e-118">Requirements</span></span>



| <span data-ttu-id="7b86e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b86e-119">Requirement</span></span> | <span data-ttu-id="7b86e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7b86e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7b86e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b86e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7b86e-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b86e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7b86e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b86e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7b86e-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b86e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b86e-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7b86e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b86e-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b86e-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b86e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b86e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b86e-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7b86e-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7b86e-129">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7b86e-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





