---
title: Mensagem de WM_COMPAREITEM (WinUser. h)
description: Enviado para determinar a posição relativa de um novo item na lista classificada de uma caixa de combinação ou caixa de listagem desenhada pelo proprietário.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- Controles de WM_COMPAREITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454612"
---
# <a name="wm_compareitem-message"></a><span data-ttu-id="623f4-104">Mensagem do WM \_ COMPAREITEM</span><span class="sxs-lookup"><span data-stu-id="623f4-104">WM\_COMPAREITEM message</span></span>

<span data-ttu-id="623f4-105">Enviado para determinar a posição relativa de um novo item na lista classificada de uma caixa de combinação ou caixa de listagem desenhada pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="623f4-105">Sent to determine the relative position of a new item in the sorted list of an owner-drawn combo box or list box.</span></span> <span data-ttu-id="623f4-106">Sempre que o aplicativo adiciona um novo item, o sistema envia essa mensagem ao proprietário de uma caixa de combinação ou caixa de listagem criada com o estilo [**de \_ classificação**](list-box-styles.md) [**CBS \_**](combo-box-styles.md) ou lbs.</span><span class="sxs-lookup"><span data-stu-id="623f4-106">Whenever the application adds a new item, the system sends this message to the owner of a combo box or list box created with the [**CBS\_SORT**](combo-box-styles.md) or [**LBS\_SORT**](list-box-styles.md) style.</span></span>


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="623f4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="623f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623f4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="623f4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="623f4-109">Especifica o identificador do controle que enviou a mensagem **de \_ COMPAREITEM do WM** .</span><span class="sxs-lookup"><span data-stu-id="623f4-109">Specifies the identifier of the control that sent the **WM\_COMPAREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="623f4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="623f4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="623f4-111">Ponteiro para uma estrutura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) que contém os identificadores e os dados fornecidos pelo aplicativo para dois itens na caixa de combinação ou de listagem.</span><span class="sxs-lookup"><span data-stu-id="623f4-111">Pointer to a [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure that contains the identifiers and application-supplied data for two items in the combo or list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623f4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="623f4-112">Return value</span></span>

<span data-ttu-id="623f4-113">O valor de retorno indica a posição relativa dos dois itens.</span><span class="sxs-lookup"><span data-stu-id="623f4-113">The return value indicates the relative position of the two items.</span></span> <span data-ttu-id="623f4-114">Pode ser qualquer um dos valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="623f4-114">It may be any of the values shown in the following table.</span></span>



| <span data-ttu-id="623f4-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="623f4-115">Return code</span></span>                                                                          | <span data-ttu-id="623f4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="623f4-116">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="623f4-117"><dt>**Valor**</dt></span><span class="sxs-lookup"><span data-stu-id="623f4-117"><dt>**Value**</dt></span></span> </dl> | <span data-ttu-id="623f4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="623f4-118">Meaning</span></span><br/>                                           |
| <dl> <span data-ttu-id="623f4-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="623f4-119"><dt>**-1**</dt></span></span> </dl>    | <span data-ttu-id="623f4-120">O item 1 precede o item 2 na ordem classificada.</span><span class="sxs-lookup"><span data-stu-id="623f4-120">Item 1 precedes item 2 in the sorted order.</span></span><br/>       |
| <dl> <span data-ttu-id="623f4-121"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="623f4-121"><dt>**0**</dt></span></span> </dl>     | <span data-ttu-id="623f4-122">Os itens 1 e 2 são equivalentes na ordem classificada.</span><span class="sxs-lookup"><span data-stu-id="623f4-122">Items 1 and 2 are equivalent in the sorted order.</span></span><br/> |
| <dl> <span data-ttu-id="623f4-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="623f4-123"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="623f4-124">O item 1 segue o item 2 na ordem classificada.</span><span class="sxs-lookup"><span data-stu-id="623f4-124">Item 1 follows item 2 in the sorted order.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="623f4-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="623f4-125">Remarks</span></span>

<span data-ttu-id="623f4-126">Quando o proprietário de uma caixa de combinação ou caixa de listagem desenhada pelo proprietário recebe essa mensagem, o proprietário retorna um valor que indica qual dos itens especificados pela estrutura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) aparecerá antes do outro.</span><span class="sxs-lookup"><span data-stu-id="623f4-126">When the owner of an owner-drawn combo box or list box receives this message, the owner returns a value indicating which of the items specified by the [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure will appear before the other.</span></span> <span data-ttu-id="623f4-127">Normalmente, o sistema envia essa mensagem várias vezes até determinar a posição exata para o novo item.</span><span class="sxs-lookup"><span data-stu-id="623f4-127">Typically, the system sends this message several times until it determines the exact position for the new item.</span></span>

<span data-ttu-id="623f4-128">Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um **bool** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="623f4-128">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="623f4-129">O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="623f4-129">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="623f4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="623f4-130">Requirements</span></span>



| <span data-ttu-id="623f4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="623f4-131">Requirement</span></span> | <span data-ttu-id="623f4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="623f4-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="623f4-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="623f4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="623f4-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="623f4-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="623f4-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="623f4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="623f4-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="623f4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="623f4-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="623f4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="623f4-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="623f4-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="623f4-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="623f4-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="623f4-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="623f4-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="623f4-141">**COMPAREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="623f4-141">**COMPAREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

<span data-ttu-id="623f4-142">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="623f4-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="623f4-143">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="623f4-143">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

