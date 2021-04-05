---
title: NM_RELEASEDCAPTURE código de notificação (commctrl. h)
description: Notifica uma janela pai do controle que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 222a3be1-20f1-43c6-b982-852512209a45
keywords:
- NM_RELEASEDCAPTURE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1510fd3bbdd6877dba279cbfb9c69c14146a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918874"
---
# <a name="nm_releasedcapture-notification-code"></a><span data-ttu-id="f3569-105">\_Código de notificação nm RELEASEDCAPTURE</span><span class="sxs-lookup"><span data-stu-id="f3569-105">NM\_RELEASEDCAPTURE notification code</span></span>

<span data-ttu-id="f3569-106">Notifica uma janela pai do controle que o controle está liberando a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="f3569-106">Notifies a control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="f3569-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3569-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f3569-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3569-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3569-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3569-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3569-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="f3569-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3569-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3569-111">Return value</span></span>

<span data-ttu-id="f3569-112">A menos que especificado de outra forma, o controle ignora o valor de retorno deste código de notificação.</span><span class="sxs-lookup"><span data-stu-id="f3569-112">Unless otherwise specified, the control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3569-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3569-113">Requirements</span></span>



| <span data-ttu-id="f3569-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3569-114">Requirement</span></span> | <span data-ttu-id="f3569-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f3569-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3569-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3569-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f3569-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3569-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3569-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3569-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f3569-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3569-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3569-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3569-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3569-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3569-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





