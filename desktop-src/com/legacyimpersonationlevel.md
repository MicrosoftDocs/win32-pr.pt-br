---
title: LegacyImpersonationLevel
description: Define o nível padrão de representação para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- COM valor do registro LegacyImpersonationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810837"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Define o nível padrão de representação para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente. Se você estiver alterando esse valor para afetar as configurações de segurança para um aplicativo COM específico, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ Word** equivalente às constantes de nível de imp da RPC \_ C \_ \_ .



| Valor | Constante                        |
|-------|---------------------------------|
| 1     | nível de imp do RPC \_ C- \_ \_ \_ anônimo   |
| 2     | \_identificação de \_ nível de imp \_ \_ de RPC C    |
| 3     | \_representação de \_ nível de imp \_ \_ do RPC C |
| 4     | \_delegado de \_ nível de imp \_ \_ de RPC C    |



 

Se esse valor de registro não estiver presente, o nível de representação padrão estabelecido pelo sistema será 2 (a identificação do nível de imp do RPC \_ C \_ \_ \_ ).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Definindo a segurança de todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




