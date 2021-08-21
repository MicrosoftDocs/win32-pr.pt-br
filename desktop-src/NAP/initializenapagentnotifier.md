---
title: Função InitializeNapAgentNotifier (NapUtil.h)
description: Assina o processo de chamada para notificações de alteração de estado napAgent e notificações de alteração de estado de quarentena.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- Nap da função InitializeNapAgentNotifier
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac2d874f6138bcc1fbc97952d4464e56e05b0a497c7b0ff98e9c05e8c8434e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133451"
---
# <a name="initializenapagentnotifier-function"></a>Função InitializeNapAgentNotifier

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **função InitializeNapAgentNotifier** assina o processo de chamada para notificações de alteração de estado napAgent e notificações de alteração de estado de quarentena. Essas notificações são fornecidas pelo serviço NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ Em\]
</dt> <dd>

Um [**valor NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica o tipo de notificações de serviço a ser recebido.

</dd> <dt>

*hNotifyEvent* \[ Em\]
</dt> <dd>

Um alça de evento usado para notificação. O chamador deve passar um alça aberta para o *parâmetro hNotifyEvent.* O chamador também deve fechar o alçamento de evento quando ele não for mais necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado



| Código de retorno                                                                                                | Descrição                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Inicialização concluída com êxito.<br/>                                                         |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Falha de inicialização.<br/>                                                                         |
| <dl> <dt>**ERRO \_ JÁ \_ INICIALIZADO**</dt> </dl> | O processo já assinou notificações de serviço NapAgent do *tipo* especificado. <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Um argumento inválido foi passado. <br/>                                                               |



 

## <a name="remarks"></a>Comentários

Essa função não é thread-safe.

Cada processo que requer uma assinatura para notificações de  serviço NapAgent do tipo especificado deve chamar **InitializeNapAgentNotifier** para assinar notificações. Se um processo deve assinar mais de um tipo de notificação, ele deve chamar **InitializeNapAgentNotifier** uma vez para cada tipo de notificação.

Depois que um processo não exigir mais notificações, o processo deverá chamar [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) para o tipo *especificado.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





