---
title: RBN_ENDDRAG código de notificação (commctrl. h)
description: Enviado por um controle rebar quando o usuário para de arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- RBN_ENDDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb6c538679d793ed2407775b4238cea475ba4ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009551"
---
# <a name="rbn_enddrag-notification-code"></a><span data-ttu-id="5b95d-105">Código de notificação do RBN \_ ENDarraste</span><span class="sxs-lookup"><span data-stu-id="5b95d-105">RBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="5b95d-106">Enviado por um controle rebar quando o usuário para de arrastar uma banda.</span><span class="sxs-lookup"><span data-stu-id="5b95d-106">Sent by a rebar control when the user stops dragging a band.</span></span> <span data-ttu-id="5b95d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5b95d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5b95d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b95d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b95d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b95d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b95d-110">Ponteiro para uma estrutura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="5b95d-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b95d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b95d-111">Return value</span></span>

<span data-ttu-id="5b95d-112">O valor de retorno para este código de notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="5b95d-112">The return value for this notification code is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b95d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b95d-113">Requirements</span></span>



| <span data-ttu-id="5b95d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b95d-114">Requirement</span></span> | <span data-ttu-id="5b95d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5b95d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b95d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b95d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5b95d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b95d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b95d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b95d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5b95d-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b95d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b95d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b95d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b95d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b95d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





