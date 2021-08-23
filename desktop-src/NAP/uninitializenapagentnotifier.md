---
title: Função UninitializeNapAgentNotifier (NapUtil.h)
description: Cancela a assinatura do processo de chamada de notificações de alteração de estado napAgent e notificações de alteração de estado de quarentena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- Nap da função UninitializeNapAgentNotifier
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b474ea95dcb2e3bd5c756cefa825463f3384e798492ccdcf794641a16fbfc450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065256"
---
# <a name="uninitializenapagentnotifier-function"></a>Função UninitializeNapAgentNotifier

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **função UninitializeNapAgentNotifier** cancela a assinatura do processo de chamada de notificações de alteração de estado napAgent e notificações de alteração de estado de quarentena. Essas notificações são fornecidas pelo serviço NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ Em\]
</dt> <dd>

Um [**valor NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica o tipo de notificações de serviço do qual cancelar a assinatura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função não tem valores de retorno.

## <a name="remarks"></a>Comentários

Essa função não é thread-safe.

Cada processo inscrito nas notificações de serviço NapAgent do tipo especificado deve chamar **UninitializeNapAgentNotifier** para cancelar a assinatura de notificações.  Se um processo for inscrito em mais de um tipo de notificação, ele deverá chamar **UninitializeNapAgentNotifier** uma vez para cada tipo de notificação.

Essa função falhará silenciosamente se o processo não tivesse chamado [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) anteriormente para o tipo de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





