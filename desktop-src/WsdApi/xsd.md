---
description: Especifica um arquivo XSD a ser processado para obter informações de contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: Elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f790375c34a4d5afc3dc345691c8e26e5f95cebe0bbde283e2986e838cce554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995086"
---
# <a name="xsd-element"></a>Elemento xsd

Especifica um arquivo XSD a ser processado para obter informações de contrato.

## <a name="usage"></a>Uso

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a>Atributos



| Atributo           | Type                       | Obrigatório       | Descrição                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| **path**<br/> | cadeia de caracteres pathname<br/> | Sim<br/> | Arquivo e caminho do arquivo de entrada XSD.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                               | Descrição                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**typeUri**](typeuri.md)<br/> | Especifica um tipo a ser incluído de um arquivo XSD.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
typeUri*
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                                     | Descrição                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentários

A cadeia de caracteres filename também deve incluir informações completas de caminho.

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




