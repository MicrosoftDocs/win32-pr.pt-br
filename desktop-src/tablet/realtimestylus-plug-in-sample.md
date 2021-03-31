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
# <a name="realtimestylus-plug-in-sample"></a><span data-ttu-id="838ca-103">Exemplo de plug-in RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="838ca-103">RealTimeStylus Plug-in Sample</span></span>

<span data-ttu-id="838ca-104">Este aplicativo demonstra como trabalhar com a classe [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="838ca-104">This application demonstrates working with the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span> <span data-ttu-id="838ca-105">Para obter uma visão geral detalhada das APIs StylusInput, incluindo a classe **RealTimeStylus** , consulte [acessando e manipulando a entrada da caneta](accessing-and-manipulating-stylus-input.md).</span><span class="sxs-lookup"><span data-stu-id="838ca-105">For a detailed overview of the StylusInput APIs, including the **RealTimeStylus** class, see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span> <span data-ttu-id="838ca-106">Para obter informações sobre plug-ins síncronos e assíncronos, consulte [plug-ins e a classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="838ca-106">For information about synchronous and asynchronous plug-ins, see [Plug-ins and the RealTimeStylus Class](plug-ins-and-the-realtimestylus-class.md).</span></span>

## <a name="overview-of-the-sample"></a><span data-ttu-id="838ca-107">Visão geral do exemplo</span><span class="sxs-lookup"><span data-stu-id="838ca-107">Overview of the Sample</span></span>

<span data-ttu-id="838ca-108">Plug-ins, os objetos que implementam a interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) podem ser adicionados a um objeto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="838ca-108">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface can be added to a [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="838ca-109">Este aplicativo de exemplo usa vários tipos de plug-in:</span><span class="sxs-lookup"><span data-stu-id="838ca-109">This sample application uses several types of plug-in:</span></span>

-   <span data-ttu-id="838ca-110">Plug-in de filtro de pacote: modifica pacotes.</span><span class="sxs-lookup"><span data-stu-id="838ca-110">Packet Filter Plug-in: Modifies packets.</span></span> <span data-ttu-id="838ca-111">O plug-in de filtro de pacote neste exemplo modifica informações de pacote restringindo todos os dados de pacote (x, y) em uma área retangular.</span><span class="sxs-lookup"><span data-stu-id="838ca-111">The packet filter plug-in in this sample modifies packet information by constraining all (x,y) packet data within a rectangular area.</span></span>
-   <span data-ttu-id="838ca-112">Plug-in de processador dinâmico personalizado: modifica as qualidades de renderização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="838ca-112">Custom Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="838ca-113">O plug-in de renderização dinâmica personalizado neste exemplo modifica a maneira como a tinta é renderizada ao desenhar um pequeno círculo em volta de cada ponto (x, y) em um traço.</span><span class="sxs-lookup"><span data-stu-id="838ca-113">The custom dynamic rendering plug-in in this sample modifies the way ink is rendered by drawing a small circle around each (x,y) point on a stroke.</span></span>
-   <span data-ttu-id="838ca-114">Plug-in de processamento dinâmico: modifica as qualidades de renderização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="838ca-114">Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="838ca-115">Este exemplo demonstra o uso do objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) como um plug-in para lidar com a renderização dinâmica da tinta.</span><span class="sxs-lookup"><span data-stu-id="838ca-115">This sample demonstrates use of the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object as a plug-in to handle dynamic rendering of ink.</span></span>
-   <span data-ttu-id="838ca-116">Plug-in do reconhecedor de gestos: reconhece gestos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="838ca-116">Gesture Recognizer Plug-in: Recognizes application gestures.</span></span> <span data-ttu-id="838ca-117">Este exemplo demonstra o uso do objeto [**GestureRecognizer**](gesturerecognizer-class.md) como um plug-in para reconhecer gestos de aplicativo (quando executado em um sistema com o reconhecedor de gestos da Microsoft presente).</span><span class="sxs-lookup"><span data-stu-id="838ca-117">This sample demonstrates use of the [**GestureRecognizer**](gesturerecognizer-class.md) object as a plug-in to recognize application gestures (when running on a system with the Microsoft gesture recognizer present).</span></span>

<span data-ttu-id="838ca-118">Além disso, este exemplo fornece uma interface do usuário que permite ao usuário adicionar, remover e alterar a ordem de cada plug-in na coleção.</span><span class="sxs-lookup"><span data-stu-id="838ca-118">In addition, this sample provides a user interface that enables the user to add, remove, and change the order of each plug-in in the collection.</span></span> <span data-ttu-id="838ca-119">A solução de exemplo contém dois projetos, RealTimeStylusPluginApp e RealTimeStylusPlugins.</span><span class="sxs-lookup"><span data-stu-id="838ca-119">The sample solution contains two projects, RealTimeStylusPluginApp and RealTimeStylusPlugins.</span></span> <span data-ttu-id="838ca-120">RealTimeStylusPluginApp contém a interface do usuário para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="838ca-120">RealTimeStylusPluginApp contains the user interface for the sample.</span></span> <span data-ttu-id="838ca-121">RealTimeStylusPlugins contém as implementações dos plug-ins. O projeto RealTimeStylusPlugins define o namespace RealTimeStylusPlugins, que contém o filtro de pacote e plug-ins de processamento dinâmico personalizado. Esse namespace é referenciado pelo projeto RealTimeStylusPluginApp.</span><span class="sxs-lookup"><span data-stu-id="838ca-121">RealTimeStylusPlugins contains the implementations of the plug-ins. The RealTimeStylusPlugins project defines the RealTimeStylusPlugins namespace, which contains the packet filter and custom dynamic renderer plug-ins. This namespace is referenced by the RealTimeStylusPluginApp project.</span></span> <span data-ttu-id="838ca-122">O projeto RealTimeStylusPlugins usa os namespaces [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))e [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="838ca-122">The RealTimeStylusPlugins project uses the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)), and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces.</span></span>

