---
title: Informações de erro estendidas para o usuário
description: Se as informações de erro estendidas estão disponíveis, os componentes que participam da criação das informações de erro estendidas devem facilitar a encontrar o problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d2c7a67bb678472fbd3abbf90e0885590c795e2ffc46213a7acbb397da149c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021301"
---
# <a name="extended-error-information-for-the-user"></a>Informações de erro estendidas para o usuário

Se as informações de erro estendidas estão disponíveis, os componentes que participam da criação das informações de erro estendidas devem facilitar a encontrar o problema. A primeira etapa é analisar o último registro de erro estendido e determinar em qual computador e em qual processo o problema foi originado. Geralmente, essa é a causa do erro \_ RPC \_ \* S. Localizar o local de detecção e determinar o que significam os parâmetros para esse local de detecção. Normalmente, eles indicam uma falha de uma chamada de função ou uma verificação específica. A partir daí, determine por que a função ou a verificação falha e tome uma ação corretiva.

Os registros antes do último registro indicam o caminho pelo qual o erro chegou e geralmente servem como uma verificação de sanidade em vez de um auxiliar no processo de solução de problemas.

 

 




