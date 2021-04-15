---
description: Este programa demonstra como copiar e colar a tinta em outro aplicativo. Ele também permite que o usuário Copie uma seleção de traços e cole o resultado no objeto de tinta existente.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Exemplo de área de transferência de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95c5da0bc0ba9a7e3a1b4e1a5c52784f10fb2023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501628"
---
# <a name="ink-clipboard-sample"></a><span data-ttu-id="7dc4c-104">Exemplo de área de transferência de tinta</span><span class="sxs-lookup"><span data-stu-id="7dc4c-104">Ink Clipboard Sample</span></span>

<span data-ttu-id="7dc4c-105">Este programa demonstra como copiar e colar a tinta em outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-105">This program demonstrates how to copy and paste ink into another application.</span></span> <span data-ttu-id="7dc4c-106">Ele também permite que o usuário Copie uma seleção de traços e cole o resultado no objeto de tinta existente.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-106">It also enables the user to copy a selection of strokes and paste the result into the existing ink object.</span></span>

<span data-ttu-id="7dc4c-107">Os seguintes modos de área de transferência estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="7dc4c-107">The following clipboard modes are available:</span></span>

-   <span data-ttu-id="7dc4c-108">Formato serializado da tinta (ISF)</span><span class="sxs-lookup"><span data-stu-id="7dc4c-108">Ink serialized format (ISF)</span></span>
-   <span data-ttu-id="7dc4c-109">Metarquivo</span><span class="sxs-lookup"><span data-stu-id="7dc4c-109">Metafile</span></span>
-   <span data-ttu-id="7dc4c-110">EMF (Metarquivo Avançado)</span><span class="sxs-lookup"><span data-stu-id="7dc4c-110">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="7dc4c-111">Bitmap</span><span class="sxs-lookup"><span data-stu-id="7dc4c-111">Bitmap</span></span>
-   <span data-ttu-id="7dc4c-112">Tinta do texto</span><span class="sxs-lookup"><span data-stu-id="7dc4c-112">Text Ink</span></span>
-   <span data-ttu-id="7dc4c-113">Tinta do esboço</span><span class="sxs-lookup"><span data-stu-id="7dc4c-113">Sketch Ink</span></span>

<span data-ttu-id="7dc4c-114">A tinta do texto e a tinta do esboço são dois tipos de controles de tinta usados como texto ou desenho, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-114">Text ink and sketch ink are two types of ink controls used as text or drawing respectively.</span></span> <span data-ttu-id="7dc4c-115">É possível colar ISF, tinta de texto e esboço de tinta em tinta existente.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-115">It is possible to paste ISF, text ink, and sketch ink into existing ink.</span></span>

<span data-ttu-id="7dc4c-116">Além da área de transferência, este exemplo também ilustra como selecionar traços com a ferramenta de laço.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-116">In addition to the clipboard, this sample also illustrates how to select strokes with the lasso tool.</span></span> <span data-ttu-id="7dc4c-117">O usuário pode mover os traços selecionados e modificar seus atributos de desenho.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-117">The user can move selected strokes and modify their drawing attributes.</span></span> <span data-ttu-id="7dc4c-118">Essa funcionalidade é um subconjunto da funcionalidade de seleção já fornecida pelo controle de sobreposição de tinta; Ele é implementado aqui para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-118">This functionality is a subset of the selection functionality already provided by the ink overlay control; it is implemented here for illustrative purposes.</span></span>

<span data-ttu-id="7dc4c-119">Os recursos a seguir são usados neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="7dc4c-119">The following features are used in this sample:</span></span>

