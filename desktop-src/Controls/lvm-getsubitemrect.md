---
title: Mensagem de LVM_GETSUBITEMRECT (commctrl. h)
description: Recupera informações sobre o retângulo delimitador de um subitem em um controle de exibição de lista.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- Controles de LVM_GETSUBITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086159"
---
# <a name="lvm_getsubitemrect-message"></a><span data-ttu-id="401a8-104">\_Mensagem GETSUBITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="401a8-104">LVM\_GETSUBITEMRECT message</span></span>

<span data-ttu-id="401a8-105">Recupera informações sobre o retângulo delimitador de um subitem em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="401a8-105">Retrieves information about the bounding rectangle for a subitem in a list-view control.</span></span> <span data-ttu-id="401a8-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**ListView \_ GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (recomendado).</span><span class="sxs-lookup"><span data-stu-id="401a8-106">You can send this message explicitly or by using the [**ListView\_GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) macro (recommended).</span></span> <span data-ttu-id="401a8-107">Esta mensagem destina-se a ser usada somente com controles de exibição de lista que usam o estilo de [**\_ relatório LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="401a8-107">This message is intended to be used only with list-view controls that use the [**LVS\_REPORT**](list-view-window-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="401a8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="401a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="401a8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="401a8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="401a8-110">Índice do item pai do subitem.</span><span class="sxs-lookup"><span data-stu-id="401a8-110">Index of the subitem's parent item.</span></span>

</dd> <dt>

<span data-ttu-id="401a8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="401a8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="401a8-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá as informações de retângulo delimitador de subitem.</span><span class="sxs-lookup"><span data-stu-id="401a8-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the subitem bounding rectangle information.</span></span> <span data-ttu-id="401a8-113">Seus membros devem ser inicializados de acordo com as seguintes relações de membro/valor:</span><span class="sxs-lookup"><span data-stu-id="401a8-113">Its members must be initialized according to the following member/value relationships:</span></span>



| <span data-ttu-id="401a8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="401a8-114">Value</span></span>                                                                                                                             | <span data-ttu-id="401a8-115">Significado</span><span class="sxs-lookup"><span data-stu-id="401a8-115">Meaning</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="401a8-116"><dt>**Início**</dt></span><span class="sxs-lookup"><span data-stu-id="401a8-116"><dt>**top**</dt></span></span> </dl>    | <span data-ttu-id="401a8-117">O índice baseado em um do subitem.</span><span class="sxs-lookup"><span data-stu-id="401a8-117">The one-based index of the subitem.</span></span><br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="401a8-118"><dt>**mantida**</dt></span><span class="sxs-lookup"><span data-stu-id="401a8-118"><dt>**left**</dt></span></span> </dl> | <span data-ttu-id="401a8-119">Valor do sinalizador (consulte comentários).</span><span class="sxs-lookup"><span data-stu-id="401a8-119">Flag value (see remarks).</span></span> <span data-ttu-id="401a8-120">Indica a parte do subitem de exibição de lista para o qual recuperar o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="401a8-120">Indicates the portion of the list-view subitem for which to retrieve the bounding rectangle.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="401a8-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="401a8-121">Return value</span></span>

<span data-ttu-id="401a8-122">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="401a8-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="401a8-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="401a8-123">Remarks</span></span>

<span data-ttu-id="401a8-124">A seguir estão os valores de sinalizador que podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="401a8-124">Following are the flag values that may be set.</span></span>



| <span data-ttu-id="401a8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="401a8-125">Requirement</span></span> | <span data-ttu-id="401a8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="401a8-126">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="401a8-127">**Valor de sinalizador**</span><span class="sxs-lookup"><span data-stu-id="401a8-127">**Flag Value**</span></span> | <span data-ttu-id="401a8-128">**Significado**</span><span class="sxs-lookup"><span data-stu-id="401a8-128">**Meaning**</span></span>                                                                                                         |
| <span data-ttu-id="401a8-129">limites do LVIR \_</span><span class="sxs-lookup"><span data-stu-id="401a8-129">LVIR\_BOUNDS</span></span>   | <span data-ttu-id="401a8-130">Retorna o retângulo delimitador do item inteiro, incluindo o ícone e o rótulo.</span><span class="sxs-lookup"><span data-stu-id="401a8-130">Returns the bounding rectangle of the entire item, including the icon and label.</span></span>                                    |
| <span data-ttu-id="401a8-131">ícone de LVIR \_</span><span class="sxs-lookup"><span data-stu-id="401a8-131">LVIR\_ICON</span></span>     | <span data-ttu-id="401a8-132">Retorna o retângulo delimitador do ícone ou ícone pequeno.</span><span class="sxs-lookup"><span data-stu-id="401a8-132">Returns the bounding rectangle of the icon or small icon.</span></span>                                                           |
| <span data-ttu-id="401a8-133">rótulo de LVIR \_</span><span class="sxs-lookup"><span data-stu-id="401a8-133">LVIR\_LABEL</span></span>    | <span data-ttu-id="401a8-134">Retorna o retângulo delimitador do item inteiro, incluindo o ícone e o rótulo.</span><span class="sxs-lookup"><span data-stu-id="401a8-134">Returns the bounding rectangle of the entire item, including the icon and label.</span></span> <span data-ttu-id="401a8-135">Isso é idêntico aos limites de LVIR \_ .</span><span class="sxs-lookup"><span data-stu-id="401a8-135">This is identical to LVIR\_BOUNDS.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="401a8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="401a8-136">Requirements</span></span>



| <span data-ttu-id="401a8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="401a8-137">Requirement</span></span> | <span data-ttu-id="401a8-138">Valor</span><span class="sxs-lookup"><span data-stu-id="401a8-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="401a8-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="401a8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="401a8-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="401a8-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="401a8-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="401a8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="401a8-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="401a8-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="401a8-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="401a8-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="401a8-144"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="401a8-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

