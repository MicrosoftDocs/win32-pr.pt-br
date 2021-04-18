---
title: Mensagem de MCIWNDM_GETINACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM GETINACTIVETIMER recupera o período de atualização usado quando a janela MCIWnd é a janela inativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETINACTIVETIMER
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810307"
---
# <a name="mciwndm_getinactivetimer-message"></a><span data-ttu-id="0b08f-105">\_Mensagem MCIWNDM GETINACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="0b08f-105">MCIWNDM\_GETINACTIVETIMER message</span></span>

<span data-ttu-id="0b08f-106">A mensagem **MCIWNDM \_ GETINACTIVETIMER** recupera o período de atualização usado quando a janela MCIWnd é a janela inativa.</span><span class="sxs-lookup"><span data-stu-id="0b08f-106">The **MCIWNDM\_GETINACTIVETIMER** message retrieves the update period used when the MCIWnd window is the inactive window.</span></span> <span data-ttu-id="0b08f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="0b08f-107">You can send this message explicitly or by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span>


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="0b08f-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0b08f-108">Return Value</span></span>

<span data-ttu-id="0b08f-109">Retorna o período de atualização, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="0b08f-109">Returns the update period, in milliseconds.</span></span> <span data-ttu-id="0b08f-110">O valor padrão é 2000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="0b08f-110">The default value is 2000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b08f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b08f-111">Requirements</span></span>



| <span data-ttu-id="0b08f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b08f-112">Requirement</span></span> | <span data-ttu-id="0b08f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="0b08f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0b08f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b08f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0b08f-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b08f-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0b08f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b08f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0b08f-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b08f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0b08f-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0b08f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b08f-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b08f-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b08f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b08f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b08f-121">**MCIWndGetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="0b08f-121">**MCIWndGetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





