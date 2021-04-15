---
title: Mensagem de LVM_GETFOCUSEDGROUP (commctrl. h)
description: Obtém o grupo que tem o foco. Envie essa mensagem explicitamente ou usando a macro do ListView \_ Getconcentrour.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- Controles de LVM_GETFOCUSEDGROUP de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454629"
---
# <a name="lvm_getfocusedgroup-message"></a><span data-ttu-id="0aa37-105">Mensagem do LVM \_ GETfocaling</span><span class="sxs-lookup"><span data-stu-id="0aa37-105">LVM\_GETFOCUSEDGROUP message</span></span>

<span data-ttu-id="0aa37-106">Obtém o grupo que tem o foco.</span><span class="sxs-lookup"><span data-stu-id="0aa37-106">Gets the group that has the focus.</span></span> <span data-ttu-id="0aa37-107">Envie essa mensagem explicitamente ou usando a macro do [**ListView \_ getconcentrour**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .</span><span class="sxs-lookup"><span data-stu-id="0aa37-107">Send this message explicitly or by using the [**ListView\_GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0aa37-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0aa37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa37-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0aa37-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0aa37-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0aa37-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0aa37-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0aa37-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0aa37-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0aa37-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa37-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0aa37-113">Return value</span></span>

<span data-ttu-id="0aa37-114">Retorna o índice do grupo com o estado de LVGS \_ focalizado ou-1 se não houver nenhum grupo com o estado de LVGS \_ focalizado.</span><span class="sxs-lookup"><span data-stu-id="0aa37-114">Returns the index of the group with state of LVGS\_FOCUSED, or -1 if there is no group with state of LVGS\_FOCUSED.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa37-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa37-115">Requirements</span></span>



| <span data-ttu-id="0aa37-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa37-116">Requirement</span></span> | <span data-ttu-id="0aa37-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0aa37-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa37-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0aa37-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa37-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0aa37-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0aa37-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0aa37-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa37-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0aa37-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0aa37-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0aa37-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa37-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa37-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





