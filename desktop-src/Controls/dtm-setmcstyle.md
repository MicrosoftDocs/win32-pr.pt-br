---
title: Mensagem de DTM_SETMCSTYLE (commctrl. h)
description: Define o estilo de um controle do seletor de data e hora (DTP). Envie essa mensagem explicitamente ou usando a macro DateTime \_ SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- Controles de DTM_SETMCSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085942"
---
# <a name="dtm_setmcstyle-message"></a><span data-ttu-id="c0c4f-105">\_Mensagem DTM SETMCSTYLE</span><span class="sxs-lookup"><span data-stu-id="c0c4f-105">DTM\_SETMCSTYLE message</span></span>

<span data-ttu-id="c0c4f-106">Define o estilo de um controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="c0c4f-106">Sets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="c0c4f-107">Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="c0c4f-107">Send this message explicitly or by using the [**DateTime\_SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0c4f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0c4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0c4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0c4f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0c4f-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c0c4f-111">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0c4f-111">*lParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="c0c4f-112">Um valor de estilo.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-112">A style value.</span></span> <span data-ttu-id="c0c4f-113">Para obter mais informações, consulte <a href="month-calendar-control-styles.md">estilos de controle de calendário mensal</a>.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-113">For more information see <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0c4f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0c4f-114">Return value</span></span>

<span data-ttu-id="c0c4f-115">Retorna o valor do estilo anterior.</span><span class="sxs-lookup"><span data-stu-id="c0c4f-115">Returns the value of the previous style.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0c4f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0c4f-116">Requirements</span></span>



| <span data-ttu-id="c0c4f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0c4f-117">Requirement</span></span> | <span data-ttu-id="c0c4f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c0c4f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c4f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0c4f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0c4f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0c4f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0c4f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0c4f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0c4f-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0c4f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0c4f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0c4f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0c4f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0c4f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





