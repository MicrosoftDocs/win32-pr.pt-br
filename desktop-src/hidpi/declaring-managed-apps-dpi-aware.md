---
title: Desenvolver um aplicativo WPF com reconhecimento de DPI por monitor
description: Observação Esta página aborda o desenvolvimento WPF herdado para Windows 8.1. Se você estiver desenvolvendo aplicativos do WPF para o Windows 10, consulte a documentação mais recente no GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Interface do usuário do Windows, aplicativos com reconhecimento de DPI
- Interface do usuário do Windows, DPI alto
- Aplicativos com reconhecimento de DPI
- DPI alto
- Escrevendo aplicativos Win32 com reconhecimento de DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084543"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>Desenvolver um aplicativo WPF com reconhecimento de DPI por monitor

**APIs importantes**

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **Esta página aborda o desenvolvimento WPF herdado para Windows 8.1.** Se você estiver desenvolvendo aplicativos do WPF para o Windows 10, consulte a <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentação mais recente no github.</a>

 

O Windows 8.1 oferece aos desenvolvedores novas funcionalidades para criar aplicativos de área de trabalho que reconhecem o DPI por monitor. Para aproveitar essa funcionalidade, um aplicativo com reconhecimento de DPI por monitor deve fazer o seguinte:

-   Alterar as dimensões da janela para manter um tamanho físico que pareça consistente em qualquer exibição
-   Refazer layout e renderizar novamente os gráficos para o novo tamanho da janela
-   Selecionar as fontes que são dimensionadas adequadamente para o nível de DPI
-   Selecionar e carregar ativos de bitmap que são personalizados para o nível de DPI

Para facilitar a criação de um aplicativo com reconhecimento de DPI por monitor, o Windows 8.1 fornece o seguinte Win32APIs da Microsoft:

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (ou entrada de manifesto de DPI) define o processo para um nível de reconhecimento de DPI especificado, que determina como o Windows dimensiona a interface do usuário. Isso substitui [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) retorna o nível de reconhecimento de DPI. Isso substitui [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) retorna o DPI de um monitor.
-   A notificação da janela do [**WM \_ DPICHANGED**](wm-dpichanged.md) é enviada para aplicativos com reconhecimento de DPI por monitor quando a posição de uma janela é alterada de modo que a maior parte de sua área cruza um monitor com um DPI diferente do DPI antes da alteração da posição ou quando o usuário move o controle deslizante de exibição. Para criar um aplicativo que seja redimensionado e renderizado novamente quando um usuário o mover para uma exibição diferente, use essa notificação.

Para obter mais detalhes sobre vários níveis de reconhecimento de DPI com suporte para aplicativos de área de trabalho no Windows 8.1 consulte o tópico [escrevendo DPI-Aware desktop e aplicativos Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

## <a name="dpi-scaling-and-wpf"></a>Escala de DPI e WPF

Os aplicativos Windows Presentation Foundation (WPF) são, por padrão, reconhecem o DPI do sistema. Para obter definições dos diferentes níveis de reconhecimento de DPI, consulte o tópico [escrevendo DPI-Aware aplicativos de área de trabalho e Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)). O sistema de gráficos do WPF usa unidades independentes de dispositivo para habilitar a resolução e a independência do dispositivo. O WPF dimensiona cada pixel independente de dispositivo automaticamente com base no DPI atual do sistema. Isso permite que os aplicativos do WPF sejam dimensionados automaticamente quando a DPI do monitor em que a janela está estiver no mesmo DPI do sistema. No entanto, como os aplicativos WPF são reconhecendo o DPI do sistema, o aplicativo será dimensionado pelo sistema operacional quando o aplicativo for movido para um monitor com um DPI diferente ou quando o controle deslizante no painel de controle for usado para alterar o DPI. O dimensionamento no sistema operacional pode fazer com que os aplicativos WPF pareçam borrados, especialmente quando o dimensionamento é não integral. Para evitar o dimensionamento de aplicativos do WPF, eles precisam ser atualizados para que haja reconhecimento de DPI por monitor.

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>Instruções de exemplo de WPF de acordo com reconhecimento de monitor

O [exemplo de WPF com reconhecimento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) é um aplicativo WPF de exemplo atualizado para ser compatível com dpi por monitor. O exemplo consiste em dois projetos:

-   NativeHelpers. vcxproj: Este é um projeto auxiliar nativo que implementa a funcionalidade básica para criar um aplicativo WPF como reconhecimento de DPI por monitor utilizando o Win32APIs acima. O projeto contém duas classes:
    -   PerMonDPIHelpers: uma classe que fornece funções auxiliares para operações relacionadas a DPI, como recuperar o DPI atual do monitor ativo, definindo um processo para ser compatível com DPI por meio do monitor, etc.
    -   PerMonitorDPIWindow: uma classe base derivada de **System. Windows. Window** que implementa a funcionalidade para fazer com que uma janela do aplicativo WPF seja compatível com dpi por monitor. Ajusta o tamanho da janela, o tamanho da renderização de gráficos e o tamanho da fonte com base no DPI do monitor em vez do DPI do sistema.
