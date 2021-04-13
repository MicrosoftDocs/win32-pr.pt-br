---
title: Estrutura DLGITEMTEMPLATEEX
description: Um bloco de texto usado por um modelo de caixa de diálogo estendida para descrever a caixa de diálogo estendida. Para obter uma descrição do formato de um modelo de caixa de diálogo estendido, consulte DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Caixas de diálogo da estrutura DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369894"
---
# <a name="dlgitemtemplateex-structure"></a><span data-ttu-id="0fb6c-105">Estrutura DLGITEMTEMPLATEEX</span><span class="sxs-lookup"><span data-stu-id="0fb6c-105">DLGITEMTEMPLATEEX structure</span></span>

<span data-ttu-id="0fb6c-106">Um bloco de texto usado por um modelo de caixa de diálogo estendida para descrever a caixa de diálogo estendida.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-106">A block of text used by an extended dialog box template to describe the extended dialog box.</span></span> <span data-ttu-id="0fb6c-107">Para obter uma descrição do formato de um modelo de caixa de diálogo estendido, consulte [**DLGTEMPLATEEX**](dlgtemplateex.md).</span><span class="sxs-lookup"><span data-stu-id="0fb6c-107">For a description of the format of an extended dialog box template, see [**DLGTEMPLATEEX**](dlgtemplateex.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb6c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fb6c-108">Syntax</span></span>


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="0fb6c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="0fb6c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0fb6c-110">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-110">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-112">O identificador de contexto da ajuda para o controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-112">The help context identifier for the control.</span></span> <span data-ttu-id="0fb6c-113">Quando o sistema envia uma mensagem de [**\_ ajuda do WM**](../shell/wm-help.md) , ele passa o valor **HelpID** no membro **dwContextId** da estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="0fb6c-113">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes the **helpID** value in the **dwContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-114">**comstyle**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-114">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-116">Os estilos estendidos para uma janela.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-116">The extended styles for a window.</span></span> <span data-ttu-id="0fb6c-117">Esse membro não é usado para criar controles em caixas de diálogo, mas os aplicativos que usam modelos de caixa de diálogo podem usá-lo para criar outros tipos de janelas.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-117">This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="0fb6c-118">Para obter uma lista de valores, consulte [**estilos de janela estendidos**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="0fb6c-118">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-119">**style**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-119">**style**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-120">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-120">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-121">O estilo do controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-121">The style of the control.</span></span> <span data-ttu-id="0fb6c-122">Esse membro pode ser uma combinação de [valores de estilo de janela](/windows/desktop/winmsg/window-styles) ( **como WS \_ Border**) e um ou mais dos [valores de estilo de controle](/windows/desktop/Controls/common-control-styles) (como a **BS \_** , e **es \_ à esquerda**).</span><span class="sxs-lookup"><span data-stu-id="0fb6c-122">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) (such as **WS\_BORDER**) and one or more of the [control style values](/windows/desktop/Controls/common-control-styles) (such as **BS\_PUSHBUTTON** and **ES\_LEFT**).</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-123">**x**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-123">**x**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-124">Tipo: **curto**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-124">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-125">A coordenada x, nas unidades da caixa de diálogo, do canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-125">The x-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="0fb6c-126">Essa coordenada é sempre relativa ao canto superior esquerdo da área do cliente da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-126">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-127">**y**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-127">**y**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-128">Tipo: **curto**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-128">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-129">A coordenada y, nas unidades da caixa de diálogo, do canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-129">The y-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="0fb6c-130">Essa coordenada é sempre relativa ao canto superior esquerdo da área do cliente da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-130">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-131">**CX**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-131">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-132">Tipo: **curto**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-132">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-133">A largura, nas unidades da caixa de diálogo, do controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-133">The width, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-134">**Cy**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-134">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-135">Tipo: **curto**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-135">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-136">A altura, nas unidades da caixa de diálogo, do controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-136">The height, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-137">**id**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-137">**id**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-138">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-139">O identificador de controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-139">The control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-140">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-140">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-141">Tipo: **sz \_ ou \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-141">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-142">Uma matriz de comprimento variável de elementos de 16 bits que especifica a classe de janela do controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-142">A variable-length array of 16-bit elements that specifies the window class of the control.</span></span> <span data-ttu-id="0fb6c-143">Se o primeiro elemento dessa matriz for qualquer valor diferente de 0xFFFF, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de uma classe de janela registrada.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-143">If the first element of this array is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

