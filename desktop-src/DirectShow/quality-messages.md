---
description: Mensagens de qualidade
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Mensagens de qualidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500369"
---
# <a name="quality-messages"></a>Mensagens de qualidade

As mensagens de qualidade são definidas com a estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) . Essa estrutura contém os seguintes membros:

-   **Tipo:** Definido pela enumeração [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) ; Famine, indicando que o filtro está recebendo poucos dados ou inundações, indicando que o filtro está recebendo muitos dados.
-   **Proporção:** O ajuste solicitado na taxa de dados, de uma linha de base de 1000. Por exemplo, 750 indica 75% e 1500 indica 150%.
-   **Tarde:** Tempo de referência que indica o atraso do exemplo mais recente. O valor será negativo se o exemplo chegou cedo.
-   **Carimbo de data/hora:** O carimbo de data/hora no exemplo mais recente.

Por exemplo, suponha que um exemplo com um carimbo de data/hora de 240 milissegundos (MS) atinja o renderizador em 280 MS, fluxo de tempo. O processador cria uma mensagem de qualidade do tipo Famine. O exemplo chegou 40 MS atrasado, portanto, o membro **atrasado** é 400000. (Todos os tempos de referência estão em unidades de 100 nanossegundos.) O membro do **carimbo de data/hora** é 2,4 milhões.

Para o membro de **proporção** , o renderizador pode usar uma média em execução para calcular o valor. Talvez as amostras cheguem ao tempo, e este exemplo é uma anomalia. Nesse caso, o renderizador pode solicitar apenas uma pequena correção. Por outro lado, se os exemplos forem consistentemente atrasados, o renderizador poderá solicitar uma correção maior.

O controle de qualidade é manipulado por meio da interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) . Ele contém dois métodos.

-   [**Notificar**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): envia uma mensagem de qualidade.
-   [**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): especifica um Gerenciador de qualidade personalizado.

Um objeto que implementa o **IQualityControl** recebe mensagens de qualidade por meio de seu método **Notify** . Ele pode tratar a mensagem ou passar a mensagem para outro objeto. Se o aplicativo chamar o método **SetSink** do objeto, o objeto deverá delegar o controle de qualidade para o Gerenciador de qualidade especificado.

 

 



