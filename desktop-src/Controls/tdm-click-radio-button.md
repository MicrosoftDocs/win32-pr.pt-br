---
title: Mensagem de TDM_CLICK_RADIO_BUTTON (commctrl. h)
description: Simula a ação de um botão de opção clique em uma caixa de diálogo de tarefa.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- Controles de TDM_CLICK_RADIO_BUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919080"
---
# <a name="tdm_click_radio_button-message"></a><span data-ttu-id="f89a8-104">\_Mensagem do \_ botão de opção de clique do TDM \_</span><span class="sxs-lookup"><span data-stu-id="f89a8-104">TDM\_CLICK\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="f89a8-105">Simula a ação de um botão de opção clique em uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="f89a8-105">Simulates the action of a radio button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="f89a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f89a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f89a8-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f89a8-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f89a8-108">Um valor **int** que especifica a ID do botão de opção a ser clicado.</span><span class="sxs-lookup"><span data-stu-id="f89a8-108">An **int** value that specifies the ID of the radio button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="f89a8-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f89a8-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f89a8-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f89a8-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f89a8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f89a8-111">Return value</span></span>

<span data-ttu-id="f89a8-112">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f89a8-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f89a8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f89a8-113">Remarks</span></span>

<span data-ttu-id="f89a8-114">A ID do botão de opção especificado é enviada para a função de retorno de chamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte de um [botão de \_ opção TDN \_ \_ clicado](tdn-radio-button-clicked.md) no código de notificação.</span><span class="sxs-lookup"><span data-stu-id="f89a8-114">The specified radio button ID is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_RADIO\_BUTTON\_CLICKED](tdn-radio-button-clicked.md) notification code.</span></span> <span data-ttu-id="f89a8-115">Depois que a função de retorno de chamada retornar, o botão de opção será selecionado.</span><span class="sxs-lookup"><span data-stu-id="f89a8-115">After the callback function returns, the radio button will be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="f89a8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f89a8-116">Requirements</span></span>



| <span data-ttu-id="f89a8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f89a8-117">Requirement</span></span> | <span data-ttu-id="f89a8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f89a8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f89a8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f89a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f89a8-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f89a8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f89a8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f89a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f89a8-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f89a8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f89a8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f89a8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f89a8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f89a8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

