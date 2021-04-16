---
title: Mensagem de LVM_GETGROUPSTATE (commctrl. h)
description: Obtém o estado de um grupo especificado. Envie essa mensagem explicitamente ou usando a \_ macro Getgroupstate do ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- Controles de LVM_GETGROUPSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454699"
---
# <a name="lvm_getgroupstate-message"></a><span data-ttu-id="7b24c-105">Mensagem do LVM \_ GETgroupstate</span><span class="sxs-lookup"><span data-stu-id="7b24c-105">LVM\_GETGROUPSTATE message</span></span>

<span data-ttu-id="7b24c-106">Obtém o estado de um grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="7b24c-106">Gets the state for a specified group.</span></span> <span data-ttu-id="7b24c-107">Envie essa mensagem explicitamente ou usando a macro [**\_ getgroupstate do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .</span><span class="sxs-lookup"><span data-stu-id="7b24c-107">Send this message explicitly or by using the [**ListView\_GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b24c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b24c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b24c-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b24c-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b24c-110">Especifica o Group by **iGroupId** (consulte a estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="7b24c-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="7b24c-111">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b24c-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b24c-112">Especifica os valores de estado a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="7b24c-112">Specifies the state values to retrieve.</span></span> <span data-ttu-id="7b24c-113">Essa é uma combinação dos sinalizadores listados para o membro de **estado** de [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span><span class="sxs-lookup"><span data-stu-id="7b24c-113">This is a combination of the flags listed for the **state** member of [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b24c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b24c-114">Return value</span></span>

<span data-ttu-id="7b24c-115">Retorna a combinação de valores de estado que são definidos.</span><span class="sxs-lookup"><span data-stu-id="7b24c-115">Returns the combination of state values that are set.</span></span> <span data-ttu-id="7b24c-116">Por exemplo, se *lParam* for LVGS \_ recolhido e o valor retornado for zero, o \_ estado LVGS recolhido não será definido.</span><span class="sxs-lookup"><span data-stu-id="7b24c-116">For example, if *lParam* is LVGS\_COLLAPSED and the value returned is zero, the LVGS\_COLLAPSED state is not set.</span></span> <span data-ttu-id="7b24c-117">Zero será retornado se o grupo não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="7b24c-117">Zero is returned if the group is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b24c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b24c-118">Requirements</span></span>



| <span data-ttu-id="7b24c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b24c-119">Requirement</span></span> | <span data-ttu-id="7b24c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7b24c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b24c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b24c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7b24c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b24c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b24c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b24c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7b24c-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b24c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b24c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b24c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b24c-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b24c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





