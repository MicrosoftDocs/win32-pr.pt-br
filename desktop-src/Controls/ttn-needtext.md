---
title: TTN_NEEDTEXT código de notificação (commctrl. h)
description: Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Este código de notificação é idêntico a TTN \_ GETDISPINFO. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085804"
---
# <a name="ttn_needtext-notification-code"></a><span data-ttu-id="b125a-106">Código de notificação do TTN \_ NEEDTEXT</span><span class="sxs-lookup"><span data-stu-id="b125a-106">TTN\_NEEDTEXT notification code</span></span>

<span data-ttu-id="b125a-107">Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="b125a-107">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="b125a-108">Este código de notificação é idêntico a [TTN \_ GETDISPINFO](ttn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="b125a-108">This notification code is identical to [TTN\_GETDISPINFO](ttn-getdispinfo.md).</span></span> <span data-ttu-id="b125a-109">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b125a-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b125a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b125a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b125a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b125a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b125a-112">Ponteiro para uma estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que identifica a ferramenta que precisa de texto e recebe as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b125a-112">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b125a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b125a-113">Return value</span></span>

<span data-ttu-id="b125a-114">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="b125a-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b125a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b125a-115">Remarks</span></span>

<span data-ttu-id="b125a-116">Preencha os membros apropriados da estrutura para retornar as informações solicitadas ao controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b125a-116">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="b125a-117">Se o manipulador de mensagens definir o membro **uFlags** da estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) para ttf \_ di \_ SETITEM, o controle ToolTip armazenará as informações e não a solicitará novamente.</span><span class="sxs-lookup"><span data-stu-id="b125a-117">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="b125a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b125a-118">Requirements</span></span>



| <span data-ttu-id="b125a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b125a-119">Requirement</span></span> | <span data-ttu-id="b125a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b125a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b125a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b125a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b125a-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b125a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b125a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b125a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b125a-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b125a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b125a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b125a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b125a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b125a-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b125a-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b125a-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b125a-128">**TTN \_ NEEDTEXTW** (Unicode) e **TTN \_ NEEDTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b125a-128">**TTN\_NEEDTEXTW** (Unicode) and **TTN\_NEEDTEXTA** (ANSI)</span></span><br/>                 |



 

 





