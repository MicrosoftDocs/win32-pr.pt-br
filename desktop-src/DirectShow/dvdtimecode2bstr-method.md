---
description: O método DVDTimeCode2bstr recupera uma cadeia de caracteres que indica a hora atual no disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Método DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90bda68bafa462af5d425c62368b51f8b4b08ce2dfc310276e8f26b7c4601fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148599"
---
# <a name="dvdtimecode2bstr-method"></a>Método DVDTimeCode2bstr

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDTimeCode2bstr` método recupera uma cadeia de caracteres que indica a hora atual no disco.

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*
</dt> <dd>

Especifica a hora atual no disco em relação ao início do título como um Número obtido por meio do evento [**EC \_ DVD CURRENT \_ \_ HMSF \_ TIME.**](ec-dvd-current-hmsf-time.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna uma Cadeia de caracteres de 11 caracteres no formato "hh:mm:ss:ff" que representa as horas, minutos, segundos e quadros que definem a hora atual.

## <a name="remarks"></a>Comentários

Esse método é somente leitura.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Manipulando notificações de eventos de DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



