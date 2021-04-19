---
title: Mensagem de LBSELCHSTRING (Commdlg. h)
description: Uma caixa de diálogo abrir ou salvar como envia a mensagem registrada LBSELCHSTRING para o procedimento de gancho quando a seleção é alterada em qualquer uma das caixas de listagem ou caixas de combinação da caixa de diálogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Caixas de diálogo de mensagem LBSELCHSTRING
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
ms.openlocfilehash: 137429b8fa7eb29fb96ec579e0240c4c282d0766
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590763"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="892c3-104">Mensagem LBSELCHSTRING</span><span class="sxs-lookup"><span data-stu-id="892c3-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="892c3-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="892c3-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="892c3-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="892c3-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="892c3-107">Uma caixa de diálogo **abrir** ou **salvar como** envia a mensagem registrada **LBSELCHSTRING** para o procedimento de gancho quando a seleção é alterada em qualquer uma das caixas de listagem ou caixas de combinação da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="892c3-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="892c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="892c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="892c3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="892c3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="892c3-110">O identificador da caixa de listagem ou da caixa de combinação na qual a seleção foi alterada.</span><span class="sxs-lookup"><span data-stu-id="892c3-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="892c3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="892c3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="892c3-112">A palavra de ordem inferior Especifica o número de item da cadeia de caracteres selecionada na caixa de listagem ou na caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="892c3-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="892c3-113">A palavra de ordem superior especifica o tipo de alteração de seleção.</span><span class="sxs-lookup"><span data-stu-id="892c3-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="892c3-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="892c3-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="892c3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="892c3-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="892c3-116">Significado</span><span class="sxs-lookup"><span data-stu-id="892c3-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="892c3-117"><dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="892c3-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="892c3-118">O item é o único item selecionado em uma caixa de listagem de seleção única.</span><span class="sxs-lookup"><span data-stu-id="892c3-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="892c3-119"><dt>**CD \_ LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="892c3-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="892c3-120">O item é um dos itens selecionados em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="892c3-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="892c3-121"><dt>**CD \_ LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="892c3-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="892c3-122">O item não está mais selecionado em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="892c3-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="892c3-123"><dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="892c3-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="892c3-124">Não existem itens em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="892c3-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="892c3-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="892c3-125">Return value</span></span>

<span data-ttu-id="892c3-126">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="892c3-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="892c3-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="892c3-127">Remarks</span></span>

<span data-ttu-id="892c3-128">O procedimento de gancho deve especificar a constante **LBSELCHSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="892c3-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="892c3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="892c3-129">Requirements</span></span>



| <span data-ttu-id="892c3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="892c3-130">Requirement</span></span> | <span data-ttu-id="892c3-131">Valor</span><span class="sxs-lookup"><span data-stu-id="892c3-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="892c3-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="892c3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="892c3-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="892c3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="892c3-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="892c3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="892c3-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="892c3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="892c3-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="892c3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="892c3-137"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="892c3-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="892c3-138">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="892c3-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="892c3-139">**LBSELCHSTRINGW** (Unicode) e **LBSELCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="892c3-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="892c3-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="892c3-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="892c3-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="892c3-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="892c3-142">**\_SELCHANGE CDN**</span><span class="sxs-lookup"><span data-stu-id="892c3-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="892c3-143">**\_TYPECHANGE CDN**</span><span class="sxs-lookup"><span data-stu-id="892c3-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="892c3-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="892c3-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="892c3-145">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="892c3-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="892c3-146">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="892c3-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

