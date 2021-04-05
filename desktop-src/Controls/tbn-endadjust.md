---
title: TBN_ENDADJUST código de notificação (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas de que o usuário parou de personalizar uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- TBN_ENDADJUST de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009258"
---
# <a name="tbn_endadjust-notification-code"></a><span data-ttu-id="be89e-105">Código de notificação do TBN \_ ENDajuste</span><span class="sxs-lookup"><span data-stu-id="be89e-105">TBN\_ENDADJUST notification code</span></span>

<span data-ttu-id="be89e-106">Notifica uma janela pai da barra de ferramentas de que o usuário parou de personalizar uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="be89e-106">Notifies a toolbar's parent window that the user has stopped customizing a toolbar.</span></span> <span data-ttu-id="be89e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="be89e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="be89e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be89e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be89e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be89e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be89e-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="be89e-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be89e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be89e-111">Return value</span></span>

<span data-ttu-id="be89e-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="be89e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be89e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be89e-113">Requirements</span></span>



| <span data-ttu-id="be89e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="be89e-114">Requirement</span></span> | <span data-ttu-id="be89e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="be89e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be89e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be89e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="be89e-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be89e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be89e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be89e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="be89e-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be89e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be89e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be89e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="be89e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be89e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





