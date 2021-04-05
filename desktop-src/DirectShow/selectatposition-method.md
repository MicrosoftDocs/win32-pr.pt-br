---
description: O método SelectAtPosition seleciona o botão de menu nas coordenadas do ponteiro do mouse especificado.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Método SelectAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645837"
---
# <a name="selectatposition-method"></a>Método SelectAtPosition

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SelectAtPosition` método seleciona o botão de menu nas coordenadas do ponteiro do mouse especificado.

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
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

Selecionar meramente realça o botão. Para enviar o comando associado a um botão que foi selecionado, chame [**ActivateButton**](activatebutton-method.md).

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
</dt> </dl>

 

 



