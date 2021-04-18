---
description: 'Veja a seguir as opções de exibição e processamento relacionado de texto para dar suporte a efeitos de tipografia finas ou scripts complexos: Text functionsEdit controlsRich Edit controlsUniscribe'
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Processamento de script complexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e4be6295bff949c8e29036ef3af496c673575e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810338"
---
# <a name="complex-script-processing"></a>Processamento de script complexo

Veja a seguir as opções de exibição e processamento relacionado de texto para dar suporte a efeitos de tipografia finas ou scripts complexos:

-   Funções de texto
-   Editar controles
-   Controles de edição avançados
-   Cancelar

As opções escolhidas dependem dos seguintes fatores:

-   O tipo de texto ou scripts.
-   O modelo de implementação, por exemplo, o layout de texto e a manipulação de quebra de linha pelo aplicativo.
-   Atualização de um aplicativo existente em relação à criação de um novo aplicativo.

Em geral, um aplicativo que executa o processamento de script relativamente simples pode escolher qualquer opção para processar scripts complexos. No entanto, para o controle mais completo do processamento de script complexo, o Uniscribe é recomendado.

## <a name="complex-script-processing-using-text-functions"></a>Processamento de script complexo usando funções de texto

Os aplicativos que usam a maior parte do texto sem formatação, ou seja, texto que usa a mesma face de tipos, peso, cor e assim por diante, têm tradicionalmente escrito o texto e os comprimentos de linha medidos usando funções de texto padrão, como [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)e [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa). Essas funções dão suporte ao processamento de scripts complexos e efeitos de tipografia finas. Para obter mais informações, consulte [fontes e texto](../gdi/fonts-and-text.md).

Em geral, o suporte a texto padrão é transparente para aplicativos que processam scripts complexos. No entanto, você deve estar ciente de algumas regras específicas a serem seguidas na escrita de aplicativos que dão suporte a tipografia fina e processamento de scripts complexos:

-   Seu aplicativo deve salvar caracteres em um buffer e exibir uma linha inteira de texto ao mesmo tempo, em vez de, por exemplo, chamar [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) em cada caractere conforme ele é digitado pelo usuário. Esse mecanismo permite que os módulos de modelagem de texto avançados usem o contexto para reordenar e gerar [glifos](uniscribe-glossary.md) corretamente.
-   O aplicativo deve usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar o comprimento da linha, em vez de calcular comprimentos de linha de larguras de caracteres em cache, já que a largura de um glifo pode variar por contexto.
-   Opcionalmente, o aplicativo deve adicionar suporte à ordem de leitura da direita para a esquerda e ao alinhamento à direita.
-   A reordenação e o processamento contextual necessários para scripts complexos ou a tipografia fina exigem um aumento significativo no processamento da exibição de texto básico para scripts simples. Portanto, para evitar problemas de desempenho, seu aplicativo não deve processar grandes quantidades de texto antes de exibir os resultados e retornar o controle ao usuário.

## <a name="complex-script-processing-using-edit-controls"></a>Processamento de script complexo usando controles de edição

Os controles de edição padrão do Windows foram estendidos para dar suporte a texto multilíngüe e scripts complexos. O suporte estendido inclui entrada e exibição, bem como o movimento correto do cursor sobre clusters de caracteres, por exemplo, nos scripts tailandês e Devanágari. Para obter mais informações, consulte [Editar controles](../controls/edit-controls.md).

## <a name="complex-script-processing-using-rich-edit-controls"></a>Processamento de script complexo usando controles de edição avançados

A edição avançada 3,0 é uma coleção de interfaces de nível superior que aproveita o Uniscribe para isolar aplicativos de layout de texto das complexidades de determinados scripts. O Rich Edit é a maneira mais simples de os aplicativos exibirem scripts complexos, embora seu objetivo principal não seja necessariamente o layout de texto. O Rich Edit fornece edição rápida e versátil de texto multilíngüe Unicode avançado e texto simples e simples. Ele inclui interfaces de mensagens e COM abrangentes, edição de texto, formatação, quebra de linha, layout de tabela simples, layout de texto vertical, layout de texto bidirecional, suporte a Índico e tailandês, uma interface de usuário de edição muito parecida com o Microsoft Word e interfaces de modelo de objeto de texto.

Juntamente com as interfaces de edição sofisticadas, os aplicativos podem usar a função Rich [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) de edição para analisar automaticamente, Formatar, posicionar e quebrar linhas. Para obter mais informações, consulte [rich edit Controls](../controls/rich-edit-controls.md).

## <a name="complex-script-processing-using-uniscribe"></a>Processamento de script complexo usando o Uniscribe

O [Uniscribe](uniscribe.md) fornece o suporte mais amplo para o processamento de texto que envolve efeitos de tipografia fina e scripts complexos. Ele dá suporte a regras complexas encontradas em scripts como árabe, Devanágari e tailandês. Ele lida com scripts escritos da direita para a esquerda, como árabe e Hebraico, e dá suporte à combinação de scripts. O Uniscribe também expõe recursos de fonte [OpenType](opentype-font-format.md) que podem ser usados por aplicativos para controlar efeitos de tipografia fina. Para obter mais informações, consulte [processamento de scripts complexos](processing-complex-scripts.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Uniscribe](about-uniscribe.md)
</dt> <dt>

[Processando scripts complexos](processing-complex-scripts.md)
</dt> </dl>

 

 
