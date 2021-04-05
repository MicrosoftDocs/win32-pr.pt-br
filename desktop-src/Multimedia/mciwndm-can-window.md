---
title: Mensagem de MCIWNDM_CAN_WINDOW (VFW. h)
description: A \_ mensagem de janela MCIWNDM pode \_ determinar se um dispositivo MCI dá suporte a comandos MCI orientados por janela. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanWindow.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_WINDOW
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918327"
---
# <a name="mciwndm_can_window-message"></a><span data-ttu-id="ed47d-105">MCIWNDM \_ pode \_ janela de mensagem</span><span class="sxs-lookup"><span data-stu-id="ed47d-105">MCIWNDM\_CAN\_WINDOW message</span></span>

<span data-ttu-id="ed47d-106">A mensagem de **\_ \_ janela MCIWNDM pode** determinar se um dispositivo MCI dá suporte a comandos MCI orientados por janela.</span><span class="sxs-lookup"><span data-stu-id="ed47d-106">The **MCIWNDM\_CAN\_WINDOW** message determines if an MCI device supports window-oriented MCI commands.</span></span> <span data-ttu-id="ed47d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) .</span><span class="sxs-lookup"><span data-stu-id="ed47d-107">You can send this message explicitly or by using the [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) macro.</span></span>


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ed47d-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ed47d-108">Return Value</span></span>

<span data-ttu-id="ed47d-109">Retornará **true** se o dispositivo der suporte a comandos MCI orientados por janela ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ed47d-109">Returns **TRUE** if the device supports window-oriented MCI commands or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed47d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed47d-110">Requirements</span></span>



| <span data-ttu-id="ed47d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed47d-111">Requirement</span></span> | <span data-ttu-id="ed47d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ed47d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ed47d-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed47d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ed47d-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed47d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed47d-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed47d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ed47d-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed47d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed47d-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed47d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed47d-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed47d-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed47d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed47d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed47d-120">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="ed47d-120">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





