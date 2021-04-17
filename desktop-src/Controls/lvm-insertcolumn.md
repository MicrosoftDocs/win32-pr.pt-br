---
title: Mensagem de LVM_INSERTCOLUMN (commctrl. h)
description: Insere uma nova coluna em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro InsertColumn do ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- Controles de LVM_INSERTCOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499664"
---
# <a name="lvm_insertcolumn-message"></a><span data-ttu-id="f7b87-105">\_Mensagem INSERTCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="f7b87-105">LVM\_INSERTCOLUMN message</span></span>

<span data-ttu-id="f7b87-106">Insere uma nova coluna em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="f7b87-106">Inserts a new column in a list-view control.</span></span> <span data-ttu-id="f7b87-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ InsertColumn do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="f7b87-107">You can send this message explicitly or by using the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7b87-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7b87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b87-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7b87-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b87-110">Índice da nova coluna.</span><span class="sxs-lookup"><span data-stu-id="f7b87-110">Index of the new column.</span></span>

</dd> <dt>

<span data-ttu-id="f7b87-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7b87-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b87-112">Ponteiro para uma estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contém os atributos da nova coluna.</span><span class="sxs-lookup"><span data-stu-id="f7b87-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the attributes of the new column.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b87-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7b87-113">Return value</span></span>

<span data-ttu-id="f7b87-114">Retorna o índice da nova coluna se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f7b87-114">Returns the index of the new column if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b87-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7b87-115">Remarks</span></span>

<span data-ttu-id="f7b87-116">As colunas são visíveis somente na exibição de relatório (detalhes).</span><span class="sxs-lookup"><span data-stu-id="f7b87-116">Columns are visible only in report (details) view.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b87-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7b87-117">Requirements</span></span>



| <span data-ttu-id="f7b87-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b87-118">Requirement</span></span> | <span data-ttu-id="f7b87-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f7b87-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b87-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7b87-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b87-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7b87-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7b87-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7b87-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b87-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7b87-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7b87-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7b87-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b87-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b87-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





