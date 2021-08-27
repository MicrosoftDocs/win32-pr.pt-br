---
description: Define o texto ou CDATA a ser reutilizado pelo elemento include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: elemento macro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee876e04934a328e73b6e45d8442249ad3d749fc3b40fa45652c89979fcff6e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991716"
---
# <a name="macro-element"></a>elemento macro

Define o texto ou CDATA a ser reutilizado pelo elemento [**include**](include.md) .

## <a name="usage"></a>Uso

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo           | Type                         | Obrigatório       | Descrição                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **name**<br/> | Cadeia de caracteres \_<br/> | Sim<br/> | O nome da macro.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                     | Descrição                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentários

WsdCodeGen define uma macro chamada **DoNotModify**. Quando essa macro é incluída, o código gerado contém um bloco de comentário de alta visibilidade que instrui os desenvolvedores a não modificar o código gerado.

O XML a seguir mostra como incluir a macro **DoNotModify** . Esse XML pode ser adicionado a um arquivo de configuração XML para WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




