---
description: Assina notificações de alteração de status de serviço usando uma função de retorno de chamada.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Função SubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: 83bd7bc3f937794f14cbe1d2877bc53ce7d347a8f45fd4f0ddb3e9d0ee9a52a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888452"
---
# <a name="subscribeservicechangenotifications-function"></a>Função SubscribeServiceChangeNotifications

Assina notificações de alteração de status de serviço usando uma função de retorno de chamada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hService* \[ no\]
</dt> <dd>

Um identificador para o serviço ou um identificador para o Gerenciador de controle de serviço (SCM) para monitorar as alterações.

Identificadores para serviços são retornados pela função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) e [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e devem ter o direito de acesso de **\_ \_ status de consulta de serviço** . Os identificadores para o Gerenciador de controle de serviço são retornados pela função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) e devem ter o direito de acesso do **serviço de \_ \_ enumeração \_ SC Manager** .

</dd> <dt>

*eEventType* \[ no\]
</dt> <dd>

Especifica o tipo de alterações de status que devem ser relatadas. Esse parâmetro é definido como um dos valores especificados no [**tipo de \_ evento \_ SC**](sc-event-type.md). O comportamento dessa função é diferente dependendo do tipo de evento da seguinte maneira.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**Sc \_ \_ \_ Alteração de banco de dados de eventos**</dt> <dt>0</dt> </dl> | Um serviço foi adicionado ou excluído. O parâmetro *hService* deve ser um identificador para o SCM.<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**Sc \_ \_ \_ Alteração de propriedade de evento**</dt> <dt>1</dt> </dl> | Uma ou mais propriedades de serviço foram atualizadas. O parâmetro *hService* deve ser um identificador para o serviço.<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**Sc \_ \_ \_ Alteração do status do evento**</dt> <dt>2</dt> </dl>       | O status de um serviço foi alterado. O parâmetro *hService* deve ser um identificador para o serviço.<br/>              |



 

</dd> <dt>

*pCallback* \[ no\]
</dt> <dd>

Especifica a função de retorno de chamada. O retorno de chamada deve ser definido como tendo um tipo de **\_ retorno de \_ chamada de notificação SC**. Para obter mais informações, consulte Comentários.

</dd> <dt>

*pCallbackContext* \[ em, opcional\]
</dt> <dd>

Um ponteiro que representa o contexto para este retorno de chamada de notificação.

</dd> <dt>

*pSubscription* \[ fora\]
</dt> <dd>

Retorna um ponteiro para a assinatura resultante do registro de retorno de chamada de notificação. O chamador é responsável por chamar [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) para parar de receber notificações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno **será \_ êxito no erro**.

Se a função falhar, o valor de retorno será um dos [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

## <a name="remarks"></a>Comentários

A função de retorno de chamada é declarada da seguinte maneira:


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



A função de retorno de chamada recebe um ponteiro para o contexto fornecido pelo chamador. O retorno de chamada é invocado como resultado do evento de alteração de status do serviço. Quando o retorno de chamada é invocado, ele é fornecido com uma bitmask de valores **\_ \_ * xxx*** de notificação de serviço que indicam o tipo de alteração de status do serviço. Quando o retorno de chamada é fornecido com zero em vez de um valor válido de **notificação de serviço \_ \_ * xxx***, o aplicativo deve verificar o que foi alterado.

A função de retorno de chamada não deve bloquear a execução. Se você espera que a execução da função de retorno de chamada seja demorada, descarregue o trabalho que você executa na função de retorno de chamada para um thread separado, enfileirando um item de trabalho para um thread em um pool de threads. Alguns tipos de trabalho que podem fazer a função de retorno de chamada levará tempo incluem a execução de e/s de arquivo, a espera de um evento e a realização de chamadas de procedimento remoto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

