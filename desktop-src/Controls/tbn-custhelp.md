---
title: TBN_CUSTHELP código de notificação (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas de que o usuário escolheu o botão ajuda na caixa de diálogo Personalizar barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- TBN_CUSTHELP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824268"
---
# <a name="tbn_custhelp-notification-code"></a><span data-ttu-id="cbaa0-105">Código de notificação do TBN \_ CUSTHELP</span><span class="sxs-lookup"><span data-stu-id="cbaa0-105">TBN\_CUSTHELP notification code</span></span>

<span data-ttu-id="cbaa0-106">Notifica uma janela pai da barra de ferramentas de que o usuário escolheu o botão ajuda na caixa de diálogo Personalizar barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="cbaa0-106">Notifies a toolbar's parent window that the user has chosen the Help button in the Customize Toolbar dialog box.</span></span> <span data-ttu-id="cbaa0-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cbaa0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cbaa0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbaa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbaa0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbaa0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbaa0-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="cbaa0-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbaa0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbaa0-111">Return value</span></span>

<span data-ttu-id="cbaa0-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="cbaa0-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbaa0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbaa0-113">Requirements</span></span>



| <span data-ttu-id="cbaa0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbaa0-114">Requirement</span></span> | <span data-ttu-id="cbaa0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cbaa0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbaa0-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbaa0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cbaa0-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbaa0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cbaa0-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbaa0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cbaa0-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cbaa0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cbaa0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbaa0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbaa0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbaa0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





