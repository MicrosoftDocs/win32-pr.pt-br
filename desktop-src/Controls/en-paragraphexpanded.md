---
title: EN_PARAGRAPHEXPANDED código de notificação (RichEdit. h)
description: Notifica um pai do controle de edição rico de que um contorno foi expandido. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- EN_PARAGRAPHEXPANDED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f862260c0653d23b0b53649a2c05e59820e3808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455234"
---
# <a name="en_paragraphexpanded-notification-code"></a><span data-ttu-id="89e98-105">\_Código de notificação en PARAGRAPHEXPANDED</span><span class="sxs-lookup"><span data-stu-id="89e98-105">EN\_PARAGRAPHEXPANDED notification code</span></span>

<span data-ttu-id="89e98-106">Notifica um pai do controle de edição rico de que um contorno foi expandido.</span><span class="sxs-lookup"><span data-stu-id="89e98-106">Notifies a rich edit control's parent that an outline has been expanded.</span></span> <span data-ttu-id="89e98-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="89e98-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="89e98-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89e98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89e98-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89e98-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89e98-110">Uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="89e98-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89e98-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89e98-111">Requirements</span></span>



| <span data-ttu-id="89e98-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="89e98-112">Requirement</span></span> | <span data-ttu-id="89e98-113">Valor</span><span class="sxs-lookup"><span data-stu-id="89e98-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89e98-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89e98-114">Minimum supported client</span></span><br/> | <span data-ttu-id="89e98-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89e98-115">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89e98-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89e98-116">Minimum supported server</span></span><br/> | <span data-ttu-id="89e98-117">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89e98-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89e98-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89e98-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="89e98-119"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="89e98-119"><dt>Richedit.h</dt></span></span> </dl> |



 

 





