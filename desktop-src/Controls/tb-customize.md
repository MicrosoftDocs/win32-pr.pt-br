---
title: Mensagem de TB_CUSTOMIZE (commctrl. h)
description: Exibe a caixa de diálogo Personalizar barra de ferramentas.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- Controles de TB_CUSTOMIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749069"
---
# <a name="tb_customize-message"></a><span data-ttu-id="df733-104">Mensagem de personalização de TB \_</span><span class="sxs-lookup"><span data-stu-id="df733-104">TB\_CUSTOMIZE message</span></span>

<span data-ttu-id="df733-105">Exibe a caixa de diálogo **Personalizar barra de ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="df733-105">Displays the **Customize Toolbar** dialog box.</span></span>

## <a name="parameters"></a><span data-ttu-id="df733-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df733-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df733-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df733-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df733-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="df733-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="df733-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df733-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df733-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="df733-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df733-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df733-111">Return value</span></span>

<span data-ttu-id="df733-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="df733-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df733-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="df733-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="df733-114">A barra de ferramentas deve manipular as notificações [tbn \_ QUERYINSERT](tbn-queryinsert.md) e [tbn \_ QUERYDELETE](tbn-querydelete.md) para que a caixa de diálogo **Personalizar barra de ferramentas** seja exibida.</span><span class="sxs-lookup"><span data-stu-id="df733-114">The toolbar must handle the [TBN\_QUERYINSERT](tbn-queryinsert.md) and [TBN\_QUERYDELETE](tbn-querydelete.md) notifications for the **Customize Toolbar** dialog box to appear.</span></span> <span data-ttu-id="df733-115">Se a barra de ferramentas não tratar essas notificações, a **\_ personalização de TB** não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="df733-115">If the toolbar does not handle those notifications, **TB\_CUSTOMIZE** has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df733-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df733-116">Requirements</span></span>



| <span data-ttu-id="df733-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="df733-117">Requirement</span></span> | <span data-ttu-id="df733-118">Valor</span><span class="sxs-lookup"><span data-stu-id="df733-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df733-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df733-119">Minimum supported client</span></span><br/> | <span data-ttu-id="df733-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df733-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df733-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df733-121">Minimum supported server</span></span><br/> | <span data-ttu-id="df733-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df733-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df733-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df733-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="df733-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df733-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





