---
title: RBN_MINMAX código de notificação (commctrl. h)
description: Enviado por um controle rebar antes de maximizar ou minimizar uma banda. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- RBN_MINMAX de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749071"
---
# <a name="rbn_minmax-notification-code"></a><span data-ttu-id="48b9a-105">Código de notificação do RBN \_ por minMax</span><span class="sxs-lookup"><span data-stu-id="48b9a-105">RBN\_MINMAX notification code</span></span>

<span data-ttu-id="48b9a-106">Enviado por um controle rebar antes de maximizar ou minimizar uma banda.</span><span class="sxs-lookup"><span data-stu-id="48b9a-106">Sent by a rebar control prior to maximizing or minimizing a band.</span></span> <span data-ttu-id="48b9a-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="48b9a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_MINMAX
```



## <a name="parameters"></a><span data-ttu-id="48b9a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48b9a-108">Parameters</span></span>

<span data-ttu-id="48b9a-109">Este código de notificação não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="48b9a-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48b9a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48b9a-110">Return value</span></span>

<span data-ttu-id="48b9a-111">Retornar um valor diferente de zero para impedir que a operação ocorra, zero para permitir que ele continue.</span><span class="sxs-lookup"><span data-stu-id="48b9a-111">Return a nonzero value to prevent the operation from taking place, zero to allow it to continue.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b9a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48b9a-112">Requirements</span></span>



| <span data-ttu-id="48b9a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="48b9a-113">Requirement</span></span> | <span data-ttu-id="48b9a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="48b9a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48b9a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48b9a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="48b9a-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48b9a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48b9a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48b9a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="48b9a-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48b9a-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48b9a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48b9a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="48b9a-120"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48b9a-120"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





