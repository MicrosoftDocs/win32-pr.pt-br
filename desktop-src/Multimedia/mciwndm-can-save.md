---
title: Mensagem de MCIWNDM_CAN_SAVE (VFW. h)
description: O MCIWNDM \_ pode \_ salvar a mensagem determina se um dispositivo MCI pode salvar dados. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_SAVE
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454801"
---
# <a name="mciwndm_can_save-message"></a><span data-ttu-id="7314c-105">MCIWNDM \_ pode \_ salvar a mensagem</span><span class="sxs-lookup"><span data-stu-id="7314c-105">MCIWNDM\_CAN\_SAVE message</span></span>

<span data-ttu-id="7314c-106">O **MCIWNDM \_ pode \_ salvar** a mensagem determina se um dispositivo MCI pode salvar dados.</span><span class="sxs-lookup"><span data-stu-id="7314c-106">The **MCIWNDM\_CAN\_SAVE** message determines if an MCI device can save data.</span></span> <span data-ttu-id="7314c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .</span><span class="sxs-lookup"><span data-stu-id="7314c-107">You can send this message explicitly or by using the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro.</span></span>


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="7314c-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7314c-108">Return Value</span></span>

<span data-ttu-id="7314c-109">Retornará **true** se o dispositivo der suporte a salvar ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7314c-109">Returns **TRUE** if the device supports saving or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7314c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7314c-110">Requirements</span></span>



| <span data-ttu-id="7314c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7314c-111">Requirement</span></span> | <span data-ttu-id="7314c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7314c-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7314c-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7314c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7314c-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7314c-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7314c-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7314c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7314c-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7314c-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7314c-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7314c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7314c-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7314c-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7314c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7314c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7314c-120">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="7314c-120">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





