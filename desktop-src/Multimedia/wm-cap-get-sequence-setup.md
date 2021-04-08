---
title: Mensagem de WM_CAP_GET_SEQUENCE_SETUP (VFW. h)
description: A \_ mensagem de configuração de sequência Get da Cap do WM \_ \_ \_ recupera as configurações atuais dos parâmetros de captura de streaming. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureGetSetup.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_SEQUENCE_SETUP
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917966"
---
# <a name="wm_cap_get_sequence_setup-message"></a><span data-ttu-id="ae02c-105">\_Mensagem de \_ \_ configuração da sequência get \_ do WM Cap</span><span class="sxs-lookup"><span data-stu-id="ae02c-105">WM\_CAP\_GET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="ae02c-106">A mensagem de **\_ \_ \_ \_ configuração de sequência Get da Cap do WM** recupera as configurações atuais dos parâmetros de captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="ae02c-106">The **WM\_CAP\_GET\_SEQUENCE\_SETUP** message retrieves the current settings of the streaming capture parameters.</span></span> <span data-ttu-id="ae02c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) .</span><span class="sxs-lookup"><span data-stu-id="ae02c-107">You can send this message explicitly or by using the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro.</span></span>


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="ae02c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae02c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae02c-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="ae02c-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="ae02c-110">Tamanho, em bytes, da estrutura referenciada por **s**.</span><span class="sxs-lookup"><span data-stu-id="ae02c-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="ae02c-111"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="ae02c-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="ae02c-112">Ponteiro para uma estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="ae02c-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae02c-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ae02c-113">Return Value</span></span>

<span data-ttu-id="ae02c-114">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ae02c-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae02c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae02c-115">Remarks</span></span>

<span data-ttu-id="ae02c-116">Para obter informações sobre os parâmetros usados para controlar a captura de streaming, consulte a estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="ae02c-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae02c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae02c-117">Requirements</span></span>



| <span data-ttu-id="ae02c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae02c-118">Requirement</span></span> | <span data-ttu-id="ae02c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ae02c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ae02c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae02c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae02c-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ae02c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ae02c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae02c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae02c-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ae02c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ae02c-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ae02c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae02c-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae02c-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae02c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae02c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae02c-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ae02c-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ae02c-128">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ae02c-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





