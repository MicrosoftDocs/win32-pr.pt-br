---
title: Mensagem de MCIWNDM_GETACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM GETACTIVETIMER recupera o período de atualização usado quando a janela MCIWnd é a janela ativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETACTIVETIMER
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086506"
---
# <a name="mciwndm_getactivetimer-message"></a><span data-ttu-id="4a2d0-105">\_Mensagem MCIWNDM GETACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="4a2d0-105">MCIWNDM\_GETACTIVETIMER message</span></span>

<span data-ttu-id="4a2d0-106">A mensagem **MCIWNDM \_ GETACTIVETIMER** recupera o período de atualização usado quando a janela MCIWnd é a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="4a2d0-106">The **MCIWNDM\_GETACTIVETIMER** message retrieves the update period used when the MCIWnd window is the active window.</span></span> <span data-ttu-id="4a2d0-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="4a2d0-107">You can send this message explicitly or by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span>


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="4a2d0-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4a2d0-108">Return Value</span></span>

<span data-ttu-id="4a2d0-109">Retorna o período de atualização em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="4a2d0-109">Returns the update period in milliseconds.</span></span> <span data-ttu-id="4a2d0-110">O padrão é 500 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="4a2d0-110">The default is 500 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2d0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a2d0-111">Requirements</span></span>



| <span data-ttu-id="4a2d0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2d0-112">Requirement</span></span> | <span data-ttu-id="4a2d0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4a2d0-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4a2d0-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a2d0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2d0-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a2d0-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4a2d0-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a2d0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2d0-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a2d0-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4a2d0-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4a2d0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a2d0-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2d0-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2d0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a2d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2d0-121">**MCIWndGetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="4a2d0-121">**MCIWndGetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





