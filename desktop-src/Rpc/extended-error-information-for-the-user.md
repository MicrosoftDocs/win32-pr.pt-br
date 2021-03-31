---
title: Informações de erro estendidas para o usuário
description: Se informações de erro estendidas estiverem disponíveis, os componentes que participam da criação das informações de erro estendidas devem facilitar a localização do problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822711"
---
# <a name="extended-error-information-for-the-user"></a>Informações de erro estendidas para o usuário

Se informações de erro estendidas estiverem disponíveis, os componentes que participam da criação das informações de erro estendidas devem facilitar a localização do problema. A primeira etapa é examinar o último registro de erro estendido e determinar em qual computador e qual processo o problema foi originado. Isso é geralmente a causa do erro de RPC \_ S \_ \* . Localize o local de detecção e determine quais são os parâmetros para esse local de detecção. Normalmente, eles indicam uma falha de uma chamada de função ou de uma verificação específica. A partir daí, determine por que a função ou verificação falha e execute uma ação corretiva.

Os registros antes do último registro indicam o caminho pelo qual o erro chegou e geralmente servem como uma verificação de sanidade, em vez de um auxílio no processo de solução de problemas.

 

 




