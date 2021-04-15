---
title: TVN_SINGLEEXPAND código de notificação (commctrl. h)
description: Enviado por um controle de exibição de árvore com o \_ estilo de TVs SINGLEEXPAND quando o usuário abre ou fecha um item de árvore usando um único clique do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454822"
---
# <a name="tvn_singleexpand-notification-code"></a><span data-ttu-id="d7b88-105">Código de notificação do TVN \_ SINGLEEXPAND</span><span class="sxs-lookup"><span data-stu-id="d7b88-105">TVN\_SINGLEEXPAND notification code</span></span>

<span data-ttu-id="d7b88-106">Enviado por um controle de exibição de árvore com o estilo de [**TVs \_ SINGLEEXPAND**](tree-view-control-window-styles.md) quando o usuário abre ou fecha um item de árvore usando um único clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="d7b88-106">Sent by a tree-view control with the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style when the user opens or closes a tree item using a single click of the mouse.</span></span> <span data-ttu-id="d7b88-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d7b88-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a><span data-ttu-id="d7b88-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7b88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b88-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7b88-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7b88-110">Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="d7b88-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b88-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7b88-111">Return value</span></span>

<span data-ttu-id="d7b88-112">Retorne \_ o padrão TVNRET para permitir que o comportamento padrão ocorra.</span><span class="sxs-lookup"><span data-stu-id="d7b88-112">Return TVNRET\_DEFAULT to allow the default behavior to occur.</span></span> <span data-ttu-id="d7b88-113">Para modificar o comportamento padrão, retorne:</span><span class="sxs-lookup"><span data-stu-id="d7b88-113">To modify the default behavior, return:</span></span>



| <span data-ttu-id="d7b88-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d7b88-114">Return code</span></span>                                                                                    | <span data-ttu-id="d7b88-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7b88-115">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7b88-116"><dt>**TVNRET \_ SKIPOLD**</dt></span><span class="sxs-lookup"><span data-stu-id="d7b88-116"><dt>**TVNRET\_SKIPOLD**</dt></span></span> </dl> | <span data-ttu-id="d7b88-117">Ignorar o processamento padrão do item que está sendo desmarcado.</span><span class="sxs-lookup"><span data-stu-id="d7b88-117">Skip default processing of the item being unselected.</span></span><br/> |
| <dl> <span data-ttu-id="d7b88-118"><dt>**TVNRET \_ SKIPNEW**</dt></span><span class="sxs-lookup"><span data-stu-id="d7b88-118"><dt>**TVNRET\_SKIPNEW**</dt></span></span> </dl> | <span data-ttu-id="d7b88-119">Ignorar o processamento padrão do item que está sendo selecionado.</span><span class="sxs-lookup"><span data-stu-id="d7b88-119">Skip default processing of the item being selected.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="d7b88-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7b88-120">Remarks</span></span>

<span data-ttu-id="d7b88-121">Para ignorar o processamento padrão de itens selecionados e não selecionados, retorne TVNRET \_ SKIPOLD e TVNRET \_ SKIPNEW combinando-os com um OR lógico.</span><span class="sxs-lookup"><span data-stu-id="d7b88-121">To skip default processing of selected and unselected items, return both TVNRET\_SKIPOLD and TVNRET\_SKIPNEW by combining them with a logical OR.</span></span>

<span data-ttu-id="d7b88-122">Esse código de notificação é enviado somente por controles de exibição de árvore que têm o estilo [**\_ SINGLEEXPAND de TVs**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d7b88-122">This notification code is only sent by tree-view controls that have the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7b88-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7b88-123">Requirements</span></span>



| <span data-ttu-id="d7b88-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7b88-124">Requirement</span></span> | <span data-ttu-id="d7b88-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d7b88-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b88-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b88-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b88-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7b88-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7b88-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b88-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b88-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7b88-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7b88-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7b88-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7b88-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7b88-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





