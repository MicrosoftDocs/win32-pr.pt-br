---
title: Recurso de caixa de diálogo
description: Define uma caixa de diálogo. | Recurso de caixa de diálogo
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menus de recursos de caixa de diálogo e outros recursos
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760788"
---
# <a name="dialog-resource"></a><span data-ttu-id="551c8-105">Recurso de caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="551c8-105">DIALOG resource</span></span>

<span data-ttu-id="551c8-106">Define uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-106">Defines a dialog box.</span></span> <span data-ttu-id="551c8-107">A instrução define a posição e as dimensões da caixa de diálogo na tela, bem como o estilo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span>

> [!Note]  
> <span data-ttu-id="551c8-108">A **caixa de diálogo** é uma ID de recurso obsoleta.</span><span class="sxs-lookup"><span data-stu-id="551c8-108">**DIALOG** is an obsolete resource ID.</span></span> <span data-ttu-id="551c8-109">Os novos aplicativos devem usar o [**DIALOGEX**](dialogex-resource.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-109">New applications should use [**DIALOGEX**](dialogex-resource.md).</span></span>

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a><span data-ttu-id="551c8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="551c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="551c8-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="551c8-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="551c8-112">Nome exclusivo ou um valor inteiro de 16 bits sem sinal exclusivo que identifica a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-112">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="551c8-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*</span><span class="sxs-lookup"><span data-stu-id="551c8-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="551c8-114">Opções para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-114">Options for the dialog box.</span></span> <span data-ttu-id="551c8-115">Isso pode ser zero ou mais das instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="551c8-115">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="551c8-116">Instrução</span><span class="sxs-lookup"><span data-stu-id="551c8-116">Statement</span></span>                                                        | <span data-ttu-id="551c8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="551c8-117">Description</span></span>                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="551c8-118">[**Legenda**](caption-statement.md) "*texto*"</span><span class="sxs-lookup"><span data-stu-id="551c8-118">[**CAPTION**](caption-statement.md) "*text*"</span></span>                    | <span data-ttu-id="551c8-119">Legenda da caixa de diálogo se ela tiver uma barra de título.</span><span class="sxs-lookup"><span data-stu-id="551c8-119">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="551c8-120">Para obter mais informações, consulte [**legenda**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-120">For more information, see [**CAPTION**](caption-statement.md).</span></span>                                                                             |
| <span data-ttu-id="551c8-121">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="551c8-121">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="551c8-122">Valor **DWORD** definido pelo usuário para uso pelas ferramentas de recurso.</span><span class="sxs-lookup"><span data-stu-id="551c8-122">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="551c8-123">Esse valor não é usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="551c8-123">This value is not used by the system.</span></span> <span data-ttu-id="551c8-124">Para obter mais informações, consulte [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-124">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span>                |
| <span data-ttu-id="551c8-125">[](class-statement.md) *Classe* de classe</span><span class="sxs-lookup"><span data-stu-id="551c8-125">[**CLASS**](class-statement.md) *class*</span></span>                         | <span data-ttu-id="551c8-126">Um inteiro não assinado de 16 bits ou uma cadeia de caracteres entre aspas duplas ("), que identifica a classe da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-126">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="551c8-127">Para obter mais informações, consulte [**classe**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-127">For more information, see [**CLASS**](class-statement.md).</span></span>      |
| <span data-ttu-id="551c8-128">**Filestyle =** *estilos estendidos*</span><span class="sxs-lookup"><span data-stu-id="551c8-128">**EXSTYLE=** *extended-styles*</span></span>                                   | <span data-ttu-id="551c8-129">Estilo de janela estendida da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-129">Extended window style of the dialog box.</span></span> <span data-ttu-id="551c8-130">Para obter mais informações, consulte [**comstyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-130">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>                                                                                     |
| <span data-ttu-id="551c8-131"> *Pontos* de fonte, *face de tipos*</span><span class="sxs-lookup"><span data-stu-id="551c8-131">**FONT** *pointsize*, *typeface*</span></span>                                 | <span data-ttu-id="551c8-132">Tamanho do ponto e tipo da fonte.</span><span class="sxs-lookup"><span data-stu-id="551c8-132">Point size and typeface for the font.</span></span> <span data-ttu-id="551c8-133">Para obter mais informações, consulte [**fonte**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-133">For more information, see [**FONT**](font-statement.md).</span></span>                                                                                              |
| <span data-ttu-id="551c8-134">[](language-statement.md) *Idioma* do idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="551c8-134">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="551c8-135">Idioma da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-135">Language of the dialog box.</span></span> <span data-ttu-id="551c8-136">Para obter mais informações, consulte [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-136">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                                |
| <span data-ttu-id="551c8-137"> *Menuname* do menu</span><span class="sxs-lookup"><span data-stu-id="551c8-137">**MENU** *menuname*</span></span>                                              | <span data-ttu-id="551c8-138">Menu a ser usado.</span><span class="sxs-lookup"><span data-stu-id="551c8-138">Menu to be used.</span></span> <span data-ttu-id="551c8-139">Esse valor é o nome do menu ou seu identificador de inteiro.</span><span class="sxs-lookup"><span data-stu-id="551c8-139">This value is either the name of the menu or its integer identifier.</span></span>                                                                                                        |
| <span data-ttu-id="551c8-140">[](style-statement.md) *Estilos* de estilo</span><span class="sxs-lookup"><span data-stu-id="551c8-140">[**STYLE**](style-statement.md) *styles*</span></span>                        | <span data-ttu-id="551c8-141">Estilos da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-141">Styles of the dialog box.</span></span> <span data-ttu-id="551c8-142">Para obter mais informações, consulte [**estilo**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-142">For more information, see [**STYLE**](style-statement.md).</span></span>                                                                                                        |
| <span data-ttu-id="551c8-143">[](version-statement.md) *DWORD* da versão</span><span class="sxs-lookup"><span data-stu-id="551c8-143">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="551c8-144">Valor **DWORD** definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="551c8-144">User-defined **DWORD** value.</span></span> <span data-ttu-id="551c8-145">Essa instrução destina-se ao uso por ferramentas de recursos adicionais e não é usada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="551c8-145">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="551c8-146">Para obter mais informações, consulte [**versão**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-146">For more information, see [**VERSION**](version-statement.md).</span></span> |



 

</dd> </dl>

<span data-ttu-id="551c8-147">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="551c8-147">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="551c8-148">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="551c8-148">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="551c8-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="551c8-149">Remarks</span></span>

<span data-ttu-id="551c8-150">A função [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retorna as unidades base da caixa de diálogo em pixels.</span><span class="sxs-lookup"><span data-stu-id="551c8-150">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="551c8-151">O significado exato das coordenadas depende do estilo definido pela instrução de opção de [**estilo**](style-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="551c8-151">The exact meaning of the coordinates depends on the style defined by the [**STYLE**](style-statement.md) option statement.</span></span> <span data-ttu-id="551c8-152">Para caixas de diálogo de estilo filho, as coordenadas são relativas à origem da janela pai, a menos que a caixa de diálogo tenha o estilo **DS \_ ABSALIGN**; nesse caso, as coordenadas são relativas à origem da tela de exibição.</span><span class="sxs-lookup"><span data-stu-id="551c8-152">For child-style dialog boxes, the coordinates are relative to the origin of the parent window, unless the dialog box has the style **DS\_ABSALIGN**; in that case, the coordinates are relative to the origin of the display screen.</span></span>

<span data-ttu-id="551c8-153">Não use o estilo **\_ filho WS** com uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="551c8-153">Do not use the **WS\_CHILD** style with a modal dialog box.</span></span> <span data-ttu-id="551c8-154">A função [**caixa**](/windows/win32/api/winuser/nf-winuser-dialogboxa) sempre desabilita o pai/proprietário da caixa de diálogo recém-criada.</span><span class="sxs-lookup"><span data-stu-id="551c8-154">The [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function always disables the parent/owner of the newly created dialog box.</span></span> <span data-ttu-id="551c8-155">Quando uma janela pai é desabilitada, suas janelas filhas são desabilitadas implicitamente.</span><span class="sxs-lookup"><span data-stu-id="551c8-155">When a parent window is disabled, its child windows are implicitly disabled.</span></span> <span data-ttu-id="551c8-156">Como a janela pai da caixa de diálogo estilo filho está desabilitada, a caixa de diálogo estilo filho também é.</span><span class="sxs-lookup"><span data-stu-id="551c8-156">Since the parent window of the child-style dialog box is disabled, the child-style dialog box is too.</span></span>

<span data-ttu-id="551c8-157">Se uma caixa de diálogo tiver o estilo **DS \_ ABSALIGN** , as coordenadas para seu canto superior esquerdo serão relativas à origem da tela em vez de ao canto superior esquerdo da janela pai.</span><span class="sxs-lookup"><span data-stu-id="551c8-157">If a dialog box has the **DS\_ABSALIGN** style, the dialog coordinates for its upper-left corner are relative to the screen origin instead of to the upper-left corner of the parent window.</span></span> <span data-ttu-id="551c8-158">Normalmente, você usaria esse estilo quando quisesse que a caixa de diálogo fosse iniciada em uma parte específica da exibição, independentemente de onde a janela pai possa estar na tela.</span><span class="sxs-lookup"><span data-stu-id="551c8-158">You would typically use this style when you wanted the dialog box to start in a specific part of the display no matter where the parent window may be on the screen.</span></span>

<span data-ttu-id="551c8-159">A caixa de **diálogo** de nome também pode ser usada como o parâmetro Class-Name para a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela com atributos de caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="551c8-159">The name **DIALOG** can also be used as the class-name parameter to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function to create a window with dialog-box attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="551c8-160">Exemplos</span><span class="sxs-lookup"><span data-stu-id="551c8-160">Examples</span></span>

<span data-ttu-id="551c8-161">O seguinte demonstra o uso da instrução **Dialog** :</span><span class="sxs-lookup"><span data-stu-id="551c8-161">The following demonstrates the usage of the **DIALOG** statement:</span></span>

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a><span data-ttu-id="551c8-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="551c8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="551c8-163">Usando caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="551c8-163">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="551c8-164">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="551c8-164">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="551c8-165">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="551c8-165">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="551c8-166">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="551c8-166">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="551c8-167">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="551c8-167">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="551c8-168">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="551c8-168">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="551c8-169">**Caixa**</span><span class="sxs-lookup"><span data-stu-id="551c8-169">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="551c8-170">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="551c8-170">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="551c8-171">**IDIOMA**</span><span class="sxs-lookup"><span data-stu-id="551c8-171">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="551c8-172">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="551c8-172">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="551c8-173">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="551c8-173">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="551c8-174">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="551c8-174">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="551c8-175">**Versão**</span><span class="sxs-lookup"><span data-stu-id="551c8-175">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
