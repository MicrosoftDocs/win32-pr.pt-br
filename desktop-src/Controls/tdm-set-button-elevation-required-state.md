---
title: Mensagem de TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (commctrl. h)
description: Especifica se um determinado botão de diálogo de tarefa ou link de comando deve ter um ícone de escudo de UAC (controle de conta de usuário); ou seja, se a ação invocada pelo botão requer elevação.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- Controles de TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086320"
---
# <a name="tdm_set_button_elevation_required_state-message"></a><span data-ttu-id="9b605-104">\_Mensagem de \_ \_ \_ estado necessário de elevação do botão \_ de TDM Set</span><span class="sxs-lookup"><span data-stu-id="9b605-104">TDM\_SET\_BUTTON\_ELEVATION\_REQUIRED\_STATE message</span></span>

<span data-ttu-id="9b605-105">Especifica se um determinado botão de diálogo de tarefa ou link de comando deve ter um ícone de escudo de UAC (controle de conta de usuário); ou seja, se a ação invocada pelo botão requer elevação.</span><span class="sxs-lookup"><span data-stu-id="9b605-105">Specifies whether a given task dialog button or command link should have a User Account Control (UAC) shield icon; that is, whether the action invoked by the button requires elevation.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b605-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b605-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b605-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b605-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b605-108">A ID do botão de ação ou link de comando a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9b605-108">The ID of the push button or command link to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="9b605-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b605-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b605-110">Defina como 0 para designar que a ação invocada pelo botão não requer elevação.</span><span class="sxs-lookup"><span data-stu-id="9b605-110">Set to 0 to designate that the action invoked by the button does not require elevation.</span></span> <span data-ttu-id="9b605-111">Defina como diferente de zero para designar que a ação requer elevação.</span><span class="sxs-lookup"><span data-stu-id="9b605-111">Set to nonzero to designate that the action requires elevation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b605-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b605-112">Return value</span></span>

<span data-ttu-id="9b605-113">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9b605-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b605-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b605-114">Requirements</span></span>



| <span data-ttu-id="9b605-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b605-115">Requirement</span></span> | <span data-ttu-id="9b605-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9b605-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b605-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b605-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9b605-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b605-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b605-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b605-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9b605-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9b605-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b605-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b605-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b605-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b605-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





