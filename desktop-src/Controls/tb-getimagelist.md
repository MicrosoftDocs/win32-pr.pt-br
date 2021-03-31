---
title: Mensagem de TB_GETIMAGELIST (commctrl. h)
description: Recupera a lista de imagens que um controle Toolbar usa para exibir botões em seu estado padrão. Um controle Toolbar usa essa lista de imagens para exibir botões quando eles não estão ativos ou desabilitados.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- Controles de TB_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644343"
---
# <a name="tb_getimagelist-message"></a><span data-ttu-id="38dcf-105">Mensagem de TB \_ GETimagelist</span><span class="sxs-lookup"><span data-stu-id="38dcf-105">TB\_GETIMAGELIST message</span></span>

<span data-ttu-id="38dcf-106">Recupera a lista de imagens que um controle Toolbar usa para exibir botões em seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="38dcf-106">Retrieves the image list that a toolbar control uses to display buttons in their default state.</span></span> <span data-ttu-id="38dcf-107">Um controle Toolbar usa essa lista de imagens para exibir botões quando eles não estão ativos ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="38dcf-107">A toolbar control uses this image list to display buttons when they are not hot or disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="38dcf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38dcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38dcf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38dcf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38dcf-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="38dcf-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="38dcf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38dcf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38dcf-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="38dcf-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38dcf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38dcf-113">Return value</span></span>

<span data-ttu-id="38dcf-114">Retorna o identificador para a lista de imagens, ou **NULL** se nenhuma lista de imagens for definida.</span><span class="sxs-lookup"><span data-stu-id="38dcf-114">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="38dcf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38dcf-115">Requirements</span></span>



| <span data-ttu-id="38dcf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="38dcf-116">Requirement</span></span> | <span data-ttu-id="38dcf-117">Valor</span><span class="sxs-lookup"><span data-stu-id="38dcf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38dcf-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38dcf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38dcf-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38dcf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38dcf-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38dcf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38dcf-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38dcf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38dcf-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38dcf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="38dcf-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="38dcf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





