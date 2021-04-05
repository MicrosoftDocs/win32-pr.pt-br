---
title: Mensagem de ICM_GETQUALITY (VFW. h)
description: A \_ mensagem ICM getquality consulta um driver de compactação de vídeo para retornar sua configuração de qualidade atual.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- Multimídia do Windows de mensagem ICM_GETQUALITY
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c4fa2a26e1fe5fa111585ce0a59422a2fe9b072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919218"
---
# <a name="icm_getquality-message"></a><span data-ttu-id="c5d1d-104">\_Mensagem de GETquality do ICM</span><span class="sxs-lookup"><span data-stu-id="c5d1d-104">ICM\_GETQUALITY message</span></span>

<span data-ttu-id="c5d1d-105">A mensagem **ICM \_ getquality** consulta um driver de compactação de vídeo para retornar sua configuração de qualidade atual.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-105">The **ICM\_GETQUALITY** message queries a video compression driver to return its current quality setting.</span></span>


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="c5d1d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5d1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d1d-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="c5d1d-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="c5d1d-108">Endereço para conter o valor de qualidade atual.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-108">Address to contain the current quality value.</span></span> <span data-ttu-id="c5d1d-109">Os valores de qualidade variam de 0 a 10.000.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d1d-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c5d1d-110">Return Value</span></span>

<span data-ttu-id="c5d1d-111">Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="c5d1d-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d1d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5d1d-112">Requirements</span></span>



| <span data-ttu-id="c5d1d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5d1d-113">Requirement</span></span> | <span data-ttu-id="c5d1d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c5d1d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5d1d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5d1d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d1d-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c5d1d-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c5d1d-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5d1d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d1d-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c5d1d-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c5d1d-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c5d1d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5d1d-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d1d-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d1d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5d1d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d1d-122">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="c5d1d-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c5d1d-123">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="c5d1d-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





