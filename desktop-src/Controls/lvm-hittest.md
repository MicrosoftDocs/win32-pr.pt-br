---
title: Mensagem de LVM_HITTEST (commctrl. h)
description: Determina qual item de exibição de lista, se houver, está em uma posição especificada. Você pode enviar essa mensagem explicitamente ou usando a \_ macro HitTest do ListView.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- Controles de LVM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918964"
---
# <a name="lvm_hittest-message"></a><span data-ttu-id="62abb-105">Mensagem de HITTEST do LVM \_</span><span class="sxs-lookup"><span data-stu-id="62abb-105">LVM\_HITTEST message</span></span>

<span data-ttu-id="62abb-106">Determina qual item de exibição de lista, se houver, está em uma posição especificada.</span><span class="sxs-lookup"><span data-stu-id="62abb-106">Determines which list-view item, if any, is at a specified position.</span></span> <span data-ttu-id="62abb-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ HitTest do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="62abb-107">You can send this message explicitly or by using the [**ListView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="62abb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62abb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62abb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62abb-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62abb-110">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="62abb-110">Must be 0.</span></span> <span data-ttu-id="62abb-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="62abb-111">**Windows Vista.**</span></span> <span data-ttu-id="62abb-112">Deve ser-1 se os membros **iGroup** e **ISubItem** da estrutura *lParam* forem recuperados.</span><span class="sxs-lookup"><span data-stu-id="62abb-112">Should be -1 if the **iGroup** and **iSubItem** members of the *lParam* structure are to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="62abb-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62abb-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62abb-114">Ponteiro para uma estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) que contém a posição para o teste de clique e recebe informações sobre os resultados do teste de clique.</span><span class="sxs-lookup"><span data-stu-id="62abb-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure that contains the position to hit test and receives information about the results of the hit test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62abb-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62abb-115">Return value</span></span>

<span data-ttu-id="62abb-116">Retorna o índice do item na posição especificada, se houver, ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="62abb-116">Returns the index of the item at the specified position, if any, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="62abb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62abb-117">Requirements</span></span>



| <span data-ttu-id="62abb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62abb-118">Requirement</span></span> | <span data-ttu-id="62abb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="62abb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62abb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62abb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62abb-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62abb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62abb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62abb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62abb-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62abb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62abb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62abb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62abb-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62abb-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





