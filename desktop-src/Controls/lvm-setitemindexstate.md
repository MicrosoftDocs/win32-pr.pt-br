---
title: Mensagem de LVM_SETITEMINDEXSTATE (commctrl. h)
description: Define o estado de um item de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro SetItemIndexState do ListView.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- Controles de LVM_SETITEMINDEXSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009127"
---
# <a name="lvm_setitemindexstate-message"></a><span data-ttu-id="66303-105">\_Mensagem SETITEMINDEXSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="66303-105">LVM\_SETITEMINDEXSTATE message</span></span>

<span data-ttu-id="66303-106">Define o estado de um item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="66303-106">Sets the state of a list-view item.</span></span> <span data-ttu-id="66303-107">Envie essa mensagem explicitamente ou usando a macro [**\_ SetItemIndexState do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .</span><span class="sxs-lookup"><span data-stu-id="66303-107">Send this message explicitly or by using the [**ListView\_SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="66303-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66303-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66303-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66303-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66303-110">Um ponteiro para uma estrutura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para o item.</span><span class="sxs-lookup"><span data-stu-id="66303-110">A pointer to an [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the item.</span></span> <span data-ttu-id="66303-111">O processo de chamada é responsável por alocar essa estrutura e definir os membros.</span><span class="sxs-lookup"><span data-stu-id="66303-111">The calling process is responsible for allocating this structure and setting the members.</span></span>

</dd> <dt>

<span data-ttu-id="66303-112">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66303-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66303-113">Um ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="66303-113">A pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="66303-114">O processo de chamada é responsável por alocar memória para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="66303-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="66303-115">Defina o membro de **estado** como uma ou mais (como uma combinação bit a bit) dos sinalizadores de [Estados de item de exibição de lista](list-view-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="66303-115">Set the **state** member to one or more (as a bitwise combination) of the [List-View Item States](list-view-item-states.md) flags.</span></span> <span data-ttu-id="66303-116">Defina o membro **stateMask** da estrutura para indicar os bits válidos do membro de **estado** .</span><span class="sxs-lookup"><span data-stu-id="66303-116">Set the **stateMask** member of the structure to indicate the valid bits of the **state** member.</span></span> <span data-ttu-id="66303-117">Para obter mais informações, consulte o membro **stateMask** da estrutura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="66303-117">For more information, see the **stateMask** member of the **LVITEM** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66303-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66303-118">Return value</span></span>

<span data-ttu-id="66303-119">Retorna um dos seguintes valores do tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="66303-119">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="66303-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="66303-120">Return code</span></span>                                                                                  | <span data-ttu-id="66303-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="66303-121">Description</span></span>                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="66303-122"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="66303-122"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="66303-123">Não foi possível definir o estado.</span><span class="sxs-lookup"><span data-stu-id="66303-123">The state could not be set.</span></span><br/>                            |
| <dl> <span data-ttu-id="66303-124"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="66303-124"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="66303-125">O controle de exibição de lista não estava pronto para a operação.</span><span class="sxs-lookup"><span data-stu-id="66303-125">The list-view control was not ready for the operation.</span></span><br/> |
| <dl> <span data-ttu-id="66303-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66303-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="66303-127">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="66303-127">The operation was successful.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="66303-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66303-128">Requirements</span></span>



| <span data-ttu-id="66303-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="66303-129">Requirement</span></span> | <span data-ttu-id="66303-130">Valor</span><span class="sxs-lookup"><span data-stu-id="66303-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66303-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66303-131">Minimum supported client</span></span><br/> | <span data-ttu-id="66303-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66303-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66303-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66303-133">Minimum supported server</span></span><br/> | <span data-ttu-id="66303-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66303-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66303-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66303-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="66303-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66303-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





