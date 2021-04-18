---
description: Comece a aprender as noções básicas da criação de ótimos aplicativos de área de trabalho nesta seção.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Introdução
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84879e6373f4bfeb5a7e4b6a6138423d7688afe2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764541"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Introdução aos aplicativos do Windows para desktop que usam a API do Win32

A API do Win32 (também chamada de API do Windows) é plataforma original para aplicativos nativos do Windows em C/C++ que exigem acesso direto ao Windows e ao hardware. Ele fornece uma experiência de desenvolvimento de primeira classe sem depender de um ambiente de tempo de execução gerenciado como .NET e WinRT (para aplicativos UWP para Windows 10). Isso torna a API do Win32 a plataforma preferida para aplicativos que precisam do nível mais alto de desempenho e acesso direto ao hardware do sistema.

> [!NOTE]
> Esta documentação aborda como criar aplicativos do Windows para desktop com a API do Win32. A API do Win32 é uma das várias plataformas de aplicativos que você pode usar para criar aplicativos para Windows de área de trabalho. Para obter mais informações sobre outras plataformas de aplicativos, consulte [escolher sua plataforma](/windows/apps/desktop/choose-your-platform).

## <a name="get-set-up"></a>Prepare-se para começar

Siga estas instruções e comece a criar aplicativos de área de trabalho para o Windows 10 que usam a API do Win32.

1. Baixe ou atualize o Visual Studio 2019. Se ainda não tem o Visual Studio 2019, você pode instalar o Microsoft Visual Studio Community 2019 gratuitamente. Ao instalar o Visual Studio, certifique-se de selecionar a opção **desenvolvimento de área de trabalho com C++** . Para links de download, consulte nossa página de [downloads](https://developer.microsoft.com/windows/downloads) .

    > [!NOTE]
    > Ao instalar o Visual Studio, você pode opcionalmente selecionar as opções desenvolvimento de **área de trabalho .net** e **desenvolvimento de plataforma universal do Windows** para acesso a outros tipos de projeto e plataformas de aplicativos para a criação de aplicativos para Windows desktop.

2. Se você quiser criar seu aplicativo de desktop em um [pacote MSIX](/windows/msix/desktop/desktop-to-uwp-root) e testar ou depurar o aplicativo empacotado em seu computador de desenvolvimento, será necessário [habilitar o modo de desenvolvedor em seu computador](/windows/uwp/get-started/enable-your-device-for-development).

> [!NOTE]
> Para scripts que você pode usar para configurar o computador de desenvolvimento e instalar outros recursos ou pacotes, confira [este projeto do GitHub](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Saiba como criar aplicativos de desktop usando a API do Win32

Se você for novo na criação de aplicativos de área de trabalho usando a API do Win32, os tutoriais e artigos a seguir ajudarão você a começar.

| Tópico        | Descrição      |
|---------------|-----------------|
| [Criar seu primeiro aplicativo Win32 do C++](LearnWin32/learn-to-program-for-windows.md)    | Este tutorial ensina como escrever um programa do Windows em C++ usando o Win32 e APIs COM.  |
| [Criar seu primeiro aplicativo usando o DirectX](direct3dgetstarted/building-your-first-directx-app.md) | Este tutorial básico ajudará você a começar a usar o desenvolvimento de aplicativos DirectX.            |
| [Guia de programação para o Windows de 64 bits](WinProg64/programming-guide-for-64-bit-windows.md)    | Descreve a programação para versões de 64 bits do sistema operacional Windows. |
| [Usando os cabeçalhos do Windows](WinProg/using-the-windows-headers.md)     | Fornece uma visão geral de algumas das convenções usadas nos arquivos de cabeçalho do Windows. |

Você também pode procurar [exemplos do aplicativo de desktop](https://github.com/Microsoft/Windows-classic-samples).

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Modernizar seus aplicativos de área de trabalho para Windows 10

Se você tiver um aplicativo Win32 de área de trabalho existente, há muitos recursos no Plataforma Universal do Windows (UWP) que você pode usar para oferecer a melhor experiência possível no Windows 10. Por exemplo, a partir do Windows 10, versão 1903, você pode hospedar controles de XAML do UWP em seu aplicativo Win32 de desktop usando um recurso chamado ilhas XAML.

A maioria desses recursos de UWP está disponível como componentes modulares que você pode adotar em seu aplicativo de desktop em seu próprio ritmo sem precisar reescrever o aplicativo inteiro. Você pode aprimorar seu aplicativo de área de trabalho existente escolhendo quais partes do Windows 10 e UWP adotar.

Para obter mais informações, consulte [Modernize seus aplicativos da área de trabalho](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Opcionalmente, você pode configurar seu computador de desenvolvimento para usar [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/). C++/WinRT é uma projeção de linguagem C++ 17 totalmente padrão, que permite consumir facilmente Windows Runtime APIs Windows Runtime (WinRT) do seu aplicativo de área de trabalho do C++ Win32. O C++/WinRT é implementado como uma biblioteca baseada em arquivo de cabeçalho.

Para configurar o projeto para C++/WinRT:

* Para novos projetos, você pode instalar a [Extensão do Visual Studio Extension (VSIX) para C++/WinRT](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) e usar um dos modelos de projeto C++/WinRT incluídos nessa extensão.
* Para projetos de aplicativos da área de trabalho do Windows existentes, você pode instalar o pacote NuGet [Microsoft. Windows. CppWinRT](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) no projeto.

Para obter mais detalhes sobre essas opções, confira [este artigo](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>O que há de novo para APIs do Win32 no Windows 10

Para saber mais sobre as novas APIs do Win32 que foram introduzidas no Windows 10, consulte [o que há de novo](whats-new.md).

## <a name="get-started-with-win32-features-and-technologies"></a>Introdução aos recursos e tecnologias do Win32

Existem APIs do Win32 para muitos recursos e tecnologias do Windows 10, incluindo a interface do usuário principal e as APIs de janela, áudio e gráficos e rede. Para obter orientações e exemplos de código sobre como usar essas APIs, [consulte nosso índice de recursos e tecnologias](desktop-app-technologies.md).

## <a name="related-topics"></a>Tópicos relacionados

* [Desenvolver aplicativos da área de trabalho](/windows/apps/desktop)
* [Referência da API do Windows](/windows/desktop/api/)
* [Índice de API do Windows](/windows/desktop/apiindex/api-index-portal)
* [Referência do Windows Runtime C++](/windows/desktop/winrt/reference)
