---
description: Permite que as páginas do lado do servidor hospedadas em um assistente verifiquem se o usuário foi autenticado por meio de um conta Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Método NewWDEvents. PassportAuthenticate (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f462053281efd97b75422c55ce23829688d18ac153ecb92c7544eafb8f356b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942396"
---
# <a name="newwdeventspassportauthenticate-method"></a>Método NewWDEvents. PassportAuthenticate

Permite que as páginas do lado do servidor hospedadas em um assistente verifiquem se o usuário foi autenticado por meio de um conta Microsoft.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrSignInUrl* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma cadeia de caracteres que contém a URL de uma página da Web que redireciona para o log de conta Microsoft na interface do usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **booliano**

Defina como **true** se a autenticação for realizada com sucesso; caso contrário, **false** .

## <a name="remarks"></a>Comentários

Esse método pode ser chamado mesmo se um usuário já estiver conectado a um conta Microsoft. Nesse caso, o método retorna **true** sem exibir o log de conta Microsoft na interface do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 6,0 ou posterior)</dt> </dl> |



 

 
