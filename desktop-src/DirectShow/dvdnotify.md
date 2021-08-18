---
description: O evento DVDNotify notifica uma aplicação de muitos eventos de DVD e instruções de disco diferentes.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988deaf53fb2b50555b4cf19a38684610aa0822a270dfba079defab92ce8aec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148699"
---
# <a name="dvdnotify"></a>DVDNotify

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDNotify` evento notifica uma aplicação de muitos eventos de DVD e instruções de disco diferentes.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Especifica o código de notificação de evento de DVD.

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*
</dt> <dd>

Pode conter informações adicionais relacionadas ao evento.

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

Pode conter informações adicionais relacionadas ao evento.

</dd> </dl>

## <a name="remarks"></a>Comentários

[Códigos de notificação de eventos de DVD](dvd-notification-codes.md) fornece uma explicação completa de todos os códigos de notificação de evento de DVD e seus parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment.h</dt> </dl> |



 

 




