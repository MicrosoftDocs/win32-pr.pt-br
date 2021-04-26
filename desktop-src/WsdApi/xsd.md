---
description: Especifica um arquivo XSD para processar informações de contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994543"
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



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




