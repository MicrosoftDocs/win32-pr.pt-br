---
title: TCN_KEYDOWN código de notificação (commctrl. h)
description: Notifica uma janela pai do controle guia que uma tecla foi pressionada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- TCN_KEYDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756420"
---
# <a name="tcn_keydown-notification-code"></a><span data-ttu-id="64ef9-105">Código de notificação do TCN \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="64ef9-105">TCN\_KEYDOWN notification code</span></span>

<span data-ttu-id="64ef9-106">Notifica uma janela pai do controle guia que uma tecla foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="64ef9-106">Notifies a tab control's parent window that a key has been pressed.</span></span> <span data-ttu-id="64ef9-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="64ef9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="64ef9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64ef9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64ef9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64ef9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64ef9-110">Ponteiro para uma estrutura [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) .</span><span class="sxs-lookup"><span data-stu-id="64ef9-110">Pointer to an [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64ef9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64ef9-111">Return value</span></span>

<span data-ttu-id="64ef9-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="64ef9-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="64ef9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64ef9-113">Requirements</span></span>



| <span data-ttu-id="64ef9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="64ef9-114">Requirement</span></span> | <span data-ttu-id="64ef9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="64ef9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64ef9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64ef9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="64ef9-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64ef9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64ef9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64ef9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="64ef9-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64ef9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64ef9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64ef9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="64ef9-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64ef9-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





