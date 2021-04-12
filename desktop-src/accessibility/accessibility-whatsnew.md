---
description: Descreve as recentes inovações e atualizações para recursos de acessibilidade, ferramentas, documentação e exemplos do Windows.
title: O que há de novo na acessibilidade do Windows para desenvolvedores
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 44d8c453b09bc73e71006e132199c18b275860af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457165"
---
# <a name="new-windows-accessibility-features-tools-documentation-and-samples-for-developers"></a>Novos recursos de acessibilidade do Windows, ferramentas, documentação e exemplos para desenvolvedores

A plataforma Windows está constantemente sendo atualizada com novos recursos de acessibilidade e automação para desenvolvedores.

[Instale as ferramentas e o SDK](https://developer.microsoft.com/windows/downloads/#_blank) no Windows 10 e você está pronto para criar um novo aplicativo universal do Windows ou explorar como é possível usar o código do aplicativo existente no Windows.

Para obter mais informações sobre as ferramentas mais recentes disponíveis para testar a implementação de acessibilidade de seus aplicativos Windows e Web, consulte [testando a acessibilidade](accessibility-testwithuia.md).

## <a name="whats-new-for-windows-10-may-2019-update-version-1903"></a>O que há de novo no Windows 10 pode ser 2019 atualização (versão 1903)

Os seguintes recursos, ferramentas, diretrizes para desenvolvedores, exemplos e vídeos foram disponibilizados para a [atualização do Windows 10 2019](https://blogs.windows.com/windowsexperience/2019/04/08/releasing-the-may-2019-update-to-the-release-preview-ring/#oTrOrMWFFgWJuCqO.97).

| Versão | Plataforma | Recurso | Descrição | Link |
| --- | --- | --- | --- | --- |
| 1903 | Win32 | Automação de interface do usuário compatível com IAccessible2 | Os clientes de automação da interface do usuário agora podem acessar diretamente as informações de provedores de IAccessible2, como o navegador Chrome. | N/D |
| 1903 | UWP | Visibilidade da barra de rolagem  | As barras de rolagem são ocultadas automaticamente quando não estão sendo interagindo. | [Propriedade UISettings. AutoHideScrollBars](/uwp/api/windows.ui.viewmanagement.uisettings.autohidescrollbars) |
| 1903 | Win32 | A automação da IU dá suporte à marcação estruturada | Pretendido, mas não limitado a, análise de MathML. | N/D |

## <a name="whats-new-for-windows-10-october-2018-update-version-1809"></a>Novidades do Windows 10 de outubro de 2018 atualização (versão 1809)

Os seguintes recursos, ferramentas, diretrizes para desenvolvedores, exemplos e vídeos foram disponibilizados para a [atualização do Windows 10 de outubro de 2018](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/#R6DJStjqlIkK34BT.97).

| Versão | Plataforma | Recurso | Descrição | Link |
| --- | --- | --- | --- | --- |
| 1809 | Win32 | A automação da IU dá suporte a eventos de alteração de posição de texto ativo | Os provedores de automação da interface do usuário podem definir explicitamente uma posição inicial dentro de um intervalo de texto. Os clientes de tecnologia assistencial (AT) podem transmitir essa posição a um usuário. Por exemplo, se um usuário clicar em um link para uma âncora na mesma página (um link de indicador), o novo local será fornecido ao em. | [Interface IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | A automação da interface do usuário dá suporte à União de eventos | Melhora o desempenho ao tentar detectar, filtrar e ignorar eventos de MSAA e UIA TextChanged duplicados gerados por alguns provedores. | [Interface IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | A automação de IU dá suporte ao comportamento de recuperação de conexão | As mensagens de um cliente de automação de interface do usuário para um provedor são suspensas (por padrão, por dois segundos) se o provedor não estiver respondendo. Isso reduz a frequência de tempos limite estendidos e minimiza a inundação de um provedor não responsivo com eventos e solicitações. | [Interface IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | UWP | Serviços avançados de leitura de tela | EM clientes sabem o local de leitura de tela audível (controle ou conteúdo) e o modo de leitura. | [Classe ScreenReaderService](/uwp/api/windows.ui.accessibility.screenreaderservice) |
| 1809 | Win32, UWP | Automação da interface do usuário dá suporte a janelas de diálogo | Provedores de automação de interface do usuário podem marcar elementos UIA especificamente como janelas de diálogo. A ATs geralmente apresenta caixas de diálogo diferentes aos usuários.  | [IUIAutomationElement9](https://review.docs.microsoft.com/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/><br/>[Classe ContentDialog](/uwp/api/windows.ui.xaml.controls.contentdialog) |
| 1809 |  UWP | Colocar texto em escala  | Dimensiona o tamanho do texto em aplicativos e páginas da Web. | [Evento UISettings. TextScaleFactorChanged](/uwp/api/windows.ui.viewmanagement.uisettings.textscalefactorchanged)<br/><br/>[Dimensionamento de texto](/windows/uwp/design/input/text-scaling) |
