---
description: Começar a aprender os conceitos básicos da criação de ótimos aplicativos da área de trabalho nesta seção.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Introdução
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f791589d73447798a7721c52164a2002b48a792959c698b835039293ce6004d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755006"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Começar a usar aplicativos Windows área de trabalho que usam a API do Win32

A API do Win32 (também chamada de API do Windows) é plataforma original para aplicativos nativos do Windows em C/C++ que exigem acesso direto ao Windows e ao hardware. Ele fornece uma experiência de desenvolvimento de primeira classe sem depender de um ambiente de runtime gerenciado, como .NET e WinRT (para aplicativos UWP para Windows 10). Isso torna a API do Win32 a plataforma preferida para aplicativos que precisam do nível mais alto de desempenho e acesso direto ao hardware do sistema.

> [!NOTE]
> Esta documentação aborda como criar aplicativos Windows área de trabalho com a API do Win32. A API do Win32 é uma das várias plataformas de aplicativo que você pode usar para criar aplicativos Windows área de trabalho. Para obter mais informações sobre outras plataformas de aplicativo, [consulte Escolher sua plataforma](/windows/apps/desktop/choose-your-platform).

## <a name="get-set-up"></a>Prepare-se para começar

Siga estas instruções e comece a criar aplicativos da área de trabalho Windows 10 que usam a API do Win32.

1. Baixe ou atualize Visual Studio 2019. Se ainda não tem o Visual Studio 2019, você pode instalar o Microsoft Visual Studio Community 2019 gratuitamente. Ao instalar o Visual Studio, selecione a opção Desenvolvimento **de área de trabalho com C++.** Para links de download, consulte nossa [página Downloads.](https://developer.microsoft.com/windows/downloads)

    > [!NOTE]
    > Ao instalar o Visual Studio, opcionalmente, você pode selecionar as opções desenvolvimento de área de trabalho **do .NET** e Desenvolvimento da Plataforma **Universal Windows** para acesso a outros tipos de projeto e plataformas de aplicativos para a criação de aplicativos Windows área de trabalho.

2. Se você quiser criar seu aplicativo da área de trabalho em um pacote [MSIX](/windows/msix/desktop/desktop-to-uwp-root) e testar ou depurar o aplicativo empacotado no computador de desenvolvimento, será necessário habilitar o Modo de Desenvolvedor no [computador.](/windows/uwp/get-started/enable-your-device-for-development)

> [!NOTE]
> Para scripts que você pode usar para configurar seu computador de desenvolvimento e instalar outros recursos ou pacotes, confira [este GitHub projeto](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Saiba como criar aplicativos da área de trabalho usando a API do Win32

Se você for novo na criação de aplicativos da área de trabalho usando a API do Win32, os tutoriais e artigos a seguir ajudarão você a começar.

| Tópico        | Descrição      |
|---------------|-----------------|
| [Criar seu primeiro aplicativo C++ Win32](LearnWin32/learn-to-program-for-windows.md)    | Este tutorial ensina a escrever um programa Windows em C++ usando APIs Win32 e COM.  |
| [Criar seu primeiro aplicativo usando o DirectX](direct3dgetstarted/building-your-first-directx-app.md) | Este tutorial básico lhe dará uma introdução ao desenvolvimento de aplicativos DirectX.            |
| [Guia de programação para 64 bits Windows](WinProg64/programming-guide-for-64-bit-windows.md)    | Descreve a programação para versões de 64 bits do Windows operacional. |
| [Usando os Windows de dados](WinProg/using-the-windows-headers.md)     | Fornece uma visão geral de algumas das convenções usadas nos arquivos de Windows de dados. |

Você também pode procurar os [exemplos de aplicativo da área de trabalho.](https://github.com/Microsoft/Windows-classic-samples)

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Modernizar seus aplicativos da área de trabalho para Windows 10

Se você tiver um aplicativo Win32 da área de trabalho existente, há muitos recursos na UWP (Plataforma Universal de Windows) que você pode usar para fornecer a melhor experiência possível no Windows 10. Por exemplo, começando no Windows 10, versão 1903, você pode hospedar controles XAML UWP em seu aplicativo Win32 da área de trabalho usando um recurso chamado Ilhas XAML.

A maioria desses recursos UWP está disponível como componentes modulares que você pode adotar em seu aplicativo da área de trabalho em seu próprio ritmo sem precisar reescrever todo o aplicativo. Você pode aprimorar seu aplicativo da área de trabalho existente escolhendo quais partes do Windows 10 e UWP adotar.

Para obter mais informações, consulte [Modernize seus aplicativos da área de trabalho](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Opcionalmente, você pode configurar seu computador de desenvolvimento para usar [o C++/WinRT.](/windows/uwp/cpp-and-winrt-apis/) O C++/WinRT é uma projeção de linguagem C++1 Windows 7 moderna totalmente padrão que permite que você consuma facilmente APIs de runtime Windows APIs do WinRT (Runtime) do seu aplicativo de área de trabalho C++ Win32. O C++/WinRT é implementado como uma biblioteca baseada em arquivo de título.

Para configurar o projeto para C++/WinRT:

* Para novos projetos, você pode instalar a [Extensão do Visual Studio Extension (VSIX) para C++/WinRT](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) e usar um dos modelos de projeto C++/WinRT incluídos nessa extensão.
* Para projetos de Windows da área de trabalho existentes, você pode instalar o [Microsoft.Windows. CppWinRT](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) NuGet pacote no projeto.

Para obter mais detalhes sobre essas opções, confira [este artigo](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Novidades das APIs do Win32 no Windows 10

Para saber mais sobre as novas APIs do Win32 que foram introduzidas no Windows 10, confira [novidades.](whats-new.md)

## <a name="get-started-with-win32-features-and-technologies"></a>Começar a trabalhar com tecnologias e recursos do Win32

As APIs win32 existem para muitos recursos e tecnologias no Windows 10, incluindo interface do usuário principal e APIs de janela, áudio e gráficos e rede. Para obter diretrizes e exemplos de código sobre como usar essas APIs, [consulte nosso índice de recursos e tecnologias](desktop-app-technologies.md).

## <a name="related-topics"></a>Tópicos relacionados

* [Criar aplicativos da área de trabalho](/windows/apps/desktop)
* [Windows Referência de API](/windows/desktop/api/)
* [Índice de API do Windows](/windows/desktop/apiindex/api-index-portal)
* [Windows Referência C++ de runtime](/windows/desktop/winrt/reference)
