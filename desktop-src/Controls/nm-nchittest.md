---
title: NM_NCHITTEST código de notificação (commctrl. h)
description: NM_NCHITTEST código de notificação – enviado por um controle rebar quando o controle recebe uma \_ mensagem do WM NCHITTEST. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST de código de notificação controles do Windows
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
ms.openlocfilehash: 68ede0ac017fbe5146cd68e51e2a38c7f66c7898
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112314"
---
# <a name="nm_nchittest-notification-code"></a><span data-ttu-id="2296f-105">\_Código de notificação nm NCHITTEST</span><span class="sxs-lookup"><span data-stu-id="2296f-105">NM\_NCHITTEST notification code</span></span>

<span data-ttu-id="2296f-106">Enviado por um controle rebar quando o controle recebe uma mensagem de [**\_ NCHITTEST do WM**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="2296f-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="2296f-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2296f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2296f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2296f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2296f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2296f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2296f-110">Um ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="2296f-110">A pointer to a [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="2296f-111">O membro *pt* contém as coordenadas do mouse da mensagem de teste de clique.</span><span class="sxs-lookup"><span data-stu-id="2296f-111">The *pt* member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2296f-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2296f-112">Return value</span></span>

<span data-ttu-id="2296f-113">A menos que especificado de outra forma, retorna zero para permitir que o controle execute o processamento padrão da mensagem de teste de clique ou retorne um dos valores de HT \* documentados em [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para substituir o processamento de teste de clique padrão.</span><span class="sxs-lookup"><span data-stu-id="2296f-113">Unless otherwise specified, return zero to allow the control to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2296f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2296f-114">Requirements</span></span>



| <span data-ttu-id="2296f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2296f-115">Requirement</span></span> | <span data-ttu-id="2296f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2296f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2296f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2296f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2296f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2296f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2296f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2296f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2296f-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2296f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2296f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2296f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2296f-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2296f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

