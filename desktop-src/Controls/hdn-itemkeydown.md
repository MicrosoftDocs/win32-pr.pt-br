---
title: HDN_ITEMKEYDOWN código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de cabeçalho que uma tecla foi pressionada com um item selecionado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009753"
---
# <a name="hdn_itemkeydown-notification-code"></a><span data-ttu-id="1b6cc-105">Código de notificação do HDN de \_ ISkeydown</span><span class="sxs-lookup"><span data-stu-id="1b6cc-105">HDN\_ITEMKEYDOWN notification code</span></span>

<span data-ttu-id="1b6cc-106">Notifica uma janela pai do controle de cabeçalho que uma tecla foi pressionada com um item selecionado.</span><span class="sxs-lookup"><span data-stu-id="1b6cc-106">Notifies a header control's parent window that a key has been pressed with an item selected.</span></span> <span data-ttu-id="1b6cc-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1b6cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1b6cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b6cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b6cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b6cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b6cc-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações adicionais sobre a chave que está sendo pressionada.</span><span class="sxs-lookup"><span data-stu-id="1b6cc-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b6cc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b6cc-111">Return value</span></span>

<span data-ttu-id="1b6cc-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1b6cc-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b6cc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b6cc-113">Requirements</span></span>



| <span data-ttu-id="1b6cc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b6cc-114">Requirement</span></span> | <span data-ttu-id="1b6cc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1b6cc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b6cc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b6cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1b6cc-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b6cc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b6cc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b6cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1b6cc-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b6cc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b6cc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b6cc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b6cc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b6cc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





