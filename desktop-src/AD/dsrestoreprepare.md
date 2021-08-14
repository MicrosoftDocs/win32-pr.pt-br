---
title: Função DsRestorePrepare (Ntdsbcli.h)
description: Conecta-se ao servidor de diretório especificado e o prepara para a operação de restauração.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Função DsRestorePrepare Active Directory
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11b844919cc459788bbd8acda722a68344ae16807e45be9bd6dcd5780b09d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191802"
---
# <a name="dsrestoreprepare-function"></a>Função DsRestorePrepare

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Começando com Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A **função DsRestorePrepare** se conecta ao servidor de diretório especificado e a prepara para a operação de restauração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szServerName* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor a ser restaurado. As malhas inativas anteriores são opcionais. O servidor deve ser o mesmo computador do onde essa função é chamada. O nome do servidor não pode conter caracteres de sublinhado ( \_ ). Um exemplo de um nome de servidor é " \\ \\ server1".

</dd> <dt>

*rtFlag* \[ Em\]
</dt> <dd>

Especifica o tipo de restauração a ser executar. Isso pode ser zero ou um dos valores a seguir.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE \_ TYPE \_ CATCHUP**


</dt> <dd>

Padrão. A versão restaurada é reconciliada por meio da lógica de reconciliação padrão para que o DIT restaurado possa sincronizar com outros computadores de servidor empresarial.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE \_ TYPE \_ AUTHORATATIVE**


</dt> <dd>

Sem suporte.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE \_ TYPE \_ ONLINE**


</dt> <dd>

Sem suporte. A restauração é executada quando o NTDS está online.

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[ Em\]
</dt> <dd>

Ponteiro para o token de expiração associado ao backup que está sendo restaurado. Esse token foi obtido da função [**DsBackupPrepare**](dsbackupprepare.md) quando o diretório foi feito backup.

Se esse parâmetro for **NULL,** o handle retornado em *phbc* só poderá ser usado para obter os diretórios de restauração com a [**função DsRestoreGetDatabaseLocations.**](dsrestoregetdatabaselocations.md) O handle não pode ser usado para nenhuma outra função de restauração.

</dd> <dt>

*cbExpiryTokenSize* \[ Em\]
</dt> <dd>

Contém o tamanho, em bytes, do token de expiração *em pvExpiryToken.*

</dd> <dt>

*phbc* \[ out\]
</dt> <dd>

Ponteiro para um **valor HBC** que recebe o alça para a restauração. Esse handle é usado ao chamar outras funções de restauração do Serviço de Diretório, como [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsRestoreEnd.**](dsrestoreend.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, retornará um código **HRESULT** padrão; caso contrário, um código de falha será retornado.

## <a name="remarks"></a>Comentários

A **função DsRestorePrepare** requer que o chamador seja membro do grupo Administradores no servidor.

**DsRestorePrepare** pode ser usado com ou sem um token fornecido. Se o token for fornecido, ele será verificado quanto à expiração e todas as operações serão permitidas no contexto retornado. Se o token não for fornecido, o contexto retornado será restrito e poderá ser usado somente para a [**função DsRestoreGetDatabaseLocations.**](dsrestoregetdatabaselocations.md) Ele não pode ser usado para a [**função DsRestoreRegister.**](dsrestoreregister.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsRestorePrepareW** (Unicode) e **DsRestorePrepareA** (ANSI)<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Restaurando um servidor do Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> </dl>

 

