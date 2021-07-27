---
description: Define um grupo de atributos que é usado por uma variedade de elementos em um arquivo XML de diário. Ele contém atributos usados para definir os limites (esquerda, superior, altura e largura) de um elemento no documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Grupo de atributos BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c51fcb9bc0041bbc030f2c67e434a964212562
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436491"
---
# <a name="boundstype-attribute-group"></a>Grupo de atributos BoundsType

Define um grupo de atributos que é usado por uma variedade de elementos em um arquivo XML de diário. Ele contém atributos usados para definir os limites (esquerda, superior, altura e largura) de um elemento no documento.

## <a name="definition"></a>Definição

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.<br/> | Qualquer inteiro.<br/>              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.<br/>  | Qualquer inteiro.<br/>              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.<br/>                                          | Qualquer inteiro não negativo.<br/> |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.<br/>                                         | Qualquer inteiro não negativo.<br/> |



 

## <a name="type-information"></a>Informações do Tipo



|                 | Valor                                      |
|-----------------|--------------------------------------------|
| **Namespace**   | urn: esquemas-Microsoft-com: Tablet: RichInk |
| **Nome do esquema** | Leitor de diário                             |



 

## <a name="remarks"></a>Comentários

**Left** e **Top** podem ser negativos porque a origem é definida pelas margens, não pela página.

 

 