-   <span data-ttu-id="7dc4c-120">O objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="7dc4c-120">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>
-   <span data-ttu-id="7dc4c-121">Suporte à área de transferência de tinta.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-121">Ink clipboard support.</span></span>
-   <span data-ttu-id="7dc4c-122">O uso do laço com o método [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) .</span><span class="sxs-lookup"><span data-stu-id="7dc4c-122">The use of the lasso with the [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method.</span></span>

<span data-ttu-id="7dc4c-123">Este exemplo demonstra o processamento de tinta, a cópia dessa tinta e a colagem da tinta em outro aplicativo, como o Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-123">This sample demonstrates rendering ink, copying that ink, and then pasting the ink into another application such as Microsoft Paint.</span></span>

## <a name="collecting-ink-and-setting-up-the-form"></a><span data-ttu-id="7dc4c-124">Coletando tinta e Configurando o formulário</span><span class="sxs-lookup"><span data-stu-id="7dc4c-124">Collecting Ink and Setting Up the Form</span></span>

<span data-ttu-id="7dc4c-125">Primeiro, faça referência às interfaces de automação do Tablet PC, que são instaladas com o <entity type="reg"/> SDK (Software Development Kit) do Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-125">First, reference the Tablet PC Automation interfaces, which are installed with the Microsoft Windows<entity type="reg"/> XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="7dc4c-126">Em seguida, o formulário declara algumas constantes e os campos que são observados posteriormente neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-126">Next, the form declares some constants and fields that are noted later in this sample.</span></span>


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



<span data-ttu-id="7dc4c-127">Por fim, no manipulador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário, o formulário é inicializado, um objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para o formulário é criado e o coletor de tinta está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-127">Finally, in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler, the form is initialized, an [InkCollector](/previous-versions/ms583683(v=vs.100)) object for the form is created and the ink collector is enabled.</span></span>


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a><span data-ttu-id="7dc4c-128">Manipulando eventos de menu</span><span class="sxs-lookup"><span data-stu-id="7dc4c-128">Handling Menu Events</span></span>

<span data-ttu-id="7dc4c-129">Os manipuladores de eventos do item de menu atualizam principalmente o estado do formulário.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-129">The menu item event handlers primarily update the form's state.</span></span>

<span data-ttu-id="7dc4c-130">O comando limpar remove o retângulo de seleção e exclui os traços do objeto de [tinta](/previous-versions/ms583670(v=vs.100)) do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-130">The Clear command removes the selection rectangle, and deletes the strokes from the ink collector's [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span>

<span data-ttu-id="7dc4c-131">O comando exit desabilita o coletor de tinta antes de sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-131">The Exit command disables the ink collector before exiting the application.</span></span>

<span data-ttu-id="7dc4c-132">O menu Editar habilita os comandos Recortar e copiar com base no estado de seleção do formulário e habilita o comando colar com base no conteúdo da área de transferência, determinado usando o método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) do objeto [Ink](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="7dc4c-132">The Edit menu enables the Cut and Copy commands based on the selection state of the form, and enables the Paste command based on the contents of the clipboard, determined by using the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method.</span></span>

<span data-ttu-id="7dc4c-133">Os comandos Recortar e copiar usam um método auxiliar para copiar tinta para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-133">The Cut and Copy commands both use a helper method to copy ink to the clipboard.</span></span> <span data-ttu-id="7dc4c-134">O comando Recortar usa um método auxiliar para excluir os traços selecionados.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-134">The Cut command uses a helper method to delete the selected strokes.</span></span>

<span data-ttu-id="7dc4c-135">O comando Paste primeiro verifica o método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) do objeto [Ink](/previous-versions/ms583670(v=vs.100)) para ver se o objeto na área de transferência pode ser colado.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-135">The Paste command first checks the [Ink](/previous-versions/ms583670(v=vs.100)) object's [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) method to see if the object on the clipboard can be pasted.</span></span> <span data-ttu-id="7dc4c-136">Em seguida, o comando Paste computa o canto superior esquerdo para a região de colagem, converte as coordenadas de pixels em espaço de tinta e cola os traços da área de transferência para o coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-136">The Paste command then computes the upper-left corner for the paste region, converts the coordinates from pixels to ink space, and pastes the strokes from the clipboard to the ink collector.</span></span> <span data-ttu-id="7dc4c-137">Por fim, a caixa de seleção é atualizada.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-137">Finally, the selection box is updated.</span></span>


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



<span data-ttu-id="7dc4c-138">Os comandos SELECT e Ink atualizam o modo do aplicativo e os atributos de desenho padrão, desmarcam a seleção atual, atualizam o estado do menu e atualizam o formulário.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-138">The Select and Ink commands update the application mode and the default drawing attributes, clear the current selection, update the menu state, and refresh the form.</span></span> <span data-ttu-id="7dc4c-139">Outros manipuladores dependem do estado do aplicativo para executar a função correta, a laço ou o layout da tinta.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-139">Other handlers rely on the application state to perform the correct function, either lassoing or laying down ink.</span></span> <span data-ttu-id="7dc4c-140">Além disso, o comando SELECT adiciona os manipuladores de eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) e [Stroke](/previous-versions/ms567622(v=vs.100)) ao coletor de tinta e o comando Ink remove esses manipuladores de eventos do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-140">In addition, the Select command adds the [NewPackets](/previous-versions/ms567621(v=vs.100)) and [Stroke](/previous-versions/ms567622(v=vs.100)) event handlers to the ink collector and the Ink command removes these event handlers from the ink collector.</span></span>

