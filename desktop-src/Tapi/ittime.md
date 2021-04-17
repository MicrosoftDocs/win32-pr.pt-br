---
description: A interface ITTime é uma interface específica de provedor para um objeto de blob de conferência SDP (Session Descriptor Protocol).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Interface ITTime (Sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758407"
---
# <a name="ittime-interface"></a>Interface ITTime

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITTime** é uma interface específica de provedor para um objeto de blob de conferência SDP (Session Descriptor Protocol). Ele fornece acesso a um conjunto de tempos de ativação para a sessão. Os métodos [**IEnumTime:: Next**](ienumtime-next.md) e [**ITTimeCollection:: Create**](ittimecollection-create.md) criam a interface **ITTime** .

## <a name="members"></a>Membros

A interface **ITTime** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITTime** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITTime** tem esses métodos.



| Método                                         | Descrição                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [**obter \_ StartTime**](ittime-get-starttime.md) | Obtém o valor de hora de início do NTP de 32 bits (protocolo NTP).<br/> |
| [**obter \_ StopTime**](ittime-get-stoptime.md)   | Obtém o valor de hora de término do NTP.<br/>                                  |
| [**colocar \_ StartTime**](ittime-put-starttime.md) | Define o valor de hora de início de NTP de 32 bits.<br/>                         |
| [**colocar \_ StopTime**](ittime-put-stoptime.md)   | Define o valor de hora de término do NTP.<br/>                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

