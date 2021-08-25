---
description: Inclui o conteúdo de uma macro ou arquivo na saída gerada.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: incluir elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8029f58d9d1627a315fcfd02aa4f311d0a717361abf587aa92c52134b78e5958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856586"
---
# <a name="include-element"></a>incluir elemento

Inclui o conteúdo de uma macro ou arquivo na saída gerada.

## <a name="usage"></a>Uso

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo            | Type                         | Obrigatório      | Descrição                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| **file**<br/>  | cadeia de \_ caracteres<br/> | Não<br/> | O caminho para o arquivo a ser incluído.<br/> <br/>  |
| **Macro**<br/> | cadeia de \_ caracteres<br/> | Não<br/> | O nome da macro a ser incluído.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Arquivo**](file.md)<br/> | Direciona o gerador de código para gerar um arquivo e especifica o nome do arquivo de saída.<br/> <br/> |



## <a name="remarks"></a>Comentários

O atributo **de macro** ou o **atributo de** arquivo deve ser especificado. Não especifique ambos os atributos.

WsdCodeGen define uma macro chamada **DoNotModify**. Quando essa macro é incluída, o código gerado contém um bloco de comentários de alta visibilidade que instrui os desenvolvedores a não modificar o código gerado.

## <a name="examples"></a>Exemplos

O XML a seguir mostra como incluir a macro **DoNotModify.** Esse XML pode ser adicionado a um arquivo de configuração XML para WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




