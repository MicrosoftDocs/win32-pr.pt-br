---
title: Mensagem de WM_CAP_SET_SEQUENCE_SETUP (VFW. h)
description: A mensagem de configuração da sequência do WM \_ Cap \_ set \_ \_ define os parâmetros de configuração usados com o streaming Capture. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSetSetup.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_SEQUENCE_SETUP
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499766"
---
# <a name="wm_cap_set_sequence_setup-message"></a><span data-ttu-id="6ee30-105">Mensagem de configuração da sequência do WM \_ Cap \_ set \_ \_</span><span class="sxs-lookup"><span data-stu-id="6ee30-105">WM\_CAP\_SET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="6ee30-106">A mensagem de **configuração da sequência do WM \_ Cap \_ \_ \_ set** define os parâmetros de configuração usados com o streaming Capture.</span><span class="sxs-lookup"><span data-stu-id="6ee30-106">The **WM\_CAP\_SET\_SEQUENCE\_SETUP** message sets the configuration parameters used with streaming capture.</span></span> <span data-ttu-id="6ee30-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) .</span><span class="sxs-lookup"><span data-stu-id="6ee30-107">You can send this message explicitly or by using the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro.</span></span>


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a><span data-ttu-id="6ee30-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ee30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee30-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="6ee30-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="6ee30-110">Tamanho, em bytes, da estrutura referenciada por **s**.</span><span class="sxs-lookup"><span data-stu-id="6ee30-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="6ee30-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span><span class="sxs-lookup"><span data-stu-id="6ee30-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span></span>
</dt> <dd>

<span data-ttu-id="6ee30-112">Ponteiro para uma estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="6ee30-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee30-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6ee30-113">Return Value</span></span>

<span data-ttu-id="6ee30-114">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6ee30-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ee30-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ee30-115">Remarks</span></span>

<span data-ttu-id="6ee30-116">Para obter informações sobre os parâmetros usados para controlar a captura de streaming, consulte a estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="6ee30-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee30-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ee30-117">Requirements</span></span>



| <span data-ttu-id="6ee30-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee30-118">Requirement</span></span> | <span data-ttu-id="6ee30-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee30-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6ee30-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ee30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee30-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ee30-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6ee30-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ee30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee30-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ee30-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6ee30-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6ee30-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ee30-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee30-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee30-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ee30-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee30-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="6ee30-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6ee30-128">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="6ee30-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





