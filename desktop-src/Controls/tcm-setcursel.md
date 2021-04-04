---
title: Mensagem de TCM_SETCURSEL (commctrl. h)
description: Seleciona uma guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setcurseal TabCtrl.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- Controles de TCM_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918477"
---
# <a name="tcm_setcursel-message"></a><span data-ttu-id="ac697-105">Mensagem de TCM \_ SETcurseal</span><span class="sxs-lookup"><span data-stu-id="ac697-105">TCM\_SETCURSEL message</span></span>

<span data-ttu-id="ac697-106">Seleciona uma guia em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="ac697-106">Selects a tab in a tab control.</span></span> <span data-ttu-id="ac697-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setcurseal TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="ac697-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac697-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac697-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac697-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac697-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac697-110">Índice da guia a ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="ac697-110">Index of the tab to select.</span></span>

</dd> <dt>

<span data-ttu-id="ac697-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac697-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ac697-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ac697-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac697-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac697-113">Return value</span></span>

<span data-ttu-id="ac697-114">Retorna o índice da guia selecionada anteriormente, se for bem-sucedido, ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ac697-114">Returns the index of the previously selected tab if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac697-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac697-115">Remarks</span></span>

<span data-ttu-id="ac697-116">Um controle guia não envia um código de notificação [TCN \_ SELCHANGING](tcn-selchanging.md) ou [TCN \_ SELCHANGE](tcn-selchange.md) quando uma guia é selecionada usando essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="ac697-116">A tab control does not send a [TCN\_SELCHANGING](tcn-selchanging.md) or [TCN\_SELCHANGE](tcn-selchange.md) notification code when a tab is selected using this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac697-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac697-117">Requirements</span></span>



| <span data-ttu-id="ac697-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac697-118">Requirement</span></span> | <span data-ttu-id="ac697-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ac697-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac697-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac697-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac697-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac697-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac697-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac697-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac697-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ac697-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac697-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac697-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac697-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac697-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





