---
description: Este aplicativo demonstra a coleta de tinta e a renderização ao usar a classe RealTimeStylus.
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: Exemplo de coleção de tinta do RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24fe67ed59ea1a69f5d0d9a2656169f2df88a450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761532"
---
# <a name="realtimestylus-ink-collection-sample"></a><span data-ttu-id="a11a1-103">Exemplo de coleção de tinta do RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="a11a1-103">RealTimeStylus Ink Collection Sample</span></span>

<span data-ttu-id="a11a1-104">Este aplicativo demonstra a coleta de tinta e a renderização ao usar a classe [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-104">This application demonstrates ink collection and rendering when using the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span>

## <a name="the-inkcollection-project"></a><span data-ttu-id="a11a1-105">O projeto InkCollection</span><span class="sxs-lookup"><span data-stu-id="a11a1-105">The InkCollection Project</span></span>

<span data-ttu-id="a11a1-106">Este exemplo consiste em uma única solução que contém um projeto, InkCollection.</span><span class="sxs-lookup"><span data-stu-id="a11a1-106">This sample consists of a single solution that contains one project, InkCollection.</span></span> <span data-ttu-id="a11a1-107">O aplicativo define o `InkCollection` namespace que contém uma única classe, também chamada de `InkCollection` .</span><span class="sxs-lookup"><span data-stu-id="a11a1-107">The application defines the `InkCollection` namespace that contains a single class, also called `InkCollection`.</span></span> <span data-ttu-id="a11a1-108">A classe herda da classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e implementa a interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-108">The class inherits from the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span>


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



<span data-ttu-id="a11a1-109">A classe InkCollection define um conjunto de constantes privadas usadas para especificar várias espessuras de tinta.</span><span class="sxs-lookup"><span data-stu-id="a11a1-109">The InkCollection Class defines a set of private constants used to specify various ink thickness.</span></span> <span data-ttu-id="a11a1-110">A classe também declara instâncias privadas da classe [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , a classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` e a classe [Renderer](/previous-versions/ms828481(v=msdn.10)) `myRenderer` .</span><span class="sxs-lookup"><span data-stu-id="a11a1-110">The class also declares private instances of the [**RealTimeStylus**](realtimestylus-class.md) class, `myRealTimeStylus`, the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) class, `myDynamicRenderer`, and the [Renderer](/previous-versions/ms828481(v=msdn.10)) class `myRenderer`.</span></span> <span data-ttu-id="a11a1-111">O **DynamicRenderer** renderiza o [traço](/previous-versions/ms552692(v=vs.100)) que está sendo coletado no momento.</span><span class="sxs-lookup"><span data-stu-id="a11a1-111">The **DynamicRenderer** renders the [Stroke](/previous-versions/ms552692(v=vs.100)) that is currently being collected.</span></span> <span data-ttu-id="a11a1-112">O objeto Renderer, `myRenderer` , renderiza objetos Stroke que já foram coletados.</span><span class="sxs-lookup"><span data-stu-id="a11a1-112">The Renderer object, `myRenderer`, renders Stroke objects that have already been collected.</span></span>


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



<span data-ttu-id="a11a1-113">A classe também declara um objeto [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` , que é usado para armazenar dados de pacote que estão sendo coletados por um ou mais objetos de [cursor](/previous-versions/ms552104(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-113">The class also declares a [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) object, `myPackets`, which is used to store packet data that is being collected by one or more [Cursor](/previous-versions/ms552104(v=vs.100)) objects.</span></span> <span data-ttu-id="a11a1-114">Os valores de [ID](/previous-versions/ms824826(v=msdn.10)) do objeto de [caneta](/previous-versions/ms824824(v=msdn.10)) são usados como a chave de Hashtable para identificar exclusivamente os dados de pacote coletados para um determinado objeto de cursor.</span><span class="sxs-lookup"><span data-stu-id="a11a1-114">The [Stylus](/previous-versions/ms824824(v=msdn.10)) object's [Id](/previous-versions/ms824826(v=msdn.10)) values are used as the hashtable key to uniquely identify the packet data collected for a given Cursor object.</span></span>

<span data-ttu-id="a11a1-115">Uma instância privada do objeto [Ink](/previous-versions/aa515768(v=msdn.10)) , `myInk` , armazena objetos [Stroke](/previous-versions/ms552692(v=vs.100)) coletados pelo `myRealTimeStylus` .</span><span class="sxs-lookup"><span data-stu-id="a11a1-115">A private instance of the [Ink](/previous-versions/aa515768(v=msdn.10)) object, `myInk`, stores [Stroke](/previous-versions/ms552692(v=vs.100)) objects collected by `myRealTimeStylus`.</span></span>


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a><span data-ttu-id="a11a1-116">O evento de carregamento de formulário</span><span class="sxs-lookup"><span data-stu-id="a11a1-116">The Form Load Event</span></span>

<span data-ttu-id="a11a1-117">No manipulador de eventos de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) para o formulário, `myDynamicRenderer` é criada uma instância usando o [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) que usa um controle como argumento e `myRenderer` é construído com um construtor sem argumento.</span><span class="sxs-lookup"><span data-stu-id="a11a1-117">In the [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler for the form, `myDynamicRenderer` is instantiated by using the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) that takes a control as an argument, and `myRenderer` is constructed with a no-argument constructor.</span></span>


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



<span data-ttu-id="a11a1-118">Preste atenção ao comentário que segue a instanciação dos renderizadores, porque `myDynamicRenderer` o usa os valores padrão para [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) ao renderizar a tinta.</span><span class="sxs-lookup"><span data-stu-id="a11a1-118">Pay attention to the comment that follows the instantiation of the renderers, because `myDynamicRenderer` uses the default values for [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) when rendering the ink.</span></span> <span data-ttu-id="a11a1-119">Esse é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="a11a1-119">This is standard behavior.</span></span> <span data-ttu-id="a11a1-120">No entanto, se você quiser fornecer a tinta renderizada por `myDynamicRenderer` uma aparência diferente da tinta renderizada pelo `myRenderer` , poderá alterar a propriedade [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) em `myDynamicRenderer` .</span><span class="sxs-lookup"><span data-stu-id="a11a1-120">However, if you wish to give the ink rendered by `myDynamicRenderer` a different look from ink rendered by `myRenderer`, you can change the [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) property on `myDynamicRenderer`.</span></span> <span data-ttu-id="a11a1-121">Para fazer isso, remova os comentários das linhas a seguir antes de compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a11a1-121">To do so, uncomment the following lines before you build and run the application.</span></span>


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



<span data-ttu-id="a11a1-122">Em seguida, o aplicativo cria o objeto [**RealTimeStylus**](realtimestylus-class.md) que é usado para receber notificações da caneta e adiciona o objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) à fila de notificação de plug-in síncrona.</span><span class="sxs-lookup"><span data-stu-id="a11a1-122">Next, the application creates the [**RealTimeStylus**](realtimestylus-class.md) object that is used to receive stylus notifications and adds the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object to the synchronous plug-in notification queue.</span></span> <span data-ttu-id="a11a1-123">Especificamente, `myRealTimeStylus` `myDynamicRenderer` o adiciona à propriedade [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-123">Specifically, `myRealTimeStylus` adds `myDynamicRenderer` to the [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) property.</span></span>


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



<span data-ttu-id="a11a1-124">O formulário é então adicionado à fila de notificação de plug-ins assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a11a1-124">The form is then added to the asynchronous plug-in notification queue.</span></span> <span data-ttu-id="a11a1-125">Especificamente, `InkCollection` é adicionado à propriedade [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-125">Specifically, `InkCollection` is added to the [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) property.</span></span> <span data-ttu-id="a11a1-126">Por fim, `myRealTimeStylus` e `myDynamicRenderer` estão habilitados e os meus pacotes e myInk são instanciados.</span><span class="sxs-lookup"><span data-stu-id="a11a1-126">Finally, `myRealTimeStylus` and `myDynamicRenderer` are enabled, and myPackets and myInk are instantiated.</span></span>


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



<span data-ttu-id="a11a1-127">Além de conectar os manipuladores de menu para alterar a cor e o tamanho da tinta, um bloco de código mais curto é necessário antes de implementar a interface.</span><span class="sxs-lookup"><span data-stu-id="a11a1-127">Aside from hooking up the menu handlers for changing ink color and size, one more brief block of code is required before implementing the interface.</span></span> <span data-ttu-id="a11a1-128">O exemplo deve manipular o evento de [pintura](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) do formulário.</span><span class="sxs-lookup"><span data-stu-id="a11a1-128">The sample must handle the form's [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event.</span></span> <span data-ttu-id="a11a1-129">No manipulador de eventos, o aplicativo deve ser atualizado `myDynamicRenderer` porque é possível que um objeto [Stroke](/previous-versions/ms552692(v=vs.100)) esteja sendo coletado no momento em que o evento de pintura ocorrer.</span><span class="sxs-lookup"><span data-stu-id="a11a1-129">In the event handler, the application must refresh `myDynamicRenderer` because it is possible that a [Stroke](/previous-versions/ms552692(v=vs.100)) object is being collected at the time the Paint event occurs.</span></span> <span data-ttu-id="a11a1-130">Nesse caso, a parte do objeto Stroke que já foi coletado precisa ser redesenhada.</span><span class="sxs-lookup"><span data-stu-id="a11a1-130">In that case, the portion of the Stroke object that has already been collected needs to be redrawn.</span></span> <span data-ttu-id="a11a1-131">O [renderizador](/previous-versions/ms828481(v=msdn.10)) estático é usado para redesenhar objetos Stroke que já foram coletados.</span><span class="sxs-lookup"><span data-stu-id="a11a1-131">The static [Renderer](/previous-versions/ms828481(v=msdn.10)) is used to re-draw Stroke objects that have already been collected.</span></span> <span data-ttu-id="a11a1-132">Esses traços estão no objeto de [tinta](/previous-versions/aa515768(v=msdn.10)) porque eles são colocados lá quando desenhados, conforme mostrado na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="a11a1-132">These strokes are in the [Ink](/previous-versions/aa515768(v=msdn.10)) object because they are placed there when drawn, as shown in the next section.</span></span>


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a><span data-ttu-id="a11a1-133">Implementando a interface IStylusAsyncPlugin</span><span class="sxs-lookup"><span data-stu-id="a11a1-133">Implementing the IStylusAsyncPlugin Interface</span></span>

<span data-ttu-id="a11a1-134">O aplicativo de exemplo define os tipos de notificações que ele tem interesse em receber na implementação da propriedade [DataInterest](/previous-versions/ms824769(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-134">The sample application defines the types of notifications it has interest in receiving in the implementation of the [DataInterest](/previous-versions/ms824769(v=msdn.10)) property.</span></span> <span data-ttu-id="a11a1-135">Portanto, a propriedade DataInterest define quais notificações o objeto [**RealTimeStylus**](realtimestylus-class.md) encaminha para o formulário.</span><span class="sxs-lookup"><span data-stu-id="a11a1-135">The DataInterest property therefore defines which notifications that the [**RealTimeStylus**](realtimestylus-class.md) object forwards to the form.</span></span> <span data-ttu-id="a11a1-136">Para este exemplo, a propriedade DataInterest define interesse em **StylusDown**, **pacotes**, **StylusUp** e notificações de **erro** por meio da enumeração [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-136">For this sample, the DataInterest property defines interest in the **StylusDown**, **Packets**, **StylusUp**, and **Error** notifications through the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span>


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
```



<span data-ttu-id="a11a1-137">A notificação [StylusDown](/previous-versions/ms824779(v=msdn.10)) ocorre quando a caneta toca na superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="a11a1-137">The [StylusDown](/previous-versions/ms824779(v=msdn.10)) notification occurs when the pen touches the digitizer surface.</span></span> <span data-ttu-id="a11a1-138">Quando isso acontece, o exemplo aloca uma matriz que é usada para armazenar os dados do pacote para o objeto da [caneta](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-138">When this happens, the sample allocates an array that is used to store the packet data for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="a11a1-139">O [StylusDownData](/previous-versions/ms824107(v=msdn.10)) do método StylusDown é adicionado à matriz e a matriz é inserida na tabela de hash usando a propriedade [ID](/previous-versions/ms824826(v=msdn.10)) do objeto Stylus como uma chave.</span><span class="sxs-lookup"><span data-stu-id="a11a1-139">The [StylusDownData](/previous-versions/ms824107(v=msdn.10)) from the StylusDown method is added to the array, and the array is inserted into the hashtable by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as a key.</span></span>


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



<span data-ttu-id="a11a1-140">A notificação de [pacotes](/previous-versions/ms824773(v=msdn.10)) ocorre quando a caneta se move na superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="a11a1-140">The [Packets](/previous-versions/ms824773(v=msdn.10)) notification occurs when the pen moves on the digitizer surface.</span></span> <span data-ttu-id="a11a1-141">Quando isso ocorre, o aplicativo adiciona novo [StylusDownData](/previous-versions/ms824107(v=msdn.10)) à matriz de pacotes para o objeto da [caneta](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a11a1-141">When this occurs, the application adds new [StylusDownData](/previous-versions/ms824107(v=msdn.10)) into the packet array for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="a11a1-142">Ele faz isso usando a propriedade [ID](/previous-versions/ms824826(v=msdn.10)) do objeto Stylus como a chave para recuperar a matriz de pacotes para a caneta da tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a11a1-142">It does this by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as the key to retrieve the packet array for the stylus from the hashtable.</span></span> <span data-ttu-id="a11a1-143">Os novos dados de pacote são inseridos na matriz recuperada.</span><span class="sxs-lookup"><span data-stu-id="a11a1-143">The new packet data is then inserted into the retrieved array.</span></span>


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



<span data-ttu-id="a11a1-144">A notificação [StylusUp](/previous-versions/ms824782(v=msdn.10)) ocorre quando a caneta sai da superfície digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="a11a1-144">The [StylusUp](/previous-versions/ms824782(v=msdn.10)) notification occurs when the pen leaves the digitizer surface.</span></span> <span data-ttu-id="a11a1-145">Quando essa notificação ocorre, o exemplo recupera a matriz de pacotes para esse objeto de [caneta](/previous-versions/ms824824(v=msdn.10)) da tabela de hash, removendo-a da tabela de hash, pois ela não é mais necessária, adiciona os novos dados de pacote e usa a matriz de dados de pacote para criar um novo objeto [Stroke](/previous-versions/ms552692(v=vs.100)) , `stroke` .</span><span class="sxs-lookup"><span data-stu-id="a11a1-145">When this notification occurs, the sample retrieves the packet array for this [Stylus](/previous-versions/ms824824(v=msdn.10)) object from the hashtable-removing it from the hashtable as it is no longer needed, adds in the new packet data, and uses the array of packet data to create a new [Stroke](/previous-versions/ms552692(v=vs.100)) object, `stroke`.</span></span>


```C++
public void StylusUp(RealTimeStylus sender, StylusUpData data)
{
    ArrayList collectedPackets = (ArrayList)myPackets[data.Stylus.Id];
    myPackets.Remove(data.Stylus.Id);

    collectedPackets.AddRange(data.GetData());

    int[] packets = (int[])(collectedPackets.ToArray(typeof(int)));
    TabletPropertyDescriptionCollection tabletProperties =
        myRealTimeStylus.GetTabletPropertyDescriptionCollection(data.Stylus.TabletContextId);

    Stroke stroke = myInk.CreateStroke(packets, tabletProperties);
    if (stroke != null) 
    {
         stroke.DrawingAttributes.Color = myDynamicRenderer.DrawingAttributes.Color;
         stroke.DrawingAttributes.Width = myDynamicRenderer.DrawingAttributes.Width;
    } 
}
```



<span data-ttu-id="a11a1-146">Para obter um exemplo que mostra o uso mais robusto da classe [**RealTimeStylus**](realtimestylus-class.md) , incluindo o uso de criação de plug-in personalizado, consulte [exemplo de plug-in do RealTimeStylus](realtimestylus-plug-in-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a11a1-146">For an example that shows more robust use of the [**RealTimeStylus**](realtimestylus-class.md) class, including the use of custom plug-in creation, see [RealTimeStylus Plug-in Sample](realtimestylus-plug-in-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a11a1-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a11a1-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a11a1-148">[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="a11a1-148">[Microsoft.Ink.Renderer](/previous-versions/ms552630(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="a11a1-149">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a11a1-149">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="a11a1-150">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a11a1-150">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="a11a1-151">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a11a1-151">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="a11a1-152">Acessando e manipulando a entrada da caneta</span><span class="sxs-lookup"><span data-stu-id="a11a1-152">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
