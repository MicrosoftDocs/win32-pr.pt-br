---
title: Recurso DIALOGEX
description: Define uma caixa de diálogo. | Recurso DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menus de recursos do DIALOGEX e outros recursos
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172798"
---
# <a name="dialogex-resource"></a><span data-ttu-id="37a07-105">Recurso DIALOGEX</span><span class="sxs-lookup"><span data-stu-id="37a07-105">DIALOGEX resource</span></span>

<span data-ttu-id="37a07-106">Define uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-106">Defines a dialog box.</span></span> <span data-ttu-id="37a07-107">A instrução define a posição e as dimensões da caixa de diálogo na tela, bem como o estilo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span> <span data-ttu-id="37a07-108">Ele também define o seguinte:</span><span class="sxs-lookup"><span data-stu-id="37a07-108">It also defines the following:</span></span>

-   <span data-ttu-id="37a07-109">IDs de ajuda na caixa de diálogo em si, bem como nos controles dentro dela.</span><span class="sxs-lookup"><span data-stu-id="37a07-109">Help IDs on the dialog itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="37a07-110">Uso da instrução [**filestyle**](exstyle-statement.md) para a própria caixa de diálogo, bem como de controles dentro da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-110">Use of the [**EXSTYLE**](exstyle-statement.md) statement for the dialog box itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="37a07-111">Espessura da fonte e configurações em itálico para a fonte a ser usada na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-111">Font weight and italic settings for the font to be used in the dialog box.</span></span>
-   <span data-ttu-id="37a07-112">Dados específicos de controle para controles dentro da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-112">Control-specific data for controls within the dialog box.</span></span>
-   <span data-ttu-id="37a07-113">Uso dos nomes de classe de sistema predefinidos **BEDIT**, **IEDIT** e **HEDIT** .</span><span class="sxs-lookup"><span data-stu-id="37a07-113">Use of the **BEDIT**, **IEDIT**, and **HEDIT** predefined system class names.</span></span>

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a><span data-ttu-id="37a07-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37a07-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37a07-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="37a07-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-116">Nome exclusivo ou um valor inteiro de 16 bits sem sinal exclusivo que identifica a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-116">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-117"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="37a07-117"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-118">Local na tela do lado esquerdo da caixa de diálogo, em unidades de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-118">Location on the screen of the left side of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-119"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="37a07-119"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-120">Local na tela da parte superior da caixa de diálogo, em unidades de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-120">Location on the screen of the top of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-121"><span id="width"></span><span id="WIDTH"></span>*Largura*</span><span class="sxs-lookup"><span data-stu-id="37a07-121"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-122">Largura da caixa de diálogo, em unidades de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-122">Width of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-123"><span id="height"></span><span id="HEIGHT"></span>*tamanho*</span><span class="sxs-lookup"><span data-stu-id="37a07-123"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-124">Altura da caixa de diálogo, em unidades de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-124">Height of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*</span><span class="sxs-lookup"><span data-stu-id="37a07-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-126">Expressão numérica que indica a ID usada para identificar a caixa de diálogo durante o processamento da [**\_ ajuda do WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="37a07-126">Numeric expression indicating the ID used to identify the dialog box during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*</span><span class="sxs-lookup"><span data-stu-id="37a07-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-128">Opções para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-128">Options for the dialog box.</span></span> <span data-ttu-id="37a07-129">Isso pode ser zero ou mais das instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="37a07-129">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="37a07-130">Instrução</span><span class="sxs-lookup"><span data-stu-id="37a07-130">Statement</span></span>                                                         | <span data-ttu-id="37a07-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="37a07-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a07-132">**Legenda** "*texto*"</span><span class="sxs-lookup"><span data-stu-id="37a07-132">**CAPTION** "*text*"</span></span>                                              | <span data-ttu-id="37a07-133">Legenda da caixa de diálogo se ela tiver uma barra de título.</span><span class="sxs-lookup"><span data-stu-id="37a07-133">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="37a07-134">Para obter mais informações, consulte a [**instrução Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-134">For more information, see [**CAPTION Statement**](caption-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="37a07-135">**Características** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="37a07-135">**CHARACTERISTICS** *dword*</span></span>                                       | <span data-ttu-id="37a07-136">Valor **DWORD** definido pelo usuário para uso pelas ferramentas de recurso.</span><span class="sxs-lookup"><span data-stu-id="37a07-136">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="37a07-137">Esse valor não é usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="37a07-137">This value is not used by the system.</span></span> <span data-ttu-id="37a07-138">Para obter mais informações, consulte [**declaração de características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-138">For more information, see [**CHARACTERISTICS Statement**](characteristics-statement.md).</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="37a07-139">_Classe_ de classe</span><span class="sxs-lookup"><span data-stu-id="37a07-139">**CLASS**_class_</span></span>                                                  | <span data-ttu-id="37a07-140">Um inteiro não assinado de 16 bits ou uma cadeia de caracteres entre aspas duplas ("), que identifica a classe da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-140">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="37a07-141">Para obter mais informações, consulte [**declaração de classe**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-141">For more information, see [**CLASS Statement**](class-statement.md).</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="37a07-142">**COMstyle** =  *estilos estendidos*</span><span class="sxs-lookup"><span data-stu-id="37a07-142">**EXSTYLE**= *extended-styles*</span></span>                                    | <span data-ttu-id="37a07-143">Estilo de janela estendida da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-143">Extended window style of the dialog box.</span></span> <span data-ttu-id="37a07-144">Para obter mais informações, consulte [**instrução de filestyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-144">For more information, see [**EXSTYLE Statement**](exstyle-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="37a07-145"> *Pontos* de fonte, "*tipo de letra*", *peso*, *itálico*, conjunto de *caracteres*</span><span class="sxs-lookup"><span data-stu-id="37a07-145">**FONT** *pointsize*, "*typeface*", *weight*, *italic*, *charset*</span></span> | <span data-ttu-id="37a07-146">Tamanho do ponto e tipo da fonte.</span><span class="sxs-lookup"><span data-stu-id="37a07-146">Point size and typeface for the font.</span></span> <span data-ttu-id="37a07-147">Para *peso*, use os \**FW \_ \** _ valores definidos em WinGDI. h.</span><span class="sxs-lookup"><span data-stu-id="37a07-147">For *weight*, use the \**FW\_\** _ values defined in WinGDI.h.</span></span> <span data-ttu-id="37a07-148">Para _italic \*, especifique TRUE para usar uma fonte em itálico; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="37a07-148">For _italic\*, specify TRUE to use an italic font, FALSE otherwise.</span></span> <span data-ttu-id="37a07-149">Para *charset*, use o valor definido no membro **LfCharSet** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="37a07-149">For *charset*, use the value defined in the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="37a07-150">Para obter a fonte definitiva para uma caixa de diálogo, um aplicativo deve especificar *charset* juntamente com outras propriedades Font.</span><span class="sxs-lookup"><span data-stu-id="37a07-150">To get the definitive font for a dialog box, an application should specify *charset* along with other font properties.</span></span> <span data-ttu-id="37a07-151">Para obter mais informações, consulte [**instrução Font**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-151">For more information, see [**FONT Statement**](font-statement.md).</span></span> |
| <span data-ttu-id="37a07-152"> *Idioma* do idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="37a07-152">**LANGUAGE** *language*, *sublanguage*</span></span>                            | <span data-ttu-id="37a07-153">Idioma da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-153">Language of the dialog box.</span></span> <span data-ttu-id="37a07-154">Para obter mais informações, consulte a [**instrução de linguagem**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-154">For more information, see [**LANGUAGE Statement**](language-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="37a07-155"> *Menuname* do menu</span><span class="sxs-lookup"><span data-stu-id="37a07-155">**MENU** *menuname*</span></span>                                               | <span data-ttu-id="37a07-156">Menu a ser usado.</span><span class="sxs-lookup"><span data-stu-id="37a07-156">Menu to be used.</span></span> <span data-ttu-id="37a07-157">Esse valor é o nome do menu ou seu identificador de inteiro.</span><span class="sxs-lookup"><span data-stu-id="37a07-157">This value is either the name of the menu or its integer identifier.</span></span> <span data-ttu-id="37a07-158">Para obter mais informações, consulte a [**instrução de menu**](menu-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-158">For more information, see [**MENU Statement**](menu-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="37a07-159"> *Estilos* de estilo</span><span class="sxs-lookup"><span data-stu-id="37a07-159">**STYLE** *styles*</span></span>                                                | <span data-ttu-id="37a07-160">Estilos da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="37a07-160">Styles of the dialog box.</span></span> <span data-ttu-id="37a07-161">Para obter mais informações, consulte [**instrução de estilo**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-161">For more information, see [**STYLE Statement**](style-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="37a07-162"> *DWORD* da versão</span><span class="sxs-lookup"><span data-stu-id="37a07-162">**VERSION** *dword*</span></span>                                               | <span data-ttu-id="37a07-163">Valor **DWORD** definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="37a07-163">User-defined **DWORD** value.</span></span> <span data-ttu-id="37a07-164">Essa instrução destina-se ao uso por ferramentas de recursos adicionais e não é usada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="37a07-164">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="37a07-165">Para obter mais informações, consulte a [**instrução de versão**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-165">For more information, see [**VERSION Statement**](version-statement.md).</span></span>                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="37a07-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*instruções de controle*</span><span class="sxs-lookup"><span data-stu-id="37a07-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-167">O corpo do recurso **DIALOGEX** é composto de qualquer número de instruções de controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-167">Body of the **DIALOGEX** resource is made up of any number of control statements.</span></span> <span data-ttu-id="37a07-168">Há quatro famílias de instruções de controle: genérico, estático, botão e editar.</span><span class="sxs-lookup"><span data-stu-id="37a07-168">There are four families of control statements: generic, static, button, and edit.</span></span> <span data-ttu-id="37a07-169">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="37a07-169">For more information, see Remarks.</span></span>

</dd> </dl>

<span data-ttu-id="37a07-170">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="37a07-170">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="37a07-171">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-171">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="37a07-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="37a07-172">Remarks</span></span>

<span data-ttu-id="37a07-173">As operações válidas que podem estar contidas em qualquer uma das expressões numéricas nas instruções de **DIALOGEX** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="37a07-173">The valid operations that may be contained in any of the numeric expressions in the statements of **DIALOGEX** are as follows:</span></span>

-   <span data-ttu-id="37a07-174">Adicionar (' + ')</span><span class="sxs-lookup"><span data-stu-id="37a07-174">Add ('+')</span></span>
-   <span data-ttu-id="37a07-175">Subtrair ('-')</span><span class="sxs-lookup"><span data-stu-id="37a07-175">Subtract ('-')</span></span>
-   <span data-ttu-id="37a07-176">Menos unário ('-')</span><span class="sxs-lookup"><span data-stu-id="37a07-176">Unary minus ('-')</span></span>
-   <span data-ttu-id="37a07-177">Não unário (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="37a07-177">Unary NOT ('~')</span></span>
-   <span data-ttu-id="37a07-178">E (' & ')</span><span class="sxs-lookup"><span data-stu-id="37a07-178">AND ('&')</span></span>
-   <span data-ttu-id="37a07-179">OU (' \| ')</span><span class="sxs-lookup"><span data-stu-id="37a07-179">OR ('\|')</span></span>

<span data-ttu-id="37a07-180">O corpo do recurso é composto de instruções genéricas, estáticas, de botão e de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="37a07-180">The body of the resource is made up of generic, static, button, and edit control statements.</span></span> <span data-ttu-id="37a07-181">Embora cada uma dessas famílias de instruções use uma sintaxe diferente para definir recursos específicos de seus controles, todas elas compartilham uma sintaxe comum para definir a posição, o tamanho, os estilos estendidos, o número de identificação da ajuda e os dados específicos do controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-181">While each of these families of statements uses a different syntax for defining specific features of its controls, they all share a common syntax for defining the position, size, extended styles, help identification number, and control-specific data.</span></span> <span data-ttu-id="37a07-182">Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-182">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

### <a name="generic-control-statements"></a><span data-ttu-id="37a07-183">Instruções de controle genérico</span><span class="sxs-lookup"><span data-stu-id="37a07-183">Generic Control Statements</span></span>

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span data-ttu-id="37a07-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="37a07-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-185">Texto da janela para o controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-185">Window text for the control.</span></span> <span data-ttu-id="37a07-186">Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-186">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="37a07-187"><span id="id"></span><span id="ID"></span>*sessão*</span><span class="sxs-lookup"><span data-stu-id="37a07-187"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-188">Identificador do controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-188">Control identifier.</span></span> <span data-ttu-id="37a07-189">Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-189">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="37a07-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span><span class="sxs-lookup"><span data-stu-id="37a07-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-191">Nome da classe.</span><span class="sxs-lookup"><span data-stu-id="37a07-191">Name of the class.</span></span> <span data-ttu-id="37a07-192">Pode ser uma cadeia de caracteres entre aspas duplas (") ou uma das seguintes classes de sistema predefinidas: **botão**, **estático**, **Editar**, **ListBox**, **ScrollBar** ou **ComboBox**.</span><span class="sxs-lookup"><span data-stu-id="37a07-192">This may be either a string enclosed in double quotation marks (") or one of the following predefined system classes: **BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR**, or **COMBOBOX**.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-193"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="37a07-193"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-194">Estilos de janela (os valores explícitos **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lbs \_ \* *_, _* SBS \_ \* *_ e _* CBS \_ \*** Style definidos em winuser. H podem ser usados pela adição de um include ao arquivo. rc: `#include "winuser.h"` ).</span><span class="sxs-lookup"><span data-stu-id="37a07-194">Window styles (explicit **WS\_\**_, _\* BS\_\**_, _\* SS\_\*\*_, _\* ES\_\*\*_, _\* LBS\_\*\*_, _\* SBS\_\*\*_, and _\* CBS\_\*\*\* style values defined in Winuser.H can be used by adding an include to the .rc file: `#include "winuser.h"`).</span></span> <span data-ttu-id="37a07-195">Para obter mais informações, consulte [estilos de janela](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="37a07-195">For more information, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span>

</dd> </dl>

### <a name="static-control-statements"></a><span data-ttu-id="37a07-196">Instruções de controle estático</span><span class="sxs-lookup"><span data-stu-id="37a07-196">Static Control Statements</span></span>

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span data-ttu-id="37a07-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span><span class="sxs-lookup"><span data-stu-id="37a07-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-198">**LTEXT**, **RTEXT** ou **CTEXT**.</span><span class="sxs-lookup"><span data-stu-id="37a07-198">**LTEXT**, **RTEXT**, or **CTEXT**.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="37a07-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-200">Texto da janela para o controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-200">Window text for the control.</span></span> <span data-ttu-id="37a07-201">Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-201">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="37a07-202"><span id="id"></span><span id="ID"></span>*sessão*</span><span class="sxs-lookup"><span data-stu-id="37a07-202"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-203">Identificador do controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-203">Control identifier.</span></span> <span data-ttu-id="37a07-204">Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-204">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="button-control-statements"></a><span data-ttu-id="37a07-205">Instruções de controle de botão</span><span class="sxs-lookup"><span data-stu-id="37a07-205">Button Control Statements</span></span>

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span data-ttu-id="37a07-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span><span class="sxs-lookup"><span data-stu-id="37a07-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-207">**AUTO3STATE**, **autocaixa de seleção**, **AUTORADIOBUTTON**, **CheckBox**, **PUSHBOX**, botão de **pressão**, **RadioButton**, **STATE3** ou **UserButton**.</span><span class="sxs-lookup"><span data-stu-id="37a07-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3**, or **USERBUTTON**.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="37a07-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-209">Texto da janela para o controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-209">Window text for the control.</span></span> <span data-ttu-id="37a07-210">Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-210">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="37a07-211"><span id="id"></span><span id="ID"></span>*sessão*</span><span class="sxs-lookup"><span data-stu-id="37a07-211"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-212">Identificador do controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-212">Control identifier.</span></span> <span data-ttu-id="37a07-213">Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-213">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="edit-control-statements"></a><span data-ttu-id="37a07-214">Editar instruções de controle</span><span class="sxs-lookup"><span data-stu-id="37a07-214">Edit Control Statements</span></span>

``` syntax
editClass id
```

<dl> <dt>

<span data-ttu-id="37a07-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span><span class="sxs-lookup"><span data-stu-id="37a07-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-216">**EDITTEXT**, **BEDIT**, **HEDIT** ou **IEDIT**.</span><span class="sxs-lookup"><span data-stu-id="37a07-216">**EDITTEXT**, **BEDIT**, **HEDIT**, or **IEDIT**.</span></span>

</dd> <dt>

<span data-ttu-id="37a07-217"><span id="id"></span><span id="ID"></span>*sessão*</span><span class="sxs-lookup"><span data-stu-id="37a07-217"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="37a07-218">Identificador do controle.</span><span class="sxs-lookup"><span data-stu-id="37a07-218">Control identifier.</span></span> <span data-ttu-id="37a07-219">Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37a07-219">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="37a07-220">Confira também</span><span class="sxs-lookup"><span data-stu-id="37a07-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a07-221">Usando caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="37a07-221">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="37a07-222">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="37a07-222">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="37a07-223">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="37a07-223">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="37a07-224">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="37a07-224">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="37a07-225">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="37a07-225">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="37a07-226">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="37a07-226">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="37a07-227">**Caixa**</span><span class="sxs-lookup"><span data-stu-id="37a07-227">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="37a07-228">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="37a07-228">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="37a07-229">**LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="37a07-229">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="37a07-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="37a07-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="37a07-231">ADICIONARMENU</span><span class="sxs-lookup"><span data-stu-id="37a07-231">MENU</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="37a07-232">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="37a07-232">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="37a07-233">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="37a07-233">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="37a07-234">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="37a07-234">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
