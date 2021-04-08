---
description: Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922414"
---
# <a name="messagetypedeclarations-element"></a>elemento messageTypeDeclarations

Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.

## <a name="usage"></a>Uso

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**operacional**](operation.md)<br/> | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>  |
| [**portType**](porttype.md)<br/>   | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

As tabelas de esquema são referenciadas por definições de tipo de porta. Esse elemento é, portanto, geralmente usado logo antes dos elementos [**portTypeDefinitions**](porttypedefinitions.md) .

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




