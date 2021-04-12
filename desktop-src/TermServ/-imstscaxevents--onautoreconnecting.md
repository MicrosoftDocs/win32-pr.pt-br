---
title: Método IMsTscAxEvents OnAutoReconnecting
description: Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). | Método IMsTscAxEvents OnAutoReconnecting
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAutoReconnecting
- Método OnAutoReconnecting Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnAutoReconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298346"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a>Método IMsTscAxEvents:: OnAutoReconnecting

Chamado quando um cliente está no processo de reconexão automática de uma sessão com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

## <a name="syntax"></a>Sintaxe


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*disconnectReason* \[ no\]
</dt> <dd>

Código que descreve o motivo para a última desconexão da sessão.

</dd> <dt>

*attemptCount* \[ no\]
</dt> <dd>

Número de tentativas que foram feitas no processo de reconexão automática atual. Essa contagem aumenta em uma para cada tentativa feita.

</dd> <dt>

*pArcContinueStatus* \[ fora\]
</dt> <dd>

Ponteiro para um código retornado que especifica o estado do processo de reconexão automática. Esse código pode ser redefinido para alterar o estado do processo de reconexão automática atual.

Para obter mais informações sobre como redefinir esse código, consulte a seção comentários.

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic * * * * (0)


</dt> <dd>

O processo de reconexão está ocorrendo automaticamente. Esse é o valor padrão.

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop * * * * (1)


</dt> <dd>

O processo de reconexão foi interrompido.

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual * * * * (2)


</dt> <dd>

O processo de reconexão está ocorrendo manualmente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Implemente esse método em seu coletor de eventos para receber uma notificação de que o controle está reestabelecendo uma conexão com um servidor de Host da Sessão RD.

Quando o estado do processo de reconexão automática é alterado definindo o valor do parâmetro *pArcContinueStatus* como **autoReconnectContinueAutomatic**, esse método funciona em um modo puramente Consultivo. Os contêineres podem escutar esse evento em busca de notificações de que o processo de reconexão automática está prosseguindo. O controle continuará a tentar restabelecer automaticamente uma conexão com base em seu próprio tempo interno e contagens de tentativas. Esse método é chamado durante cada tentativa de reconexão automática a fim de notificar o contêiner.

Quando o estado do processo de reconexão automática for alterado definindo o valor do parâmetro *pArcContinueStatus* como **autoReconnectContinueStop**, a tentativa de reconexão automática atual será encerrada, uma notificação de desconexão será enviada ao contêiner e nenhuma outra notificação de reconexão automática será emitida.

> [!Note]  
> Use a propriedade [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) para habilitar ou desabilitar a reconexão automática.

 

Quando o estado do processo de reconexão automática for alterado definindo o valor do parâmetro *pArcContinueStatus* como **autoReconnectContinueManual**, o contêiner controlará manualmente o processo de reconexão automática chamando [**Connect**](imstscax-connect.md) para disparar uma tentativa de conexão ou [**Desconectar**](imstscax-disconnect.md) para cancelar o processo de reconexão automática. Uma vez definido com esse valor, o controle irá parar de fazer tentativas de reconexão automática e se tornará a política do contêiner para fazer chamadas **Connect** para disparar tentativas de reconexão automática. Isso é feito quando o contêiner fornece o comportamento da interface do usuário personalizada para reconexão automática, como reiniciar uma conexão RAS ou VPN descartada antes do processo de reconexão automática.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





