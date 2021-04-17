---
title: Método IMsTscAxEvents OnAutoReconnecting2
description: Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). | Método IMsTscAxEvents OnAutoReconnecting2
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAutoReconnecting2
- Método OnAutoReconnecting2 Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105759937"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>Método IMsTscAxEvents:: OnAutoReconnecting2

Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Esta é uma versão aprimorada do método [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) .

## <a name="syntax"></a>Sintaxe


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*disconnectReason* \[ no\]
</dt> <dd>

Código que descreve o motivo para a última desconexão da sessão.

</dd> <dt>

*NetworkAvailable* \[ no\]
</dt> <dd>

Especifica se a rede está disponível.

</dd> <dt>

*attemptCount* \[ no\]
</dt> <dd>

Número de tentativas que foram feitas no processo de reconexão automática atual. Essa contagem aumenta em uma para cada tentativa feita.

</dd> <dt>

*maxAttemptCount* \[ no\]
</dt> <dd>

O número máximo de tentativas que serão feitas no processo de reconexão automática atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





