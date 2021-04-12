---
title: Função DsBackupGetDatabaseNames (Ntdsbcli. h)
description: Obtém a lista de arquivos de banco de dados cujo backup será feito para o contexto de backup fornecido.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Função DsBackupGetDatabaseNames Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455286"
---
# <a name="dsbackupgetdatabasenames-function"></a>Função DsBackupGetDatabaseNames

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsBackupGetDatabaseNames** Obtém a lista de arquivos de banco de dados cujo backup será feito para o contexto de backup fornecido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HBC* \[ no\]
</dt> <dd>

Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pszAttachmentInfo* \[ fora\]
</dt> <dd>

Ponteiro para um ponteiro de cadeia de caracteres que recebe a lista de nomes de arquivo de banco de dados como caminhos UNC. Esse valor deve ser inicializado para **NULL** antes de chamar **DsBackupGetDatabaseNames**.

Essa lista recebe uma lista terminada por nulo de cadeias de caracteres com terminação nula.

Esse buffer é alocado pela função **DsBackupGetDatabaseNames** e deve ser liberado quando não for mais necessário chamando a função [**DsBackupFree**](dsbackupfree.md) .

O primeiro caractere de cada nome de arquivo contém uma das [**constantes BFT**](bft-constants.md) que identifica o tipo de nome. A função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) fornece apenas os seguintes tipos de nomes.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_banco de \_ dados NTDS BFT**


</dt> <dd>

O arquivo é um arquivo de banco de dados NTDS. Esse arquivo deve ser copiado para o arquivo identificado **como \_ \_ banco de dados BFT NTDS** quando os dados são restaurados.

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**LOG do BFT \_**


</dt> <dd>

O arquivo é um arquivo de log. Todos os arquivos de log são copiados para o diretório identificado como **BFT \_ log \_ dir** quando os dados são restaurados.

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_arquivo de patch do BFT \_**


</dt> <dd>

O arquivo é um arquivo de patch. Todos os arquivos de patch são copiados para o diretório identificado como **BFT \_ Checkpoint \_ dir** quando os dados são restaurados.

</dd> </dl> </dd> <dt>

*pcbSize* \[ fora\]
</dt> <dd>

Ponteiro para o valor **DWORD** que recebe o tamanho, em bytes, do buffer *pszAttachmentInfo* .

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

*HBC*, *pszAttachmentInfo* ou *pcbSize* são inválidos.

</dd> <dt>

**ERRO \_ de \_ memória insuficiente \_**
</dt> <dd>

Ocorreu uma falha de alocação de memória.

</dd> </dl>

## <a name="remarks"></a>Comentários

A função **DsBackupGetDatabaseNames** fornece uma lista dos arquivos de banco de dados necessários para um backup. Um backup completo consiste nos arquivos de banco de dados e nos arquivos de log fornecidos pela função [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) . Não há suporte para backups incrementais de servidores Active Directory.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>     |
| Nomes Unicode e ANSI<br/>   | **DsBackupGetDatabaseNamesW** (Unicode) e **DsBackupGetDatabaseNamesA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**Constantes BFT**](bft-constants.md)
</dt> <dt>

[Fazendo backup de um servidor de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

