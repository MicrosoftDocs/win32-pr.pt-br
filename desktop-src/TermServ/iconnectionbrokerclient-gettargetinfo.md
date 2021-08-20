---
title: Método GetTargetInfo IConnectionBrokerClient (Cbclient.h)
description: Solicita informações sobre o computador de destino em que a conexão deve ser redirecionada.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Método GetTargetInfo Serviços de Área de Trabalho Remota
- Método GetTargetInfo Serviços de Área de Trabalho Remota interface , IConnectionBrokerClient
- Interface IConnectionBrokerClient Serviços de Área de Trabalho Remota , método GetTargetInfo
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df214f23c09b7439843f0d7e8947d40cc32b2bf30eece887c921aac34306fbdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059184"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>Método IConnectionBrokerClient::GetTargetInfo

Solicita informações sobre o computador de destino em que a conexão deve ser redirecionada. Esse método é usado pelo redirecionador para obter informações de redirecionamento para a solicitação de conexão de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pConnectionInfo* \[ Em\]
</dt> <dd>

O endereço de uma estrutura [**CB \_ CONNECTION \_ INFO**](cb-connection-info.md) que contém informações sobre a solicitação de conexão de entrada.

</dd> <dt>

*Reservado* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro e deve ser zero.

</dd> <dt>

*hStatusEvent* \[ Em\]
</dt> <dd>

O handle de um evento que será definido sempre que houver uma atualização para o progresso da solicitação. Você é responsável por criar e fechar esse evento.

</dd> <dt>

*pTargetInfo* \[ out\]
</dt> <dd>

O endereço de uma estrutura [**CB \_ TARGET \_ INFO**](cb-target-info.md) que recebe informações sobre o computador de destino no qual a conexão de entrada deve ser redirecionada. Como esse é um método assíncrono, essa memória deve permanecer disponível até que a solicitação seja concluída. Para obter mais informações, consulte Comentários.

</dd> <dt>

*pResult* \[ out\]
</dt> <dd>

O endereço de uma **variável DWORD** que recebe um código de resultado. Como esse é um método assíncrono, essa memória deve permanecer disponível até que a solicitação seja concluída. Para obter mais informações, consulte Comentários.

Esse código de resultado será um dos valores a seguir.

<dt>

0
</dt> <dd>

Sucesso.

</dd> <dt>

0x0000400
</dt> <dd>

Não foi possível encontrar o computador de destino.

</dd> <dt>

0x0000401
</dt> <dd>

O computador de destino não está disponível.

</dd> <dt>

0x0000402
</dt> <dd>

Erro ao carregar o computador de destino.

</dd> <dt>

0x0000403
</dt> <dd>

Erro ao colocar o computador de destino online.

</dd> <dt>

0x0000404
</dt> <dd>

Erro ao redirecionar para o computador de destino.

</dd> <dt>

0x0000405
</dt> <dd>

Erro ao adoção da máquina virtual.

</dd> <dt>

0x0000406
</dt> <dd>

Erro ao inicializar a máquina virtual.

</dd> <dt>

0x0000407
</dt> <dd>

Erro ao localizar o endereço IP da máquina virtual.

</dd> <dt>

0x0000408
</dt> <dd>

O agente de sessão não pôde encontrar nenhum computador disponível no pool.

</dd> <dt>

0x0000409
</dt> <dd>

O agente de sessão cancelou a conexão.

</dd> <dt>

0x0000410
</dt> <dd>

O agente de sessão não pôde validar as configurações de conexão.

</dd> </dl> </dd> <dt>

*ppCbReq* \[ out\]
</dt> <dd>

O endereço de um ponteiro de interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) que você usa para obter atualizações de status para uma operação assíncrona. Essa interface é usada em conjunto com o *parâmetro hStatusEvent* para aguardar e obter os resultados dessa operação assíncrona.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **\_ E PENDING** se a solicitação assíncrona for criada. Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método é assíncrono. Os *parâmetros pTargetInfo* e *pResult* devem permanecer válidos até que o método [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) obtenha **CB STATUS REQUEST \_ \_ \_ COMPLETED.**

Para obter mais informações sobre como usar esse método, consulte [How to use the Conexão de Área de Trabalho Remota Broker client API](use-the-remote-desktop-connection-broker-client-api.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerClient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





