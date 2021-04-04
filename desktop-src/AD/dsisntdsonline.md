---
title: Função DsIsNTDSOnline (Ntdsbcli. h)
description: Determina se Active Directory Domain Services estão online no servidor especificado.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Função DsIsNTDSOnline Active Directory
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085595"
---
# <a name="dsisntdsonline-function"></a>Função DsIsNTDSOnline

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]

A função **DsIsNTDSOnline** determina se os Active Directory Domain Services estão online no servidor especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szServerName* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor a ser testado. Barras invertidas precedentes são opcionais. O servidor deve ser o mesmo computador do qual essa função é chamada. O nome do servidor não pode conter nenhum caractere de sublinhado ( \_ ). Um exemplo de um nome de servidor é " \\ \\ Server1".

</dd> <dt>

*pfNTDSOnline* \[ fora\]
</dt> <dd>

Ponteiro para o valor **bool** que recebe o resultado. Receberá **true** se o serviço de diretório estiver online ou **false** se o serviço de diretório estiver offline.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro do contrário. A lista a seguir lista os possíveis códigos de erro.

<dl> <dt>

**ERRO de \_ acesso \_ negado**
</dt> <dd>

O chamador não tem os privilégios de acesso apropriados para chamar essa função. A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

O servidor em *szServerName* não pode ser encontrado, não é um controlador de domínio ou *szServerName* não está formatado corretamente. Esse valor é definido em Ntdsbmsg. h.

</dd> <dt>

**Associação de RPC \_ S \_ inválida \_**
</dt> <dd>

A função [**DsIsNTDSOnline**](dsisntdsonline.md) está sendo chamada remotamente ou o servidor em *szServerName* não é um controlador de domínio.

</dd> </dl>

## <a name="remarks"></a>Comentários

Chame essa função antes de chamar qualquer uma das funções de backup ou restauração do diretório. O diretório deve estar online para executar um backup. O diretório deve estar offline para executar uma restauração.

Essa função só pode ser chamada de um controlador de domínio que também seja o servidor de destino especificado em *szServerName*. Esta função não pode ser chamada remotamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DsIsNTDSOnlineW** (Unicode) e **DsIsNTDSOnlineA** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Funções de backup de diretório](directory-backup-functions.md)
</dt> <dt>

[Fazendo backup e restaurando um servidor de Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

