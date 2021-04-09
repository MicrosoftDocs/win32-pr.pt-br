---
title: TBN_GETDISPINFO código de notificação (commctrl. h)
description: Recupera informações de exibição de um item da barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- TBN_GETDISPINFO de código de notificação controles do Windows
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086005"
---
# <a name="tbn_getdispinfo-notification-code"></a><span data-ttu-id="5d7a3-105">Código de notificação do TBN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="5d7a3-105">TBN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="5d7a3-106">Recupera informações de exibição de um item da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-106">Retrieves display information for a toolbar item.</span></span> <span data-ttu-id="5d7a3-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5d7a3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5d7a3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d7a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d7a3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d7a3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d7a3-110">Ponteiro para uma estrutura [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5d7a3-110">Pointer to an [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) structure.</span></span> <span data-ttu-id="5d7a3-111">O membro **idCommand** especifica o identificador de comando do item, o membro **lParam** contém os dados definidos pelo aplicativo do item e o membro **dwMask** especifica quais informações estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-111">The **idCommand** member specifies the item's command identifier, the **lParam** member contains the item's application-defined data, and the **dwMask** member specifies what information is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d7a3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d7a3-112">Return value</span></span>

<span data-ttu-id="5d7a3-113">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-113">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7a3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d7a3-114">Requirements</span></span>



| <span data-ttu-id="5d7a3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7a3-115">Requirement</span></span> | <span data-ttu-id="5d7a3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5d7a3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7a3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d7a3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7a3-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d7a3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d7a3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d7a3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7a3-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d7a3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d7a3-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d7a3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7a3-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d7a3-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5d7a3-123">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5d7a3-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5d7a3-124">**Tbn \_ GETDISPINFOW** (Unicode) e **tbn \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5d7a3-124">**TBN\_GETDISPINFOW** (Unicode) and **TBN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