<span data-ttu-id="7dc4c-141">Os formatos disponíveis na área de transferência quando os traços são copiados estão listados no menu Formatar e o usuário seleciona o formato para copiar a tinta dessa lista.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-141">The formats that are available on the Clipboard when strokes are copied are listed on the Format menu, and the user selects the format for copying the ink from this list.</span></span> <span data-ttu-id="7dc4c-142">Os tipos de formatos disponíveis incluem ISF (Ink serializado Format), Metafile, metarquivo avançado e bitmap.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-142">The types of formats available include Ink Serialized Format (ISF), metafile, enhanced metafile, and bitmap.</span></span> <span data-ttu-id="7dc4c-143">Os formatos de tinta de esboço e de tinta de texto são mutuamente exclusivos e contam com a tinta que está sendo copiada para a área de transferência como um objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-143">The sketch ink and text ink formats are mutually exclusive, and rely on the ink being copied to the clipboard as an OLE object.</span></span>

<span data-ttu-id="7dc4c-144">O menu estilo permite que o usuário altere as propriedades de cor e largura da caneta e de quaisquer traços selecionados.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-144">The Style menu enables the user to change the color and width properties of the pen and any selected strokes.</span></span>

<span data-ttu-id="7dc4c-145">Por exemplo, o comando vermelho define a propriedade [Color](/previous-versions/ms582103(v=vs.100)) da propriedade [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) do coletor de tinta para a cor vermelha.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-145">For example, the Red command sets the [Color](/previous-versions/ms582103(v=vs.100)) property of the ink collector's [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) property to the color red.</span></span> <span data-ttu-id="7dc4c-146">Como a propriedade [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) do objeto [cursor](/previous-versions/ms552104(v=vs.100)) não foi definida, qualquer nova tinta desenhada para o coletor de tinta é herdada para a cor de desenho padrão.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-146">Because the [DrawingAttributes](/previous-versions/ms581965(v=vs.100)) property of the [Cursor](/previous-versions/ms552104(v=vs.100)) object has not been set, any new ink drawn to the ink collector inherits to default drawing color.</span></span> <span data-ttu-id="7dc4c-147">Além disso, se qualquer traço estiver selecionado no momento, a propriedade de cor dos atributos de desenho de cada traço também será atualizada.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-147">Also, if any strokes are currently selected, each stroke's drawing attributes Color property is updated as well.</span></span>


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a><span data-ttu-id="7dc4c-148">Manipulando eventos do mouse</span><span class="sxs-lookup"><span data-stu-id="7dc4c-148">Handling Mouse Events</span></span>

<span data-ttu-id="7dc4c-149">O manipulador de eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) verifica o modo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-149">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="7dc4c-150">Se o modo for MoveInk e um botão do mouse estiver inativo, o manipulador moverá os traços usando o método move da coleção [Strokes](/previous-versions/ms552701(v=vs.100)) e atualizará a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-150">If the mode is MoveInk and a mouse button is down, then the handler moves the strokes by using the [Strokes](/previous-versions/ms552701(v=vs.100)) collection's Move method and updates the selection box.</span></span> <span data-ttu-id="7dc4c-151">Caso contrário, o manipulador verifica para determinar se o retângulo de seleção contém o cursor, habilita a coleta de tinta de forma adequada e também define o cursor de acordo.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-151">Otherwise, the handler checks to determine whether the selection rectangle contains the cursor, enables ink collection accordingly, and also sets the cursor accordingly.</span></span>

<span data-ttu-id="7dc4c-152">O manipulador de eventos [MouseDown](/previous-versions/ms567616(v=vs.100)) verifica a configuração do cursor.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-152">The [MouseDown](/previous-versions/ms567616(v=vs.100)) event handler checks the cursor setting.</span></span> <span data-ttu-id="7dc4c-153">Se o cursor for definido como [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), o manipulador definirá o modo de aplicativo como MoveInk e registrará o local do cursor.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-153">If the cursor is set to [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), then the handler sets the application mode to MoveInk and records the cursor location.</span></span> <span data-ttu-id="7dc4c-154">Caso contrário, se houver uma seleção atual, desmarque-a.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-154">Otherwise, if there is a current selection, clear it.</span></span>

