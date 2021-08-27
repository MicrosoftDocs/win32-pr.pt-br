---
title: Verificando o estado de um parâmetro de acessibilidade
description: O fragmento de código a seguir usa a função GetSystemMetrics para verificar o parâmetro de mostrar sons. Se GetSystemMetrics retornar TRUE, o aplicativo deverá apresentar todas as informações importantes no formato visual.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374520612ce96522edc1b879a49f5f30a9c7a857f9bb46a562a4ab48effebe9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122246"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Verificando o estado de um parâmetro de acessibilidade

O fragmento de código a seguir usa a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para verificar o parâmetro de mostrar sons. Se **GetSystemMetrics** retornar **true**, o aplicativo deverá apresentar todas as informações importantes no formato visual.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 