---
title: Mensagem de TCM_INSERTITEM (commctrl. h)
description: Insere uma nova guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- Controles de TCM_INSERTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769027"
---
# <a name="tcm_insertitem-message"></a><span data-ttu-id="814ba-105">\_Mensagem INSERTITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="814ba-105">TCM\_INSERTITEM message</span></span>

<span data-ttu-id="814ba-106">Insere uma nova guia em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="814ba-106">Inserts a new tab in a tab control.</span></span> <span data-ttu-id="814ba-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="814ba-107">You can send this message explicitly or by using the [**TabCtrl\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="814ba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="814ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="814ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="814ba-110">Índice da nova guia.</span><span class="sxs-lookup"><span data-stu-id="814ba-110">Index of the new tab.</span></span>

</dd> <dt>

<span data-ttu-id="814ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="814ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="814ba-112">Ponteiro para uma estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica os atributos da guia. Os membros **dwState** e **dwStateMask** dessa estrutura são ignorados por essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="814ba-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the attributes of the tab. The **dwState** and **dwStateMask** members of this structure are ignored by this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814ba-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="814ba-113">Return value</span></span>

<span data-ttu-id="814ba-114">Retorna o índice da nova guia, se for bem-sucedido, ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="814ba-114">Returns the index of the new tab if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="814ba-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="814ba-115">Requirements</span></span>



| <span data-ttu-id="814ba-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="814ba-116">Requirement</span></span> | <span data-ttu-id="814ba-117">Valor</span><span class="sxs-lookup"><span data-stu-id="814ba-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="814ba-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="814ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="814ba-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="814ba-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="814ba-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="814ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="814ba-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="814ba-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="814ba-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="814ba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="814ba-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="814ba-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="814ba-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="814ba-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="814ba-125">**TCM \_ INSERTITEMW** (Unicode) e **\_ INSERTITEMA TCM** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="814ba-125">**TCM\_INSERTITEMW** (Unicode) and **TCM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





