---
title: Mensagem de TDM_SET_ELEMENT_TEXT (commctrl. h)
description: Atualiza um elemento de texto em uma caixa de diálogo de tarefa.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- Controles de TDM_SET_ELEMENT_TEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009705"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="f771e-104">\_Mensagem de \_ texto do elemento do conjunto TDM \_</span><span class="sxs-lookup"><span data-stu-id="f771e-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="f771e-105">Atualiza um elemento de texto em uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="f771e-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="f771e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f771e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f771e-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f771e-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f771e-108">Indica o elemento a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="f771e-108">Indicates the element to update.</span></span> <span data-ttu-id="f771e-109">(Para obter uma ilustração, consulte [sobre caixas de diálogo de tarefas](task-dialogs-overview.md).) Esse parâmetro deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f771e-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="f771e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f771e-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="f771e-111">Significado</span><span class="sxs-lookup"><span data-stu-id="f771e-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="f771e-112"><dt>**conteúdo do TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f771e-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="f771e-113">Conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f771e-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="f771e-114"><dt>**\_informações expandidas do TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f771e-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="f771e-115">Informações expandidas.</span><span class="sxs-lookup"><span data-stu-id="f771e-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="f771e-116"><dt>**rodapé do TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f771e-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="f771e-117">Texto do rodapé.</span><span class="sxs-lookup"><span data-stu-id="f771e-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="f771e-118"><dt>**\_instrução principal do TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f771e-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="f771e-119">Instrução principal.</span><span class="sxs-lookup"><span data-stu-id="f771e-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="f771e-120">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f771e-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f771e-121">O novo texto a ser usado.</span><span class="sxs-lookup"><span data-stu-id="f771e-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f771e-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f771e-122">Return value</span></span>

<span data-ttu-id="f771e-123">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f771e-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f771e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="f771e-124">Remarks</span></span>

<span data-ttu-id="f771e-125">O tamanho ou o layout da caixa de diálogo de tarefa pode ser alterado para acomodar o novo texto.</span><span class="sxs-lookup"><span data-stu-id="f771e-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="f771e-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f771e-126">Examples</span></span>

<span data-ttu-id="f771e-127">O código de exemplo a seguir mostra como definir o texto de rodapé na caixa de diálogo de tarefa representada por *HWND*.</span><span class="sxs-lookup"><span data-stu-id="f771e-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="f771e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f771e-128">Requirements</span></span>



| <span data-ttu-id="f771e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f771e-129">Requirement</span></span> | <span data-ttu-id="f771e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f771e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f771e-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f771e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f771e-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f771e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f771e-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f771e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f771e-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f771e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f771e-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f771e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f771e-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f771e-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f771e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f771e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f771e-138">**\_texto do \_ elemento de atualização TDM \_**</span><span class="sxs-lookup"><span data-stu-id="f771e-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





