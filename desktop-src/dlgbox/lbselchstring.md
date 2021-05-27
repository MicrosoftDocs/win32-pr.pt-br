---
title: Mensagem LBSELCHSTRING (Commdlg.h)
description: Uma caixa de diálogo Abrir ou Salvar como envia a mensagem registrada LBSELCHSTRING ao procedimento de gancho quando a seleção muda em qualquer uma das caixas de listagem ou caixas de combinação da caixa de diálogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Caixas de diálogo da mensagem LBSELCHSTRING
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d61f88bd7cb6a84a94a3d8a246e6045f88a305
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550041"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="d4427-104">Mensagem LBSELCHSTRING</span><span class="sxs-lookup"><span data-stu-id="d4427-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="d4427-105">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="d4427-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="d4427-106">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="d4427-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="d4427-107">Uma  caixa **de** diálogo Abrir ou Salvar como envia a mensagem registrada **LBSELCHSTRING** ao procedimento de gancho quando a seleção muda em qualquer uma das caixas de listagem ou caixas de combinação da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d4427-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="d4427-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4427-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4427-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4427-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4427-110">O identificador da caixa de listagem ou caixa de combinação na qual a seleção foi alterada.</span><span class="sxs-lookup"><span data-stu-id="d4427-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="d4427-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4427-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4427-112">A palavra de ordem baixa especifica o número do item da cadeia de caracteres selecionada na caixa de listagem ou caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="d4427-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="d4427-113">A palavra de ordem alta especifica o tipo de alteração de seleção.</span><span class="sxs-lookup"><span data-stu-id="d4427-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="d4427-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4427-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d4427-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d4427-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="d4427-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d4427-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="d4427-117"><dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d4427-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="d4427-118">O item é o único item selecionado em uma caixa de listagem de seleção única.</span><span class="sxs-lookup"><span data-stu-id="d4427-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="d4427-119"><dt>**CD \_ LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d4427-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="d4427-120">O item é um dos itens selecionados em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="d4427-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="d4427-121"><dt>**CD \_ LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d4427-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="d4427-122">O item não está mais selecionado em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="d4427-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="d4427-123"><dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="d4427-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="d4427-124">Nenhum item existe em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="d4427-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4427-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4427-125">Return value</span></span>

<span data-ttu-id="d4427-126">Essa mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d4427-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4427-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4427-127">Remarks</span></span>

<span data-ttu-id="d4427-128">O procedimento de gancho deve especificar a constante **LBSELCHSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador da mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d4427-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4427-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4427-129">Requirements</span></span>



| <span data-ttu-id="d4427-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4427-130">Requirement</span></span> | <span data-ttu-id="d4427-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d4427-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4427-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4427-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d4427-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d4427-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d4427-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4427-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d4427-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d4427-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d4427-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d4427-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4427-137"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4427-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d4427-138">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d4427-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d4427-139">**LBSELCHSTRINGW** (Unicode) e **LBSELCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d4427-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="d4427-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4427-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="d4427-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d4427-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d4427-142">**\_SELCHANGE CDN**</span><span class="sxs-lookup"><span data-stu-id="d4427-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="d4427-143">**\_TYPECHANGE CDN**</span><span class="sxs-lookup"><span data-stu-id="d4427-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="d4427-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="d4427-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="d4427-145">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d4427-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d4427-146">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="d4427-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

