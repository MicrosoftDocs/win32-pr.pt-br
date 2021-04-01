---
description: Define um grupo de atributos que é usado por uma variedade de elementos em um arquivo XML de diário. Ele contém atributos usados para definir os limites (esquerda, superior, altura e largura) de um elemento no documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Grupo de atributos BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646551"
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
| **Mantida**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.<br/> | Qualquer inteiro.<br/>              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.<br/>  | Qualquer inteiro.<br/>              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.<br/>                                          | Qualquer inteiro não negativo.<br/> |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.<br/>                                         | Qualquer inteiro não negativo.<br/> |



 

## <a name="type-information"></a>Informações do Tipo



|             |                                            |
|-------------|--------------------------------------------|
| Namespace   | urn: esquemas-Microsoft-com: Tablet: RichInk |
| Nome do esquema | Leitor de diário                             |



 

## <a name="remarks"></a>Comentários

**Left** e **Top** podem ser negativos porque a origem é definida pelas margens, não pela página.

 

 




