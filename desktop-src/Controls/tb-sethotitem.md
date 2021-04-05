---
title: Mensagem de TB_SETHOTITEM (commctrl. h)
description: Define o item ativo em uma barra de ferramentas.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- Controles de TB_SETHOTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824612"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="d4b9b-104">TB de \_ mensagem SETHOTITEM</span><span class="sxs-lookup"><span data-stu-id="d4b9b-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="d4b9b-105">Define o item ativo em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d4b9b-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4b9b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4b9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b9b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4b9b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b9b-108">Índice do item que se tornará quente.</span><span class="sxs-lookup"><span data-stu-id="d4b9b-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="d4b9b-109">Se esse valor for-1, nenhum dos itens será quente.</span><span class="sxs-lookup"><span data-stu-id="d4b9b-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="d4b9b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4b9b-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d4b9b-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d4b9b-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4b9b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4b9b-112">Return value</span></span>

<span data-ttu-id="d4b9b-113">Retorna o índice do item ativo anterior, ou-1 se não houver nenhum item ativo.</span><span class="sxs-lookup"><span data-stu-id="d4b9b-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4b9b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4b9b-114">Remarks</span></span>

<span data-ttu-id="d4b9b-115">O comportamento dessa mensagem não é definido para barras de ferramentas que não têm o estilo [**\_ simples TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d4b9b-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b9b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4b9b-116">Requirements</span></span>



| <span data-ttu-id="d4b9b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4b9b-117">Requirement</span></span> | <span data-ttu-id="d4b9b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d4b9b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b9b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4b9b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b9b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4b9b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4b9b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4b9b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b9b-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4b9b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4b9b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4b9b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4b9b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4b9b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





