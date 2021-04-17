---
title: Mensagem de CBEM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- Controles de CBEM_INSERTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754811"
---
# <a name="cbem_insertitem-message"></a><span data-ttu-id="77ab4-104">\_Mensagem CBEM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="77ab4-104">CBEM\_INSERTITEM message</span></span>

<span data-ttu-id="77ab4-105">Insere um novo item em um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="77ab4-105">Inserts a new item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="77ab4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77ab4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ab4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77ab4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="77ab4-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="77ab4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="77ab4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77ab4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77ab4-110">Um ponteiro para uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que contém informações sobre o item a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="77ab4-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains information about the item to be inserted.</span></span> <span data-ttu-id="77ab4-111">Quando a mensagem é enviada, o membro **iItem** deve ser definido para indicar o índice de base zero no qual inserir o item.</span><span class="sxs-lookup"><span data-stu-id="77ab4-111">When the message is sent, the **iItem** member must be set to indicate the zero-based index at which to insert the item.</span></span> <span data-ttu-id="77ab4-112">Para inserir um item no final da lista, defina o membro **iItem** como-1.</span><span class="sxs-lookup"><span data-stu-id="77ab4-112">To insert an item at the end of the list, set the **iItem** member to -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ab4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77ab4-113">Return value</span></span>

<span data-ttu-id="77ab4-114">Retorna o índice no qual o novo item foi inserido, se for bem-sucedido, ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="77ab4-114">Returns the index at which the new item was inserted if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ab4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ab4-115">Requirements</span></span>



| <span data-ttu-id="77ab4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ab4-116">Requirement</span></span> | <span data-ttu-id="77ab4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="77ab4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77ab4-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ab4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="77ab4-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77ab4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77ab4-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ab4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="77ab4-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77ab4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77ab4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77ab4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="77ab4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77ab4-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="77ab4-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="77ab4-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="77ab4-125">**CBEM \_ INSERTITEMW** (Unicode) e **CBEM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="77ab4-125">**CBEM\_INSERTITEMW** (Unicode) and **CBEM\_INSERTITEMA** (ANSI)</span></span><br/>           |



 

 





