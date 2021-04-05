---
title: TBN_TOOLBARCHANGE código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas que o usuário personalizou uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 6c5127e6-391f-4592-8547-4cc3d3ed6cf0
keywords:
- TBN_TOOLBARCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_TOOLBARCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9c533a7a26dd1ed0f1938e6c5138bbae13c31f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918853"
---
# <a name="tbn_toolbarchange-notification-code"></a><span data-ttu-id="984e9-105">Código de notificação do TBN \_ TOOLBARCHANGE</span><span class="sxs-lookup"><span data-stu-id="984e9-105">TBN\_TOOLBARCHANGE notification code</span></span>

<span data-ttu-id="984e9-106">Notifica a janela pai da barra de ferramentas que o usuário personalizou uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="984e9-106">Notifies the toolbar's parent window that the user has customized a toolbar.</span></span> <span data-ttu-id="984e9-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="984e9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_TOOLBARCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="984e9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="984e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="984e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="984e9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="984e9-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="984e9-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="984e9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="984e9-111">Return value</span></span>

<span data-ttu-id="984e9-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="984e9-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="984e9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="984e9-113">Requirements</span></span>



| <span data-ttu-id="984e9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="984e9-114">Requirement</span></span> | <span data-ttu-id="984e9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="984e9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="984e9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="984e9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="984e9-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="984e9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="984e9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="984e9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="984e9-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="984e9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="984e9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="984e9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="984e9-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="984e9-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





