---
description: Contém dados binários codificados para uma imagem no documento do diário, se presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b1cfd62dd6c2f58c2c1da26f0a9564b8c070f5c57fdccc870fa8b52b3f37c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939826"
---
# <a name="image-element"></a>Elemento de imagem

Contém dados binários codificados para uma imagem no documento do diário, se presente.

## <a name="definition"></a>Definição

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a>Elementos pai

[**Conteúdo**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|---------------------------------------------------------|
| Tipo de elemento | ComplexType [**ImageType**](imagetype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk              |
| Nome do esquema  | Leitor de diário                                          |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Segundo plano**](background-element.md)
</dt> </dl>

 

 



