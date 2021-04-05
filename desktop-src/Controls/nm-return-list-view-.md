---
title: Código de notificação de NM_RETURN (exibição de lista) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que o controle tem o foco de entrada e que o usuário pressionou a tecla ENTER. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- NM_RETURN de código de notificação (exibição de lista) controles do Windows
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
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918873"
---
# <a name="nm_return-list-view-notification-code"></a><span data-ttu-id="8d791-105">\_Código de notificação de retorno de nm (exibição de lista)</span><span class="sxs-lookup"><span data-stu-id="8d791-105">NM\_RETURN (list view) notification code</span></span>

<span data-ttu-id="8d791-106">Notifica uma janela pai do controle de exibição de lista que o controle tem o foco de entrada e que o usuário pressionou a tecla ENTER.</span><span class="sxs-lookup"><span data-stu-id="8d791-106">Notifies a list-view control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="8d791-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8d791-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8d791-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d791-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d791-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d791-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d791-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="8d791-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d791-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d791-111">Return value</span></span>

<span data-ttu-id="8d791-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="8d791-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d791-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d791-113">Requirements</span></span>



| <span data-ttu-id="8d791-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d791-114">Requirement</span></span> | <span data-ttu-id="8d791-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8d791-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d791-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d791-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8d791-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d791-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d791-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d791-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8d791-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d791-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d791-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d791-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d791-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d791-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





