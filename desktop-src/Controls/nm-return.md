---
title: NM_RETURN código de notificação (commctrl. h)
description: Notifica uma janela pai do controle que o controle tem o foco de entrada e que o usuário pressionou a tecla ENTER. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- NM_RETURN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499600"
---
# <a name="nm_return-notification-code"></a><span data-ttu-id="255fb-105">Código de notificação de retorno de NM \_</span><span class="sxs-lookup"><span data-stu-id="255fb-105">NM\_RETURN notification code</span></span>

<span data-ttu-id="255fb-106">Notifica uma janela pai do controle que o controle tem o foco de entrada e que o usuário pressionou a tecla ENTER.</span><span class="sxs-lookup"><span data-stu-id="255fb-106">Notifies a control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="255fb-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="255fb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="255fb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="255fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="255fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="255fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="255fb-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="255fb-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="255fb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="255fb-111">Return value</span></span>

<span data-ttu-id="255fb-112">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="255fb-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="255fb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="255fb-113">Requirements</span></span>



| <span data-ttu-id="255fb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="255fb-114">Requirement</span></span> | <span data-ttu-id="255fb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="255fb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="255fb-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="255fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="255fb-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="255fb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="255fb-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="255fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="255fb-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="255fb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="255fb-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="255fb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="255fb-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="255fb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





