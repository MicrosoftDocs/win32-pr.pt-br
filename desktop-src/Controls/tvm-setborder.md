---
title: Mensagem de TVM_SETBORDER (commctrl. h)
description: Define o tamanho da borda para os itens em um controle de exibição de árvore. Você pode enviar a mensagem explicitamente ou usando a \_ macro SetBorder de TreeView.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- Controles de TVM_SETBORDER de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824514"
---
# <a name="tvm_setborder-message"></a><span data-ttu-id="24e53-105">\_Mensagem TVM SETborder</span><span class="sxs-lookup"><span data-stu-id="24e53-105">TVM\_SETBORDER message</span></span>

<span data-ttu-id="24e53-106">**Destinado ao uso interno; Não recomendado para uso em aplicativos.**</span><span class="sxs-lookup"><span data-stu-id="24e53-106">**Intended for internal use; not recommended for use in applications.**</span></span>

<span data-ttu-id="24e53-107">Define o tamanho da borda para os itens em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="24e53-107">Sets the size of the border for the items in a tree-view control.</span></span> <span data-ttu-id="24e53-108">Você pode enviar a mensagem explicitamente ou usando a macro [**\_ SetBorder de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) .</span><span class="sxs-lookup"><span data-stu-id="24e53-108">You can send the message explicitly or by using the [**TreeView\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="24e53-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24e53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24e53-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24e53-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24e53-111">Sinalizadores de ação.</span><span class="sxs-lookup"><span data-stu-id="24e53-111">Action flags.</span></span> <span data-ttu-id="24e53-112">Esse parâmetro pode ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="24e53-112">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="24e53-113">Valor</span><span class="sxs-lookup"><span data-stu-id="24e53-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="24e53-114">Significado</span><span class="sxs-lookup"><span data-stu-id="24e53-114">Meaning</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <span data-ttu-id="24e53-115"><dt>**TVSBF \_ XBORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="24e53-115"><dt>**TVSBF\_XBORDER**</dt></span></span> </dl> | <span data-ttu-id="24e53-116">Aplica o tamanho de borda especificado ao lado esquerdo dos itens no controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="24e53-116">Applies the specified border size to the left side of the items in the tree-view control.</span></span> <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <span data-ttu-id="24e53-117"><dt>**TVSBF \_ YBORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="24e53-117"><dt>**TVSBF\_YBORDER**</dt></span></span> </dl> | <span data-ttu-id="24e53-118">Aplica o tamanho de borda especificado na parte superior dos itens no controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="24e53-118">Applies the specified border size to the top of the items in the tree-view control.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="24e53-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24e53-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24e53-120">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **curto** que especifica o tamanho da borda esquerda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="24e53-120">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **SHORT** that specifies the size of the left border, in pixels.</span></span> <span data-ttu-id="24e53-121">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **curto** que especifica o tamanho da borda superior, em pixels.</span><span class="sxs-lookup"><span data-stu-id="24e53-121">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **SHORT** that specifies the size of the top border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24e53-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24e53-122">Return value</span></span>

<span data-ttu-id="24e53-123">Retorna um valor **longo** que contém o tamanho da borda anterior, em pixels.</span><span class="sxs-lookup"><span data-stu-id="24e53-123">Returns a **LONG** value that contains the previous border size, in pixels.</span></span> <span data-ttu-id="24e53-124">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o tamanho anterior da borda horizontal e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o tamanho anterior da borda vertical.</span><span class="sxs-lookup"><span data-stu-id="24e53-124">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the previous size of the horizontal border, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the previous size of the vertical border.</span></span>

## <a name="remarks"></a><span data-ttu-id="24e53-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="24e53-125">Remarks</span></span>

<span data-ttu-id="24e53-126">**Aviso de segurança:** O uso dessa mensagem pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="24e53-126">**Security Warning:** Using this message might compromise the security of your program.</span></span>

<span data-ttu-id="24e53-127">A borda do item é definida apenas para fins de espaçamento.</span><span class="sxs-lookup"><span data-stu-id="24e53-127">The item border is set just for spacing purposes.</span></span> <span data-ttu-id="24e53-128">Uma configuração bem-sucedida dispara um recálculo das barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="24e53-128">A successful setting triggers a recalculation of the scroll bars.</span></span>

<span data-ttu-id="24e53-129">Essa mensagem pode não ter suporte em versões futuras do Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="24e53-129">This message may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="24e53-130">Além disso, essa mensagem não é definida em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="24e53-130">Also, this message is not defined in commctrl.h.</span></span> <span data-ttu-id="24e53-131">Adicione as seguintes definições aos arquivos de origem do seu aplicativo para usar a mensagem:</span><span class="sxs-lookup"><span data-stu-id="24e53-131">Add the following definitions to the source files of your application to use the message:</span></span>

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a><span data-ttu-id="24e53-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24e53-132">Requirements</span></span>



| <span data-ttu-id="24e53-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="24e53-133">Requirement</span></span> | <span data-ttu-id="24e53-134">Valor</span><span class="sxs-lookup"><span data-stu-id="24e53-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24e53-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24e53-135">Minimum supported client</span></span><br/> | <span data-ttu-id="24e53-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24e53-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24e53-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24e53-137">Minimum supported server</span></span><br/> | <span data-ttu-id="24e53-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24e53-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24e53-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24e53-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="24e53-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e53-140"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e53-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="24e53-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e53-142">**TreeView \_ SetBorder**</span><span class="sxs-lookup"><span data-stu-id="24e53-142">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

