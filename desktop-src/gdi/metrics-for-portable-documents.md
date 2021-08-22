---
description: A tabela a seguir especifica as métricas de fonte mais importantes para aplicativos que exigem documentos portáteis e as funções que permitem que um aplicativo os recupere.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Métricas para documentos portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762846e6d8280c2680f47f3cb32cd847ea4e664dab47a8a0995f5505c393da3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558496"
---
# <a name="metrics-for-portable-documents"></a>Métricas para documentos portáteis

A tabela a seguir especifica as métricas de fonte mais importantes para aplicativos que exigem documentos portáteis e as funções que permitem que um aplicativo os recupere.



| Função                                               | Métrica                | Usar                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**Enumfontfamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | Recuperação de métricas de design; conversão em métricas de dispositivo.                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | Posicionamento preciso de caracteres no início e no final de margens, limites de imagem e outras quebras de texto. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **AdvanceWidths**     | Posicionamento de caracteres em uma linha.                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | Bits de incorporação de fonte.                                                                                         |
|                                                        | **otmsCharSlopeRise** | Componente Y para inclinação do cursor para fontes itálico.                                                            |
|                                                        | **otmsCharSopeRun**  | Componente X para inclinação do cursor para fontes itálico.                                                            |
|                                                        | **otmAscent**         | Espaçamento de linha.                                                                                                |
|                                                        | **otmDescent**        | Espaçamento de linha.                                                                                                |
|                                                        | **otmLineGap**        | Espaçamento de linha.                                                                                                |
|                                                        | **otmpFamilyName**    | Identificação de fonte.                                                                                         |
|                                                        | **otmpStyleName**     | Identificação de fonte.                                                                                         |
|                                                        | **otmpFullName**      | Identificação de fonte (normalmente, família e nome de estilo).                                                      |



 

Os membros **otmsCharSopeeRise**, **otmsCharSopeeRun**, **otmAscent**, **otmDescent** e **otmLineGap** da estrutura [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) são dimensionados ou transformados para corresponder ao modo de dispositivo atual e à altura física (conforme especificado no membro **tmHeight** da [estrutura NEWTEXTMETRIC).](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)

A identificação de fonte é importante nessas instâncias quando um aplicativo deve selecionar a mesma fonte, por exemplo, quando um documento é reaberto ou movido para um sistema operacional diferente. O mapeado de fonte sempre seleciona a fonte correta quando um aplicativo solicita uma fonte por nome completo. Os nomes de família e estilo fornecem entrada para a caixa de diálogo de fonte padrão, o que garante que as barras de seleção sejam corretamente colocadas.

Os **valores otmsCharSopeRise** e **otmsCharSopeRun** são usados para produzir uma aproximação próxima do ângulo itálico principal da fonte. Para fontes típicas de roman, **otmsCharSopeeRise** é 1 e **otmsCharSlopeRun** é 0. Para fontes itálico, os valores tentam aproximar o seno e o cosseno do ângulo itálico principal da fonte (em graus no sentido anti-horário após a vertical); observe que o ângulo itálico para fontes de vertical é 0. Como esses valores não são expressos em unidades de design, eles não devem ser convertidos em unidades de dispositivo.

As métricas de posicionamento de caracteres e espaçamento de linha permitem que um aplicativo compute quebras de linha independentes de dispositivo que são portáteis entre telas, impressoras, tipos e até mesmo plataformas.

**Para executar o layout da página independente do dispositivo**

1.  Normalizar todas as métricas de design para um valor COMUM de UHR (ultra alta resolução) (por exemplo, 65.536 DPI); isso impede erros de arredondar.
2.  Quebras de linha de computação com base nas métricas de UHR e na largura da página física; isso gera um ponto de partida e um ponto final de uma linha dentro do fluxo de texto.
3.  Compute a largura da página do dispositivo em unidades de dispositivo (por exemplo, pixels).
4.  Ajuste cada linha de texto na largura da página do dispositivo, usando as quebras de linha computadas na etapa 2.
5.  Quebras de página de computação usando métricas UHR e o comprimento da página física; isso gera o número de linhas por página.
6.  Compute as alturas de linha em unidades de dispositivo.
7.  Ajuste as linhas de texto na página, usando as linhas por página da etapa 5 e as alturas de linha da etapa 6.

Se todos os aplicativos adotarem essas técnicas, os desenvolvedores praticamente poderão garantir que os documentos movidos de um aplicativo para outro manterão sua aparência e formato originais.

 

 



