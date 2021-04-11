---
description: Gera constantes C para tabelas de esquema XML para tipos de mensagem.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f86043cc28b527778c91772ad731d3a271921f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165304"
---
# <a name="messagetypedefinitions-element"></a>elemento messageTypeDefinitions

Gera constantes C para tabelas de esquema XML para tipos de mensagem.

## <a name="usage"></a>Uso

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
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

Esse elemento é geralmente usado em arquivos de origem C para fornecer as tabelas de esquema declaradas por [**messageTypeDeclarations**](messagetypedeclarations.md).

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




