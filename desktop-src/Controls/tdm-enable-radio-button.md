---
title: Mensagem de TDM_ENABLE_RADIO_BUTTON (commctrl. h)
description: Habilita ou desabilita um botão de opção em uma caixa de diálogo de tarefa.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- Controles de TDM_ENABLE_RADIO_BUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919079"
---
# <a name="tdm_enable_radio_button-message"></a><span data-ttu-id="b5d6f-104">\_Mensagem do \_ botão de opção Habilitar TDM \_</span><span class="sxs-lookup"><span data-stu-id="b5d6f-104">TDM\_ENABLE\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="b5d6f-105">Habilita ou desabilita um botão de opção em uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="b5d6f-105">Enables or disables a radio button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5d6f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5d6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d6f-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5d6f-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d6f-108">Um valor **int** que especifica a ID do botão de opção a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b5d6f-108">An **int** value that specifies the ID of the radio button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="b5d6f-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5d6f-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d6f-110">Especifica o estado do botão.</span><span class="sxs-lookup"><span data-stu-id="b5d6f-110">Specifies button state.</span></span> <span data-ttu-id="b5d6f-111">Defina como 0 para desabilitar o botão; Defina como diferente de zero para habilitar o botão.</span><span class="sxs-lookup"><span data-stu-id="b5d6f-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d6f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5d6f-112">Return value</span></span>

<span data-ttu-id="b5d6f-113">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="b5d6f-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d6f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5d6f-114">Requirements</span></span>



| <span data-ttu-id="b5d6f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d6f-115">Requirement</span></span> | <span data-ttu-id="b5d6f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b5d6f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d6f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5d6f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d6f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5d6f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5d6f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5d6f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d6f-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5d6f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5d6f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5d6f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5d6f-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d6f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





