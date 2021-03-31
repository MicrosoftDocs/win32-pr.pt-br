---
description: Este aplicativo demonstra como trabalhar com a classe RealTimeStylus.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: Exemplo de plug-in RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f593bf9e4fe0fb3d8ab12674047d6c05f28617a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172063"
---
# <a name="realtimestylus-plug-in-sample"></a>Exemplo de plug-in RealTimeStylus

Este aplicativo demonstra como trabalhar com a classe [**RealTimeStylus**](realtimestylus-class.md) . Para obter uma visão geral detalhada das APIs StylusInput, incluindo a classe **RealTimeStylus** , consulte [acessando e manipulando a entrada da caneta](accessing-and-manipulating-stylus-input.md). Para obter informações sobre plug-ins síncronos e assíncronos, consulte [plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="overview-of-the-sample"></a>Visão geral do exemplo

Plug-ins, os objetos que implementam a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) podem ser adicionados a um objeto [**RealTimeStylus**](realtimestylus-class.md) . Este aplicativo de exemplo usa vários tipos de plug-in:

-   Plug-in de filtro de pacote: modifica pacotes. O plug-in de filtro de pacote neste exemplo modifica informações de pacote restringindo todos os dados de pacote (x, y) em uma área retangular.
-   Plug-in de processador dinâmico personalizado: modifica as qualidades de renderização dinâmica. O plug-in de renderização dinâmica personalizado neste exemplo modifica a maneira como a tinta é renderizada ao desenhar um pequeno círculo em volta de cada ponto (x, y) em um traço.
-   Plug-in de processamento dinâmico: modifica as qualidades de renderização dinâmica. Este exemplo demonstra o uso do objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) como um plug-in para lidar com a renderização dinâmica da tinta.
-   Plug-in do reconhecedor de gestos: reconhece gestos de aplicativo. Este exemplo demonstra o uso do objeto [**GestureRecognizer**](gesturerecognizer-class.md) como um plug-in para reconhecer gestos de aplicativo (quando executado em um sistema com o reconhecedor de gestos da Microsoft presente).

Além disso, este exemplo fornece uma interface do usuário que permite ao usuário adicionar, remover e alterar a ordem de cada plug-in na coleção. A solução de exemplo contém dois projetos, RealTimeStylusPluginApp e RealTimeStylusPlugins. RealTimeStylusPluginApp contém a interface do usuário para o exemplo. RealTimeStylusPlugins contém as implementações dos plug-ins. O projeto RealTimeStylusPlugins define o namespace RealTimeStylusPlugins, que contém o filtro de pacote e plug-ins de processamento dinâmico personalizado. Esse namespace é referenciado pelo projeto RealTimeStylusPluginApp. O projeto RealTimeStylusPlugins usa os namespaces [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))e [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .

Para obter uma visão geral dos namespaces [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) e [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) , consulte [arquitetura das APIs do StylusInput](architecture-of-the-stylusinput-apis.md).

## <a name="packet-filter-plug-in"></a>Plug-in de filtro de pacote

O plug-in de filtro de pacote é um plug-in síncrono que demonstra a modificação de pacotes. Especificamente, ele define um retângulo no formulário. Todos os pacotes que são desenhados fora da região são renderizados dentro da região. A classe de plug-in, `PacketFilterPlugin` , registra para notificação `StylusDown` de `StylusUp` eventos de `Packets` entrada de caneta, e. A classe implementa os métodos [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10))e [packets](/previous-versions/ms824756(v=msdn.10)) definidos na classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .

O construtor público para `PacketFilterPlugin` requer uma estrutura de [retângulo](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) . Esse retângulo define a área retangular, em coordenadas de espaço de tinta (. 01mm = 1 unidade HIMETRIC), na qual os pacotes estarão contidos. O retângulo é mantido em um campo privado, `rectangle` .


