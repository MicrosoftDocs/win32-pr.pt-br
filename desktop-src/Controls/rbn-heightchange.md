---
title: RBN_HEIGHTCHANGE código de notificação (commctrl. h)
description: Enviado por um controle rebar quando sua altura é alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- RBN_HEIGHTCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918387"
---
# <a name="rbn_heightchange-notification-code"></a><span data-ttu-id="8e4a1-105">Código de notificação do RBN \_ HEIGHTCHANGE</span><span class="sxs-lookup"><span data-stu-id="8e4a1-105">RBN\_HEIGHTCHANGE notification code</span></span>

<span data-ttu-id="8e4a1-106">Enviado por um controle rebar quando sua altura é alterada.</span><span class="sxs-lookup"><span data-stu-id="8e4a1-106">Sent by a rebar control when its height has changed.</span></span> <span data-ttu-id="8e4a1-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8e4a1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8e4a1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e4a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e4a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e4a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e4a1-110">Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="8e4a1-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e4a1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e4a1-111">Return value</span></span>

<span data-ttu-id="8e4a1-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="8e4a1-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4a1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e4a1-113">Remarks</span></span>

<span data-ttu-id="8e4a1-114">Controles Rebar que usam o estilo [**ccs \_ Vert**](common-control-styles.md) enviam este código de notificação quando sua largura é alterada.</span><span class="sxs-lookup"><span data-stu-id="8e4a1-114">Rebar controls that use the [**CCS\_VERT**](common-control-styles.md) style send this notification code when their width changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e4a1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e4a1-115">Requirements</span></span>



| <span data-ttu-id="8e4a1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e4a1-116">Requirement</span></span> | <span data-ttu-id="8e4a1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8e4a1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4a1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e4a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8e4a1-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e4a1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e4a1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e4a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8e4a1-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e4a1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e4a1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e4a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e4a1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e4a1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





