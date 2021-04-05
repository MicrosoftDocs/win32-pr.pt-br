---
description: O Windows Server 2008 R2 adiciona suporte para o reconhecimento de manuscrito do lado do servidor no Windows. Este tópico descreve como reconhecer manuscritos no Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Reconhecimento de manuscrito no Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008563"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a>Reconhecimento de manuscrito no Windows Server 2008 R2

O Windows Server 2008 R2 dá suporte ao reconhecimento de manuscrito do lado do servidor. O reconhecimento no lado do servidor permite que um servidor reconheça o conteúdo da entrada à caneta em páginas da Web. Isso é particularmente útil quando os usuários em uma rede especificam termos que são interpretados usando um dicionário personalizado. Por exemplo, se você tivesse um aplicativo médico que consultou um banco de dados de servidor para nomes de pacientes, esses nomes poderiam ser adicionados a outro banco de dados que seria referenciado de forma cruzada ao executar pesquisas de um formulário do Silverlight manuscrito.

## <a name="set-up-your-server-for-server-side-recognition"></a>Configurar o servidor para o reconhecimento de Server-Side

As etapas a seguir devem ser seguidas para configurar o reconhecimento do lado do servidor.

- Instalar Serviços de Reconhecimento de Manuscrito
- Instalar o suporte para o servidor Web (IIS) e o servidor de aplicativos
- Habilitar a função de experiência desktop
- Iniciar o serviço de entrada do Tablet PC

### <a name="install-ink-and-handwriting-services"></a>Instalar Serviços de Reconhecimento de Manuscrito

Para instalar os serviços de tinta e manuscrito, abra o Gerenciador de servidores clicando no ícone Gerenciador de servidores na bandeja de início rápido. No menu **recursos** , clique em **Adicionar recursos**. Certifique-se de marcar a caixa de seleção **serviços de reconhecimento de manuscrito** . A imagem a seguir mostra a caixa de diálogo **selecionar recursos** com **serviços de reconhecimento de manuscrito** selecionado.

![Caixa de diálogo Selecionar recursos com a caixa de seleção serviços de tinta e manuscrito marcada](images/setup-server-1-ink-and-handwriting.png)<br/>
*Caixa de diálogo Selecionar recursos com a caixa de seleção serviços de tinta e manuscrito marcada*

### <a name="installation-support-for-web-server-iis-and-application-server"></a>Suporte para instalação do servidor Web (IIS) e servidor de aplicativos

Abra o Gerenciador de servidores como você fez para a primeira etapa. Em seguida, você precisará adicionar o servidor Web (IIS) e as funções de servidor de aplicativos. No menu **funções** , clique em **adicionar funções**. O assistente para adicionar funções é exibido. Clique em **Próximo**. Verifique se **servidor de aplicativos** e **servidor Web (IIS)** estão selecionados. A imagem a seguir mostra a caixa de diálogo **selecionar funções de servidor** com o **servidor Web (IIS)** e funções de **servidor de aplicativos** selecionadas.

![Caixa de diálogo Selecionar funções de servidor com servidor Web (IIS) e funções de servidor de aplicativos selecionadas](images/setup-server-2-select-server-roles.png)<br/>
*Caixa de diálogo Selecionar funções de servidor com servidor Web (IIS) e funções de servidor de aplicativos selecionadas*

Ao selecionar **servidor de aplicativos**, você será solicitado a instalar a estrutura ASP.net. Clique no botão **Adicionar recursos necessários** . Depois de clicar em **Avançar**, você verá uma caixa de diálogo visão geral; clique em **Avançar**. A caixa de diálogo **selecionar serviços de função** agora deve estar disponível. Verifique se o **servidor Web (IIS)** está selecionado. A imagem a seguir mostra a caixa de diálogo **selecionar serviços de função** com o servidor Web (IIS) habilitado.

![Caixa de diálogo Selecionar Serviços de função com o servidor Web (IIS) habilitado](images/setup-server-3-select-role-services.png)<br/>
*Caixa de diálogo Selecionar Serviços de função com o servidor Web (IIS) habilitado*

Clique em **Próximo**. Uma caixa de diálogo visão geral é exibida; clique em **Avançar** novamente. Agora você verá uma página que oferece opções para funções para o servidor Web (IIS). Clique em **Próximo**. Na próxima página, o botão **instalar** ficará ativo. Clique em **instalar** e você instalará o suporte para o servidor Web (IIS) e o servidor de aplicativos.

### <a name="enable-the-desktop-experience-role"></a>Habilitar a função de experiência desktop

Para habilitar a experiência desktop, clique em **Iniciar**, **Ferramentas administrativas** e, em seguida, clique em **Gerenciador do servidor**. Selecione **Adicionar serviços** e, em seguida, selecione o serviço **experiência desktop** . A imagem a seguir mostra a caixa de diálogo **selecionar recursos** com o item de experiência desktop instalado.

