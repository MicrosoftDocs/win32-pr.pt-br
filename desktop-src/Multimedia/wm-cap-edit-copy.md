---
title: Mensagem de WM_CAP_EDIT_COPY (VFW. h)
description: A mensagem de cópia de edição da Cap do WM \_ \_ \_ copia o conteúdo do buffer de quadros de vídeo e a paleta associada para a área de transferência. Você pode enviar essa mensagem explicitamente ou usando a macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- Multimídia do Windows de mensagem WM_CAP_EDIT_COPY
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085896"
---
# <a name="wm_cap_edit_copy-message"></a><span data-ttu-id="ade46-105">\_Mensagem de \_ cópia de edição do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="ade46-105">WM\_CAP\_EDIT\_COPY message</span></span>

<span data-ttu-id="ade46-106">A mensagem de cópia de edição da Cap do WM copia o conteúdo do buffer de quadros de vídeo e a paleta associada para a área de transferência. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ade46-106">The **WM\_CAP\_EDIT\_COPY** message copies the contents of the video frame buffer and associated palette to the clipboard.</span></span> <span data-ttu-id="ade46-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .</span><span class="sxs-lookup"><span data-stu-id="ade46-107">You can send this message explicitly or by using the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro.</span></span>


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="ade46-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ade46-108">Return Value</span></span>

<span data-ttu-id="ade46-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ade46-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ade46-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ade46-110">Requirements</span></span>



| <span data-ttu-id="ade46-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ade46-111">Requirement</span></span> | <span data-ttu-id="ade46-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ade46-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ade46-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ade46-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ade46-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ade46-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ade46-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ade46-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ade46-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ade46-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ade46-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ade46-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ade46-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ade46-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ade46-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ade46-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade46-120">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ade46-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ade46-121">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ade46-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





