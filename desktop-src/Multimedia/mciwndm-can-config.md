---
title: Mensagem de MCIWNDM_CAN_CONFIG (VFW. h)
description: A mensagem de configuração de MCIWNDM \_ pode \_ determinar se um dispositivo MCI pode exibir uma caixa de diálogo de configuração. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_CONFIG
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455953"
---
# <a name="mciwndm_can_config-message"></a><span data-ttu-id="d8f4f-105">MCIWNDM \_ pode \_ Configurar a mensagem</span><span class="sxs-lookup"><span data-stu-id="d8f4f-105">MCIWNDM\_CAN\_CONFIG message</span></span>

<span data-ttu-id="d8f4f-106">A mensagem de **\_ \_ configuração de MCIWNDM pode** determinar se um dispositivo MCI pode exibir uma caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="d8f4f-106">The **MCIWNDM\_CAN\_CONFIG** message determines if an MCI device can display a configuration dialog box.</span></span> <span data-ttu-id="d8f4f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .</span><span class="sxs-lookup"><span data-stu-id="d8f4f-107">You can send this message explicitly or by using the [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) macro.</span></span>


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d8f4f-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d8f4f-108">Return Value</span></span>

<span data-ttu-id="d8f4f-109">Retorna **true** se o dispositivo der suporte à configuração ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d8f4f-109">Returns **TRUE** if the device supports configuration or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8f4f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8f4f-110">Requirements</span></span>



| <span data-ttu-id="d8f4f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8f4f-111">Requirement</span></span> | <span data-ttu-id="d8f4f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d8f4f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8f4f-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8f4f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d8f4f-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8f4f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d8f4f-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8f4f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d8f4f-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8f4f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8f4f-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d8f4f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8f4f-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8f4f-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8f4f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8f4f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f4f-120">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="d8f4f-120">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





