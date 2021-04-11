---
title: Mensagem de TB_GETHOTITEM (commctrl. h)
description: Recupera o índice do item ativo em uma barra de ferramentas.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- Controles de TB_GETHOTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455008"
---
# <a name="tb_gethotitem-message"></a><span data-ttu-id="e3164-104">TB de \_ mensagem GETHOTITEM</span><span class="sxs-lookup"><span data-stu-id="e3164-104">TB\_GETHOTITEM message</span></span>

<span data-ttu-id="e3164-105">Recupera o índice do item ativo em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e3164-105">Retrieves the index of the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3164-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3164-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3164-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3164-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e3164-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e3164-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e3164-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3164-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e3164-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e3164-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3164-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3164-111">Return value</span></span>

<span data-ttu-id="e3164-112">Retorna o índice do item ativo ou-1 se nenhum item ativo for definido.</span><span class="sxs-lookup"><span data-stu-id="e3164-112">Returns the index of the hot item, or -1 if no hot item is set.</span></span> <span data-ttu-id="e3164-113">Os controles da barra de ferramentas que não têm o estilo [**\_ simples TBSTYLE**](toolbar-control-and-button-styles.md) não têm itens quentes.</span><span class="sxs-lookup"><span data-stu-id="e3164-113">Toolbar controls that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style do not have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3164-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3164-114">Requirements</span></span>



| <span data-ttu-id="e3164-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3164-115">Requirement</span></span> | <span data-ttu-id="e3164-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e3164-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3164-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3164-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3164-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3164-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3164-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3164-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3164-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3164-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3164-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3164-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3164-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3164-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





