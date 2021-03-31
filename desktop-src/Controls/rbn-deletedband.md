---
title: RBN_DELETEDBAND código de notificação (commctrl. h)
description: Enviado por um controle rebar após a exclusão de uma banda. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- RBN_DELETEDBAND de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824580"
---
# <a name="rbn_deletedband-notification-code"></a><span data-ttu-id="c07c8-105">Código de notificação do RBN \_ DELETEDBAND</span><span class="sxs-lookup"><span data-stu-id="c07c8-105">RBN\_DELETEDBAND notification code</span></span>

<span data-ttu-id="c07c8-106">Enviado por um controle rebar após a exclusão de uma banda.</span><span class="sxs-lookup"><span data-stu-id="c07c8-106">Sent by a rebar control after a band has been deleted.</span></span> <span data-ttu-id="c07c8-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c07c8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c07c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c07c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c07c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c07c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c07c8-110">Ponteiro para uma estrutura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="c07c8-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c07c8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c07c8-111">Return value</span></span>

<span data-ttu-id="c07c8-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="c07c8-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c07c8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c07c8-113">Requirements</span></span>



| <span data-ttu-id="c07c8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c07c8-114">Requirement</span></span> | <span data-ttu-id="c07c8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c07c8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c07c8-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c07c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c07c8-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c07c8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c07c8-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c07c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c07c8-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c07c8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c07c8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c07c8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c07c8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c07c8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





