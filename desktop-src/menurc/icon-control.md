---
title: Controle de ícone
description: Define um controle de ícone. Esse controle é um ícone exibido em uma caixa de diálogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menus de controle de ícone e outros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453765"
---
# <a name="icon-control"></a>Controle de ícone

Define um controle de ícone. Esse controle é um ícone exibido em uma caixa de diálogo.

A instrução de controle **Icon** , que pode ser usada apenas em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o identificador de recurso de ícone, o identificador de controle de ícone, a posição e os atributos de um controle.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

Nome de um ícone (não um nome de arquivo) definido em outro lugar no arquivo de recurso.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Largura*
</dt> <dd>

Esse valor é ignorado e deve ser definido como zero.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*tamanho*
</dt> <dd>

Esse valor é ignorado e deve ser definido como zero.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilo de controle. Esse parâmetro é opcional. O único valor que pode ser especificado é o estilo de **\_ ícone SS** . Esse é o estilo padrão se esse parâmetro é especificado ou não.

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de ícone cujo identificador de ícone é 901 e cujo nome é myicon:

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CONE**](icon-resource.md)
</dt> </dl>

 

 