<span data-ttu-id="7dc4c-155">O manipulador de eventos [MouseUp](/previous-versions/ms567618(v=vs.100)) verifica o modo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-155">The [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler checks the application mode.</span></span> <span data-ttu-id="7dc4c-156">Se o modo for MoveInk, o manipulador definirá o modo de aplicativo com base no estado selecionado do comando SELECT.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-156">If the mode is MoveInk, then the handler sets the application mode based on the Select command's checked state.</span></span>

<span data-ttu-id="7dc4c-157">O evento [NewPackets](/previous-versions/ms567621(v=vs.100)) é gerado no modo de seleção quando o coletor de tinta recebe novos dados de pacote.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-157">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised in selection mode when the ink collector receives new packet data.</span></span> <span data-ttu-id="7dc4c-158">Se o aplicativo estiver no modo de seleção, será necessário interceptar os novos pacotes e usá-los para desenhar o laço de seleção.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-158">If the application is in selection mode, it is necessary to intercept the new packets and use them to draw the selection lasso.</span></span>

<span data-ttu-id="7dc4c-159">A coordenada de cada pacote é convertida em pixels, restrita à área de desenho e adicionada à coleção de pontos do laço.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-159">Each packet's coordinate is converted to pixels, constrained to the drawing area, and added to the lasso's collection of points.</span></span> <span data-ttu-id="7dc4c-160">Um método auxiliar é chamado para desenhar o laço no formulário.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-160">A helper method is then called to draw the lasso on the form.</span></span>

## <a name="handling-a-new-stroke"></a><span data-ttu-id="7dc4c-161">Manipulando um novo traço</span><span class="sxs-lookup"><span data-stu-id="7dc4c-161">Handling a New Stroke</span></span>

<span data-ttu-id="7dc4c-162">O evento [Stroke](/previous-versions/ms567622(v=vs.100)) é gerado no modo de seleção quando um novo traço é desenhado.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-162">The [Stroke](/previous-versions/ms567622(v=vs.100)) event is raised in the selection mode when a new stroke is drawn.</span></span> <span data-ttu-id="7dc4c-163">Se o aplicativo estiver no modo de seleção, esse traço corresponderá ao laço e será necessário atualizar as informações dos traços selecionados.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-163">If the application is in selection mode, this stroke corresponds to the lasso and it is necessary to update the selected strokes' information.</span></span>

<span data-ttu-id="7dc4c-164">O manipulador cancela o evento de [traço](/previous-versions/ms567622(v=vs.100)) , verifica se há mais de dois pontos de laço, copia a coleção de pontos em uma matriz de objetos [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) e converte as coordenadas dos pontos na matriz de pixels para o espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-164">The handler cancels the [Stroke](/previous-versions/ms567622(v=vs.100)) event, checks for more than two lasso points, copies the Points collection to an array of [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) objects, and converts the coordinates of the points in the array from pixels to ink space.</span></span> <span data-ttu-id="7dc4c-165">Em seguida, o manipulador usa o método [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) do objeto [Ink](/previous-versions/ms583670(v=vs.100)) para obter os traços selecionados pelos pontos do laço e atualiza o estado de seleção do formulário.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-165">Then, the handler uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to get the strokes selected by the lasso points and updates the selection state of the form.</span></span> <span data-ttu-id="7dc4c-166">Por fim, o traço que disparou o evento é removido da coleção de traços selecionados, a coleção de pontos de laço é esvaziada e um método auxiliar desenha o retângulo de seleção.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-166">Finally, the stroke that raised the event is removed from the collection of selected strokes, the lasso Points collection is emptied, and a helper method draws the selection rectangle.</span></span>


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a><span data-ttu-id="7dc4c-167">Copiando tinta para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="7dc4c-167">Copying Ink to the Clipboard</span></span>

<span data-ttu-id="7dc4c-168">O método auxiliar CopyInkToClipboard cria um valor de [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) , verifica o estado do menu de formato para atualizar os formatos a serem colocados na área de transferência e usa o método [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) do objeto [Ink](/previous-versions/ms583670(v=vs.100)) para copiar os traços para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-168">The CopyInkToClipboard helper method creates an [InkClipboardFormats](/previous-versions/ms583681(v=vs.100)) value, checks the Format menu's state to update the formats to put on the clipboard, and uses the [Ink](/previous-versions/ms583670(v=vs.100)) object's [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) method to copy the strokes to the clipboard.</span></span>


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a><span data-ttu-id="7dc4c-169">Atualizando uma seleção</span><span class="sxs-lookup"><span data-stu-id="7dc4c-169">Updating a Selection</span></span>

