---
title: Parâmetros de controle comuns
description: O seguinte descreve a sintaxe geral para uma instrução Control Resource-Definition.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293986"
---
# <a name="common-control-parameters"></a><span data-ttu-id="a2c2a-103">Parâmetros de controle comuns</span><span class="sxs-lookup"><span data-stu-id="a2c2a-103">Common Control Parameters</span></span>

<span data-ttu-id="a2c2a-104">O seguinte descreve a sintaxe geral para uma instrução Control Resource-Definition.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-104">The following describes the general syntax for a control resource-definition statement.</span></span> <span data-ttu-id="a2c2a-105">O significado de cada parâmetro é fornecido abaixo.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-105">The meaning of each parameter is given below.</span></span> <span data-ttu-id="a2c2a-106">Ocasionalmente, uma instrução usará um parâmetro de forma diferente ou poderá ignorar um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-106">Occasionally, a statement will use a parameter differently, or may ignore a parameter.</span></span> <span data-ttu-id="a2c2a-107">A variação específica da instrução é descrita na documentação da instrução.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-107">The statement-specific variation is described in the documentation for the statement.</span></span>

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span data-ttu-id="a2c2a-108"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-109">Texto a ser exibido com o controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-109">Text that is to be displayed with the control.</span></span> <span data-ttu-id="a2c2a-110">O texto é posicionado dentro do controle ou adjacente ao controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-110">The text is positioned within the control or adjacent to the control.</span></span>

<span data-ttu-id="a2c2a-111">Esse parâmetro deve conter zero ou mais caracteres entre aspas duplas (").</span><span class="sxs-lookup"><span data-stu-id="a2c2a-111">This parameter must contain zero or more characters enclosed in double quotation marks (").</span></span> <span data-ttu-id="a2c2a-112">As cadeias de caracteres são automaticamente terminadas em nulo e convertidas em Unicode no arquivo de recurso resultante.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-112">Strings are automatically null-terminated and converted to Unicode in the resulting resource file.</span></span>

<span data-ttu-id="a2c2a-113">Por padrão, os caracteres listados entre aspas duplas são caracteres ANSI e as sequências de escape são interpretadas como sequências de escape de byte.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-113">By default, the characters listed between the double quotation marks are ANSI characters, and escape sequences are interpreted as byte escape sequences.</span></span> <span data-ttu-id="a2c2a-114">Se a cadeia de caracteres for precedida pelo prefixo "L", a cadeia de caracteres será uma cadeia de caracteres largos e as sequências de escape serão interpretadas como sequências de escape de 2 bytes que especificam caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-114">If the string is preceded by the "L" prefix, the string is a wide-character string and escape sequences are interpreted as 2-byte escape sequences that specify Unicode characters.</span></span> <span data-ttu-id="a2c2a-115">Se uma aspa dupla for necessária no texto, você deverá incluir duas aspas duas vezes.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-115">If a double quotation mark is required in the text, you must include the double quotation mark twice.</span></span>

