---
title: Código de notificação do NM_NCHITTEST (rebar) (commctrl. h)
description: Código de notificação de NM_NCHITTEST (rebar) – enviado por um controle rebar quando o controle recebe uma mensagem de NCHITTEST do WM \_ . Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Controles do Windows de código de notificação de NM_NCHITTEST (rebar)
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7935f1b3e990db55518c9d22537e8fb6db97962
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112324"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="75174-105">\_Código de notificação do NCHITTEST nm (rebar)</span><span class="sxs-lookup"><span data-stu-id="75174-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="75174-106">Enviado por um controle rebar quando o controle recebe uma mensagem de [**\_ NCHITTEST do WM**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="75174-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="75174-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="75174-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="75174-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75174-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75174-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75174-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75174-110">Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="75174-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="75174-111">O membro **dwItemSpec** contém o índice de banda sobre o qual ocorreu a mensagem de teste de ocorrência e o membro **pt** contém as coordenadas do mouse da mensagem de teste de clique.</span><span class="sxs-lookup"><span data-stu-id="75174-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75174-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="75174-112">Return value</span></span>

<span data-ttu-id="75174-113">Retorne zero para permitir que o rebar execute o processamento padrão da mensagem de teste de clique ou retorne um dos valores de HT \* documentados em [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para substituir o processamento de teste de clique padrão.</span><span class="sxs-lookup"><span data-stu-id="75174-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="75174-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75174-114">Requirements</span></span>



| <span data-ttu-id="75174-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="75174-115">Requirement</span></span> | <span data-ttu-id="75174-116">Valor</span><span class="sxs-lookup"><span data-stu-id="75174-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75174-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75174-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75174-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75174-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75174-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75174-119">Minimum supported server</span></span><br/> | <span data-ttu-id="75174-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75174-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75174-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75174-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="75174-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75174-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

