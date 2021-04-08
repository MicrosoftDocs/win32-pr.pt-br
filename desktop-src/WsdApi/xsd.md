---
description: Especifica um arquivo XSD para processar informações de contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828498"
---
# <a name="xsd-element"></a>elemento xsd

Especifica um arquivo XSD para processar informações de contrato.

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
| **path**<br/> | Cadeia de nome do caminho<br/> | Sim<br/> | Arquivo e caminho do arquivo de entrada XSD.<br/> <br/> |



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

A cadeia de caracteres do nome do arquivo deve incluir informações completas de caminho também.

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