```C++
public class PacketFilterPlugin:IStylusSyncPlugin  
{
    private System.Drawing.Rectangle rectangle = System.Drawing.Rectangle.Empty;
    public PacketFilterPlugin(Rectangle r)
    {
        rectangle = r;
    }
    // ...
```



A `PacketFilterPlugin` classe registra para notificações de eventos implementando o acessador get para a propriedade [DataInterest](/previous-versions/ms824752(v=msdn.10)) . Nesse caso, o plug-in tem interesse em responder às `StylusDown` `Packets` notificações,, `StylusUp` e `Error` . O exemplo retorna esses valores conforme definido na enumeração [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) . O método [StylusDown](/previous-versions/ms824761(v=msdn.10)) é chamado quando a dica de caneta entra em contato com a superfície digitalizadora. O método [StylusUp](/previous-versions/ms824764(v=msdn.10)) é chamado quando a ponta da caneta sai da superfície digitalizadora. O método de [pacotes](/previous-versions/ms824756(v=msdn.10)) é chamado quando o objeto [**RealTimeStylus**](realtimestylus-class.md) recebe pacotes. O método de [erro](/previous-versions/ms585069(v=vs.100)) é chamado quando o plug-in atual ou um plug-in anterior gera uma exceção.


```C++
public DataInterestMask DataInterest
{
    get
    {
        return DataInterestMask.StylusDown | 
               DataInterestMask.Packets | 
               DataInterestMask.StylusUp | 
               DataInterestMask.Error;
    }
}           
    //...
```



A `PacketFilterPlugin` classe manipula a maioria dessas notificações em um método auxiliar, `ModifyPacketData` . O `ModifyPacketData` método obtém os valores x e y para cada novo pacote da classe [PacketsData](/previous-versions/ms824590(v=msdn.10)) . Se qualquer valor estiver fora do retângulo, o método substituirá o valor pelo ponto mais próximo que ainda está dentro do retângulo. Este é um exemplo de como um plug-in pode substituir dados de pacote conforme eles são recebidos do fluxo de entrada da caneta.


```C++
private void ModifyPacketData(StylusDataBase data)
{
    for (int i = 0; i < data.Count ; i += data.PacketPropertyCount)
    {
        // packet data always has x followed by y followed by the rest
        int x = data[i];
        int y = data[i+1];

        // Constrain points to the input rectangle
        x = Math.Max(x, rectangle.Left);
        x = Math.Min(x, rectangle.Right);
        y = Math.Max(y, rectangle.Top);
        y = Math.Min(y, rectangle.Bottom);

        // If necessary, modify the x,y packet data
        if (x != data[i])
        {
            data[i] = x;
        }
        if (y != data[i+1])
        {
            data[i+1] = y;
        } 
    }
}
```



## <a name="custom-dynamic-renderer-plug-in"></a>Plug-in de processador dinâmico personalizado

A `CustomDynamicRenderer` classe também implementa a classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) para receber notificações de entrada de caneta. Em seguida, ele manipula a `Packets` notificação para desenhar um pequeno círculo em volta de cada novo ponto de pacote.

A classe contém uma variável [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) que contém uma referência ao objeto Graphics passado para o construtor da classe. Este é o objeto gráfico usado para renderização dinâmica.


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



Quando o plug-in personalizado de processador dinâmico recebe uma notificação de pacotes, ele extrai os dados (x, y) e desenha um pequeno círculo verde em volta do ponto. Este é um exemplo de renderização personalizada com base no fluxo de entrada da caneta.


```C++
public void Packets(RealTimeStylus sender,  PacketsData data)
{           
    for (int i = 0; i < data.Count; i += data.PacketPropertyCount)
    {
        // Packet data always has x followed by y followed by the rest
        Point point = new Point(data[i], data[i+1]);

        // Since the packet data is in Ink Space coordinates, we need to convert to Pixels...
        point.X = (int)Math.Round((float)point.X * (float)myGraphics.DpiX/2540.0F);
        point.Y = (int)Math.Round((float)point.Y * (float)myGraphics.DpiY/2540.0F);

        // Draw a circle corresponding to the packet
        myGraphics.DrawEllipse(Pens.Green, point.X - 2, point.Y - 2, 4, 4);
    }
}
```



