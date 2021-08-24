---
description: O objeto Divisor fornece recursos de análise de layout que classificam e agrupam traços em diferentes elementos estruturais.
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: Análise de tinta com o objeto divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d036428bbe32c42e6419c2218e6196a0b89a892137e55d141d5553d360c0a652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939547"
---
# <a name="ink-analysis-with-the-divider-object"></a>Análise de tinta com o objeto divisor

O [objeto Divisor](/previous-versions/ms583616(v=vs.100)) fornece recursos de análise de layout que classificam e agrupam traços em diferentes elementos estruturais.

## <a name="divider-object"></a>Objeto Divisor

O [objeto Divisor](/previous-versions/ms583616(v=vs.100)) analisa traços conforme você os adiciona ou remove. Você pode recuperar a classificação e o agrupamento atuais dos traços analisados em um objeto [DivisionResult](/previous-versions/ms583620(v=vs.100)) chamando o método [Divide](/previous-versions/ms568936(v=vs.100)) do objeto Divider.

Os traços analisados [pelo objeto Divider](/previous-versions/ms583616(v=vs.100)) são mantidos na propriedade [Strokes](/previous-versions/ms582090(v=vs.100)) do objeto Divider. Como uma [coleção strokes](/previous-versions/ms552701(v=vs.100)) é uma referência a dados de tinta [](/previous-versions/ms583670(v=vs.100)) e não são os dados reais em si, as alterações no objeto ink pai da coleção Strokes podem invalidar a coleção Strokes. Para obter mais informações sobre dados de tinta, consulte [Dados de tinta.](ink-data.md)

O [objeto Divisor](/previous-versions/ms583616(v=vs.100)) usa um contexto de reconhecedor para melhorar sua análise de segmentos de reconhecimento e gerar texto de reconhecimento para elementos manuscritos. Se um contexto de reconhecedor não for atribuído à propriedade [RecognizerContext](/previous-versions/ms582089(v=vs.100)) do objeto divisor ou os reconhecedores não estão instalados, o recurso de análise de layout executará a divisão do segmento de reconhecimento e nenhum texto será associado ao objeto [DivisionResult.](/previous-versions/ms583620(v=vs.100)) Para obter mais informações sobre o reconhecimento de tinta, consulte [Reconhecimento de tinta.](ink-recognition.md)

## <a name="divisionresult-object"></a>Objeto DivisionResult

Cada [objeto DivisionResult](/previous-versions/ms583620(v=vs.100)) registra a análise de layout dos traços contidos pelo objeto [Divider](/previous-versions/ms583616(v=vs.100)) no momento em que o [método Divide](/previous-versions/ms568936(v=vs.100)) é chamado. O objeto DivisionResult também armazena uma cópia dos traços que foram usados na análise.

O [objeto DivisionResult](/previous-versions/ms583620(v=vs.100)) grupos os resultados da análise por tipo de elemento estrutural. O [**método ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) do objeto DivisionResult retorna em uma coleção [DivisionUnits](/previous-versions/ms583625(v=vs.100)) a coleção de todos os elementos estruturais de um determinado tipo. A [enumeração InkDivisionType](/previous-versions/ms552251(v=vs.100)) define os tipos de elemento que a análise de layout reconhece.

A tabela a seguir descreve os tipos de elemento na [enumeração InkDivisionType.](/previous-versions/ms552251(v=vs.100))



| Nome                 | Descrição                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Segment<br/>   | Um segmento de reconhecimento.<br/>                                                |
| Linha<br/>      | Uma linha de manuscrito que contém um ou mais segmentos de reconhecimento.<br/> |
| Paragraph<br/> | Um bloco de traços que contém uma ou mais linhas de manuscrito.<br/>    |
| Desenho<br/>   | Tinta que não é texto.<br/>                                                 |



 

A imagem a seguir mostra um exemplo dos diferentes tipos de elemento que o [objeto DivisionResult](/previous-versions/ms583620(v=vs.100)) reconhece.

![ilustração de diferentes tipos de elemento que o objeto divisionresult reconhece](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>Objetos DivisionUnits Collection e DivisionUnit

Cada [coleção DivisionUnits](/previous-versions/ms583625(v=vs.100)) é uma cópia do resultado da análise de layout para um único tipo de elemento estrutural. O [objeto DivisionUnit](/previous-versions/ms583624(v=vs.100)) representa um elemento individual na coleção DivisionUnits. Cada elemento estrutural tem uma referência aos traços que comem o elemento. Se os reconhecedores estão instalados, os elementos de manuscrito têm texto de reconhecimento disponível. Os elementos do segmento de linha e reconhecimento também incluem uma matriz de rotação que pode girar os traços de um elemento de vertical para horizontal.

O [tópico Exemplo de Divisor](ink-divider-sample.md) de Tinta Digital demonstra como usar um objeto [Divisor](/previous-versions/ms583616(v=vs.100)) com objetos [ink](/previous-versions/ms583670(v=vs.100)) para executar a análise de layout de tinta.

Para obter mais informações sobre como usar a análise de tinta, consulte [O objeto divisor](the-divider-object.md).

 

