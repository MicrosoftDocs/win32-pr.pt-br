---
title: Mensagem de TB_GETTOOLTIPS (commctrl. h)
description: Recupera o identificador para o controle ToolTip, se houver, associado à barra de ferramentas.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- Controles de TB_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009450"
---
# <a name="tb_gettooltips-message"></a><span data-ttu-id="fc87d-104">Mensagem de $ \_ Tooltips de TB</span><span class="sxs-lookup"><span data-stu-id="fc87d-104">TB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="fc87d-105">Recupera o identificador para o controle ToolTip, se houver, associado à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="fc87d-105">Retrieves the handle to the tooltip control, if any, associated with the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc87d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc87d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc87d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc87d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fc87d-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fc87d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fc87d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc87d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fc87d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fc87d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc87d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc87d-111">Return value</span></span>

<span data-ttu-id="fc87d-112">Retorna o identificador para o controle ToolTip, ou **NULL** se a barra de ferramentas não tiver nenhuma dica de ferramenta associada.</span><span class="sxs-lookup"><span data-stu-id="fc87d-112">Returns the handle to the tooltip control, or **NULL** if the toolbar has no associated tooltip.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc87d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc87d-113">Requirements</span></span>



| <span data-ttu-id="fc87d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc87d-114">Requirement</span></span> | <span data-ttu-id="fc87d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fc87d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc87d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc87d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc87d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc87d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc87d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc87d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc87d-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc87d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc87d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc87d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc87d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc87d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





