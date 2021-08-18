---
description: O método SelectAndActivateButton seleciona e ativa o botão especificado.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Método SelectAndActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d141616356db5daf2ebcb19579b924f6d4cab956e03d876d0254666d55b5702b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951905"
---
# <a name="selectandactivatebutton-method"></a>Método SelectAndActivateButton

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SelectAndActivateButton` método seleciona e ativa o botão especificado.

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*Ibutton*
</dt> <dd>

Especifica o botão como um Inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Use esse método ao implementar a manipulação personalizada do mouse depois de [**definir DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true.**

Esse método realça o botão especificado e o ativa automaticamente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**BotõesAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