<span data-ttu-id="7dc4c-170">O método auxiliar SetSelection atualiza o selectedStrokes arquivado e, se a coleção for **nula** ou **vazia**, o retângulo de seleção será definido como o retângulo vazio.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-170">The SetSelection helper method updates the selectedStrokes filed and if the collection is **NULL** or **EMPTY**, the selection rectangle is set to the empty rectangle.</span></span> <span data-ttu-id="7dc4c-171">Se a coleção [Strokes](/previous-versions/ms552701(v=vs.100)) selecionada não estiver vazia, o método setseleções executará as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="7dc4c-171">If the selected [Strokes](/previous-versions/ms552701(v=vs.100)) collection is not empty the SetSelection method performs the following steps:</span></span>

-   <span data-ttu-id="7dc4c-172">Determina o retângulo delimitador usando o método [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) da coleção Strokes</span><span class="sxs-lookup"><span data-stu-id="7dc4c-172">Determines the bounding rectangle by using the [GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) method of the strokes collection</span></span>
-   <span data-ttu-id="7dc4c-173">Converte as coordenadas de retângulo do espaço de tinta em pixels</span><span class="sxs-lookup"><span data-stu-id="7dc4c-173">Converts the rectangle coordinates from ink space to pixels</span></span>
-   <span data-ttu-id="7dc4c-174">Replana o retângulo para fornecer algum espaço visual entre ele e os traços selecionados</span><span class="sxs-lookup"><span data-stu-id="7dc4c-174">Inflates the rectangle to provide some visual space between it and the selected strokes</span></span>
-   <span data-ttu-id="7dc4c-175">Cria identificadores de seleção para a caixa de seleção atual</span><span class="sxs-lookup"><span data-stu-id="7dc4c-175">Creates selection handles for the current selection box</span></span>

<span data-ttu-id="7dc4c-176">Finalmente, o método setselecting define a visibilidade das alças de seleção e define a propriedade [redesenhar](/previous-versions/ms571706(v=vs.100)) do coletor de tinta como **false**, se os traços estiverem selecionados.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-176">Finally, the SetSelection method sets the visibility of the selection handles and sets the ink collector's [AutoRedraw](/previous-versions/ms571706(v=vs.100)) property to **FALSE**, if strokes are selected.</span></span>


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a><span data-ttu-id="7dc4c-177">Desenhando o laço</span><span class="sxs-lookup"><span data-stu-id="7dc4c-177">Drawing the Lasso</span></span>

<span data-ttu-id="7dc4c-178">O laço é desenhado como uma série de pontos abertos que seguem o caminho do traço do laço e uma linha de conector tracejada entre as duas extremidades.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-178">The lasso is drawn as a series of open dots that follow the path of the lasso stroke and a dashed connector line between the two ends.</span></span> <span data-ttu-id="7dc4c-179">O evento [NewPackets](/previous-versions/ms567621(v=vs.100)) é gerado como o laço está sendo desenhado e o manipulador de eventos passa as informações de traço para o método DrawLasso.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-179">The [NewPackets](/previous-versions/ms567621(v=vs.100)) event is raised as the lasso is being drawn, and the event handler passes the stroke information to the DrawLasso method.</span></span>

<span data-ttu-id="7dc4c-180">O método auxiliar DrawLasso primeiro remove a linha do conector antigo e, em seguida, itera nos pontos no traço.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-180">The DrawLasso helper method first removes the old connector line and then iterates over the points in the stroke.</span></span> <span data-ttu-id="7dc4c-181">Em seguida, DrawLasso calcula onde posicionar os pontos ao longo do traço e os desenha.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-181">Then, DrawLasso calculates where to place the dots along the stroke and draws them.</span></span> <span data-ttu-id="7dc4c-182">Por fim, ele desenha uma nova linha de conector.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-182">Finally, it draws a new connector line.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="7dc4c-183">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="7dc4c-183">Closing the Form</span></span>

<span data-ttu-id="7dc4c-184">O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) , myinkcollector.</span><span class="sxs-lookup"><span data-stu-id="7dc4c-184">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object, myInkCollector.</span></span>

 

 