-   WPFApplication. csproj: aplicativo de exemplo do WPF que consome o PerMonitorDPIWindow (PerMonitorDPIWindow) e mostra como a janela do aplicativo e a renderização são redimensionadas quando a janela é movida para um monitor com um DPI diferente ou quando o controle deslizante no painel de controle de exibição é usado para alterar o DPI.

Para executar o exemplo, siga as etapas abaixo:

1.  Baixar e descompactar o [exemplo de WPF com reconhecimento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
2.  Iniciar Microsoft Visual Studio e selecionar **arquivo > abrir > projeto/solução**
3.  Navegue até o diretório que contém o exemplo descompactado. Vá para o diretório chamado para o exemplo e clique duas vezes no arquivo da solução do Visual Studio (. sln)
4.  Pressione F7 ou use **compilar > Compilar solução** para criar o exemplo
5.  Pressione CTRL + F5 ou use **Debug > iniciar sem depuração** para executar o exemplo

Para ver o impacto da alteração de DPI em um aplicativo do WPF que é atualizado para ter reconhecimento de DPI por monitor usando a classe base no exemplo, mova a janela do aplicativo para e de exibições que tenham DPIs diferentes. À medida que a janela é movida entre monitores, o tamanho da janela e a escala da interface do usuário são atualizados com base no DPI da exibição usando o sistema gráfico escalonável do WPF, em vez de ser dimensionado pelo sistema operacional. A interface do usuário do aplicativo é renderizada nativamente e não aparece borrada. Se você não tiver dois monitores com DPI diferente, altere o DPI alterando o controle deslizante no painel de controle de exibição. Alterar o controle deslizante e clicar em **aplicar** redimensionará a janela do aplicativo e atualizará a escala da interface do usuário automaticamente.

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>Atualizando um aplicativo existente do WPF para ter reconhecimento de DPI por monitor usando o projeto auxiliar no exemplo do WPF

Se você tiver um aplicativo existente do WPF e desejar aproveitar o projeto auxiliar de DPI do exemplo para torná-lo ciente de DPI, siga estas etapas.

1.  Baixar e descompactar o exemplo de WPF com reconhecimento de monitor
2.  Inicie o Visual Studio e selecione **arquivo > abrir > projeto/solução**
3.  Navegue até o diretório que contém um aplicativo existente do WPF e clique duas vezes no arquivo da solução do Visual Studio (. sln)
4.  Clique com o botão direito do mouse em **solução > adicionar > projeto existente** ![ uma captura de tela que ilustra a seleção de menu Adicionar: projeto existente](images/scrvs-image1.png)
5.  Na caixa de diálogo seleção de arquivo, navegue até o diretório que contém o exemplo descompactado. Abra o diretório chamado para o exemplo, navegue até a pasta "NativeHelpers", selecione o arquivo de projeto Visual C++ "NativeHelpers. vcxproj" e clique em **OK**
6.  Clique com o botão direito do mouse no projeto NativeHelpers e selecione **Compilar**. Isso irá gerar NativeHelpers.dll que serão adicionadas como uma referência ao aplicativo do WPF na próxima etapa ![ uma captura de tela ilustrando a seleção do menu Build](images/scrvs-image2.png)
7.  Adicione uma referência a NativeHelpers.dll de seu aplicativo WPF. Expanda seu projeto de aplicativo WPF, clique com o botão direito do mouse em **referências** e clique em **Adicionar referência..** .
8.  Na caixa de diálogo resultante, expanda a seção **solução** . Em **projetos**, selecione NativeHelpers e clique em **OK** ![ uma captura de tela ilustrando a caixa de diálogo do Resource Manager](images/scrvs-image3.png)
9.  Expanda seu projeto de aplicativo WPF, expanda **Propriedades** e abra **AssemblyInfo. cs**. Faça as seguintes adições ao AssemblyInfo. cs
    -   Adicione referência a System. Windows. Media na seção de referência (usando System. Windows. Media;)
    -   Adicionar o atributo DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )

    ![uma captura de tela que ilustra as propriedades adicionais](images/scrvs-image4.png)
