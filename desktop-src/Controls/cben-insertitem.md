---
title: CBEN_INSERTITEM código de notificação (commctrl. h)
description: Enviado quando um novo item é inserido no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ccd05ea75015479ef32415d920bbe639664ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645229"
---
# <a name="cben_insertitem-notification-code"></a><span data-ttu-id="10b7d-105">Código de notificação do CBEN \_ INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="10b7d-105">CBEN\_INSERTITEM notification code</span></span>

<span data-ttu-id="10b7d-106">Enviado quando um novo item é inserido no controle.</span><span class="sxs-lookup"><span data-stu-id="10b7d-106">Sent when a new item has been inserted in the control.</span></span> <span data-ttu-id="10b7d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="10b7d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="10b7d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10b7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b7d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10b7d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10b7d-110">Um ponteiro para uma estrutura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contém informações sobre o código de notificação e o item que foi inserido.</span><span class="sxs-lookup"><span data-stu-id="10b7d-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure containing information about the notification code and the item that was inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b7d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10b7d-111">Return value</span></span>

<span data-ttu-id="10b7d-112">O aplicativo que processa esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="10b7d-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b7d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10b7d-113">Requirements</span></span>



| <span data-ttu-id="10b7d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b7d-114">Requirement</span></span> | <span data-ttu-id="10b7d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="10b7d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10b7d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10b7d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="10b7d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10b7d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10b7d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10b7d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="10b7d-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10b7d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10b7d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10b7d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b7d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b7d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





