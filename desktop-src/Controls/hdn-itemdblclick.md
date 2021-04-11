---
title: HDN_ITEMDBLCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que o usuário clicou duas vezes no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ . Somente os controles de cabeçalho que são definidos para o \_ estilo de botões HDS enviam este código de notificação.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163618"
---
# <a name="hdn_itemdblclick-notification-code"></a><span data-ttu-id="e33bd-106">Código de notificação do HDN \_ ITEMDBLCLICK</span><span class="sxs-lookup"><span data-stu-id="e33bd-106">HDN\_ITEMDBLCLICK notification code</span></span>

<span data-ttu-id="e33bd-107">Notifica uma janela pai do controle de cabeçalho que o usuário clicou duas vezes no controle.</span><span class="sxs-lookup"><span data-stu-id="e33bd-107">Notifies a header control's parent window that the user double-clicked the control.</span></span> <span data-ttu-id="e33bd-108">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e33bd-108">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="e33bd-109">Somente os controles de cabeçalho que são definidos para o estilo de [**\_ botões HDS**](header-control-styles.md) enviam este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="e33bd-109">Only header controls that are set to the [**HDS\_BUTTONS**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e33bd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e33bd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e33bd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e33bd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e33bd-112">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="e33bd-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e33bd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e33bd-113">Return value</span></span>

<span data-ttu-id="e33bd-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e33bd-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e33bd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e33bd-115">Requirements</span></span>



| <span data-ttu-id="e33bd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e33bd-116">Requirement</span></span> | <span data-ttu-id="e33bd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e33bd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e33bd-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e33bd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e33bd-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e33bd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e33bd-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e33bd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e33bd-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e33bd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e33bd-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e33bd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e33bd-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e33bd-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e33bd-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e33bd-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e33bd-125">**HDN \_ ITEMDBLCLICKW** (Unicode) e **HDN \_ ITEMDBLCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e33bd-125">**HDN\_ITEMDBLCLICKW** (Unicode) and **HDN\_ITEMDBLCLICKA** (ANSI)</span></span><br/>         |



 

 





