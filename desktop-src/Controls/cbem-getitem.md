---
title: Mensagem de CBEM_GETITEM (commctrl. h)
description: Obtém informações de item para um determinado item ComboBoxEx.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- Controles de CBEM_GETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754378"
---
# <a name="cbem_getitem-message"></a><span data-ttu-id="95428-104">\_Mensagem CBEM GETITEM</span><span class="sxs-lookup"><span data-stu-id="95428-104">CBEM\_GETITEM message</span></span>

<span data-ttu-id="95428-105">Obtém informações de item para um determinado item ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="95428-105">Gets item information for a given ComboBoxEx item.</span></span>

## <a name="parameters"></a><span data-ttu-id="95428-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95428-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95428-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95428-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="95428-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="95428-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="95428-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95428-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95428-110">Um ponteiro para uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que recebe as informações do item.</span><span class="sxs-lookup"><span data-stu-id="95428-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that receives the item information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95428-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95428-111">Return value</span></span>

<span data-ttu-id="95428-112">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="95428-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="95428-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="95428-113">Remarks</span></span>

<span data-ttu-id="95428-114">Quando a mensagem é enviada, os membros **iItem** e **Mask** da estrutura devem ser definidos para indicar o índice do item de destino e o tipo de informações a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="95428-114">When the message is sent, the **iItem** and **mask** members of the structure must be set to indicate the index of the target item and the type of information to be retrieved.</span></span> <span data-ttu-id="95428-115">Outros membros são definidos conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="95428-115">Other members are set as needed.</span></span> <span data-ttu-id="95428-116">Por exemplo, para recuperar texto, você deve definir o \_ sinalizador de texto CBEIF em **Mask** e atribuir um valor a **cchTextMax**.</span><span class="sxs-lookup"><span data-stu-id="95428-116">For example, to retrieve text, you must set the CBEIF\_TEXT flag in **mask**, and assign a value to **cchTextMax**.</span></span> <span data-ttu-id="95428-117">Definir o membro **iItem** como-1 recuperará o item exibido no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="95428-117">Setting the **iItem** member to -1 will retrieve the item displayed in the edit control.</span></span>

<span data-ttu-id="95428-118">Se o \_ sinalizador de texto CBEIF for definido no membro **Mask** da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , o controle poderá alterar o membro **pszText** da estrutura para apontar para o novo texto em vez de preencher o buffer com o texto solicitado.</span><span class="sxs-lookup"><span data-stu-id="95428-118">If the CBEIF\_TEXT flag is set in the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="95428-119">Os aplicativos não devem pressupor que o texto sempre será colocado no buffer solicitado.</span><span class="sxs-lookup"><span data-stu-id="95428-119">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="95428-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95428-120">Requirements</span></span>



| <span data-ttu-id="95428-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="95428-121">Requirement</span></span> | <span data-ttu-id="95428-122">Valor</span><span class="sxs-lookup"><span data-stu-id="95428-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95428-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95428-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95428-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95428-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95428-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95428-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95428-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95428-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95428-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95428-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="95428-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95428-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="95428-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="95428-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="95428-130">**CBEM \_ GETITEMW** (Unicode) e **CBEM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="95428-130">**CBEM\_GETITEMW** (Unicode) and **CBEM\_GETITEMA** (ANSI)</span></span><br/>                 |



 

 





