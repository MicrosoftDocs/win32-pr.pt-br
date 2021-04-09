---
title: Mensagem de MCIWNDM_GETDEVICEID (VFW. h)
description: A \_ mensagem MCIWNDM DeviceID recupera o identificador do dispositivo MCI aberto no momento para usar com a função mciSendCommand. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETDEVICEID
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008977"
---
# <a name="mciwndm_getdeviceid-message"></a><span data-ttu-id="eeafc-105">\_Mensagem MCIWNDM DeviceID</span><span class="sxs-lookup"><span data-stu-id="eeafc-105">MCIWNDM\_GETDEVICEID message</span></span>

<span data-ttu-id="eeafc-106">A mensagem **MCIWNDM DeviceID \_** recupera o identificador do dispositivo MCI aberto no momento para usar com a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="eeafc-106">The **MCIWNDM\_GETDEVICEID** message retrieves the identifier of the currently open MCI device to use with the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="eeafc-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="eeafc-107">You can send this message explicitly or by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span>


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="eeafc-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="eeafc-108">Return Value</span></span>

<span data-ttu-id="eeafc-109">Retorna o identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eeafc-109">Returns the device identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeafc-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeafc-110">Requirements</span></span>



| <span data-ttu-id="eeafc-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeafc-111">Requirement</span></span> | <span data-ttu-id="eeafc-112">Valor</span><span class="sxs-lookup"><span data-stu-id="eeafc-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eeafc-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eeafc-113">Minimum supported client</span></span><br/> | <span data-ttu-id="eeafc-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eeafc-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eeafc-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eeafc-115">Minimum supported server</span></span><br/> | <span data-ttu-id="eeafc-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eeafc-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eeafc-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eeafc-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeafc-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeafc-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeafc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="eeafc-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="eeafc-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eeafc-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eeafc-121">**MCIWndGetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eeafc-121">**MCIWndGetDeviceID**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

