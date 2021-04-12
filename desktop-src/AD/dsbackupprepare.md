---
title: Função DsBackupPrepare (Ntdsbcli. h)
description: Prepara o diretório no servidor especificado para o backup online e retorna um identificador de contexto de backup usado nas chamadas subsequentes para outras funções de backup.
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
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455285"
---
# <a name="dsbackupprepare-function"></a>Função DsBackupPrepare

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsBackupPrepare** prepara o diretório no servidor especificado para o backup online e retorna um identificador de contexto de backup usado em chamadas subsequentes para outras funções de backup.

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

*szBackupServer* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor para backup. Barras invertidas precedentes são opcionais. O servidor deve ser o mesmo computador do qual essa função é chamada. O nome do servidor não pode conter um caractere de sublinhado ( \_ ). Um exemplo de um nome de servidor é " \\ \\ Server1".

</dd> <dt>

*grbit* \[ no\]
</dt> <dd>

Determina se será feito backup dos arquivos de log. Esse valor deve ser sempre 0 porque não há suporte para backups incrementais.

</dd> <dt>

*btBackupType* \[ no\]
</dt> <dd>

Especifica o tipo de backup. Isso pode ser um dos valores a seguir.

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**tipo de BACKUP \_ \_ completo**


</dt> <dd>

Especifica um backup completo. O backup do diretório completo (DIT, arquivos de log e arquivos de atualização) é feito. Todos os dados são submetidos a backup e os arquivos de log de transações são truncados. Somente backups completos têm suporte.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_ \_ somente logs de tipo de backup \_**


</dt> <dd>

Não há suporte para esse valor. Especifica que somente os logs de banco de dados, e não o banco de dados, serão submetidos a backup. Isso normalmente é usado ao executar um backup diferencial ou incremental.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**tipo de BACKUP \_ \_ incremental**


</dt> <dd>

Não há suporte para esse valor. **DsBackupPrepare** retorna **um \_ \_ parâmetro inválido de erro**.

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[ fora\]
</dt> <dd>

Ponteiro para um valor **pVoid** que recebe um ponteiro para um token de expiração associado a este backup. *pcbExpiryTokenSize* recebe o tamanho, em bytes, desses dados. O chamador deve salvar o conteúdo desse token com o backup, pois o token deve ser passado para [**DsRestorePrepare**](dsrestoreprepare.md) ao tentar restaurar os dados. Depois que o token tiver sido armazenado e não for mais necessário, o chamador deverá liberar a memória alocada usando [**DsBackupFree**](dsbackupfree.md).

</dd> <dt>

*pcbExpiryTokenSize* \[ fora\]
</dt> <dd>

Ponteiro para um valor **DWORD** que recebe o tamanho, em bytes, do token em *ppvExpiryToken*.

</dd> <dt>

*phbc* \[ fora\]
</dt> <dd>

Aponta para um valor **HBC** que recebe o identificador para o backup. Esse identificador é usado ao chamar outras funções de backup do serviço de diretório, como [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsBackupEnd**](dsbackupend.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro do contrário. A lista a seguir lista outros códigos de erro possíveis.

<dl> <dt>

**ERRO de \_ acesso \_ negado**
</dt> <dd>

O chamador não tem os privilégios de acesso apropriados para chamar essa função. A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**\_parâmetro inválido de erro \_**
</dt> <dd>

*szBackupServer* ou *phbcBackupContext* não são válidos.

</dd> <dt>

**ERRO \_ de \_ memória insuficiente \_**
</dt> <dd>

Ocorreu uma falha de alocação de memória.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

O servidor no *szBackupServer* não pôde ser encontrado, não é um controlador de domínio ou *szBackupServer* não está formatado corretamente. Esse valor é definido em ntdsbmsg. h.

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* e/ou *pcbExpiryTokenSize* são inválidos. Esse valor é definido em Ntdsbmsg. h.

</dd> <dt>

**Associação de RPC \_ S \_ inválida \_**
</dt> <dd>

A função é chamada remotamente ou o servidor no *szServerName* não é um controlador de domínio.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa função requer que o chamador tenha o **privilégio \_ \_ nome de backup se** . A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para alterar o contexto de segurança no qual essa função é chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
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

[Fazendo backup de um servidor de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

