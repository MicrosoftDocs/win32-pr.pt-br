---
description: Cancela a assinatura de notificações de alteração de status do serviço.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Função UnsubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829143"
---
# <a name="unsubscribeservicechangenotifications-function"></a>Função UnsubscribeServiceChangeNotifications

Cancela a assinatura de notificações de alteração de status do serviço. Essa função usa assinaturas retornadas por [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).

## <a name="syntax"></a>Sintaxe


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSubscription* \[ no\]
</dt> <dd>

Um ponteiro para a assinatura a ser cancelada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

**UnsubscribeServiceChangeNotifications** não retorna até que os retornos de chamada em andamento pendentes sejam concluídos. Portanto, você não pode chamar **UnsubscribeServiceChangeNotifications** no retorno de chamada sem causar um deadlock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




