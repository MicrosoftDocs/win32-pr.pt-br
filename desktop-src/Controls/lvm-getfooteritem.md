---
title: Mensagem de LVM_GETFOOTERITEM (commctrl. h)
description: Obtém informações sobre um item de rodapé em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterItem do ListView.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- Controles de LVM_GETFOOTERITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008860"
---
# <a name="lvm_getfooteritem-message"></a><span data-ttu-id="5a26c-105">\_Mensagem GETFOOTERITEM LVM</span><span class="sxs-lookup"><span data-stu-id="5a26c-105">LVM\_GETFOOTERITEM message</span></span>

<span data-ttu-id="5a26c-106">Obtém informações sobre um item de rodapé em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="5a26c-106">Gets information on a footer item in a list-view control.</span></span> <span data-ttu-id="5a26c-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .</span><span class="sxs-lookup"><span data-stu-id="5a26c-107">Send this message explicitly or by using the [**ListView\_GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a26c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a26c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a26c-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a26c-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a26c-110">O índice do item.</span><span class="sxs-lookup"><span data-stu-id="5a26c-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="5a26c-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5a26c-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a26c-112">Um ponteiro para uma estrutura [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) para receber um valor para os membros **State** e/ou **pszText** de acordo com o valor do membro **Mask** .</span><span class="sxs-lookup"><span data-stu-id="5a26c-112">A pointer to a [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) structure to receive a value for the **state** and/or **pszText** members according to the value of the **mask** member.</span></span> <span data-ttu-id="5a26c-113">O processo de chamada é responsável por alocar essa estrutura e definir seus membros para indicar ao destinatário quais informações retornar.</span><span class="sxs-lookup"><span data-stu-id="5a26c-113">The calling process is responsible for allocating this structure and setting its members to indicate to the receiver what information to return.</span></span> <span data-ttu-id="5a26c-114">Para obter mais informações, consulte **LVFOOTERITEM**.</span><span class="sxs-lookup"><span data-stu-id="5a26c-114">For more information, see **LVFOOTERITEM**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a26c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a26c-115">Return value</span></span>

<span data-ttu-id="5a26c-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5a26c-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a26c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a26c-117">Requirements</span></span>



| <span data-ttu-id="5a26c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a26c-118">Requirement</span></span> | <span data-ttu-id="5a26c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5a26c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a26c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a26c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a26c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a26c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a26c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a26c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a26c-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a26c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a26c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a26c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a26c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a26c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





