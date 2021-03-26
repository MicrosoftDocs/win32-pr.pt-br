---
description: A tabela a seguir especifica as métricas de fonte mais importantes para aplicativos que exigem documentos portáteis e as funções que permitem que um aplicativo os recupere.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Métricas para documentos portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c840b1b8e8014086b97098a44890f170a6bd11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967651"
---
# <a name="metrics-for-portable-documents"></a>Métricas para documentos portáteis

A tabela a seguir especifica as métricas de fonte mais importantes para aplicativos que exigem documentos portáteis e as funções que permitem que um aplicativo os recupere.



| Função                                               | Métrica                | Uso                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | Recuperação de métricas de design; conversão para métricas do dispositivo.                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | Posicionamento preciso de caracteres no início e no final das margens, limites de imagem e outras quebras de texto. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **AdvanceWidths**     | Posicionamento de caracteres em uma linha.                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | Bits de inserção de fonte.                                                                                         |
|                                                        | **otmsCharSlopeRise** | Componente Y para a inclinação do cursor para fontes em itálico.                                                            |
|                                                        | **otmsCharSlopeRun**  | Componente X para a inclinação do cursor para fontes em itálico.                                                            |
|                                                        | **otmAscent**         | Espaçamento de linha.                                                                                                |
|                                                        | **otmDescent**        | Espaçamento de linha.                                                                                                |
|                                                        | **otmLineGap**        | Espaçamento de linha.                                                                                                |
|                                                        | **otmpFamilyName**    | Identificação da fonte.                                                                                         |
|                                                        | **otmpStyleName**     | Identificação da fonte.                                                                                         |
|                                                        | **otmpFullName**      | Identificação de fonte (normalmente, nome de família e estilo).                                                      |



 

Os membros **otmsCharSlopeRise**, **otmsCharSlopeRun**, **otmAscent**, **otmDescent** e **otmLineGap** da estrutura [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) são dimensionados ou transformados para corresponder ao modo de dispositivo atual e à altura física (conforme especificado no membro **tmHeight** da estrutura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) ).

A identificação da fonte é importante nessas instâncias quando um aplicativo deve selecionar a mesma fonte, por exemplo, quando um documento é reaberto ou movido para um sistema operacional diferente. O mapeador de fontes sempre seleciona a fonte correta quando um aplicativo solicita uma fonte por nome completo. Os nomes de família e estilo fornecem entrada para a caixa de diálogo fonte padrão, o que garante que as barras de seleção sejam colocadas corretamente.

Os valores **otmsCharSlopeRise** e **otmsCharSlopeRun** são usados para produzir uma aproximação aproximada do ângulo principal em itálico da fonte. Para fontes romanos típicas, **otmsCharSlopeRise** é 1 e **otmsCharSlopeRun** é 0. Para fontes em itálico, os valores tentam aproximar o seno e o cosseno do ângulo de itálico principal da fonte (em graus no sentido anti-horário além da vertical); Observe que o ângulo em itálico para fontes verticais é 0. Como esses valores não são expressos em unidades de design, eles não devem ser convertidos em unidades de dispositivo.

As métricas de posicionamento de caracteres e espaçamento de linha permitem que um aplicativo Compute quebras de linha independentes de dispositivo que são portáteis entre telas, impressoras, typesetters e até mesmo plataformas.

**Para executar o layout de página independente de dispositivo**

1.  Normalizar todas as métricas de design para um valor comum de UHR (resolução extremamente alta) (por exemplo, 65.536 DPI); Isso evita erros de arredondamento.
2.  Computação de quebras de linha com base em métricas de UHR e largura de página física; Isso produz um ponto de partida e um ponto final de uma linha dentro do fluxo de texto.
3.  Calcule a largura da página do dispositivo nas unidades do dispositivo (por exemplo, pixels).
4.  Ajuste cada linha de texto na largura da página do dispositivo, usando as quebras de linha computadas na etapa 2.
5.  Computar quebras de página usando métricas UHR e o comprimento físico da página; Isso produz o número de linhas por página.
6.  Calcule as alturas de linha nas unidades do dispositivo.
7.  Ajuste as linhas de texto na página, usando as linhas por página da etapa 5 e as alturas de linha da etapa 6.

Se todos os aplicativos adotarem essas técnicas, os desenvolvedores poderão praticamente garantir que os documentos movidos de um aplicativo para outro manterão sua aparência e formato originais.

 

 



