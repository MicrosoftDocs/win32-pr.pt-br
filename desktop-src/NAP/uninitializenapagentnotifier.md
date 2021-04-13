---
title: Função UninitializeNapAgentNotifier (NapUtil. h)
description: Cancela a assinatura do processo de chamada de notificações de alteração de estado NapAgent e notificações de alteração de estado de quarentena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- Função UninitializeNapAgentNotifier NAP
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
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369478"
---
# <a name="uninitializenapagentnotifier-function"></a>Função UninitializeNapAgentNotifier

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **UninitializeNapAgentNotifier** cancela a assinatura do processo de chamada das notificações de alteração de estado NapAgent e das notificações de alteração de estado de quarentena. Essas notificações são fornecidas pelo serviço NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ de no\]
</dt> <dd>

Um valor de [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica o tipo de notificações de serviço da qual cancelar a assinatura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta função não tem valores de retorno.

## <a name="remarks"></a>Comentários

Essa função não é thread-safe.

Cada processo assinado para notificações de serviço NapAgent do *tipo* especificado deve chamar **UninitializeNapAgentNotifier** para cancelar a assinatura de notificações. Se um processo for assinado para mais de um tipo de notificação, ele deverá chamar **UninitializeNapAgentNotifier** uma vez para cada tipo de notificação.

Essa função falhará silenciosamente se o processo não tiver chamado anteriormente [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) para o tipo de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





