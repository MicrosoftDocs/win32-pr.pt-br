---
description: Gera constantes C para tabelas de esquema XML para tipos de mensagem.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: Elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a94fabdd2ceb2d32052a692f6daa1abba0a52f16d5d1b7dd0a4cef07d33de09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757076"
---
# <a name="messagetypedefinitions-element"></a>Elemento messageTypeDefinitions

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
| [**Operação**](operation.md)<br/> | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>  |
| [**Porttype**](porttype.md)<br/>   | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/> |



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
| [**Arquivo**](file.md)<br/> | Saída de um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse elemento geralmente é usado em arquivos de origem C para fornecer as tabelas de esquema declaradas por [**messageTypeDeclarations**](messagetypedeclarations.md).

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




