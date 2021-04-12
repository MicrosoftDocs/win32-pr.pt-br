---
description: O exemplo de declarações automáticas aborda um cenário hipotético de um assessor de seguros.
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: Exemplo de formulário de declarações automáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5ff78a3c38036ef9352660b4d7959e2ad87e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297027"
---
# <a name="auto-claims-form-sample"></a><span data-ttu-id="df6a7-103">Exemplo de formulário de declarações automáticas</span><span class="sxs-lookup"><span data-stu-id="df6a7-103">Auto Claims Form Sample</span></span>

<span data-ttu-id="df6a7-104">O exemplo de declarações automáticas aborda um cenário hipotético de um assessor de seguros.</span><span class="sxs-lookup"><span data-stu-id="df6a7-104">The Auto Claims sample addresses a hypothetical scenario for an insurance assessor.</span></span> <span data-ttu-id="df6a7-105">O trabalho do assessor exige que ele visite os clientes em sua residência ou empresa e insira suas informações de declaração em um formulário.</span><span class="sxs-lookup"><span data-stu-id="df6a7-105">The assessor's work requires him or her to visit with clients at their home or business and to enter their claim information into a form.</span></span> <span data-ttu-id="df6a7-106">Para aumentar a produtividade do assessor, seu departamento de ti desenvolve um aplicativo de Tablet que permite que ele Insira informações de declaração com rapidez e precisão por meio de dois controles de tinta: os controles [InkEdit](/previous-versions/ms835842(v=msdn.10)) e [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="df6a7-106">To increase the assessor's productivity, his IT department develops a tablet application that enables him or her to quickly and accurately enter claim information through two ink controls: [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls.</span></span>

<span data-ttu-id="df6a7-107">Neste exemplo, um controle [InkEdit](/previous-versions/ms835842(v=msdn.10)) é usado para cada campo de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="df6a7-107">In this sample, a [InkEdit](/previous-versions/ms835842(v=msdn.10)) control is used for each text input field.</span></span> <span data-ttu-id="df6a7-108">Um usuário insere as informações relevantes sobre uma apólice de seguro e veículo nesses campos com uma caneta.</span><span class="sxs-lookup"><span data-stu-id="df6a7-108">A user enters the relevant information about an insurance policy and vehicle into these fields with a pen.</span></span> <span data-ttu-id="df6a7-109">O controle [InkPicture](/previous-versions/ms583740(v=vs.100)) é usado para adicionar tinta em uma imagem do automóvel para realçar áreas danificadas do automóvel.</span><span class="sxs-lookup"><span data-stu-id="df6a7-109">The [InkPicture](/previous-versions/ms583740(v=vs.100)) control is used to add ink over an automobile image to highlight damaged areas of the automobile.</span></span> <span data-ttu-id="df6a7-110">O exemplo de declarações automáticas está disponível para \# o C e o Microsoft Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="df6a7-110">The Auto Claims sample is available for C\# and Microsoft Visual Basic .NET.</span></span> <span data-ttu-id="df6a7-111">Este tópico descreve o Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="df6a7-111">This topic describes the Visual Basic .NET.</span></span>

<span data-ttu-id="df6a7-112">A classe autodeclarations é definida como uma subclasse de [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , e uma classe aninhada é definida para criar e gerenciar camadas de tinta para diferentes tipos de danos.</span><span class="sxs-lookup"><span data-stu-id="df6a7-112">The AutoClaims Class is defined as a subclass of [System.Windows.Forms.Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , and a nested class is defined for creating and managing layers of ink for different types of damage.</span></span> <span data-ttu-id="df6a7-113">Quatro manipuladores de eventos são definidos para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="df6a7-113">Four event handlers are defined to perform the following tasks:</span></span>

-   <span data-ttu-id="df6a7-114">Inicializando as camadas de formulário e de tinta.</span><span class="sxs-lookup"><span data-stu-id="df6a7-114">Initializing the form and ink layers.</span></span>
-   <span data-ttu-id="df6a7-115">Redesenhando o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="df6a7-115">Redrawing the [InkPicture](/previous-versions/ms583740(v=vs.100)) control.</span></span>
-   <span data-ttu-id="df6a7-116">Selecionando uma camada de tinta na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="df6a7-116">Selecting an ink layer through the list box.</span></span>
-   <span data-ttu-id="df6a7-117">Alterando a visibilidade de uma camada de tinta.</span><span class="sxs-lookup"><span data-stu-id="df6a7-117">Changing the visibility of an ink layer.</span></span>

> [!Note]  
> <span data-ttu-id="df6a7-118">As versões deste exemplo estão disponíveis em C \# e Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="df6a7-118">Versions of this sample are available in C\# and Visual Basic .NET.</span></span> <span data-ttu-id="df6a7-119">A versão discutida nesta seção é Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="df6a7-119">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="df6a7-120">Os conceitos são os mesmos entre as versões.</span><span class="sxs-lookup"><span data-stu-id="df6a7-120">The concepts are the same between versions.</span></span>

 

## <a name="defining-the-form-and-ink-layers"></a><span data-ttu-id="df6a7-121">Definindo as camadas de formulário e de tinta</span><span class="sxs-lookup"><span data-stu-id="df6a7-121">Defining the Form and Ink Layers</span></span>

<span data-ttu-id="df6a7-122">Você precisa importar o namespace [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="df6a7-122">You need to import the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace:</span></span>


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



<span data-ttu-id="df6a7-123">Em seguida, na classe autodeclarations, uma classe aninhada `InkLayer` é definida e uma matriz de quatro `InkLayer` objetos é declarada.</span><span class="sxs-lookup"><span data-stu-id="df6a7-123">Next, in the AutoClaims Class, a nested `InkLayer` class is defined and an array of four `InkLayer` objects is declared.</span></span> <span data-ttu-id="df6a7-124">(InkLayer contém um objeto [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) para armazenar a tinta e valores de [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) e **booliano** para armazenar a cor e o estado oculto da camada.) Um quinto objeto Ink é declarado para lidar com a tinta para o [InkPicture](/previous-versions/ms583740(v=vs.100)) quando todas as camadas de tinta estiverem ocultas.</span><span class="sxs-lookup"><span data-stu-id="df6a7-124">(InkLayer contains an [Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100)) object for storing ink, and [System.Drawing.Color](/dotnet/api/system.drawing.color?view=netcore-3.1) and **Boolean** values for storing the color and hidden state of the layer.) A fifth Ink object is declared to handle ink for the [InkPicture](/previous-versions/ms583740(v=vs.100)) when all of the ink layers are hidden.</span></span>


```VB
' Declare the array of ink layers used the vehicle illustration.
Dim inkLayers(3) As InkLayer

' Declare an empty ink object (used when we don't want to draw
' any ink).
Dim emptyInk As Ink

' Declare a value to hold the index of selected ink
Dim selectedIndex As Integer

' Declare a value to hold whether the selected ink is hidden
Dim selectedHidden As Boolean 
```




```VB
// Declare the array of ink layers used the vehicle illustration.
InkLayer[] inkLayers;

// Declare an empty ink object (used when we don't want to draw
// any ink).
Ink emptyInk;

// Declare a value to hold the index of selected ink
int selectedIndex = -1;

// Declare a value to hold whether the selected ink is hidden
bool selectedHidden = false;
```



<span data-ttu-id="df6a7-125">Cada camada tem seu próprio objeto de [tinta](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="df6a7-125">Each layer has its own [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span> <span data-ttu-id="df6a7-126">Há quatro áreas discretas de interesse no formulário de declaração (corpo, Windows, pneus e faróis), de modo que quatro objetos InkLayer são usados.</span><span class="sxs-lookup"><span data-stu-id="df6a7-126">There are four discrete areas of interest in the claim form (body, windows, tires, and headlights), so four InkLayer objects are used.</span></span> <span data-ttu-id="df6a7-127">Um usuário pode exibir qualquer combinação de camadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="df6a7-127">A user can view any combination of layers at once.</span></span>

## <a name="initializing-the-form-and-ink-layers"></a><span data-ttu-id="df6a7-128">Inicializando o formulário e as camadas de tinta</span><span class="sxs-lookup"><span data-stu-id="df6a7-128">Initializing the Form and Ink Layers</span></span>

<span data-ttu-id="df6a7-129">O `Load` manipulador de eventos Inicializa o objeto de [tinta](/previous-versions/ms583670(v=vs.100)) e os quatro `InkLayer` objetos.</span><span class="sxs-lookup"><span data-stu-id="df6a7-129">The `Load` event handler initializes the [Ink](/previous-versions/ms583670(v=vs.100)) object and the four `InkLayer` objects.</span></span>


```VB
' Initialize the empty ink
emptyInk = New Ink()

' Initialize the four different layers of ink on the vehicle diagram:  
' vehicle body, windows, tires, and headlights.
inkLayers(0) = New InkLayer(New Ink(), Color.Red, False)
inkLayers(1) = New InkLayer(New Ink(), Color.Violet, False)
inkLayers(2) = New InkLayer(New Ink(), Color.LightGreen, False)
inkLayers(3) = New InkLayer(New Ink(), Color.Aqua, False)
```




```VB
// Initialize the empty ink
emptyInk = new Ink();

// Initialize the four different layers of ink on the vehicle diagram:  
// vehicle body, windows, tires, and headlights.
inkLayers = new InkLayer[4];
inkLayers[0] = new InkLayer(new Ink(), Color.Red, false);
inkLayers[1] = new InkLayer(new Ink(), Color.Violet, false);
inkLayers[2] = new InkLayer(new Ink(), Color.LightGreen, false);
inkLayers[3] = new InkLayer(new Ink(), Color.Aqua, false);
```



<span data-ttu-id="df6a7-130">Em seguida, selecione a primeira entrada (corpo) na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="df6a7-130">Then, select the first entry (Body) in the list box.</span></span>


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



<span data-ttu-id="df6a7-131">Por fim, defina a cor da tinta para o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) para a entrada da caixa de listagem selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="df6a7-131">Finally, set the ink color for the [InkPicture](/previous-versions/ms583740(v=vs.100)) control to the currently selected list box entry.</span></span>


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a><span data-ttu-id="df6a7-132">Redesenhando o controle InkPicture</span><span class="sxs-lookup"><span data-stu-id="df6a7-132">Redrawing the InkPicture Control</span></span>

<span data-ttu-id="df6a7-133">No manipulador de eventos de [pintura](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) herdado do controle [InkPicture](/previous-versions/ms583740(v=vs.100)) , as camadas de tinta são verificadas para determinar quais estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="df6a7-133">In the [InkPicture](/previous-versions/ms583740(v=vs.100)) Control's inherited [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event handler, the ink layers are checked to determine which are hidden.</span></span> <span data-ttu-id="df6a7-134">Se uma camada não estiver oculta, o procedimento de evento a exibirá usando o método [draw](/previous-versions/ms828488(v=msdn.10)) da propriedade [Renderer](/previous-versions/ms582196(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="df6a7-134">If a layer is not hidden, the event procedure displays it by using the [Renderer](/previous-versions/ms582196(v=vs.100)) property's [Draw](/previous-versions/ms828488(v=msdn.10)) method.</span></span> <span data-ttu-id="df6a7-135">Se você examinar o pesquisador de objetos, verá que a propriedade Microsoft. Ink. InkPicture. Renderer é definida como um objeto [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="df6a7-135">If you look in the Object Browser, you'll see that the Microsoft.Ink.InkPicture.Renderer property is defined as a [Microsoft.Ink.Renderer](/previous-versions/ms828481(v=msdn.10)) object:</span></span>


```VB
Private Sub inkPictVehicle_Paint(ByVal sender As System.Object, ByVal e As System.Windows.Forms.PaintEventArgs) Handles inkPictVehicle.Paint
    Dim layer As InkLayer

    ' Cycle through each ink layer.  If it is visible, paint it.
    ' Note that it is necessary to customize the paint
    ' behavior, since we want to hide/show different ink layers.
    For Each layer In inkLayers
        If (Not layer.Hidden) Then
            inkPictVehicle.Renderer.Draw(e.Graphics, layer.ActiveInk.Strokes)
        End If
    Next
End Sub
```




```VB
private void inkPictVehicle_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    // Cycle through each ink layer.  If it is visible, paint it.
    // Note that it is necessary to customize the paint
    // behavior, since we want to hide/show different ink layers.
    foreach (InkLayer layer in inkLayers)
    {
        if (!layer.Hidden)
        {
             inkPictVehicle.Renderer.Draw(e.Graphics,layer.ActiveInk.Strokes);
        }
    }          
}
```



## <a name="selecting-an-ink-layer-through-the-list-box"></a><span data-ttu-id="df6a7-136">Selecionando uma camada de tinta na caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="df6a7-136">Selecting an Ink Layer through the List Box</span></span>

<span data-ttu-id="df6a7-137">Quando o usuário seleciona um item na caixa de listagem, o manipulador de eventos [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) primeiro verifica se a seleção foi alterada e se o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) não está coletando tinta no momento.</span><span class="sxs-lookup"><span data-stu-id="df6a7-137">When the user selects an item in the list box, the [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="df6a7-138">Em seguida, ele define a cor da tinta do controle InkPicture como a cor apropriada para a camada de tinta selecionada.</span><span class="sxs-lookup"><span data-stu-id="df6a7-138">It then sets the ink color of the InkPicture control to the appropriate color for the selected ink layer.</span></span> <span data-ttu-id="df6a7-139">Além disso, ele atualiza a caixa de seleção Ocultar camada para refletir o status oculto da camada de tinta selecionada.</span><span class="sxs-lookup"><span data-stu-id="df6a7-139">Also, it updates the Hide Layer check box to reflect the selected ink layer's hidden status.</span></span> <span data-ttu-id="df6a7-140">Por fim, o método de [atualização](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) herdado do controle InkPicture é usado para exibir apenas as camadas desejadas dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="df6a7-140">Finally, the InkPicture control's inherited [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
       Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
       End If
   End If
End Sub
```




```VB
private void lstAnnotationLayer_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Provided that the new selected index value is different than
    // the previous value...
    if (lstAnnotationLayer.SelectedIndex != selectedIndex) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Set the ink and visiblity of the current ink layer
            inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
            chHideLayer.Checked = inkLayers[lstAnnotationLayer.SelectedIndex].Hidden;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;
    
            selectedIndex = lstAnnotationLayer.SelectedIndex;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the selection to its previous value.
            lstAnnotationLayer.SelectedIndex = selectedIndex;
            MessageBox.Show("Cannot change active ink while collecting ink.");
        }
    }
}
```



## <a name="changing-the-visibility-of-an-ink-layer"></a><span data-ttu-id="df6a7-141">Alterando a visibilidade de uma camada de tinta</span><span class="sxs-lookup"><span data-stu-id="df6a7-141">Changing the Visibility of an Ink Layer</span></span>

<span data-ttu-id="df6a7-142">O `CheckedChanged` manipulador de eventos primeiro verifica se a seleção foi alterada e se o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) não está coletando tinta no momento.</span><span class="sxs-lookup"><span data-stu-id="df6a7-142">The `CheckedChanged` event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="df6a7-143">Em seguida, ele atualiza o status oculto da camada de tinta selecionada, define o InkEnabled do controle InkPicture como **false**,.</span><span class="sxs-lookup"><span data-stu-id="df6a7-143">It then updates the selected ink layer's hidden status, sets the InkPicture control's InkEnabled to **FALSE**, .</span></span>

<span data-ttu-id="df6a7-144">Em seguida, a propriedade InkEnabled do controle InkPicture é definida como **false** antes de atualizar sua propriedade Ink.</span><span class="sxs-lookup"><span data-stu-id="df6a7-144">Next, the InkPicture control's InkEnabled property is set to **FALSE** before updating its Ink property.</span></span>

<span data-ttu-id="df6a7-145">Por fim, o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) é habilitado ou desabilitado para a parte específica do veículo com base em se a caixa de seleção Ocultar camada está marcada e o método de [atualização](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) do controle InkPicture é usado para exibir apenas as camadas desejadas dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="df6a7-145">Finally, the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is either enabled or disabled for the particular vehicle part based on whether the Hide Layer check box is selected, and the InkPicture control's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
        Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
        End If
    End If
End Sub
```




```VB
private void chHideLayer_CheckedChanged(object sender, System.EventArgs e)
{
    // Provided that the new checked hidden value is different than
    // the previous value...
    if (chHideLayer.Checked != selectedHidden) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Update the array indicating the visibility of each ink layer
            inkLayers[lstAnnotationLayer.SelectedIndex].Hidden = chHideLayer.Checked;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
 
            // If the layer is marked hidden, disable ink collections
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;

            // Update the previous checkbox value to reflect the current
            selectedHidden = chHideLayer.Checked;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden;
            MessageBox.Show("Cannot change visiblity while collecting ink.");
        }
    }
}
```



## <a name="closing-the-form"></a><span data-ttu-id="df6a7-146">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="df6a7-146">Closing the Form</span></span>

<span data-ttu-id="df6a7-147">No código gerado pelo Windows Form Designer, os controles [InkEdit](/previous-versions/ms835842(v=msdn.10)) e [InkPicture](/previous-versions/ms583740(v=vs.100)) são adicionados à lista de componentes do formulário quando o formulário é inicializado.</span><span class="sxs-lookup"><span data-stu-id="df6a7-147">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="df6a7-148">Quando o formulário é fechado, os controles InkEdit e InkPicture são descartados, bem como os outros componentes do formulário, pelo método [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) do formulário.</span><span class="sxs-lookup"><span data-stu-id="df6a7-148">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) method.</span></span> <span data-ttu-id="df6a7-149">O método Dispose do formulário também descarta os objetos de [tinta](/previous-versions/ms583670(v=vs.100)) criados para o formulário.</span><span class="sxs-lookup"><span data-stu-id="df6a7-149">The form's Dispose method also disposes the [Ink](/previous-versions/ms583670(v=vs.100)) objects that are created for the form.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df6a7-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df6a7-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="df6a7-151">[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="df6a7-151">[Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="df6a7-152">Controle InkPicture</span><span class="sxs-lookup"><span data-stu-id="df6a7-152">InkPicture Control</span></span>](inkpicture-control.md)
</dt> <dt>

[<span data-ttu-id="df6a7-153">Controle InkEdit</span><span class="sxs-lookup"><span data-stu-id="df6a7-153">InkEdit Control</span></span>](inkedit-control.md)
</dt> </dl>

 

 
