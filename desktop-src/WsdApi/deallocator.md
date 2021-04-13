---
description: Especifica o tipo de desalocação a ser usado por uma função de stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento dealocador
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165311"
---
# <a name="deallocator-element"></a>elemento dealocador

Especifica o tipo de desalocação a ser usado por uma função de stub.

## <a name="usage"></a>Uso

``` syntax
<deallocator/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                               | Descrição                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Gera implementações para funções de stub para operações de tipo de porta.<br/> <br/> |



## <a name="remarks"></a>Comentários

O tipo de desalocação deve ser colocado em um par de <deallocator></deallocator> marcas. As cadeias de caracteres a seguir são valores válidos de dealocador:

-   nenhum
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   free
-   excluir
-   deleteArray
-   Versão

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