![Caixa de diálogo Selecionar recursos com o serviço de experiência de área de trabalho selecionado](images/setup-server-4-desktop-experience.png)<br/>
*Caixa de diálogo Selecionar recursos com o serviço de experiência de área de trabalho selecionado*

Clique em **Avançar** para instalar a experiência desktop.

### <a name="start-the-tablet-service"></a>Iniciar o serviço do Tablet

Depois de instalar o serviço de experiência desktop, o serviço de entrada do Tablet PC será exibido no menu **Serviços** . Para acessar o menu **Serviços** , clique em **Iniciar**, **Ferramentas administrativas** e, em seguida, clique em **Serviços**. Para iniciar o serviço, clique com o botão direito do mouse em **serviço de entrada do Tablet PC** e clique em **Iniciar**. A imagem a seguir mostra o menu **Serviços** com o serviço de entrada do Tablet PC iniciado.

![Menu de serviços com o serviço de entrada do Tablet PC iniciado](images/setup-server-5-tablet-pc-input-service.png)<br/>
*Menu de serviços com o serviço de entrada do Tablet PC iniciado*

## <a name="performing-server-side-recognition-using-silverlight"></a>Executando o reconhecimento de Server-Side usando o Silverlight

Esta seção mostra como criar um aplicativo Web que usa o Silverlight para capturar a entrada de manuscrito. Use as etapas a seguir para programar o reconhecedor no Visual Studio 2008.

- Instale e atualize o Visual Studio 2008 para adicionar suporte ao Silverlight.
- Crie um novo projeto do Silverlight no Visual Studio 2008.
- Adicione as referências de serviço necessárias ao seu projeto.
- Crie um serviço WCF do Silverlight para reconhecimento de tinta.
- Adicione a referência de serviço ao seu projeto de cliente.
- Adicione a classe InkCollector ao projeto InkRecognition.
- Remover diretivas de transporte seguras da configuração do cliente

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a>Instalar e atualizar o Visual Studio 2008 para adicionar suporte ao Silverlight

Antes de começar, você deve executar as etapas a seguir no servidor Windows Server 2008 R2.

