---
title: Mensagem de ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: A \_ mensagem ICM GETDEFAULTKEYFRAMERATE consulta um driver de compactação de vídeo para seu espaçamento padrão (ou preferencial) de quadro-chave. Você pode enviar essa mensagem explicitamente ou usando a macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- Multimídia do Windows de mensagem ICM_GETDEFAULTKEYFRAMERATE
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369672"
---
# <a name="icm_getdefaultkeyframerate-message"></a><span data-ttu-id="13ebd-105">\_Mensagem GETDEFAULTKEYFRAMERATE de ICM</span><span class="sxs-lookup"><span data-stu-id="13ebd-105">ICM\_GETDEFAULTKEYFRAMERATE message</span></span>

<span data-ttu-id="13ebd-106">A mensagem **ICM \_ GETDEFAULTKEYFRAMERATE** consulta um driver de compactação de vídeo para seu espaçamento padrão (ou preferencial) de quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="13ebd-106">The **ICM\_GETDEFAULTKEYFRAMERATE** message queries a video compression driver for its default (or preferred) key-frame spacing.</span></span> <span data-ttu-id="13ebd-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .</span><span class="sxs-lookup"><span data-stu-id="13ebd-107">You can send this message explicitly or by using the [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) macro.</span></span>


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="13ebd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13ebd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ebd-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="13ebd-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="13ebd-110">Endereço para conter o espaçamento de quadro de chave preferencial.</span><span class="sxs-lookup"><span data-stu-id="13ebd-110">Address to contain the preferred key-frame spacing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ebd-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="13ebd-111">Return Value</span></span>

<span data-ttu-id="13ebd-112">Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="13ebd-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ebd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ebd-113">Requirements</span></span>



| <span data-ttu-id="13ebd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ebd-114">Requirement</span></span> | <span data-ttu-id="13ebd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="13ebd-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13ebd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13ebd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13ebd-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="13ebd-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13ebd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13ebd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13ebd-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="13ebd-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13ebd-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="13ebd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="13ebd-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="13ebd-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13ebd-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="13ebd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ebd-123">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="13ebd-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="13ebd-124">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="13ebd-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





