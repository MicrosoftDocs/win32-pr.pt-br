---
title: TTN_GETDISPINFO código de notificação (commctrl. h)
description: Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- TTN_GETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824562"
---
# <a name="ttn_getdispinfo-notification-code"></a><span data-ttu-id="ae789-105">Código de notificação do TTN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="ae789-105">TTN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="ae789-106">Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="ae789-106">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="ae789-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ae789-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ae789-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae789-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae789-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae789-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae789-110">Ponteiro para uma estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que identifica a ferramenta que precisa de texto e recebe as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="ae789-110">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae789-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae789-111">Return value</span></span>

<span data-ttu-id="ae789-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="ae789-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae789-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae789-113">Remarks</span></span>

<span data-ttu-id="ae789-114">Preencha os membros apropriados da estrutura para retornar as informações solicitadas ao controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="ae789-114">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="ae789-115">Se o manipulador de mensagens definir o membro **uFlags** da estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) para ttf \_ di \_ SETITEM, o controle ToolTip armazenará as informações e não a solicitará novamente.</span><span class="sxs-lookup"><span data-stu-id="ae789-115">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae789-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae789-116">Requirements</span></span>



| <span data-ttu-id="ae789-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae789-117">Requirement</span></span> | <span data-ttu-id="ae789-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ae789-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae789-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae789-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae789-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae789-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae789-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae789-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae789-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae789-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae789-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae789-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae789-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae789-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ae789-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ae789-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ae789-126">**TTN \_ GETDISPINFOW** (Unicode) e **TTN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ae789-126">**TTN\_GETDISPINFOW** (Unicode) and **TTN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