- Instale o Visual Studio 2008.
- Instale o [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).
- Instale [o SDK do Microsoft Silverlight 5](https://www.microsoft.com/silverlight/).

Depois de instalar esses aplicativos e atualizações, você estará pronto para criar o aplicativo Web de reconhecimento do lado do servidor.

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a>Criar um novo projeto Web do Silverlight no Visual Studio 2008

No menu **Arquivo**, clique em **Novo Projeto**. Selecione o modelo de aplicativo do Silverlight na lista de projetos do Visual C \# . Nomeie o projeto InkRecognition e clique em **OK**. A imagem a seguir mostra o \# projeto C Silverlight selecionado e nomeado InkRecognition.

![\#projeto Silverlight c selecionado, com o nome InkRecognition](images/project-1-new-project.png)<br/>
*\#projeto Silverlight c selecionado, com o nome InkRecognition*

Depois de clicar em **OK**, uma caixa de diálogo solicitará que você adicione um aplicativo do Silverlight ao seu projeto. Selecione **Adicionar um novo projeto Web ASP.net à solução para hospedar o Silverlight** e clique em **OK**. A imagem a seguir mostra como configurar o projeto de exemplo antes de clicar em **OK**.

![Caixa de diálogo com solicitação para adicionar um aplicativo do Silverlight a um projeto](images/project-2-add-a-new-aspnetproject.png)<br/>
*Caixa de diálogo com solicitação para adicionar um aplicativo do Silverlight a um projeto*

### <a name="add-the-necessary-service-references-to-your-project"></a>Adicionar as referências de serviço necessárias ao seu projeto

Agora você tem o projeto de cliente Silverlight genérico (InkRecognition) com um projeto Web (InkRecognition. Web) configurado em sua solução. O projeto será aberto com Page. XAML e default. aspx aberto. Feche essas janelas e adicione as referências System. Runtime. Serialization e System. ServiceModel ao projeto InkRecognition clicando com o botão direito do mouse na pasta referências no projeto InkRecognition e selecionando **Adicionar referência**. A imagem a seguir mostra a caixa de diálogo com as referências de requisito selecionadas.

![Caixa de diálogo Adicionar referências com System. Runtime. Serialization e System. ServiceModel selecionados](images/project-3a-add-references-to-inkreco.png)<br/>
*Caixa de diálogo Adicionar referências com System. Runtime. Serialization e System. ServiceModel selecionados*

Em seguida, você precisa adicionar as referências de System. ServiceModel e Microsoft. Ink ao projeto InkRecognition. Web. A referência de Microsoft. Ink não aparecerá nas referências do .NET por padrão, portanto, pesquise a pasta do Windows para Microsoft.Ink.dll. Depois de localizar a DLL, adicione o assembly às referências do projeto: selecione a guia **procurar** , altere para a pasta que contém Microsoft.Ink.dll, selecione Microsoft.Ink.dll e clique em **OK**. A imagem a seguir mostra a solução do projeto no Windows Explorer com todos os assemblies de referência adicionados.

![projeto InkRecognition no Windows Explorer com todos os assemblies de referência adicionados](images/project-3b-with-reference-assemblies.png)<br/>
*projeto InkRecognition no Windows Explorer com todos os assemblies de referência adicionados*

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a>Criar um serviço WCF do Silverlight para reconhecimento de tinta

Em seguida, você adicionará um serviço WCF para reconhecimento de tinta ao projeto. Clique com o botão direito do mouse no projeto InkRecognition. Web, clique em **Adicionar** e em **novo item**. Selecione o modelo de serviço WCF Silverlight, altere o nome para InkRecogitionService e clique em **Adicionar**. A imagem a seguir mostra a caixa de diálogo **Adicionar novo item** com o serviço WCF do Silverlight selecionado e nomeado.

![Caixa de diálogo Adicionar novo item com o serviço WCF do Silverlight selecionado e nomeado](images/project-4-add-wcf-service.png)<br/>
*Caixa de diálogo Adicionar novo item com o serviço WCF do Silverlight selecionado e nomeado*

Depois de adicionar o serviço WCF Silverlight, o código de serviço por trás do, InkRecognitionService. cs, será aberto. Substitua o código do serviço pelo código a seguir.

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a>Adicionar a referência de serviço ao seu projeto de cliente

Agora que você tem o serviço WCF do Silverlight para InkRecognition, você consumirá o serviço do seu aplicativo cliente. Clique com o botão direito do mouse no projeto InkRecognition e selecione **Adicionar referência de serviço**. Na caixa de diálogo **Adicionar referência de serviço** exibida, selecione **descobrir** para descobrir serviços da solução atual. InkRecognitionService aparecerá no painel serviços. Clique duas vezes em InkRecognitionService no painel serviços, altere o namespace para InkRecognitionServiceReference e clique em **OK**. A imagem a seguir mostra a caixa de diálogo **Adicionar referência de serviço** com InkRecognitionService selecionado e o namespace alterado.

![Caixa de diálogo Adicionar referência de serviço com inkrecognitionservice selecionado e namespace alterado](images/project-5-discover-service-reference.png)<br/>
*Caixa de diálogo Adicionar referência de serviço com inkrecognitionservice selecionado e namespace alterado*

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a>Adicionar a classe InkCollector ao projeto InkRecognition

Clique com o botão direito do mouse no projeto InkRecognition, clique em **Adicionar** e em **novo item**. No menu do **Visual \# c** , selecione **\# classe C**. Nomeie a classe como InkCollector. A imagem a seguir mostra a caixa de diálogo com a \# classe C selecionada e nomeada.

![Caixa de diálogo Adicionar novo item com a \# classe c selecionada e nomeada](images/project-6-add-ink-collector.png)<br/>
*Caixa de diálogo Adicionar novo item com a \# classe c selecionada e nomeada*

Depois de adicionar a classe InkCollector, a definição de classe será aberta. Substitua o código no coletor de tinta pelo código a seguir.

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a>Atualizar o XAML para a página padrão e adicionar um code-behind para reconhecimento de manuscrito

Agora que você tem uma classe que coleta tinta, será necessário atualizar o XAML em Page. XAML com o XAML a seguir. O código a seguir adiciona um gradiente amarelo à área de entrada, um controle InkCanvas e um botão que irá disparar o reconhecimento.

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

Substitua a página code-behind, Page. XAML. cs, pelo código a seguir, que adicionará um manipulador de eventos para o botão **reconhecer** .

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a>Remover diretivas de transporte seguras da configuração do cliente

Antes de consumir o serviço WCF, você deve remover todas as opções de transporte seguro da configuração de serviço, pois os transportes seguros atualmente não têm suporte nos serviços WCF do Silverlight 2,0. No projeto InkRecognition, atualize as configurações de segurança em perreferences. ClientConfig. Alterar o XML de segurança de

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

como

```XML
       <security mode="None"/>
```

Agora, seu aplicativo deve ser executado. A imagem a seguir mostra como o aplicativo aparece em awebpagewith algum manuscrito inserido na caixa de reconhecimento.

![Aplicativo em awebpagewith algum manuscrito inserido na caixa de reconhecimento](images/demo-1.png)<br/>
*Aplicativo em awebpagewith algum manuscrito inserido na caixa de reconhecimento*

A imagem a seguir mostra o texto reconhecido na lista suspensa **resultado** .

![Aplicativo em awebpagewith texto reconhecido na lista suspensa de resultados](images/demo-2.png)<br/>
*Aplicativo em awebpagewith texto reconhecido na lista suspensa de resultados*

 

 



