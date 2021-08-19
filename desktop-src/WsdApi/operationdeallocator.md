---
description: Especifica o desaloqueador de tipo a ser usado por uma função de stub de operações.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: Elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ce2902bbfac16cb096da334cf3f22a12c68e3720d575fa303b8f3b133c9328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991686"
---
# <a name="operationdeallocator-element"></a>Elemento operationDeallocator

Especifica o desaloqueador de tipo a ser usado pela função stub de uma operação.

## <a name="usage"></a>Uso

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo                  | Type                         | Obrigatório       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **desalocador**<br/> | cadeia de \_ caracteres<br/> | Sim<br/> | O desalocador a ser usado para a operação.<br/> <br/> As cadeias de caracteres a seguir são valores válidos.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span><dt>***nenhum****</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> <dt>****WSDFreeLinkedMemory****</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> <dt>****CoTaskMemFree****</dt> <span id="free"></span> <span id="FREE"></span> <dt>****free****</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>****delete****</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>****deleteArray****</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>****Versão****</dt> </dl> |
| **operation**<br/>   | cadeia de \_ caracteres<br/> | Sim<br/> | O nome da operação.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                               | Descrição                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Gera implementações para funções stub para operações de tipo de porta.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




