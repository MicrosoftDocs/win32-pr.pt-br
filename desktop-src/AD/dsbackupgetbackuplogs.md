---
title: Função DsBackupGetBackupLogs (Ntdsbcli.h)
description: Obtém a lista de arquivos de log que devem ser armazenados em backup para o contexto de backup determinado.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Função DsBackupGetBackupLogs Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a240ef514fc62450a04f512f04d985380b79fa20daaee9ff4b27ccb71027a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430097"
---
# <a name="dsbackupgetbackuplogs-function"></a>Função DsBackupGetBackupLogs

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Começando com Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A **função DsBackupGetBackupLogs** obtém a lista de arquivos de log que devem ser armazenados em backup para o contexto de backup determinado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hbc* \[ Em\]
</dt> <dd>

Contém o alça de contexto de backup obtido com a [**função DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*pszBackupLogFiles* \[ out\]
</dt> <dd>

Ponteiro para um ponteiro de cadeia de caracteres que recebe a lista de nomes de arquivo de log como caminhos UNC. Inicialize esse valor como **NULL** antes de **chamar DsBackupGetBackupLogs.**

Essa lista recebe uma lista de terminação nula dupla de cadeias de caracteres terminadas em nulo único.

Esse buffer é alocado pela função **DsBackupGetBackupLogs** e deve ser liberado quando não for mais necessário chamando a [**função DsBackupFree.**](dsbackupfree.md)

O primeiro caractere de cada um dos nomes de arquivo contém uma das [**Constantes BFT**](bft-constants.md) que identifica o tipo de nome.

</dd> <dt>

*pcbSize* \[ out\]
</dt> <dd>

Ponteiro para **o valor DWORD** que recebe o tamanho, em bytes, do buffer *pszBackupLogFiles.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro Win32 ou RPC caso contrário. A lista a seguir lista outros códigos de erro possíveis.

<dl> <dt>

**ACESSO \_ DE ERRO \_ NEGADO**
</dt> <dd>

O chamador não tem os privilégios de acesso adequados para chamar essa função. A [**função DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**ERRO \_ PARÂMETRO \_ INVÁLIDO**
</dt> <dd>

*hbc*, *pszBackupLogFiles* ou *pcbSize* é inválido.

</dd> <dt>

**ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**
</dt> <dd>

Ocorreu uma falha de alocação de memória.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **função DsBackupGetBackupLogs** fornece uma lista dos arquivos de log necessários para um backup. Um backup completo consiste nos arquivos de banco de dados fornecidos pela [**função DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) e pelos arquivos de log. Não há suporte para backups incrementais de servidores do Active Directory.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsBackupGetBackupLogsW** (Unicode) e **DsBackupGetBackupLogsA** (ANSI)<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**Constantes BFT**](bft-constants.md)
</dt> <dt>

[Fazer o back-up de um servidor do Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

