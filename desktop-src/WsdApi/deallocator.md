---
description: Especifica o tipo de desalocação a ser usado por uma função de stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento dealocador
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2617ce92dcd0c2763f77b0bc6f0fb5c1beea1c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881052"
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

O tipo de desalocador deve ser incluído em um par de &lt; marcas de desalocação &gt; </deallocator> . As cadeias de caracteres a seguir são valores válidos de dealocador:

-   nenhum
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   livre
-   excluir
-   deleteArray
-   Versão

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




