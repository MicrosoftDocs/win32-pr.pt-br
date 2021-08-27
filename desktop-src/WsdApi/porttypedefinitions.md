---
description: Gera constantes C para tipos de porta.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9beb5b6697f53ecc3a9f7c805338c6ccebd9901d483607b100f5d1602ff4c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071386"
---
# <a name="porttypedefinitions-element"></a>elemento portTypeDefinitions

Gera constantes C para tipos de porta.

## <a name="usage"></a>Uso

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                   | Descrição                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codinome**](codename.md)<br/>                   | Especifica o nome a ser usado para o tipo de porta no código gerado. Por padrão, o nome do código é gerado com o nome qualificado do tipo de porta.<br/> <br/>         |
| [**eventStubFunction**](eventstubfunction.md)<br/> | Especifica se as referências de função stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações de notificação.<br/> <br/>        |
| [**Operação**](operation.md)<br/>                 | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                                                                                                  |
| [**Porttype**](porttype.md)<br/>                   | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                                                                                                 |
| [**stubFunction**](stubfunction.md)<br/>           | Especifica se as referências de função stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações de uso único e de duas vias.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Arquivo**](file.md)<br/> | Saída de um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse elemento geralmente é usado em arquivos de origem C para fornecer as constantes de tipo de porta declaradas por [**portTypeDeclarations**](porttypedeclarations.md).

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




