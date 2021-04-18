---
description: Gera declarações para funções de stub para operações de tipo de porta.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815583"
---
# <a name="stubdeclarations-element"></a>elemento stubDeclarations

Gera declarações para funções de stub para operações de tipo de porta.

## <a name="usage"></a>Uso

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**LostFocus**](events.md)<br/>       | Especifica se os eventos relacionados estão incluídos nas funções geradas.<br/> <br/> |
| [**operacional**](operation.md)<br/> | Especifica uma operação para a qual o código deve ser gerado.<br/> <br/>                 |
| [**portType**](porttype.md)<br/>   | Especifica o tipo de porta para o qual o código deve ser gerado.<br/> <br/>                |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




