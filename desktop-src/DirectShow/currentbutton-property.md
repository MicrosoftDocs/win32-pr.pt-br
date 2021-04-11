---
description: A propriedade CurrentButton recupera o número do botão de menu selecionado.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Propriedade CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296021"
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

Esta propriedade é somente leitura sem valor padrão. Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



