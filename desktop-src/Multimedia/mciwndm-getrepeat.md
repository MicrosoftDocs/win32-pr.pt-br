---
title: Mensagem de MCIWNDM_GETREPEAT (VFW. h)
description: A \_ mensagem MCIWNDM getrepetir determina se a reprodução contínua foi ativada. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetRepeat.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETREPEAT
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085248"
---
# <a name="mciwndm_getrepeat-message"></a><span data-ttu-id="50ef3-105">MCIWNDM \_ getrepetir mensagem</span><span class="sxs-lookup"><span data-stu-id="50ef3-105">MCIWNDM\_GETREPEAT message</span></span>

<span data-ttu-id="50ef3-106">A mensagem **MCIWNDM \_ getrepetir** determina se a reprodução contínua foi ativada.</span><span class="sxs-lookup"><span data-stu-id="50ef3-106">The **MCIWNDM\_GETREPEAT** message determines if continuous playback has been activated.</span></span> <span data-ttu-id="50ef3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="50ef3-107">You can send this message explicitly or by using the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="50ef3-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="50ef3-108">Return Value</span></span>

<span data-ttu-id="50ef3-109">Retornará **true** se a reprodução contínua for ativada ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="50ef3-109">Returns **TRUE** if continuous playback is activated or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ef3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50ef3-110">Requirements</span></span>



| <span data-ttu-id="50ef3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="50ef3-111">Requirement</span></span> | <span data-ttu-id="50ef3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="50ef3-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="50ef3-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50ef3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="50ef3-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="50ef3-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="50ef3-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50ef3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="50ef3-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="50ef3-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="50ef3-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="50ef3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="50ef3-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="50ef3-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50ef3-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="50ef3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ef3-120">**MCIWndGetRepeat**</span><span class="sxs-lookup"><span data-stu-id="50ef3-120">**MCIWndGetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





