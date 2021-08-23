---
title: Visão geral dos estilos visuais
description: Este tópico descreve estilos visuais e identifica os Windows componentes que os suportam. Ele também explica as etapas que você deve seguir para usar estilos visuais em seus aplicativos.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237ac858e1a60e615a6af177728102fb7e6ea1737a3a2d94d93091264b02121a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077712"
---
# <a name="visual-styles-overview"></a>Visão geral dos estilos visuais

Este tópico descreve estilos visuais e identifica os Windows componentes que os suportam. Ele também explica as etapas que você deve seguir para usar estilos visuais em seus aplicativos. Este tópico inclui as seções a seguir:

-   [Temas e estilos visuais](#themes-and-visual-styles)
-   [Componentes de estilos visuais](#visual-styles-components)
-   [Requisitos de aplicativo para dar suporte a estilos visuais](#application-requirements-for-supporting-visual-styles)
-   [Tópicos relacionados](#related-topics)

## <a name="themes-and-visual-styles"></a>Temas e estilos visuais

Windows inclui vários recursos que permitem que os usuários adaptem a interface do usuário para acomodar suas necessidades e preferências individuais. Esses recursos incluem temas, que foram introduzidos no Microsoft Plus! para Windows 95. Um tema é uma coleção selecionável pelo usuário de configurações que inclui papel de parede, cursores, fontes, sons e ícones. A seguir estão algumas características dos temas.

-   As configurações de tema são especificadas em arquivos .theme que têm um formato semelhante a win.ini arquivos.
-   Um ISV (fornecedor independente de software) pode criar e distribuir um arquivo .theme com um produto.
-   Em versões anteriores Windows Vista, os arquivos de tema são exibidos na guia Tema do painel de controle Exibir. No Windows Vista e posterior, os temas são exibidos no painel de controle Personalização.

Para obter mais informações sobre arquivos .theme, consulte [Formato de arquivo de tema](themesfileformat-overview.md).

Um estilo visual é uma especificação que define a aparência do Windows controles comuns. Os estilos visuais são associados a temas; ou seja, um arquivo .theme contém uma seção que especifica o estilo visual a ser aplicado quando o tema específico está ativo. A seguir estão algumas características dos estilos visuais.

-   Os usuários podem alterar o estilo visual a qualquer momento selecionando um tema diferente.
-   Você deve usar a API de estilos visuais para aplicar o estilo visual ativo no momento aos controles personalizados ou desenhados pelo proprietário do aplicativo, se for o caso.
-   As informações que definem um estilo visual são armazenadas em um arquivo .msstyles. A Microsoft não dá suporte à autoração de arquivos .msstyles.


A ilustração a seguir mostra uma caixa de diálogo simples com uma barra de tarefas, em uma área de trabalho Windows 7 que usa o tema Windows Aero sem transparência. Como o aplicativo não está configurado para usar estilos visuais, os botões aparecem da mesma forma, independentemente das configurações de tema.

![captura de tela de uma caixa de diálogo com botões que não usam transparência](images/tb-wostyles.png)

Por outro lado, a ilustração a seguir mostra a mesma caixa de diálogo na mesma área de trabalho, mas desta vez o aplicativo foi configurado para funcionar com estilos visuais. Observe a aparência diferente dos botões na área do cliente. Os botões parecem diferentes porque o sistema aplicou os estilos visuais definidos no tema Aero.

![captura de tela de uma caixa de diálogo com botões que usam transparência](images/tb-withstyles.png)

O exemplo a seguir mostra uma caixa de diálogo semelhante em uma Windows 8 desktop. No Windows 8, os estilos visuais estão sempre ativos, portanto, Windows 8 aplicativos têm temas "gratuitamente".

![captura de tela de uma caixa de diálogo simples na área de trabalho do Windows 8](images/tb-win8.png)

## <a name="visual-styles-components"></a>Componentes de estilos visuais

Os estilos visuais são suportados pelos seguintes componentes:

-   Versão 6 ou posterior da biblioteca de controle comum (ComCtl32.dll)
-   A API de estilos visuais implementada no UxTheme.dll
-   Serviço temas
-   Um ou mais arquivos de definição de estilo visual (.msstyles)

A API de estilos visuais depende de um serviço do sistema chamado Temas. A biblioteca de controle comum consulta o serviço Temas para obter informações relacionadas ao estilo e, até Windows 7, usa o serviço para renderizar controles no estilo visual atual.

No Windows 8 posterior, a API de estilos visuais ainda funcionará se o serviço Temas estiver desligado. Isso significa que os controles comuns e a área não cliente das janelas ainda terão estilos visuais quando o serviço Temas estiver desligado. Os Windows 8 recursos que ainda exigem o serviço Temas incluem:

-   Alterando o estilo visual, normalmente por meio da **página Personalização** **do PC Configurações**.
-   Otimizações de desempenho envolvidas na troca de usuários, logo off, desligamento e compartilhamento entre sessões do usuário.

A API de estilos visuais obtém informações de estilo do arquivo .msstyles associado ao tema selecionado no momento. O arquivo .msstyles contém um conjunto de métricas, fontes, cores e bitmaps que definem um estilo visual

## <a name="application-requirements-for-supporting-visual-styles"></a>Requisitos de aplicativo para dar suporte a estilos visuais

Para usar estilos visuais, seu aplicativo deve estar em execução em um sistema operacional que contenha ComCtl32.dll versão 6 ou posterior. Se você quiser que seu aplicativo use ComCtl32.dll versão 6, deverá adicionar um manifesto do aplicativo ou uma diretiva do compilador para especificar que a versão 6 deve ser usada se ela estiver disponível. Para obter informações sobre como criar um manifesto do aplicativo que permite que seu aplicativo use estilos visuais, consulte [Habilitando estilos visuais.](cookbook-overview.md)

Para controles comuns, nenhuma ação é necessária para garantir que os controles sejam exibidos no estilo visual preferencial do usuário.

Se seu aplicativo contiver controles personalizados ou desenhados pelo proprietário, você precisará usar a API de estilos visuais para recuperar informações sobre o estilo visual ativo no momento e desenhar os controles nesse estilo.

Para Windows versões anteriores Windows 8, os aplicativos normalmente precisam fornecer dois caminhos de código separados para desenhar controles personalizados e desenhados pelo proprietário. Um caminho de código desenha os controles quando um tema que usa estilos visuais está ativo e outro caminho de código desenha os controles quando o tema clássico Windows ou um tema de alto contraste está ativo. No Windows 8, no entanto, os estilos visuais estão sempre ativos, portanto, caminhos de código de temas separados não são necessários. Aplicativos que são manifestos para Windows 8 temas de alto contraste "gratuitamente". Para obter mais informações, consulte [Support Alto Contraste Themes](supporting-high-contrast-themes.md).

Para obter mais informações sobre, consulte [Using Visual Styles with Custom and Owner-Drawn Controls](using-visual-styles.md) and Visual Styles [Reference](uxctl-ref.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estilos visuais](themes-overview.md)
</dt> </dl>

 

 




