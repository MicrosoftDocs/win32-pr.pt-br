---
title: Controle PUSHBUTTON (menus e outros recursos)
description: Define um controle de botão de push. O controle é um retângulo arredondado que contém o texto determinado. O texto é centralizado no controle . O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menus de controle PUSHBUTTON e outros recursos
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24db89c986f3f6d466f1710bc18420f9da9eec3348eada10e95582a882fe25e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776996"
---
# <a name="pushbutton-control"></a>Controle PUSHBUTTON

Define um controle de botão de push. O controle é um retângulo arredondado que contém o texto determinado. O texto é centralizado no controle . O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para o botão de push, que pode ser uma combinação do estilo **BS \_ PUSHBUTTON** e dos seguintes estilos: **WS \_ TABSTOP,** **WS \_ DISABLED** e **WS \_ GROUP**.

Se você não especificar um estilo, o estilo padrão será `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da **instrução PUSHBUTTON:**

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Getdialogbaseunits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Botões](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 