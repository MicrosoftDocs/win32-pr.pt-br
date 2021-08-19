---
title: Função DsRestoreGetDatabaseLocations (Ntdsbcli.h)
description: Obtém os locais em que os arquivos de backup devem ser copiados durante uma operação de restauração.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Função DsRestoreGetDatabaseLocations active directory
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c5626e2e0dc679a4669bb5d8be8096b6ae0629aeed7c833f397b5f9bca45db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429988"
---
# <a name="dsrestoregetdatabaselocations-function"></a>Função DsRestoreGetDatabaseLocations

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Começando com Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A **função DsRestoreGetDatabaseLocations** obtém os locais em que os arquivos de backup devem ser copiados durante uma operação de restauração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hbc* \[ Em\]
</dt> <dd>

Contém o handle de contexto de restauração obtido com a [**função DsRestorePrepare.**](dsrestoreprepare.md)

</dd> <dt>

*pszDatabaseLocationList* \[ out\]
</dt> <dd>

Ponteiro para um ponteiro de cadeia de caracteres que recebe a lista de locais de banco de dados como caminhos UNC. Essa lista recebe uma lista de terminação nula dupla de cadeias de caracteres terminadas em nulo único.

Esse buffer é alocado pela função **DsRestoreGetDatabaseLocations** e deve ser liberado quando não for mais necessário chamando a [**função DsBackupFree.**](dsbackupfree.md)

O primeiro caractere de cada um dos nomes de arquivo contém uma das [**Constantes BFT**](bft-constants.md) que identifica o tipo de nome. A **função DsRestoreGetDatabaseLocations** fornece apenas os seguintes tipos de nome.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**


</dt> <dd>

O arquivo de banco de dados NTDS deve ser copiado para esse arquivo. Esse é o arquivo que foi identificado como **BFT \_ NTDS \_ DATABASE** quando o backup foi executado.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ LOG \_ DIR**


</dt> <dd>

Todos os arquivos de log são copiados para esse diretório. Os arquivos de log foram identificados como **LOG BFT \_** quando o backup foi executado.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**DIR DO \_ PONTO DE VERIFICAÇÃO do BFT \_**


</dt> <dd>

Todos os arquivos de patch são copiados para esse diretório. Os arquivos de patch foram identificados como **BFT \_ PATCH \_ FILE** quando o backup foi executado.

</dd> </dl> </dd> <dt>

*pcbSize* \[ out\]
</dt> <dd>

Ponteiro para **o valor DWORD** que recebe o tamanho, em bytes, do buffer *pszDatabaseLocationList.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro Win32 ou RPC caso contrário. A lista a seguir lista possíveis códigos de erro.

<dl> <dt>

**ACESSO \_ DE ERRO \_ NEGADO**
</dt> <dd>

O chamador não tem os privilégios de acesso adequados para chamar essa função. A [**função DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**ERRO \_ PARÂMETRO \_ INVÁLIDO**
</dt> <dd>

*hbc*, *pszDatabaseLocationList* ou *pcbSize* são inválidos.

</dd> <dt>

**ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**
</dt> <dd>

Ocorreu uma falha de alocação de memória.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **função DsRestoreGetDatabaseLocations** pode ser usada para obter os diretórios de restauração sem acesso aos dados de backup. Para fazer isso, chame [**DsRestorePrepare**](dsrestoreprepare.md) com **NULL** para o *parâmetro pvExpiryToken.* Isso faz **com que DsRestorePrepare** retorne um handle de contexto restrito que só pode ser usado com a **função DsRestoreGetDatabaseLocations.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>                 |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>               |
| Nomes Unicode e ANSI<br/>   | **DsRestoreGetDatabaseLocationsW** (Unicode) e **DsRestoreGetDatabaseLocationsA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> <dt>

[Restaurando o Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

