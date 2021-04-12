---
title: Controle RTEXT
description: Define um controle de texto alinhado à direita.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menus de controle do RTEXT e outros recursos
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454059"
---
# <a name="rtext-control"></a>Controle RTEXT

Define um controle de texto alinhado à direita. O controle é um retângulo simples que exibe o texto determinado alinhado à direita no retângulo. O texto é formatado antes de ser exibido. As palavras que ultrapassaram o final de uma linha são automaticamente encapsuladas no início da próxima linha. Palavras que são maiores que a largura do controle são truncadas.

A instrução **RTEXT** , que pode ser usada somente em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o texto, o identificador, as dimensões e os atributos do controle.

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos para o controle de texto, que pode ser qualquer combinação dos seguintes: **WS \_ TabStop** e **WS \_ Group**.

Se você não especificar um estilo, o estilo padrão será `SS_RIGHT | WS_GROUP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução **RTEXT** :

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CONTROLO**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> </dl>

 

 