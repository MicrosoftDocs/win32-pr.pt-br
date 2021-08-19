---
title: Função DsBackupEnd (Ntdsbcli.h)
description: Chamado para encerrar uma operação de backup.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Função DsBackupEnd Active Directory
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479a1641a6d347837733da7e7d26e67b2011654e638681ec774a6ec5d931e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430246"
---
# <a name="dsbackupend-function"></a>Função DsBackupEnd

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Começando com Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A **função DsBackupEnd** é chamada para encerrar uma operação de backup.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hbc* \[ Em\]
</dt> <dd>

Contém o alça de contexto de backup obtido com a [**função DsBackupPrepare.**](dsbackupprepare.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro Win32 ou RPC caso contrário. A lista a seguir lista outros códigos de erro possíveis.

<dl> <dt>

**ERRO \_ PARÂMETRO \_ INVÁLIDO**
</dt> <dd>

*hbc* não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **função DsBackupEnd** fecha os alças de associação pendentes e executa uma limpeza após uma tentativa de backup bem-sucedida ou malsucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Fazer o back-up de um servidor do Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

