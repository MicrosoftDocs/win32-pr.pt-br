---
title: Mensagem de TB_SETTOOLTIPS (commctrl. h)
description: Associa um controle ToolTip a uma barra de ferramentas.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- Controles de TB_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009122"
---
# <a name="tb_settooltips-message"></a><span data-ttu-id="91c36-104">Mensagem de TB \_ SETtooltips</span><span class="sxs-lookup"><span data-stu-id="91c36-104">TB\_SETTOOLTIPS message</span></span>

<span data-ttu-id="91c36-105">Associa um controle ToolTip a uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="91c36-105">Associates a tooltip control with a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="91c36-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91c36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c36-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91c36-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91c36-108">Identificador para o controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="91c36-108">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="91c36-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91c36-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91c36-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="91c36-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c36-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91c36-111">Return value</span></span>

<span data-ttu-id="91c36-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="91c36-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c36-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="91c36-113">Remarks</span></span>

<span data-ttu-id="91c36-114">Todos os botões adicionados a uma barra de ferramentas antes de enviar a mensagem de **TB \_ SetToolTips** não serão registrados com o controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="91c36-114">Any buttons added to a toolbar before sending the **TB\_SETTOOLTIPS** message will not be registered with the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c36-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91c36-115">Requirements</span></span>



| <span data-ttu-id="91c36-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="91c36-116">Requirement</span></span> | <span data-ttu-id="91c36-117">Valor</span><span class="sxs-lookup"><span data-stu-id="91c36-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91c36-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91c36-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91c36-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91c36-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91c36-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91c36-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91c36-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91c36-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91c36-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91c36-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91c36-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91c36-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





