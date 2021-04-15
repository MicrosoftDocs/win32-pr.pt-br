---
title: Mensagem de ICM_GETDEFAULTQUALITY (VFW. h)
description: A \_ mensagem ICM GETDEFAULTQUALITY consulta um driver de compactação de vídeo para fornecer sua configuração de qualidade padrão. Você pode enviar essa mensagem explicitamente ou usando a macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- Multimídia do Windows de mensagem ICM_GETDEFAULTQUALITY
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454807"
---
# <a name="icm_getdefaultquality-message"></a><span data-ttu-id="87418-105">\_Mensagem GETDEFAULTQUALITY de ICM</span><span class="sxs-lookup"><span data-stu-id="87418-105">ICM\_GETDEFAULTQUALITY message</span></span>

<span data-ttu-id="87418-106">A mensagem **ICM \_ GETDEFAULTQUALITY** consulta um driver de compactação de vídeo para fornecer sua configuração de qualidade padrão.</span><span class="sxs-lookup"><span data-stu-id="87418-106">The **ICM\_GETDEFAULTQUALITY** message queries a video compression driver to provide its default quality setting.</span></span> <span data-ttu-id="87418-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .</span><span class="sxs-lookup"><span data-stu-id="87418-107">You can send this message explicitly or by using the [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macro.</span></span>


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="87418-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87418-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87418-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="87418-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="87418-110">Endereço para conter o valor de qualidade padrão.</span><span class="sxs-lookup"><span data-stu-id="87418-110">Address to contain the default quality value.</span></span> <span data-ttu-id="87418-111">Os valores de qualidade variam de 0 a 10.000.</span><span class="sxs-lookup"><span data-stu-id="87418-111">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87418-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="87418-112">Return Value</span></span>

<span data-ttu-id="87418-113">Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="87418-113">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="87418-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87418-114">Requirements</span></span>



| <span data-ttu-id="87418-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="87418-115">Requirement</span></span> | <span data-ttu-id="87418-116">Valor</span><span class="sxs-lookup"><span data-stu-id="87418-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87418-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87418-117">Minimum supported client</span></span><br/> | <span data-ttu-id="87418-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="87418-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="87418-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87418-119">Minimum supported server</span></span><br/> | <span data-ttu-id="87418-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="87418-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="87418-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="87418-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="87418-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="87418-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87418-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="87418-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87418-124">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="87418-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="87418-125">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="87418-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