## <a name="the-realtimestyluspluginapp-project"></a>O projeto RealTimeStylusPluginApp

O projeto RealTimeStylusPluginApp demonstra os plug-ins descritos anteriormente, bem como os plug-ins [**GestureRecognizer**](gesturerecognizer-class.md) e [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . A interface do usuário do projeto consiste em:

-   Um formulário que contém um controle [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) usado para definir a área de entrada à tinta.
-   Um controle [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) para listar e selecionar os plug-ins disponíveis.
-   Um par de [objetos Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) para habilitar a reordenação dos plug-ins.

O projeto define uma estrutura, `PlugInListItem` , para facilitar o gerenciamento dos plug-ins usados no projeto. A `PlugInListItem` estrutura contém o plug-in e uma descrição.

A `RealTimeStylusPluginApp` própria classe implementa a classe [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Isso é necessário para que a `RealTimeStylusPluginApp` classe possa ser notificada quando o plug-in [**GestureRecognizer**](gesturerecognizer-class.md) adicionar dados de gesto à fila de saída. O aplicativo é registrado para notificação de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)). Quando os dados do gesto são recebidos, `RealTimeStylusPluginApp` o coloca uma descrição dele na barra de status na parte inferior do formulário.


```C++
public void CustomStylusDataAdded(RealTimeStylus sender, CustomStylusData data)
{
    if (data.CustomDataId == GestureRecognizer.GestureRecognitionDataGuid)
    {
        GestureRecognitionData grd = data.Data as GestureRecognitionData;
        if (grd != null)
        {
            if (grd.Count > 0)
            {
                GestureAlternate ga = grd[0];
                sbGesture.Text = "Gesture=" + ga.Id + ", Confidence=" + ga.Confidence;
            }
        }
    }
}
```



> [!Note]  
> Na implementação de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) , é interessante que você possa identificar os dados de gestos personalizados na fila de saída por GUID (usando o campo [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ) ou por tipo (usando o resultado da instrução as). O exemplo usa as duas técnicas de identificação para fins de demonstração. Qualquer uma das abordagens também é válida.

 

No manipulador de eventos Load do formulário, o aplicativo cria instâncias das `PacketFilter` classes e `CustomDynamicRenderer` e adiciona-as à caixa de listagem. Em seguida, o aplicativo tenta criar uma instância da classe [**GestureRecognizer**](gesturerecognizer-class.md) e, se for bem-sucedida, a adiciona à caixa de listagem. Isso falhará se o reconhecedor de gestos não estiver presente no sistema. Em seguida, o aplicativo instancia um objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e o adiciona à caixa de listagem. Por fim, o aplicativo habilita cada um dos plug-ins e o próprio objeto do [**RealTimeStylus**](realtimestylus-class.md) .

Outra coisa importante a ser observada sobre o exemplo é que, nos métodos auxiliares, o objeto [**RealTimeStylus**](realtimestylus-class.md) é desabilitado primeiro antes que os plug-ins sejam adicionados ou removidos e, em seguida, habilitado novamente após a conclusão da adição ou remoção.


```C++
private void RemoveFromPluginCollection(int index)
{
    IStylusSyncPlugin plugin = ((PluginListItem)chklbPlugins.Items[index]).Plugin;

    bool rtsEnabled = myRealTimeStylus.Enabled;
    myRealTimeStylus.Enabled = false;
    myRealTimeStylus.SyncPluginCollection.Remove(plugin);
    myRealTimeStylus.Enabled = rtsEnabled;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))
</dt> <dt>

[Acessando e manipulando a entrada da caneta](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[Plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[Exemplo de coleção de tinta do RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
