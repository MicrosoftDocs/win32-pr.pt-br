---
title: Confiabilidade de informações de erro estendidas
description: As informações de erro estendidas não são confiáveis.
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2cb85e31f993719e5f0a555a63dd83a80064ed76df1ebda43cf03f994dab9fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926834"
---
# <a name="reliability-of-extended-error-information"></a>Confiabilidade de informações de erro estendidas

As informações de erro estendidas não são confiáveis. Informações de erro estendidas não podem ser usadas para criar lógica de código. É apropriado verificar a presença de informações de erro estendidas e, se houver, despejar, salvar ou registrar essas informações. Mas não dependa das informações ou de seu conteúdo.

Os seguintes motivos explicam por que as informações de erro estendidas não são confiáveis:

-   A sequência e o conteúdo dos registros de erro estendidos dependem da arquitetura interna do sistema, que está sujeita a alterações. Uma determinada operação pode passar por NPFS em sistemas atuais, mas amanhã pode passar pelo TCP. Esses diferentes componentes geram códigos de erro muito diferentes e as verificações de código, portanto, não são inerentemente confiáveis e não são recomendadas.
-   A propagação de informações de erro estendidas pode ser desabilitada, conforme explicado anteriormente. Se o código de detecção estiver incluído, o aplicativo provavelmente interromperá o trabalho em determinados ambientes.
-   A propagação de informações de erro estendidas é executada da melhor maneira possível. A propagação ou a geração de informações de erro estendidas poderão falhar se não houver memória suficiente no computador para processar ou propagar a cadeia. Nessas circunstâncias, a cadeia será descartado. Alguns protocolos têm comprimentos limitados para pacotes de falha, pois geralmente não incluem muitas informações. Se o comprimento da cadeia exceder o comprimento permitido do pacote, o tempo de executar RPC começará a soltar informações da cadeia em uma tentativa de ajustar a cadeia ao pacote. O tempo de run time primeiro descarta registros, começando no penúltima gravação, indo para trás, até que apenas o primeiro e o último registros permaneçam. Se a cadeia ainda não se ajustar a um pacote, o tempo de executar descarta parâmetros de cadeia de caracteres e nomes de computador. Se um parâmetro de cadeia de caracteres for descartado, o tipo do parâmetro será definido como nenhum. Se um registro for descartado, o sinalizador EEInfoNextRecordsMissing será definido no próximo registro e EEInfoPreviousRecordsMissing será definido no registro anterior.

 

 




