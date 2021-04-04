---
title: Verificando o estado de um parâmetro de acessibilidade
description: O fragmento de código a seguir usa a função GetSystemMetrics para verificar o parâmetro de mostrar sons. Se GetSystemMetrics retornar TRUE, o aplicativo deverá apresentar todas as informações importantes no formato visual.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007639"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Verificando o estado de um parâmetro de acessibilidade

O fragmento de código a seguir usa a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para verificar o parâmetro de mostrar sons. Se **GetSystemMetrics** retornar **true**, o aplicativo deverá apresentar todas as informações importantes no formato visual.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 