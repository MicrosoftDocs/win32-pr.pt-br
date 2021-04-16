---
title: A experiência desktop
description: A nova área de trabalho do Windows 7 traz a vida dos seus aplicativos.
ms.assetid: e706167a-435b-4c32-bb64-87113f368866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3476f70c46aecceb365e17dba1803b876fd51e8d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104566413"
---
# <a name="the-desktop-experience"></a>A experiência desktop

A nova área de trabalho do Windows 7 traz a vida dos seus aplicativos. Agora, os aplicativos são mais detectáveis, informativos e interativos. As interfaces de usuário modernas e intuitivas são mais fáceis de desenvolver com o Windows 7. As novas experiências de desktop e aplicativo incluem o seguinte:

-   A barra de tarefas avançada apresenta miniaturas interativas e habilita a animação e a interação para aplicativos minimizados.
-   O conceito de destinos permite que os usuários saltem com um clique para os arquivos, locais ou tarefas que eles usam com mais frequência.
-   Novos controles e APIs para a *faixa de faixas*, com base na interface do usuário fluente do Office, estão disponíveis para adicionar facilmente controles, menus e galerias de estilo de *faixa* de medida a seus aplicativos.
-   Uma estrutura de animação ajuda você a aprimorar animações personalizadas.

Os aprimoramentos na plataforma de gadgets permitem que os aplicativos instalem gadgets complementares durante a instalação ou a experiência de primeira execução.

![Captura de tela que mostra a área de trabalho do Windows 7.](images/windows7-6.jpg)

A nova área de trabalho do Windows 7 traz a vida dos seus aplicativos

## <a name="jump-listsgetting-users-into-your-application-quickly"></a>Listas de atalhos – colocando os usuários em seu aplicativo rapidamente

As listas de atalhos ajudam os usuários a chegarem onde desejam ir mais rapidamente. As listas de atalhos são arquivos, URLs, tarefas ou itens personalizados que são abertos no aplicativo. O novo menu listas de atalhos no menu *Iniciar* e na barra de tarefas torna destinos comuns e tarefas-chave disponíveis com um único clique. O menu listas de atalhos é preenchido automaticamente com base na frequência e na forma com que os itens foram usados. Os desenvolvedores podem fornecer listas de atalhos personalizadas com base em sua própria semântica. Os aplicativos também podem definir *tarefas* para serem exibidos em seus menus — essas são ações do aplicativo que os usuários desejam acessar diretamente, como compor um email. (Consulte [extensões da barra de tarefas](../shell/taskbar-extensions.md) e [interface ICustomDestinationList](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist).)

![listas de atalhos](images/windows7-7.jpg)

As listas de atalhos ajudam os usuários a chegarem onde desejam ir mais rápido

## <a name="enhanced-taskbar"></a>Barra de tarefas aprimorada

Com a nova barra de tarefas no Windows 7, os aplicativos podem fornecer mais informações ao usuário de maneiras mais intuitivas. Por exemplo, os aplicativos podem mostrar barras de progresso em seus botões da barra de tarefas para que os usuários possam ficar cientes do progresso sem precisar manter a janela visível. Isso é útil para acompanhar operações demoradas, como cópia de arquivos, downloads, instalações ou gravação de mídia. As sobreposições de ícone podem ser exibidas na área inferior direita do botão da barra de tarefas do aplicativo e são usadas para comunicar status ou notificações (como novos emails). Novas APIs de miniatura permitem que um aplicativo defina as janelas filhas e as imagens em miniatura correspondentes para essas janelas. A barra de ferramentas de miniatura fornece um local para controlar ações comuns sem a necessidade de restauração de janelas, como *reproduzir/parar* para mídia. (Consulte [extensões da barra de tarefas](../shell/taskbar-extensions.md) e [Windows 7: recursos para desenvolvedores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples).)

## <a name="gadgets-platform"></a>Plataforma de gadgets

Os gadgets são um recurso popular da área de trabalho do Windows Vista e, no Windows 7, é ainda mais fácil para os aplicativos instalarem gadgets. No Windows 7, um aplicativo pode adicionar programaticamente um gadget à área de trabalho do Windows durante a instalação do aplicativo ou ser executado pela primeira vez. Isso significa que a experiência pronta para uso do aplicativo pode incluir uma caixa de seleção simples, por exemplo, para instalar um gadget complementar que está disponível na área de trabalho assim que o aplicativo estiver pronto para ser usado. (Consulte [introdução à plataforma de gadget](/previous-versions/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform).)

![Gadgets do Windows](images/windows7-8.jpg)

No Windows 7, é ainda mais fácil para os aplicativos instalarem gadgets

## <a name="windows-ribbon"></a>Faixa de-se do Windows



O controle da faixa de medida do Windows ajuda os desenvolvedores a melhorar a usabilidade expondo os recursos acessados com mais frequência dos seus aplicativos diretamente aos usuários finais. A faixa de faixas torna mais fácil para os usuários finais localizar e usar recursos de aplicativos, pois menos funcionalidade é oculta, levando a uma maior produtividade. A faixa de opção é projetada como uma alternativa baseada em intenção para o modelo de apresentação de comandos de menus, barras de ferramentas, painéis de tarefas e caixas de diálogo em aplicativos padrão baseados no Windows.

Os controles da faixa de faixas consistem em um conjunto de Win32APIs que substituem a funcionalidade da barra de menus de nível superior e renderizam uma interface do usuário de comando em estilo de faixa de bits. Ele é semelhante em funcionalidade e aparência à *faixa* de tipos no sistema do Office 2007. A interface do usuário é composta por vários subcontroles que incluem o seguinte:

-   Botão de aplicativo (ou Pearl)
-   Barra de ferramentas de acesso rápido
-   Controle da *faixa* de guia de guias contextuais
-   Mini-barras de ferramentas
-   Galerias de estilo

Os modelos e a criação de marcação estão disponíveis para desenvolvedores para desenvolvimento rápido e integração da funcionalidade da faixa de uma. (Consulte [Windows Ribbon Framework](../windowsribbon/-uiplat-windowsribbon-entry.md) e [Windows Ribbon Framework: recursos para desenvolvedores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsRibbon).)

![barra de ferramentas da faixa](images/windows7-9.jpg)

O controle Ribbon ajuda os desenvolvedores a melhorar a usabilidade expondo os recursos acessados com mais frequência do seu aplicativo

## <a name="animation"></a>Animação

Animações suaves são fundamentais para muitos aplicativos gráficos de interface do usuário, e o Windows 7 apresenta uma estrutura de animação nativa para gerenciar o agendamento e a execução de animações. A estrutura de animação fornece uma biblioteca de funções matemáticas úteis para especificar o comportamento ao longo do tempo e também permite que os desenvolvedores forneçam suas próprias funções de comportamento. A estrutura dá suporte à resolução sofisticada de conflitos quando várias animações tentam manipular o mesmo valor ao mesmo tempo. Um aplicativo pode especificar que uma animação deve ser concluída antes que outra possa ser iniciada e pode forçar a conclusão em uma hora definida. A nova estrutura também ajuda as animações a determinar as durações apropriadas. (Consulte [Gerenciador de animação do Windows](../uianimation/-main-portal.md).)

 

 