---
title: Confiabilidade das informações de erro estendidas
description: As informações de erro estendidas não são confiáveis.
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20edfbaa68f2a9ce80893f4f47bba33ec5ce595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634843"
---
# <a name="reliability-of-extended-error-information"></a>Confiabilidade das informações de erro estendidas

As informações de erro estendidas não são confiáveis. As informações de erro estendidas não podem ser usadas para criar lógica de código. É apropriado verificar a presença de informações de erro estendidas e, se houver, despejar, salvar ou registrar essas informações. Mas não confie nas informações ou no seu conteúdo.

Os motivos a seguir explicam por que as informações de erro estendidas não são confiáveis:

-   A sequência e o conteúdo dos registros de erro estendidos dependem da arquitetura interna do sistema, que está sujeita a alterações. Uma determinada operação pode passar por NPFS em sistemas atuais, mas amanhã poderia passar pelo TCP. Esses diferentes componentes geram códigos de erro muito diferentes, e as verificações de código, portanto, são inerentemente não confiáveis e não são recomendadas.
-   A propagação de informações de erro estendidas pode ser desabilitada, conforme explicado anteriormente. Se o código de detecção for incluído, o aplicativo provavelmente deixará de funcionar em determinados ambientes.
-   A propagação de informações de erro estendidas é executada de maneira melhor. A propagação ou geração de informações de erro estendidas pode falhar se não houver memória suficiente no computador para processar ou propagar a cadeia. Nessas circunstâncias, a cadeia será descartada. Alguns protocolos têm comprimentos limitados para pacotes de falha, pois normalmente não incluem muitas informações. Se o comprimento da cadeia exceder o comprimento permitido do pacote, o tempo de execução do RPC começará a remover as informações da cadeia em uma tentativa de ajustar a cadeia ao pacote. O tempo de execução primeiro descarta os registros, começando do registro penúltima, indo para trás, até que somente os registros First e Last permaneçam. Se a cadeia ainda não couber em um pacote, o tempo de execução descartará os parâmetros da cadeia de caracteres e os nomes dos computadores. Se um parâmetro de cadeia de caracteres for descartado, o tipo do parâmetro será definido como nenhum. Se um registro for descartado, o sinalizador EEInfoNextRecordsMissing será definido no próximo registro e EEInfoPreviousRecordsMissing será definido no registro anterior.

 

 




