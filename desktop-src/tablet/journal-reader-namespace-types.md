---
description: Esta seção documenta os tipos XML usados pelo componente de leitor de diário.
ms.assetid: 08b45fe0-a505-4cc0-9791-764a87e8f1eb
title: Tipos de namespace de leitor de diário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e8e3d812eea879ca9dd31680aa2834d6dfe50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169892"
---
# <a name="journal-reader-namespace-types"></a>Tipos de namespace de leitor de diário

Esta seção documenta os tipos XML usados pelo componente de leitor de diário.

## <a name="in-this-section"></a>Nesta seção



| Tipo                                                                                  | Descrição                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComplexType AlternatesListType**](alternateslisttype-complex-type.md)             | Define o tipo que contém a lista de alternativas de reconhecimento para uma palavra de tinta.<br/>                                                                                                                  |
| [**ComplexType de BackgroundImagetype**](backgroundimagetype-complex-type.md)           | Define o tipo que contém informações sobre a imagem de plano de fundo usada pela nota do diário, se houver.<br/>                                                                                                |
| [**ComplexType em segundo plano**](backgroundtype-complex-type.md)                     | Define o tipo que contém as informações de plano de fundo da nota do diário.<br/>                                                                                                                     |
| [**ComplexType de baselinetype**](baselinetype-complex-type.md)                         | Define o tipo que contém informações sobre a linha de base de um parágrafo.<br/>                                                                                                                       |
| [AttributeGroup BoundsType](boundstype-attributegroup.md)                            | Define um grupo de atributos que é usado por uma variedade de elementos em um arquivo XML de diário.<br/>                                                                                                             |
| [**SimpleType de ColorType**](colortype-simple-type.md)                                 | Define o tipo que é usado para especificar valores válidos para a cor de determinados elementos em um arquivo XML de diário.<br/>                                                                                      |
| [Grupo de grupos de conteúdo](contentgroup-group.md)                                          | Define o tipo que contém um conjunto de conteúdo agrupado em uma nota do diário.<br/>                                                                                                                          |
| [**ComplexType ContentType**](contenttype-complex-type.md)                           | Define o tipo que contém alguma forma de conteúdo dentro de um arquivo XML de diário.<br/>                                                                                                                      |
| [**SimpleType de ContentTypetype**](contenttypetype-simple-type.md)                     | Define o tipo que define valores válidos para o atributo **Type** do [leitor \[ \] de diário de elementos de conteúdo](content-element--journal-reader.md).<br/>                                             |
| [**ComplexType de drawingtype**](drawingtype-complex-type.md)                           | Define o tipo que contém tinta que foi classificada pelo mecanismo de análise de diário como um [elemento de desenho](drawing-element.md) (em oposição a um [elemento InkWord](inkword-element.md)).<br/>  |
| [**ComplexType de flagType**](flagtype-complex-type.md)                                 | Define o tipo que contém a imagem binária codificada e as informações de posição de um sinalizador inserido em um documento de diário.<br/>                                                                         |
| [**ComplexType GroupNodeType**](groupnodetype-complex-type.md)                       | Define o tipo que contém um conjunto de conteúdo agrupado em uma nota do diário.<br/>                                                                                                                          |
| [**ComplexType de horizontaltype**](horizontaltype-complex-type.md)                     | Define o tipo que contém informações sobre linhas horizontais usadas pelo papel de carta em uma nota do diário.<br/>                                                                                         |
| [**ImageType complexType**](imagetype-complex-type.md)                               | Define o tipo que contém as informações binárias de uma imagem em uma nota do diário. Confira também o [**complexType de backgroundimagetype**](backgroundimagetype-complex-type.md).<br/>                     |
| [**ComplexType InkWordType**](inkwordtype-complex-type.md)                           | Define o tipo que contém os dados de tinta, alternativas e confiança para o conteúdo de tinta que é um [elemento InkWord](inkword-element.md) (em oposição a um [elemento de desenho](drawing-element.md)).<br/> |
| [**ComplexType JournalPageType**](journalpagetype-complex-type.md)                   | Define o tipo que contém uma página individual em uma nota do diário.<br/>                                                                                                                                |
| [**ComplexType LineLayoutType**](linelayouttype-complex-type.md)                     | Define o tipo que contém informações sobre as linhas que são usadas em um determinado papel de carta da nota do diário.<br/>                                                                                      |
| [**LineLayoutStyleType simpleType**](linelayoutstyletype-simple-type.md)             | Define os valores válidos para o atributo **Style** do [elemento LineLayout](linelayout-element.md).<br/>                                                                                           |
| [**ComplexType LineType**](linetype-complex-type.md)                                 | Define o tipo que contém uma linha de parágrafo.<br/>                                                                                                                                                 |
| [**ComplexType de margintype**](margintype-complex-type.md)                             | Define o tipo que contém os detalhes sobre todas as margens na nota do diário, como estilo, cor e posição.<br/>                                                                               |
| [**MarginTypeType simpleType**](margintypetype-simple-type.md)                       | Define o tipo que contém valores válidos para o atributo **Type** para o [elemento Margin](margin-element.md).<br/>                                                                                |
| [**ComplexType de paragraphtype**](paragraphtype-complex-type.md)                       | Define o tipo que contém um parágrafo em uma nota do diário.<br/>                                                                                                                                          |
| [**ComplexType ParagraphLineMetricsType**](paragraphlinemetricstype-complex-type.md) | Define o tipo que contém informações sobre as métricas de linha de um parágrafo, como a linha de base.<br/>                                                                                             |
| [**ComplexType de reflowtype**](reflowtype-complex-type.md)                             | Define o tipo que indica que o grupo foi refluído.<br/>                                                                                                                                        |
| [**ComplexType ScalarTransformType**](scalartransformtype-complex-type.md)           | Define o tipo que contém as informações sobre qualquer transformação aplicada à tinta.<br/>                                                                                                                |
| [**ComplexType StationeryType**](stationerytype-complex-type.md)                     | Define o tipo que contém o papel de carta usado pela nota do diário.<br/>                                                                                                                             |
| [**ComplexType de tipo**](texttype-complex-type.md)                                 | Define o tipo que contém o valor de texto em um [ \[ leitor \] de diário de elementos de conteúdo](content-element--journal-reader.md).<br/>                                                                       |
| [**ComplexType TitleAreaType**](titleareatype-complex-type.md)                       | Define o tipo que contém informações de posição e limites para o título em uma nota do diário.<br/>                                                                                                     |
| [**ComplexType TitleInfoType**](titleinfotype-complex-type.md)                       | Define o tipo que contém informações sobre o título em uma nota do diário.<br/>                                                                                                                       |
| [**ComplexType de títulotype**](titletype-complex-type.md)                               | Define o tipo que contém informações de título para a nota do diário.<br/>                                                                                                                              |
| [**ComplexType de verticaltype**](verticaltype-complex-type.md)                         | Define o tipo que contém detalhes sobre as linhas verticais usadas em um papel de carta da nota do diário.<br/>                                                                                                |



 

 

 




