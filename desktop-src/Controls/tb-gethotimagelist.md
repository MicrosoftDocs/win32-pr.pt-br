---
title: Mensagem de TB_GETHOTIMAGELIST (commctrl. h)
description: Recupera a lista de imagens que um controle Toolbar usa para exibir botões de atalho.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- Controles de TB_GETHOTIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085672"
---
# <a name="tb_gethotimagelist-message"></a><span data-ttu-id="3ce7b-104">TB de \_ mensagem GETHOTIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="3ce7b-104">TB\_GETHOTIMAGELIST message</span></span>

<span data-ttu-id="3ce7b-105">Recupera a lista de imagens que um controle Toolbar usa para exibir botões de atalho.</span><span class="sxs-lookup"><span data-stu-id="3ce7b-105">Retrieves the image list that a toolbar control uses to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ce7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ce7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce7b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ce7b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3ce7b-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3ce7b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3ce7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ce7b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3ce7b-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3ce7b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce7b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ce7b-111">Return value</span></span>

<span data-ttu-id="3ce7b-112">Retorna o identificador para a lista de imagens que o controle usa para exibir botões quentes ou **NULL** se nenhuma lista de imagens ativas estiver definida.</span><span class="sxs-lookup"><span data-stu-id="3ce7b-112">Returns the handle to the image list that the control uses to display hot buttons, or **NULL** if no hot image list is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ce7b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ce7b-113">Remarks</span></span>

<span data-ttu-id="3ce7b-114">Um botão fica quente quando o cursor está sobre ele.</span><span class="sxs-lookup"><span data-stu-id="3ce7b-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="3ce7b-115">Os controles da barra de ferramentas devem ter o estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ simples**](toolbar-control-and-button-styles.md) ou TBSTYLE para ter itens quentes.</span><span class="sxs-lookup"><span data-stu-id="3ce7b-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce7b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ce7b-116">Requirements</span></span>



| <span data-ttu-id="3ce7b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ce7b-117">Requirement</span></span> | <span data-ttu-id="3ce7b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3ce7b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce7b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce7b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce7b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ce7b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ce7b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce7b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce7b-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ce7b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ce7b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ce7b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce7b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce7b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





