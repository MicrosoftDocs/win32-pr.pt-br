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
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103642994"
---
# <a name="operation-context-lifetime-and-threading"></a>Tempo de vida do contexto de operação e threading

O tempo de vida do contexto de operação, representado por um identificador de [ \_ \_ contexto de operação WS](ws-operation-context.md) , determina o tempo de vida das propriedades que ele contém. Portanto, um contexto só deve ser usado dentro do tempo de vida da [operação de serviço](service-operation.md) ou do retorno de chamada para o qual ele foi fornecido. O tempo de vida de uma chamada síncrona é a execução da própria função. Para uma chamada assíncrona, o tempo de vida termina quando a chamada assíncrona é concluída. O modelo de serviço não fornece nenhuma garantia sobre o contexto quando a chamada é concluída. O comportamento de depender do contexto de operação ou de qualquer uma de suas propriedades além de seu tempo de vida é indefinido.


Consulte também o exemplo de calculadora baseado em sessão, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).

## <a name="threading-model"></a>Modelo de threading

O contexto de operação dá suporte a threads livres, mas isso é verdadeiro no próprio contexto de operação e não se aplica a nenhuma das propriedades que ele contém.

Ao registrar um retorno de chamada de cancelamento para uma operação de serviço por meio da função [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , observe que o primeiro registro terá sucesso; a definição do retorno de chamada de cancelamento várias vezes, no entanto, falhará.

 

 




