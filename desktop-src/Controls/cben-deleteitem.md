---
title: CBEN_DELETEITEM código de notificação (commctrl. h)
description: Enviado quando um item foi excluído. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8b0d03ff-57fa-44dc-ab3e-05089b876e3c
keywords:
- CBEN_DELETEITEM de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBEN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c7ca7329898c9dd0c6bba76cba9d3524b017e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824720"
---
# <a name="cben_deleteitem-notification-code"></a><span data-ttu-id="b7040-105">Código de notificação do CBEN \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="b7040-105">CBEN\_DELETEITEM notification code</span></span>

<span data-ttu-id="b7040-106">Enviado quando um item foi excluído.</span><span class="sxs-lookup"><span data-stu-id="b7040-106">Sent when an item has been deleted.</span></span> <span data-ttu-id="b7040-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b7040-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DELETEITEM

    pCBEx = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b7040-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7040-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7040-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7040-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7040-110">Um ponteiro para uma estrutura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contém informações sobre o código de notificação e o item excluído.</span><span class="sxs-lookup"><span data-stu-id="b7040-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code and the deleted item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7040-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7040-111">Return value</span></span>

<span data-ttu-id="b7040-112">O aplicativo que processa esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="b7040-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7040-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7040-113">Requirements</span></span>



| <span data-ttu-id="b7040-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7040-114">Requirement</span></span> | <span data-ttu-id="b7040-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b7040-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7040-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7040-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b7040-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7040-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7040-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7040-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b7040-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7040-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7040-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7040-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7040-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7040-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





