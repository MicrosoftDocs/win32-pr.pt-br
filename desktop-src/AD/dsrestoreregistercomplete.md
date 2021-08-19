---
title: Função DsRestoreRegisterComplete (Ntdsbcli. h)
description: Chamado para desbloquear um servidor de Active Directory após a conclusão de uma operação de restauração.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Função DsRestoreRegisterComplete Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b335f67ed4d392d189553f66655797e03121cbdee6ce19dffbd9803199f6c72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429924"
---
# <a name="dsrestoreregistercomplete-function"></a>Função DsRestoreRegisterComplete

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use o [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

A função **DsRestoreRegisterComplete** é chamada para desbloquear um servidor de Active Directory após a conclusão de uma operação de restauração. Essa função é equivalente à função [**DsRestoreRegister**](dsrestoreregister.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HBC* \[ no\]
</dt> <dd>

Contém o identificador de contexto de restauração obtido com a função [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*hrRestoreState* \[ no\]
</dt> <dd>

Contém o status final da operação de restauração. Esse parâmetro deve conter **S \_ OK** se a operação de restauração tiver sido bem-sucedida ou um código de erro de outra forma.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC. A lista a seguir lista os possíveis códigos de erro.

<dl> <dt>

**ERRO de \_ acesso \_ negado**
</dt> <dd>

O chamador não tem os privilégios de acesso apropriados para chamar essa função. A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> </dl>

## <a name="remarks"></a>Comentários

Antes de reiniciar o controlador de domínio, chame essa função para fornecer o status da operação de restauração. Se o status não for bem-sucedido, o serviço de diretório não será iniciado até que um banco de dados válido tenha sido restaurado. Essa função conclui a operação de restauração e permite que Active Directory Domain Services iniciem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                               |
| Fim do suporte do servidor<br/>    | Nenhum compatível<br/>                                                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Restaurando um servidor de Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

