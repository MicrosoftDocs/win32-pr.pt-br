---
title: Função DsSetAuthIdentity (Ntdsbcli. h)
description: Define o contexto de segurança no qual as APIs de backup do diretório são chamadas.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Função DsSetAuthIdentity Active Directory
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455355"
---
# <a name="dssetauthidentity-function"></a>Função DsSetAuthIdentity

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsSetAuthIdentity** define o contexto de segurança sob o qual as APIs de backup do diretório são chamadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szUserName* \[ no\]
</dt> <dd>

A cadeia de caracteres terminada em nulo que especifica o nome de usuário.

</dd> <dt>

*szDomainName* \[ no\]
</dt> <dd>

A cadeia de caracteres terminada em nulo que especifica o nome do domínio ao qual o usuário pertence.

</dd> <dt>

*szPassword* \[ no\]
</dt> <dd>

A cadeia de caracteres terminada em nulo que especifica a senha do usuário no domínio especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, retorna um código de êxito **HRESULT** padrão; caso contrário, um código de falha será retornado.

## <a name="remarks"></a>Comentários

Se **DsSetAuthIdentity** não for chamado, o contexto de segurança do processo atual será assumido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsSetAuthIdentityW** (Unicode) e **DsSetAuthIdentityA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Fazendo backup e restaurando um servidor de Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> </dl>

 