<span data-ttu-id="0fb6c-144">Se o primeiro elemento for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de uma classe de sistema predefinida.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-144">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system class.</span></span> <span data-ttu-id="0fb6c-145">O ordinal pode ser um dos valores de Atom a seguir.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-145">The ordinal can be one of the following atom values.</span></span>



| <span data-ttu-id="0fb6c-146">Valor</span><span class="sxs-lookup"><span data-stu-id="0fb6c-146">Value</span></span>                                                                             | <span data-ttu-id="0fb6c-147">Significado</span><span class="sxs-lookup"><span data-stu-id="0fb6c-147">Meaning</span></span>               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="0fb6c-148"><dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="0fb6c-148"><dt>0x0080</dt></span></span> </dl> | <span data-ttu-id="0fb6c-149">Botão</span><span class="sxs-lookup"><span data-stu-id="0fb6c-149">Button</span></span><br/>     |
| <dl> <span data-ttu-id="0fb6c-150"><dt>0x0081</dt></span><span class="sxs-lookup"><span data-stu-id="0fb6c-150"><dt>0x0081</dt></span></span> </dl> | <span data-ttu-id="0fb6c-151">Editar</span><span class="sxs-lookup"><span data-stu-id="0fb6c-151">Edit</span></span><br/>       |
| <dl> <span data-ttu-id="0fb6c-152"><dt>0x0082</dt></span><span class="sxs-lookup"><span data-stu-id="0fb6c-152"><dt>0x0082</dt></span></span> </dl> | <span data-ttu-id="0fb6c-153">Estático</span><span class="sxs-lookup"><span data-stu-id="0fb6c-153">Static</span></span><br/>     |
| <dl> <span data-ttu-id="0fb6c-154"><dt>0x0083</dt></span><span class="sxs-lookup"><span data-stu-id="0fb6c-154"><dt>0x0083</dt></span></span> </dl> | <span data-ttu-id="0fb6c-155">Caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="0fb6c-155">List box</span></span><br/>   |
| <dl> <span data-ttu-id="0fb6c-156"><dt>0x0084</dt></span><span class="sxs-lookup"><span data-stu-id="0fb6c-156"><dt>0x0084</dt></span></span> </dl> | <span data-ttu-id="0fb6c-157">Barra de rolagem</span><span class="sxs-lookup"><span data-stu-id="0fb6c-157">Scroll bar</span></span><br/> |
| <dl> <span data-ttu-id="0fb6c-158"><dt>0x0085</dt></span><span class="sxs-lookup"><span data-stu-id="0fb6c-158"><dt>0x0085</dt></span></span> </dl> | <span data-ttu-id="0fb6c-159">Caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="0fb6c-159">Combo box</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="0fb6c-160">**title**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-160">**title**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-161">Tipo: **sz \_ ou \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-161">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-162">Uma matriz de comprimento variável de elementos de 16 bits que contém o identificador de texto inicial ou de recurso do controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-162">A variable-length array of 16-bit elements that contains the initial text or resource identifier of the control.</span></span> <span data-ttu-id="0fb6c-163">Se o primeiro elemento dessa matriz for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de um recurso, como um ícone, em um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-163">If the first element of this array is 0xFFFF, the array has one additional element that specifies the ordinal value of a resource, such as an icon, in an executable file.</span></span> <span data-ttu-id="0fb6c-164">Você pode usar um identificador de recurso para controles, como controles de ícone estáticos, que carregam e exibem um ícone ou outro recurso em vez de texto.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-164">You can use a resource identifier for controls, such as static icon controls, that load and display an icon or other resource rather than text.</span></span> <span data-ttu-id="0fb6c-165">Se o primeiro elemento for qualquer valor diferente de 0xFFFF, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o texto inicial.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-165">If the first element is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the initial text.</span></span>

</dd> <dt>

<span data-ttu-id="0fb6c-166">**extraCount**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-166">**extraCount**</span></span>
</dt> <dd>

