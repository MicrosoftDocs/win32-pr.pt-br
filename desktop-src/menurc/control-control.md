---
title: Controle de controle
description: Define um controle definido pelo usuário.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Menus de controle de controle e outros recursos
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917236"
---
# <a name="control-control"></a><span data-ttu-id="f4dd8-104">Controle de controle</span><span class="sxs-lookup"><span data-stu-id="f4dd8-104">CONTROL control</span></span>

<span data-ttu-id="f4dd8-105">Define um controle definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-105">Defines a user-defined control.</span></span>

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span data-ttu-id="f4dd8-106"><span id="class"></span><span id="CLASS"></span>*classes*</span><span class="sxs-lookup"><span data-stu-id="f4dd8-106"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="f4dd8-107">Nome redefinido, Cadeia de caracteres ou um valor inteiro sem sinal de 16 bits que define a classe.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-107">Redefined name, character string, or a 16-bit unsigned integer value that defines the class.</span></span> <span data-ttu-id="f4dd8-108">Pode ser qualquer uma das classes de controle; para obter uma lista das classes de controle, consulte a primeira lista após esta descrição.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-108">This can be any one of the control classes; for a list of the control classes, see the first list following this description.</span></span> <span data-ttu-id="f4dd8-109">Se o valor for um nome redefinido fornecido pelo aplicativo, ele deverá ser uma cadeia de caracteres entre aspas duplas (").</span><span class="sxs-lookup"><span data-stu-id="f4dd8-109">If the value is a redefined name supplied by the application, it must be a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="f4dd8-110"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="f4dd8-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="f4dd8-111">Nome redefinido ou valor inteiro que especifica o estilo do controle fornecido.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-111">Redefined name or integer value that specifies the style of the given control.</span></span> <span data-ttu-id="f4dd8-112">O significado exato do *estilo* depende do valor da *classe* .</span><span class="sxs-lookup"><span data-stu-id="f4dd8-112">The exact meaning of *style* depends on the *class* value.</span></span> <span data-ttu-id="f4dd8-113">As seções que seguem esta descrição mostram as classes de controle e os estilos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-113">The sections following this description show the control classes and corresponding styles.</span></span>

</dd> </dl>

<span data-ttu-id="f4dd8-114">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4dd8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4dd8-115">Remarks</span></span>

<span data-ttu-id="f4dd8-116">As seis classes de controle possíveis são descritas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-116">The six possible control classes are described in the following sections.</span></span>

### <a name="the-button-control-class"></a><span data-ttu-id="f4dd8-117">A classe de controle Button</span><span class="sxs-lookup"><span data-stu-id="f4dd8-117">The Button Control Class</span></span>

<span data-ttu-id="f4dd8-118">Um controle de botão é uma pequena janela filho retangular que o usuário pode ativar ou desativar clicando com o mouse.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-118">A button control is a small rectangular child window that the user can turn on or off by clicking it with the mouse.</span></span> <span data-ttu-id="f4dd8-119">Os controles de botão podem ser usados sozinhos ou em grupos e podem ser rotulados ou exibidos sem texto.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-119">Button controls can be used alone or in groups, and can either be labeled or appear without text.</span></span> <span data-ttu-id="f4dd8-120">Controles de botão normalmente alteram a aparência quando o usuário clica neles.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-120">Button controls typically change appearance when the user clicks them.</span></span>

<span data-ttu-id="f4dd8-121">Os estilos de botão são descritos no tópico a seguir: [estilos de botão](../controls/button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-121">The button styles are described in the following topic: [Button Styles](../controls/button-styles.md).</span></span>

### <a name="the-combo-box-control-class"></a><span data-ttu-id="f4dd8-122">A classe de controle da caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="f4dd8-122">The Combo Box Control Class</span></span>

<span data-ttu-id="f4dd8-123">Os controles de caixa de combinação consistem em um campo de seleção semelhante a um controle de edição, além de uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-123">Combo box controls consist of a selection field similar to an edit control plus a list box.</span></span> <span data-ttu-id="f4dd8-124">A caixa de listagem pode ser exibida sempre ou pode ser descartada quando o usuário seleciona uma "caixa pop" ao lado do campo de seleção.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-124">The list box may be displayed at all times or may be dropped down when the user selects a "pop box" next to the selection field.</span></span>

<span data-ttu-id="f4dd8-125">Dependendo do estilo da caixa de combinação, o usuário pode ou não editar o conteúdo do campo de seleção.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-125">Depending on the style of the combo box, the user can or cannot edit the contents of the selection field.</span></span> <span data-ttu-id="f4dd8-126">Se a caixa de listagem estiver visível, a digitação de caracteres na caixa de seleção fará com que a primeira entrada que corresponde aos caracteres digitados seja realçada.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-126">If the list box is visible, typing characters into the selection box will cause the first entry that matches the characters typed to be highlighted.</span></span> <span data-ttu-id="f4dd8-127">Por outro lado, a seleção de um item na caixa de listagem exibe o texto selecionado no campo seleção.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-127">Conversely, selecting an item in the list box displays the selected text in the selection field.</span></span>

<span data-ttu-id="f4dd8-128">Os estilos de controle de caixa de combinação são descritos no seguinte tópico: [estilos de caixa de combinação](../controls/combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-128">The combo box control styles are described in the following topic: [Combo Box Styles](../controls/combo-box-styles.md).</span></span>

### <a name="the-edit-control-class"></a><span data-ttu-id="f4dd8-129">A classe de controle de edição</span><span class="sxs-lookup"><span data-stu-id="f4dd8-129">The Edit Control Class</span></span>

<span data-ttu-id="f4dd8-130">Um controle de edição é uma janela filho retangular na qual o usuário pode inserir texto do teclado.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-130">An edit control is a rectangular child window in which the user can enter text from the keyboard.</span></span> <span data-ttu-id="f4dd8-131">O usuário seleciona o controle e dá a ele o foco de entrada, clicando no mouse dentro dele ou pressionando a tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-131">The user selects the control, and gives it the input focus, by clicking the mouse inside it or pressing the TAB key.</span></span> <span data-ttu-id="f4dd8-132">O usuário pode inserir texto quando o controle exibe um ponto de inserção piscando.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-132">The user can enter text when the control displays a flashing insertion point.</span></span> <span data-ttu-id="f4dd8-133">O mouse pode ser usado para mover o cursor e selecionar os caracteres a serem substituídos ou para posicionar o cursor para inserir caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-133">The mouse can be used to move the cursor and select characters to be replaced, or to position the cursor for inserting characters.</span></span> <span data-ttu-id="f4dd8-134">A tecla backspace pode ser usada para excluir caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-134">The BACKSPACE key can be used to delete characters.</span></span>

<span data-ttu-id="f4dd8-135">Os controles de edição usam a fonte de densidade fixa e exibem caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-135">Edit controls use the fixed-pitch font and display Unicode characters.</span></span> <span data-ttu-id="f4dd8-136">Eles expandem caracteres de tabulação em tantos caracteres de espaço quantos forem necessários para mover o cursor para a próxima parada de tabulação.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-136">They expand tab characters into as many space characters as are required to move the cursor to the next tab stop.</span></span> <span data-ttu-id="f4dd8-137">As paradas de tabulação são consideradas em cada oitavo posição de caractere.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-137">Tab stops are assumed to be at every eighth character position.</span></span>

<span data-ttu-id="f4dd8-138">Os estilos de controle de edição são descritos no tópico a seguir: [Editar estilos de controle](../controls/edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-138">The edit control styles are described in the following topic: [Edit Control Styles](../controls/edit-control-styles.md).</span></span>

### <a name="the-list-box-control-class"></a><span data-ttu-id="f4dd8-139">A classe de controle da caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="f4dd8-139">The List Box Control Class</span></span>

<span data-ttu-id="f4dd8-140">Os controles de caixa de listagem consistem em uma lista de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-140">List box controls consist of a list of character strings.</span></span> <span data-ttu-id="f4dd8-141">O controle é usado sempre que um aplicativo precisa apresentar uma lista de nomes, como nomes de File, que o usuário pode exibir e selecionar.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-141">The control is used whenever an application needs to present a list of names, such as filenames, that the user can view and select.</span></span> <span data-ttu-id="f4dd8-142">O usuário pode selecionar uma cadeia de caracteres apontando para a cadeia de caracteres com o mouse e clicando em um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-142">The user can select a string by pointing to the string with the mouse and clicking a mouse button.</span></span> <span data-ttu-id="f4dd8-143">Quando uma cadeia de caracteres é selecionada, ela é realçada e uma mensagem de notificação é passada para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-143">When a string is selected, it is highlighted and a notification message is passed to the parent window.</span></span> <span data-ttu-id="f4dd8-144">Uma barra de rolagem pode ser usada com um controle de caixa de listagem para rolar listas que são muito longas ou muito amplas para a janela de controle.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-144">A scroll bar can be used with a list box control to scroll lists that are too long or too wide for the control window.</span></span>

<span data-ttu-id="f4dd8-145">Os estilos de controle de caixa de listagem são descritos no seguinte tópico: [estilos de caixa de listagem](../controls/list-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-145">The list box control styles are described in the following topic: [List Box Styles](../controls/list-box-styles.md).</span></span>

### <a name="the-scroll-bar-control-class"></a><span data-ttu-id="f4dd8-146">A classe de controle Scroll-Bar</span><span class="sxs-lookup"><span data-stu-id="f4dd8-146">The Scroll-Bar Control Class</span></span>

<span data-ttu-id="f4dd8-147">Um controle de barra de rolagem é um retângulo que contém um Thumb de rolagem e tem setas de direção em ambas as extremidades.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-147">A scroll-bar control is a rectangle that contains a scroll thumb and has direction arrows at both ends.</span></span> <span data-ttu-id="f4dd8-148">A barra de rolagem envia uma mensagem de notificação para seu pai sempre que o usuário clica no controle.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-148">The scroll bar sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="f4dd8-149">O pai é responsável por atualizar a posição do Thumb, se necessário.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-149">The parent is responsible for updating the thumb position, if necessary.</span></span> <span data-ttu-id="f4dd8-150">Os controles de barra de rolagem têm a mesma aparência e função que as barras de rolagem usadas em janelas comuns.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-150">Scroll-bar controls have the same appearance and function as the scroll bars used in ordinary windows.</span></span> <span data-ttu-id="f4dd8-151">Mas, ao contrário das barras de rolagem, os controles de barra de rolagem podem ser posicionados em qualquer lugar em uma janela e usados sempre que necessário para fornecer a entrada de rolagem para uma janela.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-151">But unlike scroll bars, scroll-bar controls can be positioned anywhere within a window and used whenever needed to provide scrolling input for a window.</span></span>

<span data-ttu-id="f4dd8-152">Os estilos da barra de rolagem são descritos no seguinte tópico: [estilos de controle da barra de rolagem](../controls/scroll-bar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-152">The scroll bar styles are described in the following topic: [Scroll Bar Control Styles](../controls/scroll-bar-control-styles.md).</span></span>

### <a name="the-static-control-class"></a><span data-ttu-id="f4dd8-153">A classe de controle estático</span><span class="sxs-lookup"><span data-stu-id="f4dd8-153">The Static Control Class</span></span>

<span data-ttu-id="f4dd8-154">Os controles estáticos são campos de texto simples, caixas e retângulos que podem ser usados para rotular, caixar ou separar outros controles.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-154">Static controls are simple text fields, boxes, and rectangles that can be used to label, box, or separate other controls.</span></span> <span data-ttu-id="f4dd8-155">Os controles estáticos não utilizam nenhuma entrada e não fornecem nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f4dd8-155">Static controls take no input and provide no output.</span></span>

<span data-ttu-id="f4dd8-156">Os estilos de controle estáticos são descritos no seguinte tópico: [estilos de controle estático](../controls/static-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="f4dd8-156">The static control styles are described in the following topic: [Static Control Styles](../controls/static-control-styles.md).</span></span>

 

 