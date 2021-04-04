---
title: NM_KILLFOCUS código de notificação (commctrl. h)
description: Notifica uma janela pai do controle que o controle perdeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d7538697-8b4c-4bbd-8b06-02cbc8069a22
keywords:
- NM_KILLFOCUS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 873af3315dd58a12a61249ca59a317ca5af4b105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085161"
---
# <a name="nm_killfocus-notification-code"></a><span data-ttu-id="557b8-105">\_Código de notificação nm KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="557b8-105">NM\_KILLFOCUS notification code</span></span>

<span data-ttu-id="557b8-106">Notifica uma janela pai do controle que o controle perdeu o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="557b8-106">Notifies a control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="557b8-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="557b8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="557b8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="557b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="557b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="557b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="557b8-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="557b8-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="557b8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="557b8-111">Return value</span></span>

<span data-ttu-id="557b8-112">O valor de retorno é ignorado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="557b8-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="557b8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="557b8-113">Requirements</span></span>



| <span data-ttu-id="557b8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="557b8-114">Requirement</span></span> | <span data-ttu-id="557b8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="557b8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="557b8-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="557b8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="557b8-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="557b8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="557b8-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="557b8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="557b8-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="557b8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="557b8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="557b8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="557b8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="557b8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





