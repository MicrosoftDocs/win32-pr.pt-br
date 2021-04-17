---
title: Mensagem de BM_SETDONTCLICK (WinUser. h)
description: Define um sinalizador em um botão de opção que controla a geração de \_ mensagens bilhão clicadas quando o botão recebe o foco.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- Controles de BM_SETDONTCLICK de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754382"
---
# <a name="bm_setdontclick-message"></a><span data-ttu-id="15152-104">\_Mensagem BM SETDONTCLICK</span><span class="sxs-lookup"><span data-stu-id="15152-104">BM\_SETDONTCLICK message</span></span>

<span data-ttu-id="15152-105">Define um sinalizador em um botão de opção que controla a geração de mensagens [bilhão \_ clicadas](bn-clicked.md) quando o botão recebe o foco.</span><span class="sxs-lookup"><span data-stu-id="15152-105">Sets a flag on a radio button that controls the generation of [BN\_CLICKED](bn-clicked.md) messages when the button receives focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="15152-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15152-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15152-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15152-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15152-108">Um **bool** que especifica o estado.</span><span class="sxs-lookup"><span data-stu-id="15152-108">A **BOOL** that specifies the state.</span></span> <span data-ttu-id="15152-109">**True** para definir o sinalizador, caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="15152-109">**TRUE** to set the flag, otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="15152-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15152-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15152-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="15152-111">Not used.</span></span> <span data-ttu-id="15152-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="15152-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15152-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15152-113">Return value</span></span>

<span data-ttu-id="15152-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="15152-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="15152-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15152-115">Requirements</span></span>



| <span data-ttu-id="15152-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="15152-116">Requirement</span></span> | <span data-ttu-id="15152-117">Valor</span><span class="sxs-lookup"><span data-stu-id="15152-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15152-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15152-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15152-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15152-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="15152-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15152-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15152-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15152-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15152-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15152-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="15152-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15152-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





