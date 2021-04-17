---
title: Mensagem de TB_SETANCHORHIGHLIGHT (commctrl. h)
description: Define a configuração de realce de âncora para uma barra de ferramentas.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- Controles de TB_SETANCHORHIGHLIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755648"
---
# <a name="tb_setanchorhighlight-message"></a><span data-ttu-id="01f35-104">TB de \_ mensagem SETANCHORHIGHLIGHT</span><span class="sxs-lookup"><span data-stu-id="01f35-104">TB\_SETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="01f35-105">Define a configuração de realce de âncora para uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="01f35-105">Sets the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="01f35-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01f35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f35-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01f35-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01f35-108">Valor **bool** que especifica se o realce de âncora está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="01f35-108">**BOOL** value that specifies if anchor highlighting is enabled or disabled.</span></span> <span data-ttu-id="01f35-109">Se esse valor for diferente de zero, o realce de âncora será habilitado.</span><span class="sxs-lookup"><span data-stu-id="01f35-109">If this value is nonzero, anchor highlighting will be enabled.</span></span> <span data-ttu-id="01f35-110">Se esse valor for zero, o realce de âncora será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="01f35-110">If this value is zero, anchor highlighting will be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="01f35-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01f35-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="01f35-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="01f35-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f35-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01f35-113">Return value</span></span>

<span data-ttu-id="01f35-114">Retorna a configuração de realce da âncora anterior.</span><span class="sxs-lookup"><span data-stu-id="01f35-114">Returns the previous anchor highlight setting.</span></span> <span data-ttu-id="01f35-115">Se esse valor for diferente de zero, o realce de âncora foi habilitado.</span><span class="sxs-lookup"><span data-stu-id="01f35-115">If this value is nonzero, anchor highlighting was enabled.</span></span> <span data-ttu-id="01f35-116">Se esse valor for zero, o realce de âncora foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="01f35-116">If this value is zero, anchor highlighting was disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="01f35-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="01f35-117">Remarks</span></span>

<span data-ttu-id="01f35-118">Realce de âncora em uma barra de ferramentas significa que o último item realçado permanecerá realçado até que outro item seja realçado.</span><span class="sxs-lookup"><span data-stu-id="01f35-118">Anchor highlighting in a toolbar means that the last highlighted item will remain highlighted until another item is highlighted.</span></span> <span data-ttu-id="01f35-119">Isso ocorre mesmo que o cursor saia do controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="01f35-119">This occurs even if the cursor leaves the toolbar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="01f35-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01f35-120">Requirements</span></span>



| <span data-ttu-id="01f35-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f35-121">Requirement</span></span> | <span data-ttu-id="01f35-122">Valor</span><span class="sxs-lookup"><span data-stu-id="01f35-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01f35-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01f35-123">Minimum supported client</span></span><br/> | <span data-ttu-id="01f35-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01f35-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01f35-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01f35-125">Minimum supported server</span></span><br/> | <span data-ttu-id="01f35-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01f35-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01f35-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01f35-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="01f35-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01f35-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





