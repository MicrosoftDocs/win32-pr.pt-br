---
title: Função InitializeNapAgentNotifier (NapUtil. h)
description: Assina o processo de chamada para notificações de alteração de estado NapAgent e notificações de alteração de estado de quarentena.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- Função InitializeNapAgentNotifier NAP
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
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918232"
---
# <a name="initializenapagentnotifier-function"></a>Função InitializeNapAgentNotifier

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **InitializeNapAgentNotifier** assina o processo de chamada para as notificações de alteração de estado NapAgent e as notificações de alteração de estado de quarentena. Essas notificações são fornecidas pelo serviço NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ de no\]
</dt> <dd>

Um valor de [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica o tipo de notificações de serviço a receber.

</dd> <dt>

*hNotifyEvent* \[ no\]
</dt> <dd>

Um identificador de evento usado para notificação. O chamador deve passar um identificador aberto para o parâmetro *hNotifyEvent* . O chamador também deve fechar o identificador de eventos quando ele não for mais necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor



| Código de retorno                                                                                                | Descrição                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Inicialização concluída com êxito.<br/>                                                         |
| <dl> <dt>**E \_ falha**</dt> </dl>                     | Falha de inicialização.<br/>                                                                         |
| <dl> <dt>**ERRO \_ já \_ inicializado**</dt> </dl> | O processo já assinou as notificações do serviço NapAgent do *tipo* especificado. <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Um argumento inválido foi passado. <br/>                                                               |



 

## <a name="remarks"></a>Comentários

Essa função não é thread-safe.

Cada processo que requer uma assinatura para notificações de serviço NapAgent do *tipo* especificado deve chamar **InitializeNapAgentNotifier** para assinar notificações. Se um processo precisar assinar mais de um tipo de notificação, ele deverá chamar **InitializeNapAgentNotifier** uma vez para cada tipo de notificação.

Quando um processo não requer notificações adicionais, o processo deve chamar [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) para o *tipo* especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





