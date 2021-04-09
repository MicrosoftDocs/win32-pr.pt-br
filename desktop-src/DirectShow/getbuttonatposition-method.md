---
description: O método GetButtonAtPosition recupera o número do botão nas coordenadas especificadas sem selecioná-lo ou ativá-lo.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Método GetButtonAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087278"
---
# <a name="getbuttonatposition-method"></a>Método GetButtonAtPosition

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetButtonAtPosition` método recupera o número do botão nas coordenadas especificadas sem selecioná-lo ou ativá-lo.

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Especifica a coordenada x do ponteiro do mouse como um inteiro.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Especifica a coordenada y do ponteiro do mouse como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro especificando o botão, se houver, na posição especificada.

## <a name="remarks"></a>Comentários

Esse método retornará zero se nenhum botão estiver presente nas coordenadas fornecidas. Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



