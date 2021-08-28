---
title: AmbientAttributes.accKeyboardShortcut
description: O atributo accKeyboardShortcut especifica ou recupera uma descrição de atalho de teclado para qualquer elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes.accKeyboardShortcut Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467304bb9f38ab0683440d2a0ebc5fcc51adb92fbb1d50e8275eb36f256a159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055204"
---
# <a name="ambientattributesacckeyboardshortcut"></a>AmbientAttributes.accKeyboardShortcut

O **atributo accKeyboardShortcut** especifica ou recupera uma descrição de atalho de teclado para qualquer elemento.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de **caracteres** de leitura/gravação com um valor padrão de "" (cadeia de caracteres vazia). Para o **elemento BUTTON,** esse atributo tem um valor padrão de "Barra de Espaços ou Enter". Para o **elemento SLIDER,** o valor padrão é "Seta para a direita/para cima para aumentar, Seta para a esquerda/para baixo para diminuir".

## <a name="remarks"></a>Comentários

Esse atributo é usado para fins de acessibilidade. Ele permite que uma descrição do atalho de teclado para qualquer elemento seja lida em voz alta por um programa de leitor. Esse atributo não configura o atalho. O scripter deve fazer esse trabalho.

Esse atributo também se aplica a elementos de botão dentro do controle de grupo de botões.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





