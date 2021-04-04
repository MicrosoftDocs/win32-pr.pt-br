---
title: Controle CTEXT
description: Define um controle de texto centralizado.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menus de controle do CTEXT e outros recursos
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084500"
---
# <a name="ctext-control"></a>Controle CTEXT

Define um controle de texto centralizado. O controle é um retângulo simples que exibe o texto fornecido centralizado no retângulo. O texto é formatado antes de ser exibido. As palavras que ultrapassaram o final de uma linha são automaticamente encapsuladas no início da próxima linha. Palavras que são maiores que a largura do controle são truncadas.

A instrução [**LTEXT**](ltext-control.md) , que pode ser usada somente em uma instrução Rep, define o texto, o identificador, as dimensões e os atributos do controle.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

Texto que deve ser centralizado na área retangular do controle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser qualquer combinação dos seguintes estilos: **SS \_ Center**, **WS \_ TabStop** e **WS \_ Group**.

Se você não especificar um estilo, o estilo padrão será `SS_CENTER | WS_GROUP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de texto centralizado que é rotulado como nome de arquivo:

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CONTROLO**](control-control.md)
</dt> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 