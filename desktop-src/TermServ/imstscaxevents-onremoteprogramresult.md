---
title: Método IMsTscAxEvents OnRemoteProgramResult
description: Chamado quando um programa RemoteApp retorna um resultado para o controle de cliente.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- Método OnRemoteProgramResult Serviços de Área de Trabalho Remota
- O método OnRemoteProgramResult Serviços de Área de Trabalho Remota , interface IMsTscAxEvents
- Interface IMsTscAxEvents Serviços de Área de Trabalho Remota método , OnRemoteProgramResult
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807fbd49cc6222925f34a7e7c007fef54cbc9a3db2566f024ebc0188e9c95113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129658"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a>Método IMsTscAxEvents::OnRemoteProgramResult

Chamado quando um programa RemoteApp retorna um resultado para o controle de cliente.

## <a name="syntax"></a>Sintaxe


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrRemoteProgram* \[ Em\]
</dt> <dd>

O nome do programa RemoteApp.

</dd> <dt>

*lError* \[ Em\]
</dt> <dd>

O resultado da tentativa de iniciar o programa RemoteApp.

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))


</dt> <dd>

O programa RemoteApp foi lançado com êxito.

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))


</dt> <dd>

A sessão remota está bloqueada e o programa RemoteApp não pode ser lançado. O usuário deve inserir suas credenciais para desbloquear a sessão e, em seguida, iniciar o programa RemoteApp.

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))


</dt> <dd>

O programa RemoteApp retornou um erro de protocolo.

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))


</dt> <dd>

O programa RemoteApp não está na lista aprovada do Host da Sessão RD servidor.

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))


</dt> <dd>

O caminho de rede para o programa RemoteApp foi negado.

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))


</dt> <dd>

O arquivo do programa RemoteApp não foi encontrado.

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))


</dt> <dd>

Falha ao iniciar o programa RemoteApp.

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))


</dt> <dd>

O programa RemoteApp não pode ser lançado porque a sessão está exibindo a área de trabalho segura no momento.

</dd> </dl> </dd> <dt>

*vbIsExecutable* \[ Em\]
</dt> <dd>

Indica se o programa RemoteApp foi lançado diretamente, usando o nome executável ou indiretamente, usando uma associação de arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Implemente esse método no seu sink de eventos para receber uma notificação de que um programa RemoteApp retornou um resultado.

Esse método é chamado imediatamente depois que o controle ActiveX tenta iniciar o programa RemoteApp e o parâmetro *lError* indica o resultado da tentativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





