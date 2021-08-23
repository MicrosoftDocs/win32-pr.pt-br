---
title: Controle ICON
description: Define um controle de ícone. Esse controle é um ícone exibido em uma caixa de diálogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menus de controle ICON e outros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fc5191457996aabe4a70fefcf64235b3a9573cf12733f9ca7bff2ece6356e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034284"
---
# <a name="icon-control"></a>Controle ICON

Define um controle de ícone. Esse controle é um ícone exibido em uma caixa de diálogo.

A instrução de controle **ICON,** que só pode ser usada em uma instrução [**DIALOGEX,**](dialogex-resource.md) define o identificador de ícone-recurso, o identificador de controle de ícone, a posição e os atributos de um controle.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Nome de um ícone (não um nome de arquivo) definido em outro lugar no arquivo de recurso.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Largura*
</dt> <dd>

Esse valor é ignorado e deve ser definido como zero.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Altura*
</dt> <dd>

Esse valor é ignorado e deve ser definido como zero.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilo de controle. Esse parâmetro é opcional. O único valor que pode ser especificado é o estilo **SS \_ ICON.** Esse é o estilo padrão, independentemente de esse parâmetro ser especificado ou não.

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de ícone cujo identificador de ícone é 901 e cujo nome é myicon:

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ícone**](icon-resource.md)
</dt> </dl>

 

 




