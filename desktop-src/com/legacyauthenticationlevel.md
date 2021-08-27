---
title: LegacyAuthenticationLevel
description: Define o nível de autenticação padrão para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valor do Registro LegacyAuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6be9f562a543e4750695ec2bf967b5a261209aae70d0bf91269bc2a074a9e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096946"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

Define o nível de autenticação padrão para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não configuram sua própria segurança em todo o processo e podem impedi-los de funcionar corretamente. Se você estiver alterando esse valor para afetar as configurações de segurança de um aplicativo COM específico, deverá alterar as configurações de segurança em todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança em todo o processo, consulte [Configurando a segurança em todo o processo.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor REG \_ WORD** equivalente às \_ constantes RPC C \_ AUTHN \_ LEVEL.



| Valor | Constante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           |
| 2     | RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        |
| 3     | RPC C CHAMADA DE NÍVEL \_ \_ AUTHN \_ \_           |
| 4     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            |
| 5     | INTEGRIDADE \_ PKT NO NÍVEL DE \_ AUTHN \_ \_ RPC C \_ |
| 6     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   |



 

Se esse valor do Registro não estiver presente, o nível de autenticação padrão estabelecido pelo sistema será 2 (RPC \_ C \_ AUTHN \_ CONNECT).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Authenticationlevel**](authenticationlevel.md)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Configurando a segurança em todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




