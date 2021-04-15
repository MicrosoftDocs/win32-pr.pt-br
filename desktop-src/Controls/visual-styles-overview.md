---
title: Visão geral dos estilos visuais
description: Este tópico descreve os estilos visuais e identifica os componentes do Windows que dão suporte a eles. Ele também explica as etapas que você deve seguir para usar estilos visuais em seus aplicativos.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5663730c752fbf16c4f229a031eafa0c65bb9dbb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454463"
---
# <a name="visual-styles-overview"></a>Visão geral dos estilos visuais

Este tópico descreve os estilos visuais e identifica os componentes do Windows que dão suporte a eles. Ele também explica as etapas que você deve seguir para usar estilos visuais em seus aplicativos. Este tópico inclui as seções a seguir:

-   [Temas e estilos visuais](#themes-and-visual-styles)
-   [Componentes de estilos visuais](#visual-styles-components)
-   [Requisitos de aplicativo para dar suporte a estilos visuais](#application-requirements-for-supporting-visual-styles)
-   [Tópicos relacionados](#related-topics)

## <a name="themes-and-visual-styles"></a>Temas e estilos visuais

O Windows inclui vários recursos que permitem que os usuários personalizem a interface do usuário para acomodar suas necessidades e preferências individuais. Esses recursos incluem temas, que foram introduzidos no Microsoft Plus! para o Windows 95. Um tema é uma coleção de configurações selecionável pelo usuário que inclui papel de parede, cursores, fontes, sons e ícones. A seguir estão algumas características de temas.

-   As configurações de tema são especificadas em arquivos. Theme que têm um formato semelhante a win.ini arquivos.
-   Um fornecedor independente de software (ISV) pode criar e distribuir um arquivo. Theme com um produto.
-   Em versões anteriores ao Windows Vista, os arquivos de tema são exibidos na guia tema do painel de controle de exibição. No Windows Vista e posterior, os temas são exibidos no painel de controle de personalização.

Para obter mais informações sobre arquivos. theme, consulte [formato de arquivo de tema](themesfileformat-overview.md).

Um estilo visual é uma especificação que define a aparência dos controles comuns do Windows. Os estilos visuais são associados a temas; ou seja, um arquivo. Theme contém uma seção que especifica o estilo visual a ser aplicado quando o tema específico está ativo. A seguir estão algumas características de estilos visuais.

-   Os usuários podem alterar o estilo visual a qualquer momento selecionando um tema diferente.
-   Você deve usar a API de estilos visuais para aplicar o estilo visual ativo no momento aos controles personalizados ou desenhados pelo proprietário do aplicativo, se houver.
-   As informações que definem um estilo visual são armazenadas em um arquivo. msstyles. A Microsoft não oferece suporte à criação de arquivos. msstyles.


A ilustração a seguir mostra uma caixa de diálogo simples com uma barra de tarefas, em uma área de trabalho do Windows 7 que usa o tema Windows Aero sem transparência. Como o aplicativo não está configurado para usar estilos visuais, os botões são os mesmos, independentemente das configurações de tema.

![captura de tela de uma caixa de diálogo com botões que não usam transparência](images/tb-wostyles.png)

Por outro lado, a ilustração a seguir mostra a mesma caixa de diálogo na mesma área de trabalho, mas desta vez o aplicativo foi configurado para trabalhar com estilos visuais. Observe a aparência diferente dos botões na área do cliente. Os botões parecem diferentes porque o sistema aplicou os estilos visuais definidos no tema Aero.

![captura de tela de uma caixa de diálogo com botões que usam transparência](images/tb-withstyles.png)

O exemplo a seguir mostra uma caixa de diálogo semelhante em uma área de trabalho do Windows 8. No Windows 8, os estilos visuais estão sempre ativados e, portanto, os aplicativos do Windows 8 os recebem "gratuitamente".

![captura de tela de uma caixa de diálogo simples na área de trabalho do Windows 8](images/tb-win8.png)

## <a name="visual-styles-components"></a>Componentes de estilos visuais

Os estilos visuais têm suporte nos seguintes componentes:

-   Versão 6 ou posterior da biblioteca de controle comum (ComCtl32.dll)
-   A API de estilos visuais implementada no UxTheme.dll
-   Serviço de temas
-   Um ou mais arquivos de definição de estilo visual (. msstyles)

A API de estilos visuais depende de um serviço do sistema chamado temas. A biblioteca de controle comum consulta o serviço de temas para obter informações relacionadas ao estilo e, até o Windows 7, usa o serviço para renderizar controles no estilo visual atual.

No Windows 8 e posterior, a API de estilos visuais ainda funciona se o serviço de temas estiver desativado. Isso significa que os controles comuns e a área não cliente do Windows ainda terão estilos visuais quando o serviço de temas estiver desativado. Os recursos do Windows 8 que ainda exigem o serviço de temas incluem:

-   Alterar o estilo visual, normalmente por meio da página **personalização** das **configurações do PC**.
-   Otimizações de desempenho envolvidas na troca de usuários, logoff, desligamento e compartilhamento entre sessões de usuário.

A API de estilos visuais Obtém informações de estilo do arquivo. msstyles associado ao tema atualmente selecionado. O arquivo. msstyles contém um conjunto de métricas, fontes, cores e bitmaps que definem um estilo visual

## <a name="application-requirements-for-supporting-visual-styles"></a>Requisitos de aplicativo para dar suporte a estilos visuais

Para usar estilos visuais, seu aplicativo deve estar em execução em um sistema operacional que contém ComCtl32.dll versão 6 ou posterior. Se você quiser que seu aplicativo use ComCtl32.dll versão 6, deverá adicionar um manifesto de aplicativo ou diretiva de compilador para especificar que a versão 6 deve ser usada se estiver disponível. Para obter informações sobre como criar um manifesto de aplicativo que permite que seu aplicativo use estilos visuais, consulte [habilitando estilos visuais](cookbook-overview.md).

Para controles comuns, nenhuma ação adicional é necessária para garantir que os controles sejam exibidos no estilo visual preferencial do usuário.

Se seu aplicativo contiver controles personalizados ou desenhados pelo proprietário, você precisará usar a API de estilos visuais para recuperar informações sobre o estilo visual ativo no momento e para desenhar os controles nesse estilo.

Para versões do Windows anteriores ao Windows 8, normalmente os aplicativos precisam fornecer dois caminhos de código separados para desenhar controles personalizados e desenhados pelo proprietário. Um caminho de código desenha os controles quando um tema que usa estilos visuais está ativo e outro caminho de código desenha os controles quando o tema clássico do Windows ou um tema de alto contraste está ativo. No Windows 8, no entanto, os estilos visuais são sempre ativados, portanto, os caminhos de código separados não são necessários. Os aplicativos que são manifestados para o Windows 8 têm um alto contraste com eles "gratuitamente". Para obter mais informações, consulte [suporte a temas de alto contraste](supporting-high-contrast-themes.md).

Para obter mais informações sobre o, consulte [usando estilos visuais com controles personalizados e de Owner-Drawn](using-visual-styles.md) e [referência de estilos visuais](uxctl-ref.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estilos visuais](themes-overview.md)
</dt> </dl>

 

 




