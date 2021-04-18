---
title: Mensagem de LVM_GETCOLUMN (commctrl. h)
description: Obtém os atributos de uma coluna do controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetColumn de ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- Controles de LVM_GETCOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454632"
---
# <a name="lvm_getcolumn-message"></a><span data-ttu-id="b6fc4-105">\_Mensagem de GETcolumn do LVM</span><span class="sxs-lookup"><span data-stu-id="b6fc4-105">LVM\_GETCOLUMN message</span></span>

<span data-ttu-id="b6fc4-106">Obtém os atributos de uma coluna do controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="b6fc4-106">Gets the attributes of a list-view control's column.</span></span> <span data-ttu-id="b6fc4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .</span><span class="sxs-lookup"><span data-stu-id="b6fc4-107">You can send this message explicitly or by using the [**ListView\_GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6fc4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6fc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6fc4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6fc4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6fc4-110">O índice da coluna.</span><span class="sxs-lookup"><span data-stu-id="b6fc4-110">The index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="b6fc4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6fc4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6fc4-112">Um ponteiro para uma estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que especifica as informações para recuperar e receber informações sobre a coluna.</span><span class="sxs-lookup"><span data-stu-id="b6fc4-112">A pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that specifies the information to retrieve and receives information about the column.</span></span> <span data-ttu-id="b6fc4-113">O membro **Mask** especifica quais atributos de coluna recuperar.</span><span class="sxs-lookup"><span data-stu-id="b6fc4-113">The **mask** member specifies which column attributes to retrieve.</span></span> <span data-ttu-id="b6fc4-114">Se o membro de **máscara** especificar o \_ valor de texto LVCF, o membro **pszText** deverá conter o endereço do buffer que receberá o texto do item e o membro **cchTextMax** deverá especificar o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="b6fc4-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6fc4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6fc4-115">Return value</span></span>

<span data-ttu-id="b6fc4-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b6fc4-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6fc4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6fc4-117">Requirements</span></span>



| <span data-ttu-id="b6fc4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6fc4-118">Requirement</span></span> | <span data-ttu-id="b6fc4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b6fc4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6fc4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6fc4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6fc4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6fc4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6fc4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6fc4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6fc4-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6fc4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6fc4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6fc4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6fc4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6fc4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





