---
title: Mensagem de TB_INDETERMINATE (commctrl. h)
description: Define ou limpa o estado indeterminado do botão especificado em uma barra de ferramentas.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- Controles de TB_INDETERMINATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009193"
---
# <a name="tb_indeterminate-message"></a><span data-ttu-id="6d2a6-104">TB de \_ mensagem indeterminada</span><span class="sxs-lookup"><span data-stu-id="6d2a6-104">TB\_INDETERMINATE message</span></span>

<span data-ttu-id="6d2a6-105">Define ou limpa o estado indeterminado do botão especificado em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="6d2a6-105">Sets or clears the indeterminate state of the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d2a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d2a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d2a6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d2a6-108">Identificador de comando do botão cujo estado indeterminado deve ser definido ou limpo.</span><span class="sxs-lookup"><span data-stu-id="6d2a6-108">Command identifier of the button whose indeterminate state is to be set or cleared.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d2a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d2a6-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que indica se deve ser definido ou limpo o estado indeterminado.</span><span class="sxs-lookup"><span data-stu-id="6d2a6-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to set or clear the indeterminate state.</span></span> <span data-ttu-id="6d2a6-111">Se for **true**, o estado indeterminado será definido.</span><span class="sxs-lookup"><span data-stu-id="6d2a6-111">If **TRUE**, the indeterminate state is set.</span></span> <span data-ttu-id="6d2a6-112">Se for **false**, o estado será limpo.</span><span class="sxs-lookup"><span data-stu-id="6d2a6-112">If **FALSE**, the state is cleared.</span></span>

<span data-ttu-id="6d2a6-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6d2a6-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2a6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d2a6-114">Return value</span></span>

<span data-ttu-id="6d2a6-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6d2a6-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2a6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d2a6-116">Requirements</span></span>



| <span data-ttu-id="6d2a6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d2a6-117">Requirement</span></span> | <span data-ttu-id="6d2a6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6d2a6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2a6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d2a6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2a6-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d2a6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d2a6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d2a6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2a6-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d2a6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d2a6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d2a6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d2a6-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d2a6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

