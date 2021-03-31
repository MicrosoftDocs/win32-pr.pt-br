---
title: Mensagem de CBEM_SETITEM (commctrl. h)
description: Define os atributos de um item em um controle ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- Controles de CBEM_SETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645124"
---
# <a name="cbem_setitem-message"></a><span data-ttu-id="3d1b1-104">\_Mensagem CBEM SETITEM</span><span class="sxs-lookup"><span data-stu-id="3d1b1-104">CBEM\_SETITEM message</span></span>

<span data-ttu-id="3d1b1-105">Define os atributos de um item em um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="3d1b1-105">Sets the attributes for an item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d1b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d1b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d1b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d1b1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3d1b1-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3d1b1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3d1b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d1b1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d1b1-110">Um ponteiro para uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que contém as informações de item a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="3d1b1-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains the item information to be set.</span></span> <span data-ttu-id="3d1b1-111">Quando a mensagem é enviada, o membro **Mask** da estrutura deve ser definido para indicar quais atributos são válidos e o membro **iItem** deve especificar o índice de base zero do item a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="3d1b1-111">When the message is sent, the **mask** member of the structure must be set to indicate which attributes are valid and the **iItem** member must specify the zero-based index of the item to be modified.</span></span> <span data-ttu-id="3d1b1-112">Definir o membro **iItem** como-1 modificará o item exibido no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="3d1b1-112">Setting the **iItem** member to -1 will modify the item displayed in the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d1b1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d1b1-113">Return value</span></span>

<span data-ttu-id="3d1b1-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="3d1b1-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d1b1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d1b1-115">Requirements</span></span>



| <span data-ttu-id="3d1b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d1b1-116">Requirement</span></span> | <span data-ttu-id="3d1b1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3d1b1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1b1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d1b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1b1-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d1b1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d1b1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d1b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1b1-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d1b1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d1b1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d1b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d1b1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d1b1-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3d1b1-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3d1b1-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3d1b1-125">**CBEM \_ SETITEMW** (Unicode) e **CBEM \_ setitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3d1b1-125">**CBEM\_SETITEMW** (Unicode) and **CBEM\_SETITEMA** (ANSI)</span></span><br/>                 |



 

 





