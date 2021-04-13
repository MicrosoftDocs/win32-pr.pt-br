---
description: A propriedade ButtonsAvailable recupera o número total de botões no menu atual.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Propriedade ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370266"
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

Esta propriedade é somente leitura sem valor padrão. Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.

Chame esse método para recuperar o limite superior do intervalo de números de botões válidos.

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

 

 



