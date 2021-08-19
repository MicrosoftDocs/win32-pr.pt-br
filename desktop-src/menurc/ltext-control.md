---
title: Controle LTEXT
description: Define um controle de texto alinhado à esquerda.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menus de controle LTEXT e outros recursos
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdaafe752d547466267e8494743e8f0c99ccef0d0fb05b77db5dab2fa358f158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870270"
---
# <a name="ltext-control"></a>Controle LTEXT

Define um controle de texto alinhado à esquerda. O controle é um retângulo simples que exibe o texto determinado alinhado à esquerda no retângulo. O texto é formatado antes de ser exibido. Palavras que se estenderiam após o final de uma linha são automaticamente empacotados para o início da próxima linha. Palavras com mais tempo que a largura do controle são truncadas.

A **instrução LTEXT,** que pode ser usada somente em uma instrução [**DIALOGEX,**](dialogex-resource.md) define o texto, o identificador, as dimensões e os atributos do controle.

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser qualquer combinação do estilo **\_ RADIOBUTTON BS** e os seguintes estilos: **SS \_ LEFT,** **\_ WS TABSTOP e** **WS \_ GROUP**.

Se você não especificar um estilo, o estilo padrão será `SS_LEFT | WS_GROUP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de texto alinhado à esquerda rotulado como Nome do arquivo:

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controle**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 