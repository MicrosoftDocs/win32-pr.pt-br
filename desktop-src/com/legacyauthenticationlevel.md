---
title: LegacyAuthenticationLevel
description: Define o nível de autenticação padrão para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- COM valor do registro LegacyAuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006168"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

Define o nível de autenticação padrão para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente. Se você estiver alterando esse valor para afetar as configurações de segurança para um aplicativo COM específico, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ Word** equivalente às \_ constantes de nível de \_ autenticação RPC C \_ .



| Valor | Constante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ Authn \_ nível \_ nenhum           |
| 2     | \_conexão em \_ nível de autenticação RPC C \_ \_        |
| 3     | \_chamada de \_ nível de autenticação RPC C \_ \_           |
| 4     | \_PCT do \_ nível de autenticação RPC C \_ \_            |
| 5     | \_integridade de \_ pkt do \_ nível \_ de \_ autenticação RPC C |
| 6     | \_privacidade do \_ PCT do \_ nível \_ de \_ autenticação RPC C   |



 

Se esse valor de registro não estiver presente, o nível de autenticação padrão estabelecido pelo sistema será 2 (RPC \_ C \_ Authn \_ Connect).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**AuthenticationLevel**](authenticationlevel.md)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Definindo a segurança de todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




