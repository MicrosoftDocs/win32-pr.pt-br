---
title: depuração (Windows serviços Web)
description: Um conjunto de funções só está disponível na compilação de depuração e destina-se a testes e depuração.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Depurando serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135f81ec45028df098679c91d750915005bfc64b3ff7d072b0494badc98159fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838675"
---
# <a name="debugging-windows-web-services"></a>depuração (Windows serviços Web)

Um conjunto de funções só está disponível na compilação de depuração e destina-se a testes e depuração.


Há várias funções e variáveis de ambiente disponíveis somente no modo de depuração. Eles podem ser usados para ajudar no teste e na depuração.

-   A configuração de WsTimeout = 0 fará com que todos os tempos limite sejam INFINITOs. Isso é útil ao percorrer o depurador durante operações sensíveis ao tempo.
-   A definição de WsFailCount tem o mesmo efeito que chamar WsSetAutoFail.
-   WsFlags permite que você defina vários sinalizadores que modificam o comportamento de tempo de execução. A sintaxe é WsFlags = a, b, c. Os sinalizadores com suporte são ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest e ModifySignatureValue.

As funções a seguir são usadas com a depuração:

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




