---
title: Mensagem de MCIWNDM_CAN_RECORD (VFW. h)
description: O MCIWNDM \_ pode \_ registrar a mensagem determina se um dispositivo MCI dá suporte à gravação. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_RECORD
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455814"
---
# <a name="mciwndm_can_record-message"></a><span data-ttu-id="6b170-105">MCIWNDM \_ pode \_ registrar a mensagem</span><span class="sxs-lookup"><span data-stu-id="6b170-105">MCIWNDM\_CAN\_RECORD message</span></span>

<span data-ttu-id="6b170-106">O **MCIWNDM \_ pode \_ registrar** a mensagem determina se um dispositivo MCI dá suporte à gravação.</span><span class="sxs-lookup"><span data-stu-id="6b170-106">The **MCIWNDM\_CAN\_RECORD** message determines if an MCI device supports recording.</span></span> <span data-ttu-id="6b170-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) .</span><span class="sxs-lookup"><span data-stu-id="6b170-107">You can send this message explicitly or by using the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro.</span></span>


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="6b170-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6b170-108">Return Value</span></span>

<span data-ttu-id="6b170-109">Retornará **true** se o dispositivo der suporte à gravação ou **false** .</span><span class="sxs-lookup"><span data-stu-id="6b170-109">Returns **TRUE** if the device supports recording or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b170-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b170-110">Requirements</span></span>



| <span data-ttu-id="6b170-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b170-111">Requirement</span></span> | <span data-ttu-id="6b170-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6b170-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b170-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b170-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6b170-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b170-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b170-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b170-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6b170-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b170-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b170-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6b170-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b170-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b170-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b170-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b170-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b170-120">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="6b170-120">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





