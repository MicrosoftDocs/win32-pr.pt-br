---
description: Gera implementações para as funções QueryInterface, AddRef e Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995143"
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
| **proxyClass**<br/>  | Cadeia de caracteres \_<br/> | Sim<br/> | O nome da classe de implementação.<br/> <br/> |
| **refCountVar**<br/> | Cadeia de caracteres \_<br/> | Sim<br/> | O nome da variável de contagem de referência.<br/> <br/>  |



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



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




