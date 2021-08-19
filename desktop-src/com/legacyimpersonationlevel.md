---
title: LegacyImpersonationLevel
description: Define o nível padrão de representação para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valor do Registro LegacyImpersonationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd032e83290c18fc3a2588e382ade7730fa2ea39a7847e375b1e887cdbbb90f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048074"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Define o nível padrão de representação para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não configuram sua própria segurança em todo o processo e podem impedi-los de funcionar corretamente. Se você estiver alterando esse valor para afetar as configurações de segurança de um aplicativo COM específico, deverá alterar as configurações de segurança em todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança em todo o processo, consulte [Configurando a segurança em todo o processo.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor REG \_ WORD** equivalente às constantes DE NÍVEL DE IMP do RPC \_ \_ \_ C.



| Valor | Constante                        |
|-------|---------------------------------|
| 1     | RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS   |
| 2     | RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY    |
| 3     | REPRESENTAÇÃO NO NÍVEL DE IMP DO RPC \_ C \_ \_ \_ |
| 4     | DELEGADO DE NÍVEL DE IMP DO RPC \_ C \_ \_ \_    |



 

Se esse valor do Registro não estiver presente, o nível de representação padrão estabelecido pelo sistema será 2 (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Configurando a segurança em todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




