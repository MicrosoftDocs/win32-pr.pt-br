---
description: O método DVDTimeCode2bstr recupera uma cadeia de caracteres que indica a hora atual no disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Método DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759557"
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

Especifica a hora atual no disco em relação ao início do título como um número obtido por meio do evento [**de \_ \_ \_ \_ hora HMSF atual do DVD do EC**](ec-dvd-current-hmsf-time.md) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna uma cadeia de caracteres de 11 caracteres no formato "hh: mm: SS: FF" que representa as horas, os minutos, os segundos e os quadros que definem a hora atual.

## <a name="remarks"></a>Comentários

Este método é somente leitura.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Manipulando notificações de eventos de DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



