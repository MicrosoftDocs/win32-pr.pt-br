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
# <a name="realtimestylus-ink-collection-sample"></a>Exemplo de coleção de tinta do RealTimeStylus

Este aplicativo demonstra a coleta de tinta e a renderização ao usar a classe [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="the-inkcollection-project"></a>O projeto InkCollection

Este exemplo consiste em uma única solução que contém um projeto, InkCollection. O aplicativo define o `InkCollection` namespace que contém uma única classe, também chamada de `InkCollection` . A classe herda da classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e implementa a interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



A classe InkCollection define um conjunto de constantes privadas usadas para especificar várias espessuras de tinta. A classe também declara instâncias privadas da classe [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , a classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` e a classe [Renderer](/previous-versions/ms828481(v=msdn.10)) `myRenderer` . O **DynamicRenderer** renderiza o [traço](/previous-versions/ms552692(v=vs.100)) que está sendo coletado no momento. O objeto Renderer, `myRenderer` , renderiza objetos Stroke que já foram coletados.


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



A classe também declara um objeto [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` , que é usado para armazenar dados de pacote que estão sendo coletados por um ou mais objetos de [cursor](/previous-versions/ms552104(v=vs.100)) . Os valores de [ID](/previous-versions/ms824826(v=msdn.10)) do objeto de [caneta](/previous-versions/ms824824(v=msdn.10)) são usados como a chave de Hashtable para identificar exclusivamente os dados de pacote coletados para um determinado objeto de cursor.

Uma instância privada do objeto [Ink](/previous-versions/aa515768(v=msdn.10)) , `myInk` , armazena objetos [Stroke](/previous-versions/ms552692(v=vs.100)) coletados pelo `myRealTimeStylus` .


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a>O evento de carregamento de formulário

No manipulador de eventos de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) para o formulário, `myDynamicRenderer` é criada uma instância usando o [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) que usa um controle como argumento e `myRenderer` é construído com um construtor sem argumento.


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



Preste atenção ao comentário que segue a instanciação dos renderizadores, porque `myDynamicRenderer` o usa os valores padrão para [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) ao renderizar a tinta. Esse é o comportamento padrão. No entanto, se você quiser fornecer a tinta renderizada por `myDynamicRenderer` uma aparência diferente da tinta renderizada pelo `myRenderer` , poderá alterar a propriedade [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) em `myDynamicRenderer` . Para fazer isso, remova os comentários das linhas a seguir antes de compilar e executar o aplicativo.


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



Em seguida, o aplicativo cria o objeto [**RealTimeStylus**](realtimestylus-class.md) que é usado para receber notificações da caneta e adiciona o objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) à fila de notificação de plug-in síncrona. Especificamente, `myRealTimeStylus` `myDynamicRenderer` o adiciona à propriedade [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) .


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



O formulário é então adicionado à fila de notificação de plug-ins assíncrona. Especificamente, `InkCollection` é adicionado à propriedade [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) . Por fim, `myRealTimeStylus` e `myDynamicRenderer` estão habilitados e os meus pacotes e myInk são instanciados.


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



Além de conectar os manipuladores de menu para alterar a cor e o tamanho da tinta, um bloco de código mais curto é necessário antes de implementar a interface. O exemplo deve manipular o evento de [pintura](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) do formulário. No manipulador de eventos, o aplicativo deve ser atualizado `myDynamicRenderer` porque é possível que um objeto [Stroke](/previous-versions/ms552692(v=vs.100)) esteja sendo coletado no momento em que o evento de pintura ocorrer. Nesse caso, a parte do objeto Stroke que já foi coletado precisa ser redesenhada. O [renderizador](/previous-versions/ms828481(v=msdn.10)) estático é usado para redesenhar objetos Stroke que já foram coletados. Esses traços estão no objeto de [tinta](/previous-versions/aa515768(v=msdn.10)) porque eles são colocados lá quando desenhados, conforme mostrado na próxima seção.


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a>Implementando a interface IStylusAsyncPlugin

O aplicativo de exemplo define os tipos de notificações que ele tem interesse em receber na implementação da propriedade [DataInterest](/previous-versions/ms824769(v=msdn.10)) . Portanto, a propriedade DataInterest define quais notificações o objeto [**RealTimeStylus**](realtimestylus-class.md) encaminha para o formulário. Para este exemplo, a propriedade DataInterest define interesse em **StylusDown**, **pacotes**, **StylusUp** e notificações de **erro** por meio da enumeração [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .


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



A notificação [StylusDown](/previous-versions/ms824779(v=msdn.10)) ocorre quando a caneta toca na superfície digitalizadora. Quando isso acontece, o exemplo aloca uma matriz que é usada para armazenar os dados do pacote para o objeto da [caneta](/previous-versions/ms824824(v=msdn.10)) . O [StylusDownData](/previous-versions/ms824107(v=msdn.10)) do método StylusDown é adicionado à matriz e a matriz é inserida na tabela de hash usando a propriedade [ID](/previous-versions/ms824826(v=msdn.10)) do objeto Stylus como uma chave.


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



A notificação de [pacotes](/previous-versions/ms824773(v=msdn.10)) ocorre quando a caneta se move na superfície digitalizadora. Quando isso ocorre, o aplicativo adiciona novo [StylusDownData](/previous-versions/ms824107(v=msdn.10)) à matriz de pacotes para o objeto da [caneta](/previous-versions/ms824824(v=msdn.10)) . Ele faz isso usando a propriedade [ID](/previous-versions/ms824826(v=msdn.10)) do objeto Stylus como a chave para recuperar a matriz de pacotes para a caneta da tabela de hash. Os novos dados de pacote são inseridos na matriz recuperada.


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



A notificação [StylusUp](/previous-versions/ms824782(v=msdn.10)) ocorre quando a caneta sai da superfície digitalizadora. Quando essa notificação ocorre, o exemplo recupera a matriz de pacotes para esse objeto de [caneta](/previous-versions/ms824824(v=msdn.10)) da tabela de hash, removendo-a da tabela de hash, pois ela não é mais necessária, adiciona os novos dados de pacote e usa a matriz de dados de pacote para criar um novo objeto [Stroke](/previous-versions/ms552692(v=vs.100)) , `stroke` .


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



Para obter um exemplo que mostra o uso mais robusto da classe [**RealTimeStylus**](realtimestylus-class.md) , incluindo o uso de criação de plug-in personalizado, consulte [exemplo de plug-in do RealTimeStylus](realtimestylus-plug-in-sample.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Acessando e manipulando a entrada da caneta](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
