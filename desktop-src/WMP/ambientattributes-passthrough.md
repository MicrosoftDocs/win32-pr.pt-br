---
title: Ambiente de passagem. passThrough
description: O atributo passThrough especifica ou recupera um valor que indica se o controle passará todos os eventos do mouse para o controle sob ele.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Windows Media Player de ambiente. passThrough
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763381"
---
# <a name="ambientattributespassthrough"></a>Ambiente de passagem. passThrough

O atributo **passThrough** especifica ou recupera um valor que indica se o controle passará todos os eventos do mouse para o controle sob ele.

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                            |
|-------|--------------------------------------------------------|
| true  | O controle passa eventos para o controle sob ele. |
| false | Padrão. O controle não passa eventos pelo.         |



 

## <a name="remarks"></a>Comentários

Esse atributo será útil se, por exemplo, um controle de texto estiver sobre um controle de botão apenas para fornecer rotulagem. Nesse caso, os cliques no controle de texto devem ser passados para o controle de botão.

Não há suporte para o atributo **passThrough** nos elementos **VIEW**, **subview** e **playlist** . Ele não funcionará com o elemento **Video** se for um *vídeo*. **sem janela** é definido como false, nem com o elemento **Effects** , se houver *efeitos*. em **janela** é definido como true.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





