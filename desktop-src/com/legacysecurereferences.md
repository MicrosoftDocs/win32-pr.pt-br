---
title: LegacySecureReferences
description: Determina se as invocações AddRef/Release são protegidas para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valor do Registro LEGACYSecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3a4ab964d73fa4b194c734f28c23ff068239370088c090051464129b6caf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736543"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Determina se as **invocações de** Versão de AddRef são protegidas para aplicativos que /  não chamam [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG SZ.** Um valor de 'Y' ou 'y' indica que **AddRef** e **Release** estão protegidos. Se esse valor do Registro não estiver presente ou estiver definido como um valor diferente de 'Y' ou 'y', **AddRef** e **Release** não serão protegidos. A habilitação de referências seguras retarda as chamadas remotas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Configurando a segurança em todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




