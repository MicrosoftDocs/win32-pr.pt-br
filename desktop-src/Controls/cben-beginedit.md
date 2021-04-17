---
title: CBEN_BEGINEDIT código de notificação (commctrl. h)
description: Enviado quando o usuário ativa a lista suspensa ou clica na caixa de edição do controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- CBEN_BEGINEDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d4cc80d12b01b9374173f413f0aee3701e5040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749078"
---
# <a name="cben_beginedit-notification-code"></a><span data-ttu-id="e3f01-105">\_Código de notificação CBEN BEGINEDIT</span><span class="sxs-lookup"><span data-stu-id="e3f01-105">CBEN\_BEGINEDIT notification code</span></span>

<span data-ttu-id="e3f01-106">Enviado quando o usuário ativa a lista suspensa ou clica na caixa de edição do controle.</span><span class="sxs-lookup"><span data-stu-id="e3f01-106">Sent when the user activates the drop-down list or clicks in the control's edit box.</span></span> <span data-ttu-id="e3f01-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e3f01-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e3f01-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3f01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f01-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3f01-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3f01-110">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="e3f01-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f01-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3f01-111">Return value</span></span>

<span data-ttu-id="e3f01-112">O aplicativo que processa esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="e3f01-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f01-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3f01-113">Requirements</span></span>



| <span data-ttu-id="e3f01-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3f01-114">Requirement</span></span> | <span data-ttu-id="e3f01-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e3f01-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f01-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3f01-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f01-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3f01-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3f01-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3f01-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f01-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3f01-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3f01-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3f01-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3f01-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f01-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





