---
title: Mensagem de MCIWNDM_CAN_EJECT (VFW. h)
description: A MCIWNDM \_ pode \_ ejetar a mensagem para determinar se um dispositivo MCI pode ejetar sua mídia. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_EJECT
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645196"
---
# <a name="mciwndm_can_eject-message"></a><span data-ttu-id="65258-105">MCIWNDM \_ pode \_ ejetar a mensagem</span><span class="sxs-lookup"><span data-stu-id="65258-105">MCIWNDM\_CAN\_EJECT message</span></span>

<span data-ttu-id="65258-106">A **MCIWNDM \_ pode \_ ejetar** a mensagem para determinar se um dispositivo MCI pode ejetar sua mídia.</span><span class="sxs-lookup"><span data-stu-id="65258-106">The **MCIWNDM\_CAN\_EJECT** message determines if an MCI device can eject its media.</span></span> <span data-ttu-id="65258-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .</span><span class="sxs-lookup"><span data-stu-id="65258-107">You can send this message explicitly or by using the [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) macro.</span></span>


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="65258-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="65258-108">Return Value</span></span>

<span data-ttu-id="65258-109">Retornará **true** se o dispositivo puder ejetar sua mídia ou **false** .</span><span class="sxs-lookup"><span data-stu-id="65258-109">Returns **TRUE** if the device can eject its media or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="65258-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65258-110">Requirements</span></span>



| <span data-ttu-id="65258-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="65258-111">Requirement</span></span> | <span data-ttu-id="65258-112">Valor</span><span class="sxs-lookup"><span data-stu-id="65258-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="65258-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65258-113">Minimum supported client</span></span><br/> | <span data-ttu-id="65258-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="65258-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="65258-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65258-115">Minimum supported server</span></span><br/> | <span data-ttu-id="65258-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="65258-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="65258-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="65258-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="65258-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="65258-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65258-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="65258-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65258-120">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="65258-120">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





