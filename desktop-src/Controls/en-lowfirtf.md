---
title: EN_LOWFIRTF código de notificação (RichEdit. h)
description: Notifica a janela pai de um controle de edição rico da Microsoft que uma palavra-chave RTF (Rich Text Format) sem suporte foi recebida. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499669"
---
# <a name="en_lowfirtf-notification-code"></a><span data-ttu-id="56662-105">\_Código de notificação en LOWFIRTF</span><span class="sxs-lookup"><span data-stu-id="56662-105">EN\_LOWFIRTF notification code</span></span>

<span data-ttu-id="56662-106">Notifica a janela pai de um controle de edição rico da Microsoft que uma palavra-chave RTF (Rich Text Format) sem suporte foi recebida.</span><span class="sxs-lookup"><span data-stu-id="56662-106">Notifies the parent window of a Microsoft Rich Edit control that an unsupported Rich Text Format (RTF) keyword was received.</span></span> <span data-ttu-id="56662-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="56662-107">A Rich Edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="56662-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56662-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56662-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56662-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56662-110">A estrutura [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) .</span><span class="sxs-lookup"><span data-stu-id="56662-110">The [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56662-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56662-111">Return value</span></span>

<span data-ttu-id="56662-112">Este código de notificação não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="56662-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56662-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="56662-113">Remarks</span></span>

<span data-ttu-id="56662-114">Para receber uma \_ notificação en LOWFIRTF, especifique o \_ sinalizador enm LOWFIRTF na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="56662-114">To receive an EN\_LOWFIRTF notification, specify the ENM\_LOWFIRTF flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="56662-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56662-115">Requirements</span></span>



| <span data-ttu-id="56662-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="56662-116">Requirement</span></span> | <span data-ttu-id="56662-117">Valor</span><span class="sxs-lookup"><span data-stu-id="56662-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56662-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56662-118">Minimum supported client</span></span><br/> | <span data-ttu-id="56662-119">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="56662-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56662-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56662-120">Minimum supported server</span></span><br/> | <span data-ttu-id="56662-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56662-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56662-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56662-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="56662-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="56662-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56662-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="56662-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="56662-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="56662-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="56662-126">**ENLOWFIRTF**</span><span class="sxs-lookup"><span data-stu-id="56662-126">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[<span data-ttu-id="56662-127">**notificação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="56662-127">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





