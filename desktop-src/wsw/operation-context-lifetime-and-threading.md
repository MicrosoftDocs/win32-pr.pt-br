---
title: Tempo de vida do contexto de operação e threading
description: O tempo de vida do contexto de operação, representado por um \_ identificador de contexto de operação WS \_ , determina o tempo de vida das propriedades que ele contém.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Tempo de vida de contexto de operação e serviços Web de threading para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd2748f797e43bab750f4e02409e62e6293b39cb44d4cfd3626f86099502fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344826"
---
# <a name="operation-context-lifetime-and-threading"></a>Tempo de vida do contexto de operação e threading

O tempo de vida do contexto de operação, representado por um identificador de [ \_ \_ contexto de operação WS](ws-operation-context.md) , determina o tempo de vida das propriedades que ele contém. Portanto, um contexto só deve ser usado dentro do tempo de vida da [operação de serviço](service-operation.md) ou do retorno de chamada para o qual ele foi fornecido. O tempo de vida de uma chamada síncrona é a execução da própria função. Para uma chamada assíncrona, o tempo de vida termina quando a chamada assíncrona é concluída. O modelo de serviço não fornece nenhuma garantia sobre o contexto quando a chamada é concluída. O comportamento de depender do contexto de operação ou de qualquer uma de suas propriedades além de seu tempo de vida é indefinido.


Consulte também o exemplo de calculadora baseado em sessão, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).

## <a name="threading-model"></a>Modelo de threading

O contexto de operação dá suporte a threads livres, mas isso é verdadeiro no próprio contexto de operação e não se aplica a nenhuma das propriedades que ele contém.

Ao registrar um retorno de chamada de cancelamento para uma operação de serviço por meio da função [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , observe que o primeiro registro terá sucesso; a definição do retorno de chamada de cancelamento várias vezes, no entanto, falhará.

 

 




