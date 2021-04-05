---
title: Função DsRestoreGetDatabaseLocations (Ntdsbcli. h)
description: Obtém os locais em que os arquivos de backup devem ser copiados durante uma operação de restauração.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Função DsRestoreGetDatabaseLocations Active Directory
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
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824574"
---
# <a name="dsrestoregetdatabaselocations-function"></a>Função DsRestoreGetDatabaseLocations

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsRestoreGetDatabaseLocations** Obtém os locais em que os arquivos de backup devem ser copiados durante uma operação de restauração.

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

*HBC* \[ no\]
</dt> <dd>

Contém o identificador de contexto de restauração obtido com a função [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*pszDatabaseLocationList* \[ fora\]
</dt> <dd>

Ponteiro para um ponteiro de cadeia de caracteres que recebe a lista de locais de banco de dados como caminhos UNC. Essa lista recebe uma lista terminada por nulo de cadeias de caracteres com terminação nula.

Esse buffer é alocado pela função **DsRestoreGetDatabaseLocations** e deve ser liberado quando não for mais necessário chamando a função [**DsBackupFree**](dsbackupfree.md) .

O primeiro caractere de cada um dos nomes de arquivo contém uma das [**constantes BFT**](bft-constants.md) que identifica o tipo de nome. A função **DsRestoreGetDatabaseLocations** fornece apenas os seguintes tipos de nome.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_banco de \_ dados NTDS BFT**


</dt> <dd>

O arquivo de banco de dados NTDS deve ser copiado para esse arquivo. Esse é o arquivo que foi identificado como **\_ banco de \_ dados BFT NTDS** quando o backup foi executado.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**Dir. de log do BFT \_ \_**


</dt> <dd>

Todos os arquivos de log são copiados para esse diretório. Os arquivos de log foram identificados **como \_ log de BFT** quando o backup foi executado.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT de \_ ponto de verificação de \_ diretório**


</dt> <dd>

Todos os arquivos de patch são copiados para esse diretório. Os arquivos de patch foram identificados como um **\_ \_ arquivo de patch BFT** quando o backup foi executado.

</dd> </dl> </dd> <dt>

*pcbSize* \[ fora\]
</dt> <dd>

Ponteiro para o valor **DWORD** que recebe o tamanho, em bytes, do buffer *pszDatabaseLocationList* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC. A lista a seguir lista os possíveis códigos de erro.

<dl> <dt>

**ERRO de \_ acesso \_ negado**
</dt> <dd>

O chamador não tem os privilégios de acesso apropriados para chamar essa função. A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**\_parâmetro inválido de erro \_**
</dt> <dd>

*HBC*, *pszDatabaseLocationList* ou *pcbSize* são inválidos.

</dd> <dt>

**ERRO \_ de \_ memória insuficiente \_**
</dt> <dd>

Ocorreu uma falha de alocação de memória.

</dd> </dl>

## <a name="remarks"></a>Comentários

A função **DsRestoreGetDatabaseLocations** pode ser usada para obter os diretórios de restauração sem acesso aos dados de backup. Para fazer isso, chame [**DsRestorePrepare**](dsrestoreprepare.md) com **NULL** para o parâmetro *pvExpiryToken* . Isso faz com que o **DsRestorePrepare** retorne um identificador de contexto restrito que só pode ser usado com a função **DsRestoreGetDatabaseLocations** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                        |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>                 |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>               |
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

[Restaurando Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

