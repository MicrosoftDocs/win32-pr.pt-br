---
description: Especifica o tipo de desalocação a ser usado por uma função de stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento dealocador
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994933"
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



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




