---
title: EN_OBJECTPOSITIONS código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico quando o controle lê em objetos. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824461"
---
# <a name="en_objectpositions-notification-code"></a><span data-ttu-id="377df-105">\_Código de notificação de OBJECTPOSIÇÕES en</span><span class="sxs-lookup"><span data-stu-id="377df-105">EN\_OBJECTPOSITIONS notification code</span></span>

<span data-ttu-id="377df-106">Notifica uma janela pai do controle de edição rico quando o controle lê em objetos.</span><span class="sxs-lookup"><span data-stu-id="377df-106">Notifies a rich edit control's parent window when the control reads in objects.</span></span> <span data-ttu-id="377df-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="377df-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="377df-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="377df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="377df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="377df-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="377df-110">Uma estrutura de [**objectposições**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .</span><span class="sxs-lookup"><span data-stu-id="377df-110">An [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="377df-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="377df-111">Return value</span></span>

<span data-ttu-id="377df-112">Retornar zero para continuar a operação de **leitura** .</span><span class="sxs-lookup"><span data-stu-id="377df-112">Return zero to continue the **Read** operation.</span></span>

<span data-ttu-id="377df-113">Retornar um valor diferente de zero para interromper a operação de **leitura** .</span><span class="sxs-lookup"><span data-stu-id="377df-113">Return a nonzero value to stop the **Read** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="377df-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="377df-114">Remarks</span></span>

<span data-ttu-id="377df-115">Para receber um \_ código de notificação en objectposições, especifique o sinalizador [**enm \_ objectpositiones**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="377df-115">To receive an EN\_OBJECTPOSITIONS notification code, specify the [**ENM\_OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="377df-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="377df-116">Requirements</span></span>



| <span data-ttu-id="377df-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="377df-117">Requirement</span></span> | <span data-ttu-id="377df-118">Valor</span><span class="sxs-lookup"><span data-stu-id="377df-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="377df-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="377df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="377df-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="377df-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="377df-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="377df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="377df-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="377df-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="377df-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="377df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="377df-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="377df-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="377df-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="377df-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="377df-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="377df-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="377df-127">**em \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="377df-127">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="377df-128">**Objectposições**</span><span class="sxs-lookup"><span data-stu-id="377df-128">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[<span data-ttu-id="377df-129">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="377df-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> <dt>

<span data-ttu-id="377df-130">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="377df-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="377df-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="377df-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="377df-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="377df-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

