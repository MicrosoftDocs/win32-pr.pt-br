---
title: Mensagem de LVM_SETCOLUMN (commctrl. h)
description: Define os atributos de uma coluna de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetColumn de ListView.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- Controles de LVM_SETCOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918485"
---
# <a name="lvm_setcolumn-message"></a><span data-ttu-id="84241-105">\_Mensagem de SETcolumn do LVM</span><span class="sxs-lookup"><span data-stu-id="84241-105">LVM\_SETCOLUMN message</span></span>

<span data-ttu-id="84241-106">Define os atributos de uma coluna de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="84241-106">Sets the attributes of a list-view column.</span></span> <span data-ttu-id="84241-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .</span><span class="sxs-lookup"><span data-stu-id="84241-107">You can send this message explicitly or by using the [**ListView\_SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="84241-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84241-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84241-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84241-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84241-110">Índice da coluna.</span><span class="sxs-lookup"><span data-stu-id="84241-110">Index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="84241-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84241-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84241-112">Ponteiro para uma estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contém os novos atributos de coluna.</span><span class="sxs-lookup"><span data-stu-id="84241-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the new column attributes.</span></span> <span data-ttu-id="84241-113">O membro **Mask** especifica quais atributos de coluna definir.</span><span class="sxs-lookup"><span data-stu-id="84241-113">The **mask** member specifies which column attributes to set.</span></span> <span data-ttu-id="84241-114">Se o membro de **máscara** especificar o \_ valor de texto LVCF, o membro **pszText** será o endereço de uma cadeia de caracteres terminada em nulo e o membro **cchTextMax** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="84241-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84241-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84241-115">Return value</span></span>

<span data-ttu-id="84241-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="84241-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="84241-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84241-117">Requirements</span></span>



| <span data-ttu-id="84241-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="84241-118">Requirement</span></span> | <span data-ttu-id="84241-119">Valor</span><span class="sxs-lookup"><span data-stu-id="84241-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84241-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84241-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84241-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84241-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84241-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84241-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84241-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84241-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84241-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84241-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="84241-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84241-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="84241-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="84241-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="84241-127">**LVM \_ SETCOLUMNW** (Unicode) e **LVM \_ SETCOLUMNW** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="84241-127">**LVM\_SETCOLUMNW** (Unicode) and **LVM\_SETCOLUMNW** (ANSI)</span></span><br/>               |



 

 





