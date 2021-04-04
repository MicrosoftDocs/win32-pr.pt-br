---
title: Mensagem de WM_CAP_GET_STATUS (VFW. h)
description: A \_ mensagem de status obter do WM Cap \_ \_ recupera o status da janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_STATUS
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008830"
---
# <a name="wm_cap_get_status-message"></a><span data-ttu-id="13aa0-105">\_Mensagem de \_ status de obtenção de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="13aa0-105">WM\_CAP\_GET\_STATUS message</span></span>

<span data-ttu-id="13aa0-106">A mensagem de **\_ \_ \_ status obter do WM Cap** recupera o status da janela de captura.</span><span class="sxs-lookup"><span data-stu-id="13aa0-106">The **WM\_CAP\_GET\_STATUS** message retrieves the status of the capture window.</span></span> <span data-ttu-id="13aa0-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .</span><span class="sxs-lookup"><span data-stu-id="13aa0-107">You can send this message explicitly or by using the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro.</span></span>


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="13aa0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13aa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13aa0-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="13aa0-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="13aa0-110">Tamanho, em bytes, da estrutura referenciada por **s**.</span><span class="sxs-lookup"><span data-stu-id="13aa0-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="13aa0-111"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="13aa0-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="13aa0-112">Ponteiro para uma estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .</span><span class="sxs-lookup"><span data-stu-id="13aa0-112">Pointer to a [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13aa0-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="13aa0-113">Return Value</span></span>

<span data-ttu-id="13aa0-114">Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="13aa0-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="13aa0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="13aa0-115">Remarks</span></span>

<span data-ttu-id="13aa0-116">A estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contém o estado atual da janela de captura.</span><span class="sxs-lookup"><span data-stu-id="13aa0-116">The [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure contains the current state of the capture window.</span></span> <span data-ttu-id="13aa0-117">Como esse estado é dinâmico e muda em resposta a várias mensagens, o aplicativo deve inicializar essa estrutura após enviar a mensagem de [**VIDEOFORMAT do WM \_ Cap \_ DLG \_**](wm-cap-dlg-videoformat.md) (ou usar a macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) e sempre que precisar habilitar itens de menu ou determinar o estado real da janela.</span><span class="sxs-lookup"><span data-stu-id="13aa0-117">Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro) and whenever it needs to enable menu items or determine the actual state of the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="13aa0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13aa0-118">Requirements</span></span>



| <span data-ttu-id="13aa0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="13aa0-119">Requirement</span></span> | <span data-ttu-id="13aa0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="13aa0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13aa0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13aa0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="13aa0-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="13aa0-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13aa0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13aa0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="13aa0-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="13aa0-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13aa0-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="13aa0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="13aa0-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="13aa0-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13aa0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="13aa0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13aa0-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="13aa0-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="13aa0-129">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="13aa0-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





