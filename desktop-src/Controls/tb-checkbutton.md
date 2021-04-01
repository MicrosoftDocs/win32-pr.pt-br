---
title: Mensagem de TB_CHECKBUTTON (commctrl. h)
description: Verifica ou desmarca um determinado botão em uma barra de ferramentas.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- Controles de TB_CHECKBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7734b37da44db38d9ca09b34ad9e666cc90eb5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009774"
---
# <a name="tb_checkbutton-message"></a><span data-ttu-id="ed8a4-104">TB de \_ mensagem CHECKBUTTON</span><span class="sxs-lookup"><span data-stu-id="ed8a4-104">TB\_CHECKBUTTON message</span></span>

<span data-ttu-id="ed8a4-105">Verifica ou desmarca um determinado botão em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ed8a4-105">Checks or unchecks a given button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed8a4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed8a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8a4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed8a4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed8a4-108">Identificador de comando do botão a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="ed8a4-108">Command identifier of the button to check.</span></span>

</dd> <dt>

<span data-ttu-id="ed8a4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed8a4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed8a4-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que indica se deve marcar ou desmarcar o botão especificado.</span><span class="sxs-lookup"><span data-stu-id="ed8a4-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to check or uncheck the specified button.</span></span> <span data-ttu-id="ed8a4-111">Se for **true**, a verificação será adicionada.</span><span class="sxs-lookup"><span data-stu-id="ed8a4-111">If **TRUE**, the check is added.</span></span> <span data-ttu-id="ed8a4-112">Se for **false**, a verificação será removida.</span><span class="sxs-lookup"><span data-stu-id="ed8a4-112">If **FALSE**, the check is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8a4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed8a4-113">Return value</span></span>

<span data-ttu-id="ed8a4-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ed8a4-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed8a4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed8a4-115">Remarks</span></span>

<span data-ttu-id="ed8a4-116">Quando um botão é marcado, ele é exibido no estado pressionado.</span><span class="sxs-lookup"><span data-stu-id="ed8a4-116">When a button is checked, it is displayed in the pressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8a4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed8a4-117">Requirements</span></span>



| <span data-ttu-id="ed8a4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed8a4-118">Requirement</span></span> | <span data-ttu-id="ed8a4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ed8a4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8a4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed8a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8a4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed8a4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed8a4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed8a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8a4-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed8a4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed8a4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed8a4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed8a4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed8a4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

