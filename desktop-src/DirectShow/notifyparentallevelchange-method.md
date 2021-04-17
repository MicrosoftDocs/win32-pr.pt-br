---
description: O método NotifyParentalLevelChange habilita ou desabilita a manipulação de eventos para comandos temporários de nível de gerenciamento pai.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Método NotifyParentalLevelChange (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759433"
---
# <a name="notifyparentallevelchange-method"></a>Método NotifyParentalLevelChange

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `NotifyParentalLevelChange` método habilita ou desabilita a manipulação de eventos para comandos temporários de nível de gerenciamento pai.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*
</dt> <dd>

Especifica um valor booliano que indica se o aplicativo será notificado quando o objeto MSWebDVD encontrar segmentos de vídeo com uma classificação mais restritiva do que a classificação geral do disco.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

As notificações de gerenciamento de pais são desabilitadas por padrão. Isso significa que os comandos temporários dos pais do disco são permitidos, mas ignorados e o disco será reproduzido sem interrupção. Chame esse método durante a inicialização do seu aplicativo se você precisar manipular comandos temporários no nível de gerenciamento pai do disco. Para desabilitar o gerenciamento de pais depois que ele estiver habilitado, chame esse método com um argumento de false. Para obter mais detalhes sobre o gerenciamento de pais, consulte [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 




