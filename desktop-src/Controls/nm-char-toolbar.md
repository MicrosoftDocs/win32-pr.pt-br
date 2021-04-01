---
title: Código de notificação de NM_CHAR (barra de ferramentas) (commctrl. h)
description: Enviado por uma barra de ferramentas quando recebe uma \_ mensagem do WM Char. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Código de notificação de NM_CHAR (barra de ferramentas) controles do Windows
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824856"
---
# <a name="nm_char-toolbar-notification-code"></a><span data-ttu-id="c4880-105">\_Código de notificação de caracteres nm (barra de ferramentas)</span><span class="sxs-lookup"><span data-stu-id="c4880-105">NM\_CHAR (toolbar) notification code</span></span>

<span data-ttu-id="c4880-106">Enviado por uma barra de ferramentas quando recebe uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="c4880-106">Sent by a toolbar when it receives a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span> <span data-ttu-id="c4880-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c4880-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c4880-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4880-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4880-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4880-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4880-110">Ponteiro para uma estrutura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contém informações adicionais sobre o caractere que causou o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="c4880-110">Pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span> <span data-ttu-id="c4880-111">O membro **dwItemPrev** dessa estrutura contém o identificador de comando do item que é atualmente quente ou-1 se nenhum item está quente no momento.</span><span class="sxs-lookup"><span data-stu-id="c4880-111">The **dwItemPrev** member of this structure contains the command identifier of the item that is currently hot or -1 if no item is currently hot.</span></span> <span data-ttu-id="c4880-112">O membro **dwItemNext** dessa estrutura contém o identificador de comando do item que se tornará quente ou-1 se a chave não corresponder ao acelerador de qualquer item.</span><span class="sxs-lookup"><span data-stu-id="c4880-112">The **dwItemNext** member of this structure contains the command identifier of the item that will become hot or -1 if the key does not match any item's accelerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4880-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4880-113">Return value</span></span>

<span data-ttu-id="c4880-114">Retorna **true** para indicar que a barra de ferramentas não deve processar o caractere e **false** para que a barra de ferramentas processe o caractere.</span><span class="sxs-lookup"><span data-stu-id="c4880-114">Returns **TRUE** to indicate that the toolbar should not process the character and **FALSE** to have the toolbar process the character.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4880-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4880-115">Requirements</span></span>



| <span data-ttu-id="c4880-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4880-116">Requirement</span></span> | <span data-ttu-id="c4880-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c4880-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4880-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4880-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c4880-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4880-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4880-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4880-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c4880-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4880-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4880-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4880-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4880-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4880-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

