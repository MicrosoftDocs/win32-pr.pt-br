---
title: Método IMsTscAxEvents OnFatalError
description: Chamado quando o controle de cliente encontra um erro fatal.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnFatalError
- Método OnFatalError Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnFatalError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a10315eca4fcbf96edf123699614d29a2c0b8974f563c52148b5de75310fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000676"
---
# <a name="imstscaxeventsonfatalerror-method"></a>Método IMsTscAxEvents:: OnFatalError

Chamado quando o controle de cliente encontra um erro fatal.

## <a name="syntax"></a>Sintaxe


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ErrorCode* \[ no\]
</dt> <dd>

Indica o código de erro.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Ocorreu um erro desconhecido.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Código de erro interno 1.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Ocorreu um erro de memória insuficiente.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**Beta**


</dt> <dd>

Ocorreu um erro de criação de janela.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Código de erro interno 2.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**05**


</dt> <dd>

Código de erro interno 3. Este não é um estado válido.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**152**


</dt> <dd>

Código de erro interno 4.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7**


</dt> <dd>

Ocorreu um erro irrecuperável durante a conexão do cliente.

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Erro de inicialização do Winsock.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Em resposta a esse evento, o contêiner exibe uma mensagem de erro e é desligado.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





