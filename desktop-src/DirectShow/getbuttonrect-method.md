---
description: O método GetButtonRect recupera o retângulo para o botão especificado, em coordenadas de janela.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Método GetButtonRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087277"
---
# <a name="getbuttonrect-method"></a>Método GetButtonRect

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetButtonRect` método recupera o retângulo para o botão especificado, em coordenadas de janela.

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*
</dt> <dd>

Especifica o número do botão como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um objeto [DVDRect](dvdrect-object.md) que define o retângulo.

## <a name="remarks"></a>Comentários

Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



