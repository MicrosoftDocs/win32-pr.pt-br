---
title: Função DsBackupPrepare (Ntdsbcli.h)
description: Prepara o diretório no servidor especificado para o backup online e retorna um alça de contexto de backup usado em chamadas subsequentes para outras funções de backup.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Função DsBackupPrepare Active Directory
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea1f24c6cbf3f05ce69d8a71900bfe4d1b08899b98590dc75410b9d5ed92d90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191832"
---
# <a name="dsbackupprepare-function"></a>Função DsBackupPrepare

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Começando com Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A **função DsBackupPrepare** prepara o diretório no servidor especificado para o backup online e retorna um alça de contexto de backup usado em chamadas subsequentes para outras funções de backup.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szBackupServer* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor para backup. As malhas inativas anteriores são opcionais. O servidor deve ser o mesmo computador do onde essa função é chamada. O nome do servidor não pode conter um caractere de sublinhado ( \_ ). Um exemplo de um nome de servidor é " \\ \\ server1".

</dd> <dt>

*grbit* \[ Em\]
</dt> <dd>

Determina se os arquivos de log serão armazenados em backup. Esse valor sempre deve ser 0 porque não há suporte para backups incrementais.

</dd> <dt>

*btBackupType* \[ Em\]
</dt> <dd>

Especifica o tipo de backup. Esse pode ser um dos valores a seguir.

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**TIPO \_ DE BACKUP \_ COMPLETO**


</dt> <dd>

Especifica um backup completo. O diretório completo (DIT, arquivos de log e arquivos de atualização) é feito backup. Todos os dados são armazenados em backup e os arquivos de log de transações são truncados. Há suporte apenas para backups completos.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**SOMENTE LOGS \_ DE \_ TIPO DE \_ BACKUP**


</dt> <dd>

Não há suporte para esse valor. Especifica que somente os logs do banco de dados, e não o próprio banco de dados, terão o backup feito. Normalmente, isso é usado ao executar um backup diferencial ou incremental.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**TIPO DE BACKUP \_ \_ INCREMENTAL**


</dt> <dd>

Não há suporte para esse valor. **DsBackupPrepare retorna** **ERROR INVALID \_ \_ PARAMETER**.

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[ out\]
</dt> <dd>

Ponteiro para um **valor PVOID** que recebe um ponteiro para um token de expiração associado a esse backup. *pcbExpiryTokenSize* recebe o tamanho, em bytes, desses dados. O chamador deve salvar o conteúdo desse token com o backup porque o token deve ser passado para [**DsRestorePrepare**](dsrestoreprepare.md) ao tentar restaurar dados. Depois que o token tiver sido armazenado e não for mais necessário, o chamador deverá liberar a memória alocada usando [**DsBackupFree.**](dsbackupfree.md)

</dd> <dt>

*pcbExpiryTokenSize* \[ out\]
</dt> <dd>

Ponteiro para um **valor DWORD** que recebe o tamanho, em bytes, do token em *ppvExpiryToken.*

</dd> <dt>

*phbc* \[ out\]
</dt> <dd>

Ponteiro para um **valor HBC** que recebe o alça para o backup. Esse handle é usado ao chamar outras funções de backup do Serviço de Diretório, como [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsBackupEnd.**](dsbackupend.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro, caso contrário. A lista a seguir lista outros códigos de erro possíveis.

<dl> <dt>

**ACESSO \_ DE ERRO \_ NEGADO**
</dt> <dd>

O chamador não tem os privilégios de acesso adequados para chamar essa função. A [**função DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**ERRO \_ PARÂMETRO \_ INVÁLIDO**
</dt> <dd>

*szBackupServer* ou *phbcBackupContext não* são válidos.

</dd> <dt>

**ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**
</dt> <dd>

Ocorreu uma falha de alocação de memória.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

Não foi possível encontrar o servidor *em szBackupServer,* não é um controlador de domínio ou *szBackupServer* não está formatado corretamente. Esse valor é definido em ntdsbmsg.h.

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* e/ou *pcbExpiryTokenSize* são inválidos. Esse valor é definido em Ntdsbmsg.h.

</dd> <dt>

**ASSOCIAÇÃO INVÁLIDA DO RPC \_ S \_ \_**
</dt> <dd>

A função é chamada remotamente ou o servidor *em szServerName não* é um controlador de domínio.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa função requer que o chamador tenha o privilégio **ES \_ BACKUP \_ NAME.** A [**função DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para alterar o contexto de segurança no qual essa função é chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsBackupPrepareW** (Unicode) e **DsBackupPrepareA** (ANSI)<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupEnd**](dsbackupend.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Fazer o back-up de um servidor do Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

