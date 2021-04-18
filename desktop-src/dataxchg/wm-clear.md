---
title: Mensagem de WM_CLEAR (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de limpeza do WM para um controle de edição ou caixa de combinação para excluir (limpar) a seleção atual, se houver, do controle de edição.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- Troca de dados de mensagem WM_CLEAR
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789241"
---
# <a name="wm_clear-message"></a><span data-ttu-id="0e6a8-104">Mensagem de limpeza do WM \_</span><span class="sxs-lookup"><span data-stu-id="0e6a8-104">WM\_CLEAR message</span></span>

<span data-ttu-id="0e6a8-105">Um aplicativo envia uma mensagem de **\_ limpeza do WM** para um controle de edição ou caixa de combinação para excluir (limpar) a seleção atual, se houver, do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="0e6a8-105">An application sends a **WM\_CLEAR** message to an edit control or combo box to delete (clear) the current selection, if any, from the edit control.</span></span>


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a><span data-ttu-id="0e6a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e6a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e6a8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e6a8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e6a8-108">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0e6a8-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0e6a8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e6a8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e6a8-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0e6a8-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e6a8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e6a8-111">Return value</span></span>

<span data-ttu-id="0e6a8-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0e6a8-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e6a8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e6a8-113">Remarks</span></span>

<span data-ttu-id="0e6a8-114">A exclusão executada pela mensagem **de \_ limpeza do WM** pode ser desfeita enviando o controle de edição uma mensagem em [**\_ desfazer**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="0e6a8-114">The deletion performed by the **WM\_CLEAR** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="0e6a8-115">Para excluir a seleção atual e inserir o conteúdo excluído na área de transferência, use a mensagem de [**\_ recorte do WM**](wm-cut.md) .</span><span class="sxs-lookup"><span data-stu-id="0e6a8-115">To delete the current selection and place the deleted content on the clipboard, use the [**WM\_CUT**](wm-cut.md) message.</span></span>

<span data-ttu-id="0e6a8-116">Quando enviado para uma caixa de combinação, a mensagem de **\_ limpeza do WM** é manipulada por seu controle de edição.</span><span class="sxs-lookup"><span data-stu-id="0e6a8-116">When sent to a combo box, the **WM\_CLEAR** message is handled by its edit control.</span></span> <span data-ttu-id="0e6a8-117">Esta mensagem não tem nenhum efeito quando enviada para uma caixa de combinação com o estilo de [**CBS \_**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0e6a8-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e6a8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e6a8-118">Requirements</span></span>



| <span data-ttu-id="0e6a8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e6a8-119">Requirement</span></span> | <span data-ttu-id="0e6a8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0e6a8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6a8-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e6a8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e6a8-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e6a8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0e6a8-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e6a8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e6a8-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e6a8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e6a8-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0e6a8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e6a8-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e6a8-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e6a8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e6a8-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e6a8-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e6a8-129">**cópia do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-129">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="0e6a8-130">**recorte do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-130">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="0e6a8-131">**colar do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="0e6a8-132">**desfazer o WM \_**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="0e6a8-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0e6a8-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0e6a8-134">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="0e6a8-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

