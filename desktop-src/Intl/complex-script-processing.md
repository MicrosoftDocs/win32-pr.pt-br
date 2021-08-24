---
description: 'A seguir estão as opções para exibição e processamento relacionado de texto para dar suporte a efeitos de tipografia finos ou scripts complexos: Funções de textoEditar controles de ediçãoEditar controlesUniscrito'
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Processamento de script complexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15671aed99e0c596d83bd65a2f4a0925ff61293cf90ed37e2aed371f23f114fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754906"
---
# <a name="complex-script-processing"></a>Processamento de script complexo

Veja a seguir opções para exibição e processamento relacionado de texto para dar suporte a efeitos de tipografia finos ou scripts complexos:

-   Funções de texto
-   Editar controles
-   Controles de edição rich
-   Uniscribe

As opções escolhidas dependem dos seguintes fatores:

-   O tipo de texto ou scripts.
-   O modelo de implementação, por exemplo, o layout de texto e o tratamento da quebra de linha pelo aplicativo.
-   Atualização de um aplicativo existente versus criação de um novo aplicativo.

Em geral, um aplicativo que faz processamento de script relativamente simples pode escolher qualquer opção para processar scripts complexos. No entanto, para o controle mais completo do processamento de script complexo, é recomendável o Uniscribe.

## <a name="complex-script-processing-using-text-functions"></a>Processamento de script complexo usando funções de texto

Aplicativos que usam principalmente texto sem formatação, ou seja, texto que usa a mesma face de tipo, peso, cor e assim por diante, escrevem tradicionalmente texto e medem comprimentos de linha usando funções de texto padrão, como [**TextOut,**](/windows/win32/api/wingdi/nf-wingdi-textouta) [**ExtTextOut,**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) [**TabbedTextOut,**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta) [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)e [**GetTextExtentExPoint.**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) Essas funções suportam o processamento de scripts complexos e efeitos de tipografia finos. Para obter mais informações, consulte [Fontes e texto.](../gdi/fonts-and-text.md)

Em geral, o suporte a texto padrão é transparente para aplicativos que processam scripts complexos. No entanto, você deve estar ciente de algumas regras específicas a serem seguidas ao escrever aplicativos que suportam tipografia fina e processar scripts complexos:

-   Seu aplicativo deve salvar caracteres em um buffer e exibir uma linha inteira de texto ao mesmo tempo, em vez de, por exemplo, chamar [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) em cada caractere conforme ele é digitado pelo usuário. Esse mecanismo permite que os módulos avançados de formatação de texto usem o contexto para reordenar e gerar [glifos](uniscribe-glossary.md) corretamente.
-   O aplicativo deve usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar o comprimento da linha, em vez de calcular comprimentos de linha de larguras de caracteres armazenados em cache, pois a largura de um glifo pode variar por contexto.
-   Opcionalmente, o aplicativo deve adicionar suporte para a ordem de leitura da direita para a esquerda e o alinhamento à direita.
-   A reordenação e o processamento contextual necessários para scripts complexos ou tipografia fina exigem um aumento significativo no processamento em relação à exibição de texto básico para scripts simples. Portanto, para evitar problemas de desempenho, seu aplicativo não deve processar grandes quantidades de texto antes de exibir os resultados e retornar o controle ao usuário.

## <a name="complex-script-processing-using-edit-controls"></a>Processamento de script complexo usando controles de edição

Os controles Windows de edição padrão foram estendidos para dar suporte a textos multilíngues e scripts complexos. O suporte estendido inclui entrada e exibição, bem como a movimentação correta do cursor sobre clusters de caracteres, por exemplo, em scripts tailandês e Devanagari. Para obter mais informações, consulte [Editar controles](../controls/edit-controls.md).

## <a name="complex-script-processing-using-rich-edit-controls"></a>Processamento de script complexo usando controles de edição rich

O Rich Edit 3.0 é uma coleção de nível superior de interfaces que aproveita o Uniscribe para isolar aplicativos de layout de texto das complexidades de determinados scripts. Edição Rich é a maneira mais simples para os aplicativos exibirem scripts complexos, embora sua finalidade principal não seja necessariamente o layout de texto. A Edição Rich fornece edição rápida e versátil de texto multilíngue Unicode e texto simples simples. Ele inclui extensivas interfaces de mensagem e COM, edição de texto, formatação, quebra de linha, layout de tabela simples, layout de texto vertical, layout de texto bidirecional, suporte a indic e tailandês, uma interface do usuário de edição muito como interfaces Microsoft Word e Modelo de Objeto de Texto.

Juntamente com as interfaces de Edição Avançada, os aplicativos podem usar a função [**Rich Edit TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) para analisar, formata, posicionar e quebrar linhas automaticamente. Para obter mais informações, consulte [Rich Edit Controls](../controls/rich-edit-controls.md).

## <a name="complex-script-processing-using-uniscribe"></a>Processamento de script complexo usando Uniscribe

[O Uniscribe](uniscribe.md) fornece o suporte mais amplo para processamento de texto que envolve efeitos de tipografia finos e scripts complexos. Ele dá suporte às regras complexas encontradas em scripts como árabe, devanagari e tailandês. Ele lida com scripts escritos da direita para a esquerda, como árabe e hebraico, e dá suporte à combinação de scripts. O Uniscribe também expõe recursos [de fonte OpenType](opentype-font-format.md) que podem ser usados por aplicativos para controlar efeitos de tipografia finos. Para obter mais informações, [consulte Processing Complex Scripts](processing-complex-scripts.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Uniscribe](about-uniscribe.md)
</dt> <dt>

[Processamento de scripts complexos](processing-complex-scripts.md)
</dt> </dl>

 

 
