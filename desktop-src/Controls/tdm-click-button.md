---
title: Mensagem de TDM_CLICK_BUTTON (commctrl. h)
description: Simula a ação de um clique de botão em uma caixa de diálogo de tarefa.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- Controles de TDM_CLICK_BUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751301"
---
# <a name="tdm_click_button-message"></a><span data-ttu-id="fcffb-104">Mensagem do botão de \_ clique do TDM \_</span><span class="sxs-lookup"><span data-stu-id="fcffb-104">TDM\_CLICK\_BUTTON message</span></span>

<span data-ttu-id="fcffb-105">Simula a ação de um clique de botão em uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="fcffb-105">Simulates the action of a button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcffb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcffb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcffb-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcffb-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcffb-108">Um **int** que especifica a ID do botão a ser clicado.</span><span class="sxs-lookup"><span data-stu-id="fcffb-108">An **int** that specifies the ID of the button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="fcffb-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcffb-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcffb-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fcffb-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcffb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcffb-111">Return value</span></span>

<span data-ttu-id="fcffb-112">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="fcffb-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcffb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcffb-113">Remarks</span></span>

<span data-ttu-id="fcffb-114">A ID do botão especificada por *wParam* é enviada para a função de retorno de chamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte de um código de notificação [ \_ \_ clicado no botão TDN](tdn-button-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="fcffb-114">The button ID specified by *wParam* is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) notification code.</span></span> <span data-ttu-id="fcffb-115">Depois que a função de retorno de chamada retornar, a caixa de diálogo de tarefa será fechada se S \_ OK tiver retornado da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="fcffb-115">After the callback function returns, the task dialog is closed if S\_OK was returned from the callback function.</span></span> <span data-ttu-id="fcffb-116">Se S \_ false for retornado da função de retorno de chamada, a caixa de diálogo de tarefa permanecerá ativa.</span><span class="sxs-lookup"><span data-stu-id="fcffb-116">If S\_FALSE was returned from the callback function, the task dialog remains active.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcffb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcffb-117">Requirements</span></span>



| <span data-ttu-id="fcffb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcffb-118">Requirement</span></span> | <span data-ttu-id="fcffb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fcffb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcffb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcffb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fcffb-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcffb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcffb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcffb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fcffb-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fcffb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcffb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcffb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcffb-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcffb-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

