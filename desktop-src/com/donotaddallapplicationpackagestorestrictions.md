---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Determina se o RPCSs acrescenta automaticamente um \_ \_ Sid de todos os pacotes de aplicativos a restrições com por padrão.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363726"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

Determina se o RPCSs acrescenta automaticamente um \_ \_ Sid de todos os pacotes de aplicativos a restrições com por padrão.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor | Descrição                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Desabilita os aplicativos da Windows Store após a migração do Windows 7 para o Windows 8.                   |
| 1     | Não adiciona o SID todos \_ os \_ pacotes de aplicativos a restrições com. Esse é o padrão. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




