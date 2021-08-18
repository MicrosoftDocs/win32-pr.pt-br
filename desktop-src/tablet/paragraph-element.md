---
description: Contém um parágrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: 877bede54ef714a011903424b1f323f004264affefedbcfae0ab44f2dcf58816
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843396"
---
# <a name="paragraph-element"></a>Elemento Paragraph

Contém um parágrafo.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos pai

[**Conteúdo**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementos filho

[**Linha**](line-element.md)

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Atributos



| Atributo       | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**        | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**         | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**       | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura**      | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |
| **BlockNumber** | **xs:nonNegativeInteger** | Obrigatório | Número do bloco.                                                                           | Qualquer inteiro não negativo. |
| **LineNumber**  | **xs:nonNegativeInteger** | Obrigatório | A linha na qual o parágrafo começa.                                                 | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | ComplexType de [**paragraphtype**](paragraphtype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                      |
| Nome do esquema  | Leitor de diário                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Windows.ui.xaml.documents. h</dt> </dl> |



 

 




