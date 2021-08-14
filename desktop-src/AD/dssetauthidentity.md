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
ms.openlocfilehash: a8e4f990d1fa0c6a6a22b0068ea207be61b4aece441977b976f32f82b7b75c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695501"
---
# <a name="dssetauthidentity-function"></a>Função DsSetAuthIdentity

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. a partir do Windows Vista, use [Serviço de Cópias de Sombra de Volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

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

## <a name="return-value"></a>Valor retornado

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

 

