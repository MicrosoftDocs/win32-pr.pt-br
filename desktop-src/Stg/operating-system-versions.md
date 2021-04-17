---
title: Versões do sistema operacional
description: Esse tipo de dados DWORD deve conter o tipo de sistema operacional na palavra de ordem superior e o número de versão do sistema operacional na palavra de ordem inferior. Os valores possíveis para o sistema operacional são listados na tabela a seguir.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Armazenamento estruturado das versões do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105754486"
---
# <a name="operating-system-versions"></a>Versões do sistema operacional

Esse tipo de dados **DWORD** deve conter o tipo de sistema operacional na palavra de ordem superior e o número de versão do sistema operacional na palavra de ordem inferior. Os valores possíveis para o sistema operacional são listados na tabela a seguir.



| Sistema operacional       | Valor  |
|------------------------|--------|
| Windows de 32 bits (Win32) | 0x0002 |
| Macintosh              | 0x0001 |
| Windows de 16 bits (Win16) | 0x0000 |



 

Para sistemas operacionais Microsoft Windows, a versão do sistema operacional é a palavra de ordem inferior retornada pela função [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) . Para o Microsoft Windows, o código de exemplo a seguir define corretamente a versão do sistema operacional de origem.

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 