<span data-ttu-id="a2c2a-116">Um caractere de e comercial (&) no texto indica que o caractere a seguir é usado como um caractere mnemônico para o controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-116">An ampersand (&) character in the text indicates that the following character is used as a mnemonic character for the control.</span></span> <span data-ttu-id="a2c2a-117">Quando o controle é exibido, o e comercial não é mostrado, mas o caractere mnemônico é sublinhado.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-117">When the control is displayed, the ampersand is not shown, but the mnemonic character is underlined.</span></span> <span data-ttu-id="a2c2a-118">O usuário pode escolher o controle pressionando a tecla correspondente ao caractere mnemônico sublinhado.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-118">The user can choose the control by pressing the key corresponding to the underlined mnemonic character.</span></span> <span data-ttu-id="a2c2a-119">Para usar o e comercial como um caractere em uma cadeia de caracteres, insira dois e comercial (&&).</span><span class="sxs-lookup"><span data-stu-id="a2c2a-119">To use the ampersand as a character in a string, insert two ampersands (&&).</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-120"><span id="id"></span><span id="ID"></span>*sessão*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-121">Identificador do controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-121">Control identifier.</span></span> <span data-ttu-id="a2c2a-122">Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535 ou uma expressão aritmética simples que é avaliada como um valor nesse intervalo.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-122">This value must be a 16-bit unsigned integer in the range 0 through 65,535 or a simple arithmetic expression that evaluates to a value in that range.</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-123"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-123"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-124">Coordenada X do lado esquerdo do controle em relação ao lado esquerdo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-124">X-coordinate of the left side of the control relative to the left side of the dialog box.</span></span> <span data-ttu-id="a2c2a-125">Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-125">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="a2c2a-126">A coordenada está em unidades de caixa de diálogo e é relativa à origem da caixa de diálogo, janela ou controle que contém o controle especificado.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-126">The coordinate is in dialog units and is relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-127"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-127"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-128">Coordenada Y do lado superior do controle em relação à parte superior da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-128">Y-coordinate of the top side of the control relative to the top of the dialog box.</span></span> <span data-ttu-id="a2c2a-129">Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-129">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="a2c2a-130">A coordenada está em unidades de caixa de diálogo relativas à origem da caixa de diálogo, janela ou controle que contém o controle especificado.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-130">The coordinate is in dialog units relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-131"><span id="width"></span><span id="WIDTH"></span>*Largura*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-131"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-132">Largura do controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-132">Width of the control.</span></span> <span data-ttu-id="a2c2a-133">Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 1 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-133">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="a2c2a-134">A largura está em unidades de 1/4 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-134">The width is in 1/4-character units.</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-135"><span id="height"></span><span id="HEIGHT"></span>*tamanho*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-135"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-136">Altura do controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-136">Height of the control.</span></span> <span data-ttu-id="a2c2a-137">Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 1 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-137">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="a2c2a-138">A altura está em unidades de 1/8 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-138">The height is in 1/8-character units.</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-139"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-139"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-140">Estilos de controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-140">Control styles.</span></span> <span data-ttu-id="a2c2a-141">Use o operador OR () de or ( \| ) para combinar estilos.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-141">Use the bitwise OR (\|) operator to combine styles.</span></span> <span data-ttu-id="a2c2a-142">Para obter mais informações, consulte [estilos de janela](../winmsg/window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="a2c2a-142">For more information, see [Window Styles](../winmsg/window-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo estendido*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-144">Estilos de janela estendidos.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-144">Extended window styles.</span></span> <span data-ttu-id="a2c2a-145">Você deve especificar o *estilo* para especificar o *estilo estendido*.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-145">You must specify *style* to specify *extended-style*.</span></span> <span data-ttu-id="a2c2a-146">Para obter mais informações, consulte [**comstyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="a2c2a-146">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-148">Expressão numérica que indica a ID usada para identificar o controle durante o processamento da [**\_ ajuda do WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c2a-148">Numeric expression indicating the ID used to identify the control during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="a2c2a-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span><span class="sxs-lookup"><span data-stu-id="a2c2a-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span></span>
</dt> <dd>

<span data-ttu-id="a2c2a-150">Dados específicos de controle para o controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-150">Control-specific data for the control.</span></span> <span data-ttu-id="a2c2a-151">Quando uma caixa de diálogo é criada e um controle nessa caixa de diálogo que tem dados específicos de controle é criado, um ponteiro para esses dados é passado para o procedimento de janela do controle por meio do *lParam* da mensagem de [**\_ criação do WM**](../winmsg/wm-create.md) para esse controle.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-151">When a dialog is created, and a control in that dialog which has control-specific data is created, a pointer to that data is passed into the control's window procedure through the *lParam* of the [**WM\_CREATE**](../winmsg/wm-create.md) message for that control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2c2a-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2c2a-152">Remarks</span></span>

<span data-ttu-id="a2c2a-153">As unidades de caixa de diálogo horizontais são 1/4 da unidade de largura base da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-153">Horizontal dialog units are 1/4 of the dialog base width unit.</span></span> <span data-ttu-id="a2c2a-154">As unidades verticais são 1/8 da unidade de altura base da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-154">Vertical units are 1/8 of the dialog base height unit.</span></span> <span data-ttu-id="a2c2a-155">As unidades base da caixa de diálogo atual são computadas a partir da altura e da largura da fonte atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-155">The current dialog base units are computed from the height and width of the current system font.</span></span> <span data-ttu-id="a2c2a-156">A função [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retorna as unidades base da caixa de diálogo em pixels.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-156">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="a2c2a-157">As coordenadas são relativas à origem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a2c2a-157">The coordinates are relative to the origin of the dialog box.</span></span>

 

 