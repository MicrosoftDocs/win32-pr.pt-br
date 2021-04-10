---
title: AuthenticationLevel
description: Define o nível de autenticação para aplicativos que não chamam CoInitializeSecurity ou para aplicativos que chamam CoInitializeSecurity e especificam uma AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- COM valor do registro AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292848"
---
# <a name="authenticationlevel"></a>AuthenticationLevel

Define o nível de autenticação para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou para aplicativos que chamam **CoInitializeSecurity** e especificam uma AppID.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** equivalente às \_ constantes de nível de \_ autenticação RPC C \_ .



| Valor | Constante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ Authn \_ nível \_ nenhum           |
| 2     | \_conexão em \_ nível de autenticação RPC C \_ \_        |
| 3     | \_chamada de \_ nível de autenticação RPC C \_ \_           |
| 4     | \_PCT do \_ nível de autenticação RPC C \_ \_            |
| 5     | \_integridade de \_ pkt do \_ nível \_ de \_ autenticação RPC C |
| 6     | \_privacidade do \_ PCT do \_ nível \_ de \_ autenticação RPC C   |



 

O valor de **AuthenticationLevel** é semelhante ao valor de [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) . Se o valor de **AuthenticationLevel** estiver presente, ele será usado em vez do valor de **LegacyAuthenticationLevel** para esse AppID.

Se o valor de **AuthenticationLevel** for do tipo incorreto ou fora do intervalo, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) falhará, causando falha no marshaling da interface. Isso impede que o aplicativo faça qualquer chamada (entre apartamento, entre threads, entre processos ou entre computadores).

Os valores **AuthenticationLevel** e [**AccessPermission**](accesspermission.md) são independentes. Se um não estiver presente, o padrão será usado. As regras a seguir listam a interação entre o valor **AuthenticationLevel** e o valor **AccessPermission** :

-   Se **AuthenticationLevel** for None, os valores [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) serão ignorados (para esse aplicativo).
-   Se o **AuthenticationLevel** não estiver presente e [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) for None, os valores [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) serão ignorados (para esse aplicativo).

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

 

 




