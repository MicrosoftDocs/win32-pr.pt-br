---
title: Exibir. resizeBackgroundImage
description: O atributo resizeBackgroundImage especifica ou recupera um valor que indica se a imagem de plano de fundo pode ser redimensionada.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- Exibir. resizeBackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815518"
---
# <a name="viewresizebackgroundimage"></a>Exibir. resizeBackgroundImage

O atributo **resizeBackgroundImage** especifica ou recupera um valor que indica se a imagem de plano de fundo pode ser redimensionada.

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valores | Descrição                                      |
|--------|--------------------------------------------------|
| true   | A imagem de plano de fundo pode ser redimensionada.             |
| false  | Padrão. A imagem de plano de fundo não pode ser redimensionada. |



 

## <a name="remarks"></a>Comentários

Se você definir esse atributo como true, a imagem de plano de fundo será redimensionada para se ajustar aos valores atuais dos atributos **Width** e **Height** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**Exibir. backgroundImage**](view-backgroundimage.md)
</dt> </dl>

 

 





