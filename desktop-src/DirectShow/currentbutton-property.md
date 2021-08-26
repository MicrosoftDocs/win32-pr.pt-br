---
description: A propriedade CurrentButton recupera o número do botão de menu selecionado.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Propriedade CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b246b77283a2632f2feac4c2b374075ef9d9a205bcb71813856b9847df21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053136"
---
# <a name="currentbutton-property"></a>Propriedade CurrentButton

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentButton` propriedade recupera o número do botão de menu selecionado.

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o botão.

## <a name="remarks"></a>Comentários

Essa propriedade é somente leitura sem valor padrão. Use esse método ao implementar a manipulação personalizada do mouse depois de [**definir DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true.**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**BotõesAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