<span data-ttu-id="0fb6c-167">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-167">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0fb6c-168">O número de bytes de dados de criação que seguem esse membro.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-168">The number of bytes of creation data that follow this member.</span></span> <span data-ttu-id="0fb6c-169">Se esse valor for maior que zero, os dados de criação começarão no próximo limite de **palavra** .</span><span class="sxs-lookup"><span data-stu-id="0fb6c-169">If this value is greater than zero, the creation data begins at the next **WORD** boundary.</span></span> <span data-ttu-id="0fb6c-170">Esses dados de criação podem ser de qualquer tamanho e formato.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-170">This creation data can be of any size and format.</span></span> <span data-ttu-id="0fb6c-171">O procedimento de janela do controle deve ser capaz de interpretar os dados.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-171">The control's window procedure must be able to interpret the data.</span></span> <span data-ttu-id="0fb6c-172">Quando o sistema cria o controle, ele passa um ponteiro para esses dados no parâmetro *lParam* da mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) que ele envia para o controle.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-172">When the system creates the control, it passes a pointer to this data in the *lParam* parameter of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message that it sends to the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fb6c-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fb6c-173">Remarks</span></span>

<span data-ttu-id="0fb6c-174">Um modelo estendido para uma caixa de diálogo consiste em um cabeçalho [**DLGTEMPLATEEX**](dlgtemplateex.md) seguido por uma estrutura **DLGITEMTEMPLATEEX** para cada controle na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-174">An extended template for a dialog box consists of a [**DLGTEMPLATEEX**](dlgtemplateex.md) header followed by a **DLGITEMTEMPLATEEX** structure for each control in the dialog box.</span></span>

<span data-ttu-id="0fb6c-175">Cada estrutura **DLGITEMTEMPLATEEX** deve estar alinhada em um limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0fb6c-175">Each **DLGITEMTEMPLATEEX** structure must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="0fb6c-176">As matrizes **WindowClass** e **title** de comprimento variável devem ser alinhadas em limites de **palavras** .</span><span class="sxs-lookup"><span data-stu-id="0fb6c-176">The variable-length **windowClass** and **title** arrays must be aligned on **WORD** boundaries.</span></span> <span data-ttu-id="0fb6c-177">A matriz de dados de criação, se houver, deve estar alinhada em um limite de **palavra** .</span><span class="sxs-lookup"><span data-stu-id="0fb6c-177">The creation data array, if any, must be aligned on a **WORD** boundary.</span></span>

<span data-ttu-id="0fb6c-178">Se você especificar cadeias de caracteres nas matrizes **WindowClass** e **title** , você deverá usar cadeias Unicode.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-178">If you specify character strings in the **windowClass** and **title** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="0fb6c-179">Use a função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para gerar cadeias de caracteres Unicode de cadeias de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-179">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="0fb6c-180">Os membros **x**, **y**, **CX** e **CY** especificam valores nas unidades da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0fb6c-180">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="0fb6c-181">Você pode converter esses valores em unidades de tela (pixels) usando a função [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="0fb6c-181">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb6c-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fb6c-182">Requirements</span></span>



| <span data-ttu-id="0fb6c-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fb6c-183">Requirement</span></span> | <span data-ttu-id="0fb6c-184">Valor</span><span class="sxs-lookup"><span data-stu-id="0fb6c-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0fb6c-185">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fb6c-185">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb6c-186">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0fb6c-186">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0fb6c-187">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fb6c-187">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb6c-188">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0fb6c-188">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0fb6c-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fb6c-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="0fb6c-190">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0fb6c-191">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-191">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="0fb6c-192">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-192">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="0fb6c-193">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-193">**CreateWindowEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="0fb6c-194">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-194">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="0fb6c-195">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-195">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="0fb6c-196">**DLGTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-196">**DLGTEMPLATEEX**</span></span>](dlgtemplateex.md)
</dt> <dt>

[<span data-ttu-id="0fb6c-197">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-197">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="0fb6c-198">**criação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-198">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)
</dt> <dt>

<span data-ttu-id="0fb6c-199">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0fb6c-200">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="0fb6c-200">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="0fb6c-201">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-201">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0fb6c-202">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-202">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[<span data-ttu-id="0fb6c-203">**ajuda do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0fb6c-203">**WM\_HELP**</span></span>](../shell/wm-help.md)
</dt> </dl>

 

