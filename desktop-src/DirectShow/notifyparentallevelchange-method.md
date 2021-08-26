---
description: O método NotifyParentalLevelChange habilita ou desabilita a manipulação de eventos para comandos temporários de nível de gerenciamento dos pais.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Método NotifyParentalLevelChange (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8382b52f64d4196b0ef74e5f3285e9bb047a4e1f77d3b0e5bec4da218ee753b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997356"
---
# <a name="notifyparentallevelchange-method"></a>Método NotifyParentalLevelChange

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `NotifyParentalLevelChange` método habilita ou desabilita a manipulação de eventos para comandos temporários de nível de gerenciamento dos pais.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*
</dt> <dd>

Especifica um valor booliana que indica se o aplicativo é notificado ou não quando o objeto MSWebDVD encontra segmentos de vídeo com uma classificação mais restritiva do que a classificação geral do disco.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

As notificações de gerenciamento dos pais são desabilitadas por padrão. Isso significa que os comandos temporários dos pais do disco são permitidos, mas ignorados e o disco será reproduzir sem interrupção. Chame esse método durante a inicialização do aplicativo se você precisar lidar com comandos temporários de nível de gerenciamento dos pais do disco. Para desabilitar o gerenciamento de pais depois que ele for habilitado, chame esse método com um argumento false. Para obter mais detalhes sobre o gerenciamento dos pais, [**consulte AcceptParentalLevelChange**](acceptparentallevelchange-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment.h</dt> </dl> |



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

 

 




