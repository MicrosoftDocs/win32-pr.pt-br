---
title: Mensagem de MCIWNDM_GETPALETTE (VFW. h)
description: A \_ mensagem MCIWNDM GetPalette recupera um identificador da paleta usada por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetPalette.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETPALETTE
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008976"
---
# <a name="mciwndm_getpalette-message"></a><span data-ttu-id="cd9b6-105">\_Mensagem MCIWNDM GETpalette</span><span class="sxs-lookup"><span data-stu-id="cd9b6-105">MCIWNDM\_GETPALETTE message</span></span>

<span data-ttu-id="cd9b6-106">A mensagem **MCIWNDM \_ GetPalette** recupera um identificador da paleta usada por um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="cd9b6-106">The **MCIWNDM\_GETPALETTE** message retrieves a handle of the palette used by an MCI device.</span></span> <span data-ttu-id="cd9b6-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="cd9b6-107">You can send this message explicitly or by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span>


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="cd9b6-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cd9b6-108">Return Value</span></span>

<span data-ttu-id="cd9b6-109">Retorna o identificador da paleta se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cd9b6-109">Returns the handle of the palette if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9b6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd9b6-110">Requirements</span></span>



| <span data-ttu-id="cd9b6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd9b6-111">Requirement</span></span> | <span data-ttu-id="cd9b6-112">Valor</span><span class="sxs-lookup"><span data-stu-id="cd9b6-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cd9b6-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd9b6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cd9b6-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd9b6-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cd9b6-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd9b6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cd9b6-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd9b6-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cd9b6-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cd9b6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd9b6-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9b6-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd9b6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd9b6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9b6-120">**MCIWndGetPalette**</span><span class="sxs-lookup"><span data-stu-id="cd9b6-120">**MCIWndGetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