10. Herdar a classe de janela principal do WPF da classe base PerMonitorDPIWindow
    -   Atualize o arquivo. cs da janela principal do WPF para herdar da classe base PerMonitorDPIWindow
        -   Adicione uma referência a NativeHelpers na seção de referência adicionando a linha `using NativeHelpers;`
        -   Herdar a classe de janela principal da classe PerMonitorDPIWindow

        ![uma captura de tela ilustrando a referência do c++](images/scrvs-image5.png)
    -   Atualize o arquivo. XAML da janela principal do WPF para herdar da classe base PerMonitorDPIWindow
        -   Adicione uma referência a NativeHelpers na seção de referência adicionando a linha `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   Herdar a classe de janela principal da classe PerMonitorDPIWindow

        ![uma captura de tela ilustrando a adição da referência. XAML](images/scrvs-image6.png)
11. Pressione F7 ou use **compilar > Compilar solução** para criar o exemplo
12. Pressione CTRL + F5 ou use **Debug > iniciar sem depuração** para executar o exemplo

O aplicativo de [exemplo do WPF com reconhecimento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) ilustra como um aplicativo do WPF pode ser atualizado para que haja reconhecimento de DPI por monitor respondendo à notificação da janela [**\_ DPICHANGED do WM**](wm-dpichanged.md) . Em resposta à notificação de janela, o exemplo atualiza a transformação de escala usada pelo WPF com base no DPI atual do monitor em que a janela está. O *wParam* da notificação de janela contém o novo dpi no *wParam*. O *lParam* contém um retângulo que tem o tamanho e a posição da nova janela sugerida, dimensionada para o novo dpi.

Observação:

> [!Note]  
> Como este exemplo substitui o tamanho da janela e a transformação de escala do nó raiz da janela do WPF, o trabalho adicional pode ser exigido pelo desenvolvedor do aplicativo se:
>
> -   O tamanho da janela afeta outras partes do aplicativo como esta janela do WPF sendo hospedada dentro de outro aplicativo.
> -   O aplicativo WPF que está estendendo essa classe está definindo outra transformação no Visual raiz; o exemplo pode substituir alguma outra transformação que está sendo aplicada pelo próprio aplicativo WPF.

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>Visão geral do projeto auxiliar no exemplo do WPF

Para tornar um aplicativo existente do WPF por monitor com reconhecimento de DPI, a biblioteca NativeHelpers fornece a seguinte funcionalidade:

-   **Marca o aplicativo WPF como reconhecimento de DPI por ponitor:** O aplicativo do WPF é marcado como reconhecimento de DPI por monitor chamando [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) para o processo atual. Marcar o aplicativo como reconhecimento de DPI por monitor garantirá que

    -   O sistema operacional não dimensiona o aplicativo quando o DPI do sistema não corresponde ao DPI atual do monitor em que a janela do aplicativo está
    -   A mensagem do [**WM \_ DPICHANGED**](wm-dpichanged.md) é enviada sempre que o DPI da janela é alterado

-   **Ajusta a dimensão da janela, refazer o layout e renderizar novamente o conteúdo de gráficos e selecionar fontes com base no dpi inicial do monitor em que a janela está:** Depois que o aplicativo for marcado como com reconhecimento de DPI por monitor, o WPF ainda dimensionará o tamanho da janela, os gráficos e o tamanho da fonte com base no DPI do sistema. Desde que, na inicialização do aplicativo, não há garantia de que o DPI do sistema seja o mesmo que o DPI do monitor em que a janela é iniciada, a biblioteca ajusta esses valores depois que a janela é carregada. A classe base **PerMonitorDPIWindow** as atualiza no manipulador **OnLoaded ()** .

    O tamanho da janela é atualizado alterando as propriedades **Width** e **Height** da janela. O layout e o tamanho são atualizados com a aplicação de uma transformação de escala apropriada ao nó raiz da janela do WPF.

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   **Responde ao WM \_ Notificação da janela DPICHANGED:** atualize o tamanho da janela, os gráficos e o tamanho da fonte com base no dpi passado na notificação da janela. A classe base **PerMonitorDPIWindow** manipula a notificação de janela no método **HandleMessages ()** .

    O tamanho da janela é atualizado chamando **SetWindowPos** usando as informações passadas no *lParam* da mensagem da janela. O layout e o tamanho dos gráficos são atualizados com a aplicação de uma transformação de escala apropriada ao nó raiz da janela do WPF. O fator de escala é calculado usando o DPI passado no *wParam* da mensagem de janela.

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a>Tratamento de alteração de DPI para ativos como imagens

Para atualizar o conteúdo de gráficos, o aplicativo WPF de exemplo aplica uma transformação de escala ao nó raiz do aplicativo do WPF. Embora isso funcione bem para o conteúdo que é processado nativamente pelo WPF (Rectangle, Text etc.), isso implica que os ativos de bitmap, como as imagens, são dimensionados pelo WPF.

Para evitar bitmaps borrados causados pelo dimensionamento, o desenvolvedor de aplicativos do WPF pode gravar um controle de imagem de DPI personalizado que seleciona um ativo diferente com base na DPI atual do monitor em que a janela está. O controle de imagem pode contar com o evento **DPIChanged ()** disparado para a janela do WPF que consome do **PerMonitorDPIWindow**, quando o DPI é alterado.

> [!Note]  
> O controle de imagem também deve selecionar o controle certo durante a inicialização do aplicativo no manipulador de eventos de janela do WPF **carregado ()** .

 

 

 