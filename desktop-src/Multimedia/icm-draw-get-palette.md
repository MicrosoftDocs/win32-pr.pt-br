---
title: Mensagem de ICM_DRAW_GET_PALETTE (VFW. h)
description: A \_ mensagem ICM Draw \_ obter \_ paleta solicita um driver de renderização para retornar uma paleta.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_GET_PALETTE
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008983"
---
# <a name="icm_draw_get_palette-message"></a><span data-ttu-id="72e45-104">\_Mensagem de \_ obtenção de \_ paleta do ICM Draw</span><span class="sxs-lookup"><span data-stu-id="72e45-104">ICM\_DRAW\_GET\_PALETTE message</span></span>

<span data-ttu-id="72e45-105">A mensagem **ICM \_ draw \_ obter \_ paleta** solicita um driver de renderização para retornar uma paleta.</span><span class="sxs-lookup"><span data-stu-id="72e45-105">The **ICM\_DRAW\_GET\_PALETTE** message requests a rendering driver to return a palette.</span></span>


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="72e45-106">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="72e45-106">Return Value</span></span>

<span data-ttu-id="72e45-107">O driver deve retornar um dos seguintes: um identificador da paleta que está sendo usada, **nulo** se não tiver um identificador para retornar ou ICERR sem \_ suporte se não oferecer suporte a paletas.</span><span class="sxs-lookup"><span data-stu-id="72e45-107">The driver should return one of the following: a handle of the palette being used, **NULL** if it doesn't have a handle to return, or ICERR\_UNSUPPORTED if it doesn't support palettes.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e45-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72e45-108">Requirements</span></span>



| <span data-ttu-id="72e45-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="72e45-109">Requirement</span></span> | <span data-ttu-id="72e45-110">Valor</span><span class="sxs-lookup"><span data-stu-id="72e45-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="72e45-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72e45-111">Minimum supported client</span></span><br/> | <span data-ttu-id="72e45-112">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72e45-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="72e45-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72e45-113">Minimum supported server</span></span><br/> | <span data-ttu-id="72e45-114">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72e45-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72e45-115">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="72e45-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="72e45-116"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="72e45-116"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72e45-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="72e45-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e45-118">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="72e45-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="72e45-119">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="72e45-119">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





