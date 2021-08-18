---
description: Define um grupo de atributos que é usado por uma variedade de elementos em um arquivo XML de diário. Ele contém atributos usados para definir os limites (esquerda, superior, altura e largura) de um elemento no documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Grupo de Atributos BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba91269660875e55b92797609969ebee38d221016914d9473cd5eddd245cfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967765"
---
# <a name="boundstype-attribute-group"></a>Grupo de Atributos BoundsType

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
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitante do elemento.<br/> | Qualquer inteiro.<br/>              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais alto na caixa delimitada do elemento.<br/>  | Qualquer inteiro.<br/>              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitada para o elemento.<br/>                                          | Qualquer inteiro não negativo.<br/> |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitada para o elemento.<br/>                                         | Qualquer inteiro não negativo.<br/> |



 

## <a name="type-information"></a>Informações do Tipo



|                 | Valor                                      |
|-----------------|--------------------------------------------|
| **Namespace**   | urn:schemas-microsoft-com:tabletpc:richink |
| **Nome do esquema** | Leitor de Diário                             |



 

## <a name="remarks"></a>Comentários

**Left** e **Top** podem ser negativos porque a origem é definida pelas margens, não pela página.

 

 




