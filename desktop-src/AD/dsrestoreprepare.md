---
title: Função DsRestorePrepare (Ntdsbcli. h)
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
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085473"
---
# <a name="dsrestoreprepare-function"></a>Função DsRestorePrepare

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsRestorePrepare** conecta-se ao servidor de diretório especificado e o prepara para a operação de restauração.

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

*szServerName* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor a ser restaurado. Barras invertidas precedentes são opcionais. O servidor deve ser o mesmo computador do qual essa função é chamada. O nome do servidor não pode conter nenhum caractere de sublinhado ( \_ ). Um exemplo de um nome de servidor é " \\ \\ Server1".

</dd> <dt>

*rtFlag* \[ no\]
</dt> <dd>

Especifica o tipo de restauração a ser executada. Isso pode ser zero ou um dos valores a seguir.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**tipo de restauração \_ \_ catchup**


</dt> <dd>

Padrão. A versão restaurada é reconciliada por meio da lógica de reconciliação padrão para que a DIT restaurada possa sincronizar com outros computadores de servidor corporativo.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**tipo de restauração \_ \_ AUTHORATATIVE**


</dt> <dd>

Sem suporte.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTAURAR \_ tipo \_ online**


</dt> <dd>

Sem suporte. A restauração é executada quando o NTDS está online.

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[ no\]
</dt> <dd>

Ponteiro para o token de expiração associado ao backup que está sendo restaurado. Esse token foi obtido da função [**DsBackupPrepare**](dsbackupprepare.md) quando foi feito o backup do diretório.

Se esse parâmetro for **NULL**, o identificador retornado em *phbc* só poderá ser usado para obter os diretórios de restauração com a função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) . O identificador não pode ser usado para nenhuma outra função de restauração.

</dd> <dt>

*cbExpiryTokenSize* \[ no\]
</dt> <dd>

Contém o tamanho, em bytes, do token de expiração em *pvExpiryToken*.

</dd> <dt>

*phbc* \[ fora\]
</dt> <dd>

Ponteiro para um valor **HBC** que recebe o identificador para a restauração. Esse identificador é usado ao chamar outras funções de restauração do serviço de diretório, como [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsRestoreEnd**](dsrestoreend.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, retorna um código **HRESULT** padrão; caso contrário, um código de falha será retornado.

## <a name="remarks"></a>Comentários

A função **DsRestorePrepare** requer que o chamador seja um membro do grupo Administradores no servidor.

**DsRestorePrepare** pode ser usado com ou sem um token fornecido. Se o token for fornecido, ele será verificado quanto à expiração e todas as operações serão permitidas no contexto retornado. Se o token não for fornecido, o contexto retornado será restrito e poderá ser usado somente para a função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) . Ele não pode ser usado para a função [**DsRestoreRegister**](dsrestoreregister.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsRestorePrepareW** (Unicode) e **DsRestorePrepareA** (ANSI)<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Restaurando um servidor de Active Directory](restoring-an-active-directory-server.md)
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

 

