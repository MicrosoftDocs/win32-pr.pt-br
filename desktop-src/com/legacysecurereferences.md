---
title: LegacySecureReferences
description: Determina se invocações AddRef/Release são protegidas para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- COM valor do registro LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105782628"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Determina se as / invocações de **versão** AddRef são protegidas para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz do reg** . Um valor de ' Y ' ou ' y ' indica que **AddRef** e **Release** são protegidos. Se esse valor de registro não estiver presente ou definido com um valor diferente de ' Y ' ou ' y ', **AddRef** e **Release** não serão protegidos. A habilitação de referências seguras reduz as chamadas remotas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Definindo a segurança de todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




