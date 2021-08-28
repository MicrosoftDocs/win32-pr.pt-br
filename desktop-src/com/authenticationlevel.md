---
title: Authenticationlevel
description: Define o nível de autenticação para aplicativos que não chamam CoInitializeSecurity ou para aplicativos que chamam CoInitializeSecurity e especificam uma AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valor do Registro AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7968382ea97243c1116dd6785be34a0d1c3e6eafc6cb9ee13f16b939029a6611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120526"
---
# <a name="authenticationlevel"></a>Authenticationlevel

Define o nível de autenticação para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou para aplicativos que chamam **CoInitializeSecurity** e especificam uma AppID.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG DWORD** equivalente às \_ constantes RPC C \_ AUTHN \_ LEVEL.



| Valor | Constante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           |
| 2     | RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        |
| 3     | RPC C CHAMADA DE NÍVEL \_ \_ AUTHN \_ \_           |
| 4     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            |
| 5     | INTEGRIDADE \_ PKT NO NÍVEL DE \_ AUTHN \_ \_ RPC C \_ |
| 6     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   |



 

O **valor AuthenticationLevel** é semelhante ao [**valor LegacyAuthenticationLevel.**](legacyauthenticationlevel.md) Se o **valor AuthenticationLevel** estiver presente, ele será usado em vez do valor **LegacyAuthenticationLevel** para essa AppID.

Se o **valor AuthenticationLevel** for do tipo errado ou fora do intervalo, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) falhará, fazendo com que o marshaling de interface falhe. Isso impede que o aplicativo faz todas as chamadas (entre apartments, entre threads, entre processos ou entre computadores).

Os **valores AuthenticationLevel** [**e AccessPermission**](accesspermission.md) são independentes. Se um não estiver presente, o padrão será usado. As regras a seguir listam a interação entre o **valor AuthenticationLevel** e **o valor AccessPermission:**

-   Se **AuthenticationLevel** for NONE, os valores [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) serão ignorados (para esse aplicativo).
-   Se **AuthenticationLevel** não estiver presente e [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) for NONE, os valores [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) serão ignorados (para esse aplicativo).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de nível de autenticação](com-authentication-level-constants.md)
</dt> <dt>

[**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




