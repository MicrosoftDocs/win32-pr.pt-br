---
title: Método IConnectionBrokerClient GetTargetInfo (Cbclient. h)
description: Solicita informações sobre o computador de destino onde a conexão deve ser redirecionada.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetTargetInfo
- Método GetTargetInfo Serviços de Área de Trabalho Remota, interface IConnectionBrokerClient
- Serviços de Área de Trabalho Remota de interface IConnectionBrokerClient, método GetTargetInfo
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
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499238"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>Método IConnectionBrokerClient:: GetTargetInfo

Solicita informações sobre o computador de destino onde a conexão deve ser redirecionada. Esse método é usado pelo redirecionador para obter informações de redirecionamento para a solicitação de conexão de entrada.

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

*pConnectionInfo* \[ no\]
</dt> <dd>

O endereço de uma estrutura de [**\_ \_ informações de conexão CB**](cb-connection-info.md) que contém informações sobre a solicitação de conexão de entrada.

</dd> <dt>

*Reservado* \[ para no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro e deve ser zero.

</dd> <dt>

*hStatusEvent* \[ no\]
</dt> <dd>

O identificador de um evento que será definido sempre que houver uma atualização do andamento da solicitação. Você é responsável por criar e fechar esse evento.

</dd> <dt>

*pTargetInfo* \[ fora\]
</dt> <dd>

O endereço de uma estrutura de [**\_ \_ informações de destino CB**](cb-target-info.md) que recebe informações sobre o computador de destino em que a conexão de entrada deve ser redirecionada. Como esse é um método assíncrono, essa memória deve permanecer disponível até que a solicitação seja concluída. Para obter mais informações, consulte Comentários.

</dd> <dt>

*pResult* \[ fora\]
</dt> <dd>

O endereço de uma variável **DWORD** que recebe um código de resultado. Como esse é um método assíncrono, essa memória deve permanecer disponível até que a solicitação seja concluída. Para obter mais informações, consulte Comentários.

Esse código de resultado será um dos valores a seguir.

<dt>

0
</dt> <dd>

Sucesso.

</dd> <dt>

0x0000400
</dt> <dd>

O computador de destino não foi encontrado.

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

Erro ao ativar a máquina virtual.

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

O agente de sessão não pôde localizar nenhum computador disponível no pool.

</dd> <dt>

0x0000409
</dt> <dd>

O agente de sessão cancelou a conexão.

</dd> <dt>

0x0000410
</dt> <dd>

O agente de sessão não pôde validar as configurações de conexão.

</dd> </dl> </dd> <dt>

*ppCbReq* \[ fora\]
</dt> <dd>

O endereço de um ponteiro de interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) que você usa para obter atualizações de status para uma operação assíncrona. Essa interface é usada em conjunto com o parâmetro *hStatusEvent* para aguardar e obter os resultados dessa operação assíncrona.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **E \_ pendente** se a solicitação assíncrona for criada. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é assíncrono. Os parâmetros *pTargetInfo* e *pResult* devem permanecer válidos até que o método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) obtenha a **solicitação de status CB \_ \_ \_ concluída**.

Para obter mais informações sobre como usar esse método, consulte [como usar a API de cliente do agente de conexão de área de trabalho remota](use-the-remote-desktop-connection-broker-client-api.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerClient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





