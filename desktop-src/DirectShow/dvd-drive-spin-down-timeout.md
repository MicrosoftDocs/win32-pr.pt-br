---
description: Tempo limite de rotação da unidade de DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Tempo limite de rotação da unidade de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825925"
---
# <a name="dvd-drive-spin-down-timeout"></a>Tempo limite de rotação da unidade de DVD

Em computadores laptop, para conservar a vida útil da bateria, pode ser desejável reduzir o período de tempo que uma unidade de DVD continuará a girar depois que o usuário tiver pausado a reprodução. Por padrão, o navegador de DVD mantém o disco girando por dois minutos. Esse valor pode ser modificado no registro do Windows sob esta chave:


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



onde


```
Sec
```



é o tempo de desativação de rotação em segundos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apêndices](appendixes.md)
</dt> </dl>

 

 



