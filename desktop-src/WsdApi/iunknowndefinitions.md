---
description: Gera implementações para as funções QueryInterface, AddRef e Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763111"
---
# <a name="iunknowndefinitions-element"></a>Elemento IUnknownDefinitions

Gera implementações para as funções QueryInterface, AddRef e Release.

## <a name="usage"></a>Uso

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a>Atributos



| Atributo                  | Type                         | Obrigatório       | Descrição                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| **proxyClass**<br/>  | Cadeia de caracteres \_<br/> | Yes<br/> | O nome da classe de implementação.<br/> <br/> |
| **refCountVar**<br/> | Cadeia de caracteres \_<br/> | Yes<br/> | O nome da variável de contagem de referência.<br/> <br/>  |



## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [**interface**](interface.md)<br/> | O nome da interface a ser retornada por QueryInterface.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
interface
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




