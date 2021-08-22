---
description: A propriedade ButtonsAvailable recupera o número total de botões no menu atual.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Propriedade ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16e14675238711ef0b572477334fecba0311ca2bb54d67fc3fe012ae6d1ede9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955555"
---
# <a name="buttonsavailable-property"></a>Propriedade ButtonsAvailable

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `ButtonsAvailable` propriedade recupera o número total de botões no menu atual.

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o número de botões.

## <a name="remarks"></a>Comentários

Essa propriedade é somente leitura sem valor padrão. Use esse método ao implementar a manipulação personalizada do mouse depois de [**definir DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true.**

Chame esse método para recuperar o limite superior para o intervalo de números de botão válidos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



