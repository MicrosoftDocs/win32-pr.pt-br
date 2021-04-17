---
title: TBN_INITCUSTOMIZE código de notificação (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas que a personalização foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750936"
---
# <a name="tbn_initcustomize-notification-code"></a><span data-ttu-id="d8958-105">Código de notificação do TBN \_ INITCUSTOMIZE</span><span class="sxs-lookup"><span data-stu-id="d8958-105">TBN\_INITCUSTOMIZE notification code</span></span>

<span data-ttu-id="d8958-106">Notifica uma janela pai da barra de ferramentas que a personalização foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="d8958-106">Notifies a toolbar's parent window that customizing has started.</span></span> <span data-ttu-id="d8958-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8958-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d8958-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8958-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8958-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8958-110">Ponteiro para a estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d8958-110">Pointer to the toolbar's [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8958-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8958-111">Return value</span></span>

<span data-ttu-id="d8958-112">Retorna TBNRF \_ HIDEHELP para suprimir o botão de ajuda.</span><span class="sxs-lookup"><span data-stu-id="d8958-112">Returns TBNRF\_HIDEHELP to suppress the Help button.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8958-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8958-113">Requirements</span></span>



| <span data-ttu-id="d8958-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8958-114">Requirement</span></span> | <span data-ttu-id="d8958-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d8958-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8958-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8958-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d8958-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8958-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8958-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8958-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d8958-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8958-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8958-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8958-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8958-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8958-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





