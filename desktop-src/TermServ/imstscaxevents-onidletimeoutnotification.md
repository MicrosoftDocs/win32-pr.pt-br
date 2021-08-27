---
title: Método IMsTscAxEvents OnIdleTimeoutNotification
description: Chamado quando não há entrada de mouse ou de teclado pelo usuário durante o período definido pelo método IMsRdpClientAdvancedSettings Put \_ MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnIdleTimeoutNotification
- Método OnIdleTimeoutNotification Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnIdleTimeoutNotification
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356414d03a6b102f37f93205e0dbb8c3261cffbbb5b71a58cdb3f80acda09212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125116"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>Método IMsTscAxEvents:: OnIdleTimeoutNotification

Chamado quando não há entrada de mouse ou de teclado pelo usuário durante o período definido pelo método [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .

## <a name="syntax"></a>Sintaxe


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Por padrão, o valor da propriedade [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) é definido como zero e o sistema não monitora o tempo limite de ociosidade. Esse evento ocorrerá somente se a propriedade estiver definida como um valor diferente de zero.

O valor de [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) é redefinido automaticamente cada vez que o evento ocorre.

Os aplicativos podem usar o [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) em situações em que é útil desconectar um usuário; por exemplo, em um quiosque ou em outro cenário de terminal público.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





