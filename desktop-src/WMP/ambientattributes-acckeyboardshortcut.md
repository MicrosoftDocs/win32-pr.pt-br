---
title: Ambienteattributes. accKeyboardShortcut
description: O atributo accKeyboardShortcut especifica ou recupera uma descrição de atalho de teclado para qualquer elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AccKeyboardShortcut do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763384"
---
# <a name="ambientattributesacckeyboardshortcut"></a>Ambienteattributes. accKeyboardShortcut

O atributo **accKeyboardShortcut** especifica ou recupera uma descrição de atalho de teclado para qualquer elemento.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação com um valor padrão de "" (cadeia de caracteres vazia). Para o elemento **Button** , esse atributo tem um valor padrão de "SPACEBAR ou Enter". Para o elemento **Slider** , o valor padrão é "seta para a direita/para cima para aumentar, seta para a esquerda/para baixo para diminuir".

## <a name="remarks"></a>Comentários

Esse atributo é usado para fins de acessibilidade. Ele permite uma descrição do atalho de teclado para qualquer elemento a ser lido em voz alta por um programa leitor. Esse atributo não define o atalho. O Scripter deve fazer esse trabalho.

Esse atributo também se aplica a elementos de botão dentro do controle de grupo de botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





