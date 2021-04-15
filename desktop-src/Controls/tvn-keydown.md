---
title: TVN_KEYDOWN código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que o usuário pressionou uma tecla e o controle de exibição de árvore tem o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454615"
---
# <a name="tvn_keydown-notification-code"></a><span data-ttu-id="7fcc1-105">Código de notificação do TVN \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="7fcc1-105">TVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="7fcc1-106">Notifica uma janela pai do controle de exibição de árvore que o usuário pressionou uma tecla e o controle de exibição de árvore tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="7fcc1-106">Notifies a tree-view control's parent window that the user pressed a key and the tree-view control has the input focus.</span></span> <span data-ttu-id="7fcc1-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7fcc1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a><span data-ttu-id="7fcc1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fcc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fcc1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fcc1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fcc1-110">Ponteiro para uma estrutura [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="7fcc1-110">Pointer to an [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) structure.</span></span> <span data-ttu-id="7fcc1-111">O membro **wVKey** especifica o código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="7fcc1-111">The **wVKey** member specifies the virtual key code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fcc1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fcc1-112">Return value</span></span>

<span data-ttu-id="7fcc1-113">Se o membro **wVKey** de *lParam* for um código de chave de caractere, o caractere será usado como parte de uma pesquisa incremental.</span><span class="sxs-lookup"><span data-stu-id="7fcc1-113">If the **wVKey** member of *lParam* is a character key code, the character will be used as part of an incremental search.</span></span> <span data-ttu-id="7fcc1-114">Retorne diferente de zero para excluir o caractere da pesquisa incremental ou zero para incluir o caractere na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7fcc1-114">Return nonzero to exclude the character from the incremental search, or zero to include the character in the search.</span></span> <span data-ttu-id="7fcc1-115">Para todas as outras chaves, o valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="7fcc1-115">For all other keys, the return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcc1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fcc1-116">Requirements</span></span>



| <span data-ttu-id="7fcc1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fcc1-117">Requirement</span></span> | <span data-ttu-id="7fcc1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7fcc1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcc1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fcc1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcc1-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fcc1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fcc1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fcc1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcc1-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fcc1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fcc1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fcc1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fcc1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcc1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





