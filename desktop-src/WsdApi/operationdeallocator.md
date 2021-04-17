---
description: Especifica a desalocação de tipo a ser usada por uma função de stub de operações.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763497"
---
# <a name="operationdeallocator-element"></a>elemento operationDeallocator

Especifica a desalocação de tipo a ser usada pela função de stub de uma operação.

## <a name="usage"></a>Uso

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo                  | Type                         | Obrigatório       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **desalocador**<br/> | Cadeia de caracteres \_<br/> | Yes<br/> | O desalocador a ser usado para a operação.<br/> <br/> As cadeias de caracteres a seguir são valores válidos.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span>* * * * <dt>nenhum * * * *</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> * * * * <dt>WSDFreeLinkedMemory * * * *</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> * * * * <dt>CoTaskMemFree * * * *</dt> <span id="free"></span> <span id="FREE"></span> * * * * <dt>gratuito * *</dt> <span id="delete"></span> <span id="DELETE"></span> * * <dt>* * * * excluir * * * *</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> * * * * <dt>deleteArray * * * *</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> * * * * <dt>Versão *</dt> * * * </dl> |
| **operation**<br/>   | Cadeia de caracteres \_<br/> | Yes<br/> | O nome da operação.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                               | Descrição                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Gera implementações para funções de stub para operações de tipo de porta.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