<span data-ttu-id="838ca-123">Para obter uma visão geral dos namespaces [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) e [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) , consulte [arquitetura das APIs do StylusInput](architecture-of-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="838ca-123">For an overview of the [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces see [Architecture of the StylusInput APIs](architecture-of-the-stylusinput-apis.md).</span></span>

## <a name="packet-filter-plug-in"></a><span data-ttu-id="838ca-124">Plug-in de filtro de pacote</span><span class="sxs-lookup"><span data-stu-id="838ca-124">Packet Filter Plug-in</span></span>

<span data-ttu-id="838ca-125">O plug-in de filtro de pacote é um plug-in síncrono que demonstra a modificação de pacotes.</span><span class="sxs-lookup"><span data-stu-id="838ca-125">The packet filter plug-in is a synchronous plug-in that demonstrates packet modification.</span></span> <span data-ttu-id="838ca-126">Especificamente, ele define um retângulo no formulário.</span><span class="sxs-lookup"><span data-stu-id="838ca-126">Specifically, it defines a rectangle on the form.</span></span> <span data-ttu-id="838ca-127">Todos os pacotes que são desenhados fora da região são renderizados dentro da região.</span><span class="sxs-lookup"><span data-stu-id="838ca-127">Any packets that are drawn outside the region are rendered inside the region.</span></span> <span data-ttu-id="838ca-128">A classe de plug-in, `PacketFilterPlugin` , registra para notificação `StylusDown` de `StylusUp` eventos de `Packets` entrada de caneta, e.</span><span class="sxs-lookup"><span data-stu-id="838ca-128">The plug-in class, `PacketFilterPlugin`, registers for notification of `StylusDown`, `StylusUp`, and `Packets` pen input events.</span></span> <span data-ttu-id="838ca-129">A classe implementa os métodos [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10))e [packets](/previous-versions/ms824756(v=msdn.10)) definidos na classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="838ca-129">The class implements the [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10)), and [Packets](/previous-versions/ms824756(v=msdn.10)) methods defined on [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class.</span></span>

<span data-ttu-id="838ca-130">O construtor público para `PacketFilterPlugin` requer uma estrutura de [retângulo](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="838ca-130">The public constructor for `PacketFilterPlugin` requires a [Rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) structure.</span></span> <span data-ttu-id="838ca-131">Esse retângulo define a área retangular, em coordenadas de espaço de tinta (. 01mm = 1 unidade HIMETRIC), na qual os pacotes estarão contidos.</span><span class="sxs-lookup"><span data-stu-id="838ca-131">This rectangle defines the rectangular area, in ink space coordinates (.01mm = 1 HIMETRIC unit), in which packets will be contained.</span></span> <span data-ttu-id="838ca-132">O retângulo é mantido em um campo privado, `rectangle` .</span><span class="sxs-lookup"><span data-stu-id="838ca-132">The rectangle is held in a private field, `rectangle`.</span></span>


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



<span data-ttu-id="838ca-133">A `PacketFilterPlugin` classe registra para notificações de eventos implementando o acessador get para a propriedade [DataInterest](/previous-versions/ms824752(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="838ca-133">The `PacketFilterPlugin` class registers for event notifications by implementing the get accessor for the [DataInterest](/previous-versions/ms824752(v=msdn.10)) property.</span></span> <span data-ttu-id="838ca-134">Nesse caso, o plug-in tem interesse em responder às `StylusDown` `Packets` notificações,, `StylusUp` e `Error` .</span><span class="sxs-lookup"><span data-stu-id="838ca-134">In this case, the plug-in has interested in responding to the `StylusDown`, `Packets`, `StylusUp`, and `Error` notifications.</span></span> <span data-ttu-id="838ca-135">O exemplo retorna esses valores conforme definido na enumeração [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="838ca-135">The sample returns these values as defined in the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span> <span data-ttu-id="838ca-136">O método [StylusDown](/previous-versions/ms824761(v=msdn.10)) é chamado quando a dica de caneta entra em contato com a superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="838ca-136">The [StylusDown](/previous-versions/ms824761(v=msdn.10)) method is called when the pen tip contacts the digitizer surface.</span></span> <span data-ttu-id="838ca-137">O método [StylusUp](/previous-versions/ms824764(v=msdn.10)) é chamado quando a ponta da caneta sai da superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="838ca-137">The [StylusUp](/previous-versions/ms824764(v=msdn.10)) method is called when the pen tip leaves the digitizer surface.</span></span> <span data-ttu-id="838ca-138">O método de [pacotes](/previous-versions/ms824756(v=msdn.10)) é chamado quando o objeto [**RealTimeStylus**](realtimestylus-class.md) recebe pacotes.</span><span class="sxs-lookup"><span data-stu-id="838ca-138">The [Packets](/previous-versions/ms824756(v=msdn.10)) method is called when the [**RealTimeStylus**](realtimestylus-class.md) object receives packets.</span></span> <span data-ttu-id="838ca-139">O método de [erro](/previous-versions/ms585069(v=vs.100)) é chamado quando o plug-in atual ou um plug-in anterior gera uma exceção.</span><span class="sxs-lookup"><span data-stu-id="838ca-139">The [Error](/previous-versions/ms585069(v=vs.100)) method is called when the current plug-in or a previous plug-in throws an exception.</span></span>


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



<span data-ttu-id="838ca-140">A `PacketFilterPlugin` classe manipula a maioria dessas notificações em um método auxiliar, `ModifyPacketData` .</span><span class="sxs-lookup"><span data-stu-id="838ca-140">The `PacketFilterPlugin` class handles most of these notifications in a helper method, `ModifyPacketData`.</span></span> <span data-ttu-id="838ca-141">O `ModifyPacketData` método obtém os valores x e y para cada novo pacote da classe [PacketsData](/previous-versions/ms824590(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="838ca-141">The `ModifyPacketData` method gets the x and y values for each new packet from the [PacketsData](/previous-versions/ms824590(v=msdn.10)) class.</span></span> <span data-ttu-id="838ca-142">Se qualquer valor estiver fora do retângulo, o método substituirá o valor pelo ponto mais próximo que ainda está dentro do retângulo.</span><span class="sxs-lookup"><span data-stu-id="838ca-142">If either value is outside the rectangle, the method replaces the value with the nearest point that still falls within the rectangle.</span></span> <span data-ttu-id="838ca-143">Este é um exemplo de como um plug-in pode substituir dados de pacote conforme eles são recebidos do fluxo de entrada da caneta.</span><span class="sxs-lookup"><span data-stu-id="838ca-143">This is an example of how a plug-in can replace packet data as it is received from the pen-input stream.</span></span>


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



## <a name="custom-dynamic-renderer-plug-in"></a><span data-ttu-id="838ca-144">Plug-in de processador dinâmico personalizado</span><span class="sxs-lookup"><span data-stu-id="838ca-144">Custom Dynamic Renderer Plug-in</span></span>

<span data-ttu-id="838ca-145">A `CustomDynamicRenderer` classe também implementa a classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) para receber notificações de entrada de caneta.</span><span class="sxs-lookup"><span data-stu-id="838ca-145">The `CustomDynamicRenderer` class also implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class to receive pen-input notifications.</span></span> <span data-ttu-id="838ca-146">Em seguida, ele manipula a `Packets` notificação para desenhar um pequeno círculo em volta de cada novo ponto de pacote.</span><span class="sxs-lookup"><span data-stu-id="838ca-146">It then handles the `Packets` notification to draw a small circle around each new packet point.</span></span>

<span data-ttu-id="838ca-147">A classe contém uma variável [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) que contém uma referência ao objeto Graphics passado para o construtor da classe.</span><span class="sxs-lookup"><span data-stu-id="838ca-147">The class contains a [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) variable that holds a reference to the graphics object passed into the class constructor.</span></span> <span data-ttu-id="838ca-148">Este é o objeto gráfico usado para renderização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="838ca-148">This is the graphics object used for dynamic rendering.</span></span>


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



<span data-ttu-id="838ca-149">Quando o plug-in personalizado de processador dinâmico recebe uma notificação de pacotes, ele extrai os dados (x, y) e desenha um pequeno círculo verde em volta do ponto.</span><span class="sxs-lookup"><span data-stu-id="838ca-149">When the custom dynamic renderer plug-in receives a Packets notification, it extracts the (x,y) data and draws a small green circle around the point.</span></span> <span data-ttu-id="838ca-150">Este é um exemplo de renderização personalizada com base no fluxo de entrada da caneta.</span><span class="sxs-lookup"><span data-stu-id="838ca-150">This is an example of custom rendering based on the pen-input stream.</span></span>


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



## <a name="the-realtimestyluspluginapp-project"></a><span data-ttu-id="838ca-151">O projeto RealTimeStylusPluginApp</span><span class="sxs-lookup"><span data-stu-id="838ca-151">The RealTimeStylusPluginApp Project</span></span>

<span data-ttu-id="838ca-152">O projeto RealTimeStylusPluginApp demonstra os plug-ins descritos anteriormente, bem como os plug-ins [**GestureRecognizer**](gesturerecognizer-class.md) e [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . A interface do usuário do projeto consiste em:</span><span class="sxs-lookup"><span data-stu-id="838ca-152">The RealTimeStylusPluginApp project demonstrates the plug-ins previously described, as well as the [**GestureRecognizer**](gesturerecognizer-class.md) and [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) plug-ins. The project's user interface consists of:</span></span>

-   <span data-ttu-id="838ca-153">Um formulário que contém um controle [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) usado para definir a área de entrada à tinta.</span><span class="sxs-lookup"><span data-stu-id="838ca-153">A Form that contains a [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) control used to define the ink entry area.</span></span>
-   <span data-ttu-id="838ca-154">Um controle [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) para listar e selecionar os plug-ins disponíveis.</span><span class="sxs-lookup"><span data-stu-id="838ca-154">A [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) control to list and select the available plug-ins.</span></span>
-   <span data-ttu-id="838ca-155">Um par de [objetos Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) para habilitar a reordenação dos plug-ins.</span><span class="sxs-lookup"><span data-stu-id="838ca-155">A pair of [Button objects](/dotnet/api/system.windows.forms.button?view=netcore-3.1) to enable re-ordering the plug-ins.</span></span>

<span data-ttu-id="838ca-156">O projeto define uma estrutura, `PlugInListItem` , para facilitar o gerenciamento dos plug-ins usados no projeto.</span><span class="sxs-lookup"><span data-stu-id="838ca-156">The project defines a structure, `PlugInListItem`, to make managing the plug-ins used in the project easier.</span></span> <span data-ttu-id="838ca-157">A `PlugInListItem` estrutura contém o plug-in e uma descrição.</span><span class="sxs-lookup"><span data-stu-id="838ca-157">The `PlugInListItem` structure contains the plug-in and a description.</span></span>

<span data-ttu-id="838ca-158">A `RealTimeStylusPluginApp` própria classe implementa a classe [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="838ca-158">The `RealTimeStylusPluginApp` class itself implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) class.</span></span> <span data-ttu-id="838ca-159">Isso é necessário para que a `RealTimeStylusPluginApp` classe possa ser notificada quando o plug-in [**GestureRecognizer**](gesturerecognizer-class.md) adicionar dados de gesto à fila de saída.</span><span class="sxs-lookup"><span data-stu-id="838ca-159">This is necessary so that the `RealTimeStylusPluginApp` class can be notified when the [**GestureRecognizer**](gesturerecognizer-class.md) plug-in adds gesture data to the output queue.</span></span> <span data-ttu-id="838ca-160">O aplicativo é registrado para notificação de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="838ca-160">The application registers for notification of [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span></span> <span data-ttu-id="838ca-161">Quando os dados do gesto são recebidos, `RealTimeStylusPluginApp` o coloca uma descrição dele na barra de status na parte inferior do formulário.</span><span class="sxs-lookup"><span data-stu-id="838ca-161">When gesture data is received, `RealTimeStylusPluginApp` places a description of it on the status bar at the bottom of the form.</span></span>


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
> Na implementação de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) , é interessante que você possa identificar os dados de gestos personalizados na fila de saída por GUID (usando o campo [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ) ou por tipo (usando o resultado da instrução as). O exemplo usa as duas técnicas de identificação para fins de demonstração. <span data-ttu-id="838ca-164">Qualquer uma das abordagens também é válida.</span><span class="sxs-lookup"><span data-stu-id="838ca-164">Either approach alone is also valid.</span></span>

 

<span data-ttu-id="838ca-165">No manipulador de eventos Load do formulário, o aplicativo cria instâncias das `PacketFilter` classes e `CustomDynamicRenderer` e adiciona-as à caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="838ca-165">In the Form's Load event handler, the application creates instances of the `PacketFilter` and `CustomDynamicRenderer` classes and adds them to the list box.</span></span> <span data-ttu-id="838ca-166">Em seguida, o aplicativo tenta criar uma instância da classe [**GestureRecognizer**](gesturerecognizer-class.md) e, se for bem-sucedida, a adiciona à caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="838ca-166">The application then attempts to create an instance of the [**GestureRecognizer**](gesturerecognizer-class.md) class and, if successful, adds it to the list box.</span></span> <span data-ttu-id="838ca-167">Isso falhará se o reconhecedor de gestos não estiver presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="838ca-167">This fails if the gesture recognizer is not present on the system.</span></span> <span data-ttu-id="838ca-168">Em seguida, o aplicativo instancia um objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e o adiciona à caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="838ca-168">Next, the application instantiates a [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object and adds it to the list box.</span></span> <span data-ttu-id="838ca-169">Por fim, o aplicativo habilita cada um dos plug-ins e o próprio objeto do [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="838ca-169">Finally, the application enables each of the plug-ins and the [**RealTimeStylus**](realtimestylus-class.md) object itself.</span></span>

<span data-ttu-id="838ca-170">Outra coisa importante a ser observada sobre o exemplo é que, nos métodos auxiliares, o objeto [**RealTimeStylus**](realtimestylus-class.md) é desabilitado primeiro antes que os plug-ins sejam adicionados ou removidos e, em seguida, habilitado novamente após a conclusão da adição ou remoção.</span><span class="sxs-lookup"><span data-stu-id="838ca-170">Another important thing to note about the sample is that in the helper methods, the [**RealTimeStylus**](realtimestylus-class.md) object is first disabled before plug-ins are added or removed and then re-enabled after the addition or removal is complete.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="838ca-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="838ca-171">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="838ca-172">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="838ca-172">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="838ca-173">[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="838ca-173">[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="838ca-174">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="838ca-174">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="838ca-175">[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="838ca-175">[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="838ca-176">[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="838ca-176">[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="838ca-177">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="838ca-177">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="838ca-178">[Microsoft. StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="838ca-178">[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="838ca-179">Acessando e manipulando a entrada da caneta</span><span class="sxs-lookup"><span data-stu-id="838ca-179">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[<span data-ttu-id="838ca-180">Plug-ins e a classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="838ca-180">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="838ca-181">Exemplo de coleção de tinta do RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="838ca-181">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
