---
title: TEXT. wordWrap
description: O atributo wordWrap especifica ou recupera um valor que indica se a quebra automática de texto está habilitada ou desabilitada.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- Windows Media Player de TEXT. wordWrap
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751573"
---
# <a name="textwordwrap"></a>TEXT. wordWrap

O atributo **WordWrap** especifica ou recupera um valor que indica se a quebra automática de texto está habilitada ou desabilitada.

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | A quebra automática de texto está habilitada.                                                                             |
| false | Padrão. A quebra automática de texto está desabilitada. Se o texto não couber no controle, o texto será cortado. |



 

## <a name="remarks"></a>Comentários

O controle de texto não separa as palavras. Se uma palavra ultrapassar a largura do controle, a quebra automática de linha será empregada para mover a palavra para a próxima. Se uma única palavra for maior do que a largura do controle, essa palavra será recortada e ocupará uma única linha.

Se o atributo **Width** não for especificado, **WordWrap** será ignorado e o controle Text será redimensionado em vez de encapsular o texto.

Se as quebras de linha forem desejadas em locais específicos, elas deverão ser especificadas explicitamente em **valor** usando "&\# 13;" ou " \\ r". Se o último formulário for usado ao especificar o valor diretamente, a cadeia de caracteres deverá ser prefixada com "JScript:" e o valor real deverá estar entre aspas simples, como mostrado abaixo. Isso não será necessário se o valor for definido dinamicamente de dentro de um manipulador de eventos.

Se **WordWrap** for definido como true e **ToolTip** não for especificado, a dica de ferramenta exibirá o texto completo do atributo **Value** . Se nenhuma dica de ferramenta for desejada, defina **ToolTip** como "" (cadeia de caracteres vazia).

## <a name="examples"></a>Exemplos


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ambiente. largura**](ambientattributes-width.md)
</dt> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXT. toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





