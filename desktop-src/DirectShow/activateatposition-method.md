---
description: O método ActivateAtPosition ativa o botão de menu na posição especificada.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Método ActivateAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087875"
---
# <a name="activateatposition-method"></a>Método ActivateAtPosition

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método ActivateAtPosition ativa o botão de menu na posição especificada.

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Especifica a coordenada x como um inteiro.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Especifica a coordenada y como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

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

 

 



