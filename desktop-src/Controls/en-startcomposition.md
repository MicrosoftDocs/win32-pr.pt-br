---
title: EN_STARTCOMPOSITION código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o usuário iniciou digitando com o IME ou a estrutura de serviços de texto.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- EN_STARTCOMPOSITION de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a103431427a9325a6b74c27927fb56e65f6fe771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086181"
---
# <a name="en_startcomposition-notification-code"></a><span data-ttu-id="b9091-104">\_Código de notificação en STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="b9091-104">EN\_STARTCOMPOSITION notification code</span></span>

<span data-ttu-id="b9091-105">Notifica uma janela pai do controle de edição rico que o usuário iniciou digitando com o IME ou a [estrutura de serviços de texto](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="b9091-105">Notifies a rich edit control parent window that the user started typing with IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b9091-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9091-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9091-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9091-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9091-108">Uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="b9091-108">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9091-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9091-109">Requirements</span></span>



| <span data-ttu-id="b9091-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9091-110">Requirement</span></span> | <span data-ttu-id="b9091-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b9091-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9091-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9091-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b9091-113">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b9091-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b9091-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9091-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b9091-115">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b9091-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b9091-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9091-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9091-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9091-117"><dt>Richedit.h</dt></span></span> </dl> |



 

