---
title: TBN_QUERYDELETE código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas se um botão pode ser excluído de uma barra de ferramentas enquanto o usuário estiver personalizando a barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499235"
---
# <a name="tbn_querydelete-notification-code"></a><span data-ttu-id="fa831-105">Código de notificação do TBN \_ QUERYDELETE</span><span class="sxs-lookup"><span data-stu-id="fa831-105">TBN\_QUERYDELETE notification code</span></span>

<span data-ttu-id="fa831-106">Notifica a janela pai da barra de ferramentas se um botão pode ser excluído de uma barra de ferramentas enquanto o usuário estiver personalizando a barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="fa831-106">Notifies the toolbar's parent window whether a button may be deleted from a toolbar while the user is customizing the toolbar.</span></span> <span data-ttu-id="fa831-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fa831-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fa831-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa831-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa831-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa831-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa831-110">Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="fa831-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="fa831-111">O membro **iItem** contém o índice de base zero do botão a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="fa831-111">The **iItem** member contains the zero-based index of the button to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa831-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa831-112">Return value</span></span>

<span data-ttu-id="fa831-113">Retorna **true** para permitir que o botão seja excluído ou **false** para impedir que o botão seja excluído.</span><span class="sxs-lookup"><span data-stu-id="fa831-113">Returns **TRUE** to allow the button to be deleted, or **FALSE** to prevent the button from being deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa831-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa831-114">Requirements</span></span>



| <span data-ttu-id="fa831-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa831-115">Requirement</span></span> | <span data-ttu-id="fa831-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fa831-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa831-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa831-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa831-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa831-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa831-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa831-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa831-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa831-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa831-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa831-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa831-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa831-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





