---
title: Mensagem de TDM_UPDATE_ELEMENT_TEXT (commctrl. h)
description: Mensagem de TDM_UPDATE_ELEMENT_TEXT-atualiza um elemento de texto em uma caixa de diálogo de tarefa.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- Controles de TDM_UPDATE_ELEMENT_TEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085804"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="cc806-104">\_Mensagem de \_ texto do elemento de atualização TDM \_</span><span class="sxs-lookup"><span data-stu-id="cc806-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="cc806-105">Atualiza um elemento de texto em uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="cc806-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc806-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc806-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc806-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc806-108">Indica o elemento a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="cc806-108">Indicates the element to update.</span></span> <span data-ttu-id="cc806-109">(Para obter uma ilustração dos elementos, consulte [sobre caixas de diálogo de tarefas](task-dialogs-overview.md).) Esse parâmetro deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="cc806-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="cc806-110">Valor</span><span class="sxs-lookup"><span data-stu-id="cc806-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="cc806-111">Significado</span><span class="sxs-lookup"><span data-stu-id="cc806-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="cc806-112"><dt>**conteúdo do TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc806-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="cc806-113">Conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cc806-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="cc806-114"><dt>**\_informações expandidas do TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc806-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="cc806-115">Informações expandidas.</span><span class="sxs-lookup"><span data-stu-id="cc806-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="cc806-116"><dt>**rodapé do TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc806-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="cc806-117">Texto do rodapé.</span><span class="sxs-lookup"><span data-stu-id="cc806-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="cc806-118"><dt>**\_instrução principal do TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc806-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="cc806-119">Instrução principal.</span><span class="sxs-lookup"><span data-stu-id="cc806-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="cc806-120">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc806-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc806-121">Ponteiro para uma cadeia de caracteres Unicode que contém o novo texto.</span><span class="sxs-lookup"><span data-stu-id="cc806-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc806-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cc806-122">Return value</span></span>

<span data-ttu-id="cc806-123">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="cc806-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc806-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc806-124">Remarks</span></span>

<span data-ttu-id="cc806-125">Para evitar o recorte, o novo texto não deve ser maior do que o texto existente.</span><span class="sxs-lookup"><span data-stu-id="cc806-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="cc806-126">Definir o texto para uma cadeia de caracteres mais curta não faz com que a caixa de diálogo seja redimensionada.</span><span class="sxs-lookup"><span data-stu-id="cc806-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="cc806-127">Se o membro **pszExpandedInformation** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usada para criar a caixa de diálogo de tarefa fosse **nulo** e você enviar uma mensagem de texto de **elemento de \_ atualização \_ \_ TDM** com \_ informações expandidas do TDE \_ , nada acontecerá.</span><span class="sxs-lookup"><span data-stu-id="cc806-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="cc806-128">O acima também se aplica ao rodapé rodapé e TDE \_ .</span><span class="sxs-lookup"><span data-stu-id="cc806-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc806-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc806-129">Requirements</span></span>



| <span data-ttu-id="cc806-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc806-130">Requirement</span></span> | <span data-ttu-id="cc806-131">Valor</span><span class="sxs-lookup"><span data-stu-id="cc806-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc806-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc806-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cc806-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc806-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc806-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc806-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cc806-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc806-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc806-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc806-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc806-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc806-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc806-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cc806-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc806-139">**\_texto do \_ elemento do conjunto de TDM \_**</span><span class="sxs-lookup"><span data-stu-id="cc806-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





