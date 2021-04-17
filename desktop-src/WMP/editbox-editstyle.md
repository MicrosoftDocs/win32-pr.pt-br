---
title: Admy. editstyle
description: O atributo editstyle especifica ou recupera o estilo do controle caixa de edição.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- Admy. editstyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758220"
---
# <a name="editboxeditstyle"></a>Admy. editstyle

O atributo **editstyle** especifica ou recupera o estilo do controle caixa de edição.

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um dos valores a seguir.



| Valor     | Descrição                                                                     |
|-----------|---------------------------------------------------------------------------------|
| normal    | Padrão. Exibe texto normal em uma única linha.                                 |
| password  | Exibe asteriscos ( \* ) no lugar do texto. Só pode ser especificado em tempo de design. |
| letras maiúsculas | Exibe o texto como todas as letras maiúsculas.                                                 |
| letras minúsculas | Exibe o texto como todas as letras minúsculas.                                                 |
| número    | Exibe apenas números.                                                          |
| tiverem | Exibe várias linhas de texto. Só pode ser especificado em tempo de design.          |



 

## <a name="remarks"></a>Comentários

Esse atributo só pode ser definido como "password" ou "Multiline" em tempo de design. Se estiver definido como "Multiline", o valor não poderá ser alterado em tempo de execução.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento admy**](editbox-element.md)
</dt> </dl>

 

 





