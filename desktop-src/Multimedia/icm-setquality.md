---
title: Mensagem de ICM_SETQUALITY (VFW. h)
description: A \_ mensagem ICM setquality fornece um driver de compactação de vídeo com um nível de qualidade a ser usado durante a compactação.
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- Multimídia do Windows de mensagem ICM_SETQUALITY
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1523996ad336e64d4b34143cc26cd8d0937d5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369936"
---
# <a name="icm_setquality-message"></a><span data-ttu-id="3d76f-104">\_Mensagem ICM SETquality</span><span class="sxs-lookup"><span data-stu-id="3d76f-104">ICM\_SETQUALITY message</span></span>

<span data-ttu-id="3d76f-105">A mensagem **ICM \_ setquality** fornece um driver de compactação de vídeo com um nível de qualidade a ser usado durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="3d76f-105">The **ICM\_SETQUALITY** message provides a video compression driver with a quality level to use during compression.</span></span>


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="3d76f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d76f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d76f-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="3d76f-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="3d76f-108">Novo valor de qualidade.</span><span class="sxs-lookup"><span data-stu-id="3d76f-108">New quality value.</span></span> <span data-ttu-id="3d76f-109">Os valores de qualidade variam de 0 a 10.000.</span><span class="sxs-lookup"><span data-stu-id="3d76f-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d76f-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3d76f-110">Return Value</span></span>

<span data-ttu-id="3d76f-111">Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="3d76f-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d76f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d76f-112">Requirements</span></span>



| <span data-ttu-id="3d76f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d76f-113">Requirement</span></span> | <span data-ttu-id="3d76f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3d76f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3d76f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d76f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3d76f-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d76f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3d76f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d76f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3d76f-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d76f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3d76f-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3d76f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d76f-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d76f-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d76f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d76f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d76f-122">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="3d76f-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3d76f-123">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="3d76f-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





