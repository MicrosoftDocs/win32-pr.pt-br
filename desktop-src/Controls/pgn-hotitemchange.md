---
title: Mensagem de PGN_HOTITEMCHANGE (commctrl. h)
description: Notifica uma janela pai do controle de pager que o item quente (realçado) foi alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- Controles de PGN_HOTITEMCHANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009261"
---
# <a name="pgn_hotitemchange-message"></a><span data-ttu-id="baff9-105">\_Mensagem PGN HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="baff9-105">PGN\_HOTITEMCHANGE message</span></span>

<span data-ttu-id="baff9-106">Notifica uma janela pai do controle de pager que o item quente (realçado) foi alterado.</span><span class="sxs-lookup"><span data-stu-id="baff9-106">Notifies a pager control's parent window that the hot (highlighted) item has change.</span></span> <span data-ttu-id="baff9-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="baff9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="baff9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baff9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baff9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="baff9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baff9-110">Ponteiro para uma estrutura [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="baff9-110">Pointer to a [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baff9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="baff9-111">Return value</span></span>

<span data-ttu-id="baff9-112">Retornar zero para realçar o item ou diferente de zero para evitar o realce.</span><span class="sxs-lookup"><span data-stu-id="baff9-112">Return zero to highlight the item or nonzero to prevent highlighting.</span></span>

## <a name="remarks"></a><span data-ttu-id="baff9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="baff9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="baff9-114">Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="baff9-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="baff9-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="baff9-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="baff9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baff9-116">Requirements</span></span>



| <span data-ttu-id="baff9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="baff9-117">Requirement</span></span> | <span data-ttu-id="baff9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="baff9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="baff9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baff9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="baff9-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="baff9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="baff9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baff9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="baff9-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="baff9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="baff9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="baff9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="baff9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="baff9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





