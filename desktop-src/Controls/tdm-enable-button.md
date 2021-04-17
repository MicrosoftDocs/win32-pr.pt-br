---
title: Mensagem de TDM_ENABLE_BUTTON (commctrl. h)
description: Habilita ou desabilita um botão de ação em uma caixa de diálogo de tarefa.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- Controles de TDM_ENABLE_BUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762747"
---
# <a name="tdm_enable_button-message"></a><span data-ttu-id="07201-104">\_Mensagem de \_ botão habilitar TDM</span><span class="sxs-lookup"><span data-stu-id="07201-104">TDM\_ENABLE\_BUTTON message</span></span>

<span data-ttu-id="07201-105">Habilita ou desabilita um botão de ação em uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="07201-105">Enables or disables a push button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="07201-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07201-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07201-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07201-108">Um valor **int** que especifica a ID do botão de ação a ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="07201-108">An **int** value that specifies the ID of the push button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="07201-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07201-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07201-110">Especifica o estado do botão.</span><span class="sxs-lookup"><span data-stu-id="07201-110">Specifies button state.</span></span> <span data-ttu-id="07201-111">Defina como 0 para desabilitar o botão; Defina como diferente de zero para habilitar o botão.</span><span class="sxs-lookup"><span data-stu-id="07201-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07201-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07201-112">Return value</span></span>

<span data-ttu-id="07201-113">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="07201-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="07201-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07201-114">Requirements</span></span>



| <span data-ttu-id="07201-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="07201-115">Requirement</span></span> | <span data-ttu-id="07201-116">Valor</span><span class="sxs-lookup"><span data-stu-id="07201-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07201-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07201-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07201-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07201-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07201-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07201-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07201-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07201-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07201-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07201-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="07201-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07201-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





