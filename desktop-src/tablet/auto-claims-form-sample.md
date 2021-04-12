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
# <a name="auto-claims-form-sample"></a>Exemplo de formulário de declarações automáticas

O exemplo de declarações automáticas aborda um cenário hipotético de um assessor de seguros. O trabalho do assessor exige que ele visite os clientes em sua residência ou empresa e insira suas informações de declaração em um formulário. Para aumentar a produtividade do assessor, seu departamento de ti desenvolve um aplicativo de Tablet que permite que ele Insira informações de declaração com rapidez e precisão por meio de dois controles de tinta: os controles [InkEdit](/previous-versions/ms835842(v=msdn.10)) e [InkPicture](/previous-versions/ms583740(v=vs.100)) .

Neste exemplo, um controle [InkEdit](/previous-versions/ms835842(v=msdn.10)) é usado para cada campo de entrada de texto. Um usuário insere as informações relevantes sobre uma apólice de seguro e veículo nesses campos com uma caneta. O controle [InkPicture](/previous-versions/ms583740(v=vs.100)) é usado para adicionar tinta em uma imagem do automóvel para realçar áreas danificadas do automóvel. O exemplo de declarações automáticas está disponível para \# o C e o Microsoft Visual Basic .net. Este tópico descreve o Visual Basic .NET.

A classe autodeclarations é definida como uma subclasse de [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , e uma classe aninhada é definida para criar e gerenciar camadas de tinta para diferentes tipos de danos. Quatro manipuladores de eventos são definidos para executar as seguintes tarefas:

-   Inicializando as camadas de formulário e de tinta.
-   Redesenhando o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) .
-   Selecionando uma camada de tinta na caixa de listagem.
-   Alterando a visibilidade de uma camada de tinta.

> [!Note]  
> As versões deste exemplo estão disponíveis em C \# e Visual Basic .net. A versão discutida nesta seção é Visual Basic .NET. Os conceitos são os mesmos entre as versões.

 

## <a name="defining-the-form-and-ink-layers"></a>Definindo as camadas de formulário e de tinta

Você precisa importar o namespace [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



Em seguida, na classe autodeclarations, uma classe aninhada `InkLayer` é definida e uma matriz de quatro `InkLayer` objetos é declarada. (InkLayer contém um objeto [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) para armazenar a tinta e valores de [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) e **booliano** para armazenar a cor e o estado oculto da camada.) Um quinto objeto Ink é declarado para lidar com a tinta para o [InkPicture](/previous-versions/ms583740(v=vs.100)) quando todas as camadas de tinta estiverem ocultas.


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



Cada camada tem seu próprio objeto de [tinta](/previous-versions/ms583670(v=vs.100)) . Há quatro áreas discretas de interesse no formulário de declaração (corpo, Windows, pneus e faróis), de modo que quatro objetos InkLayer são usados. Um usuário pode exibir qualquer combinação de camadas ao mesmo tempo.

## <a name="initializing-the-form-and-ink-layers"></a>Inicializando o formulário e as camadas de tinta

O `Load` manipulador de eventos Inicializa o objeto de [tinta](/previous-versions/ms583670(v=vs.100)) e os quatro `InkLayer` objetos.


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



Em seguida, selecione a primeira entrada (corpo) na caixa de listagem.


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



Por fim, defina a cor da tinta para o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) para a entrada da caixa de listagem selecionada no momento.


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a>Redesenhando o controle InkPicture

No manipulador de eventos de [pintura](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) herdado do controle [InkPicture](/previous-versions/ms583740(v=vs.100)) , as camadas de tinta são verificadas para determinar quais estão ocultas. Se uma camada não estiver oculta, o procedimento de evento a exibirá usando o método [draw](/previous-versions/ms828488(v=msdn.10)) da propriedade [Renderer](/previous-versions/ms582196(v=vs.100)) . Se você examinar o pesquisador de objetos, verá que a propriedade Microsoft. Ink. InkPicture. Renderer é definida como um objeto [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) :


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



## <a name="selecting-an-ink-layer-through-the-list-box"></a>Selecionando uma camada de tinta na caixa de listagem

Quando o usuário seleciona um item na caixa de listagem, o manipulador de eventos [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) primeiro verifica se a seleção foi alterada e se o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) não está coletando tinta no momento. Em seguida, ele define a cor da tinta do controle InkPicture como a cor apropriada para a camada de tinta selecionada. Além disso, ele atualiza a caixa de seleção Ocultar camada para refletir o status oculto da camada de tinta selecionada. Por fim, o método de [atualização](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) herdado do controle InkPicture é usado para exibir apenas as camadas desejadas dentro do controle.


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



## <a name="changing-the-visibility-of-an-ink-layer"></a>Alterando a visibilidade de uma camada de tinta

O `CheckedChanged` manipulador de eventos primeiro verifica se a seleção foi alterada e se o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) não está coletando tinta no momento. Em seguida, ele atualiza o status oculto da camada de tinta selecionada, define o InkEnabled do controle InkPicture como **false**,.

Em seguida, a propriedade InkEnabled do controle InkPicture é definida como **false** antes de atualizar sua propriedade Ink.

Por fim, o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) é habilitado ou desabilitado para a parte específica do veículo com base em se a caixa de seleção Ocultar camada está marcada e o método de [atualização](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) do controle InkPicture é usado para exibir apenas as camadas desejadas dentro do controle.


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



## <a name="closing-the-form"></a>Fechando o formulário

No código gerado pelo Windows Form Designer, os controles [InkEdit](/previous-versions/ms835842(v=msdn.10)) e [InkPicture](/previous-versions/ms583740(v=vs.100)) são adicionados à lista de componentes do formulário quando o formulário é inicializado. Quando o formulário é fechado, os controles InkEdit e InkPicture são descartados, bem como os outros componentes do formulário, pelo método [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) do formulário. O método Dispose do formulário também descarta os objetos de [tinta](/previous-versions/ms583670(v=vs.100)) criados para o formulário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))
</dt> <dt>

[Controle InkPicture](inkpicture-control.md)
</dt> <dt>

[Controle InkEdit](inkedit-control.md)
</dt> </dl>

 

 
