---
title: Mensagem de TB_MARKBUTTON (commctrl. h)
description: Define o estado de realce de um determinado botão em um controle ToolBar.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- Controles de TB_MARKBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d42983f5fb0ef6e62716cefa2fa8db4fca87fa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009602"
---
# <a name="tb_markbutton-message"></a><span data-ttu-id="ac4e1-104">TB de \_ mensagem MARKBUTTON</span><span class="sxs-lookup"><span data-stu-id="ac4e1-104">TB\_MARKBUTTON message</span></span>

<span data-ttu-id="ac4e1-105">Define o estado de realce de um determinado botão em um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="ac4e1-105">Sets the highlight state of a given button in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac4e1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac4e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac4e1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac4e1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac4e1-108">Identificador de comando para um botão da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ac4e1-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="ac4e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac4e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac4e1-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que indica o novo estado de realce.</span><span class="sxs-lookup"><span data-stu-id="ac4e1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates the new highlight state.</span></span> <span data-ttu-id="ac4e1-111">Se **for true**, o botão será realçado.</span><span class="sxs-lookup"><span data-stu-id="ac4e1-111">If **TRUE**, the button is highlighted.</span></span> <span data-ttu-id="ac4e1-112">Se for **false**, o botão será definido como seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="ac4e1-112">If **FALSE**, the button is set to its default state.</span></span>

<span data-ttu-id="ac4e1-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ac4e1-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac4e1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac4e1-114">Return value</span></span>

<span data-ttu-id="ac4e1-115">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="ac4e1-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac4e1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac4e1-116">Requirements</span></span>



| <span data-ttu-id="ac4e1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac4e1-117">Requirement</span></span> | <span data-ttu-id="ac4e1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ac4e1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4e1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac4e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac4e1-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac4e1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac4e1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac4e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac4e1-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ac4e1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac4e1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac4e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac4e1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac4e1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

