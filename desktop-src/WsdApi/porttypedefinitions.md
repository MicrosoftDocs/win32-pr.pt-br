---
description: Gera constantes C para tipos de porta.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169651"
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
| [**Codinome**](codename.md)<br/>                   | Especifica o nome a ser usado para o tipo de porta no código gerado. Por padrão, o nome do código é gerado a partir do nome qualificado do tipo de porta.<br/> <br/>         |
| [**eventStubFunction**](eventstubfunction.md)<br/> | Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações de notificação.<br/> <br/>        |
| [**operacional**](operation.md)<br/>                 | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                                                                                                  |
| [**portType**](porttype.md)<br/>                   | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                                                                                                 |
| [**stubFunction**](stubfunction.md)<br/>           | Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações unidirecionais e bidirecionais.<br/> <br/> |



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
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse elemento é geralmente usado em arquivos de origem C para fornecer as constantes de tipo de porta declaradas por [**portTypeDeclarations**](porttypedeclarations.md).

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




