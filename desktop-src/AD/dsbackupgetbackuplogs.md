---
title: Função DsBackupGetBackupLogs (Ntdsbcli. h)
description: Obtém a lista de arquivos de log cujo backup deve ser feito para o contexto de backup fornecido.
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
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918569"
---
# <a name="dsbackupgetbackuplogs-function"></a>Função DsBackupGetBackupLogs

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsBackupGetBackupLogs** Obtém a lista de arquivos de log que devem ser submetidos a backup para o contexto de backup fornecido.

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

*HBC* \[ no\]
</dt> <dd>

Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pszBackupLogFiles* \[ fora\]
</dt> <dd>

Ponteiro para um ponteiro de cadeia de caracteres que recebe a lista de nomes de arquivos de log como caminhos UNC. Inicialize esse valor como **NULL** antes de chamar **DsBackupGetBackupLogs**.

Essa lista recebe uma lista terminada por nulo de cadeias de caracteres com terminação nula.

Esse buffer é alocado pela função **DsBackupGetBackupLogs** e deve ser liberado quando não for mais necessário chamando a função [**DsBackupFree**](dsbackupfree.md) .

O primeiro caractere de cada um dos nomes de arquivo contém uma das [**constantes BFT**](bft-constants.md) que identifica o tipo de nome.

</dd> <dt>

*pcbSize* \[ fora\]
</dt> <dd>

Ponteiro para o valor **DWORD** que recebe o tamanho, em bytes, do buffer *pszBackupLogFiles* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC. A lista a seguir lista outros códigos de erro possíveis.

<dl> <dt>

**ERRO de \_ acesso \_ negado**
</dt> <dd>

O chamador não tem os privilégios de acesso apropriados para chamar essa função. A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**\_parâmetro inválido de erro \_**
</dt> <dd>

*HBC*, *pszBackupLogFiles* ou *pcbSize* é inválido.

</dd> <dt>

**ERRO \_ de \_ memória insuficiente \_**
</dt> <dd>

Ocorreu uma falha de alocação de memória.

</dd> </dl>

## <a name="remarks"></a>Comentários

A função **DsBackupGetBackupLogs** fornece uma lista dos arquivos de log necessários para um backup. Um backup completo consiste nos arquivos de banco de dados fornecidos pela função [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) e os arquivos de log. Não há suporte para backups incrementais de servidores Active Directory.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
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

[Fazendo backup de um servidor de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

