---
description: Clicar em executar especialistas na janela especialistas da interface do usuário do Monitor de Rede inicia os especialistas selecionados para o arquivo de captura e chama a função executar. Quando iniciado, o especialista analisa o arquivo de captura usando várias funções de quadro de especialista.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Iniciar e executar especialistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc85ba39c393ac253ca688a826bc77747c8d17bea29b089250a63f6f833066c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555308"
---
# <a name="starting-and-running-experts"></a>Iniciar e executar especialistas

Clicar em **executar especialistas** na janela especialistas da interface do usuário do monitor de rede inicia os especialistas selecionados para o arquivo de captura e chama a função [**executar**](run.md) . Quando iniciado, o especialista analisa o arquivo de captura usando várias funções de quadro de especialista.

A função [**ExpertIndicateStatus**](expertindicatestatus.md) fornece informações de status do especialista. Quando você executa um especialista com Monitor de Rede, a janela de exibição de status de especialista exibe informações de status atualizadas periodicamente (de 0 a 100 por cento de conclusão).

![janela de exibição de status de especialista](images/exview.png)

O especialista está ativo até que os dados concluam sua passagem por meio do arquivo de captura. Quando a passagem for concluída, uma janela de Visualizador de Eventos será exibida. As informações nessa janela dependem do tipo de especialista que analisou os dados. A ilustração a seguir mostra uma exibição de especialista em distribuição de propriedade, que resume os dados de quadro analisados pelo especialista.

![exibição do especialista de distribuição de propriedade](images/exview1.png)

Um segundo relatório (não mostrado), resume os resultados do especialista de retransmissão do protocolo TCP.

Você também pode:

-   Crie uma entrada para uma página de referência de evento (ERP) que aconselha o usuário de condições ou problemas detectados (conforme mostrado na janela de análise).
-   Crie entradas para correções sugeridas ou dados explicativos que forneçam informações adicionais (conforme mostrado na janela de resolução).

Depois que o especialista concluir sua tarefa, Monitor de Rede removerá o especialista da memória ativa. Os especialistas devem usar as funções de memória protegida incluídas no SDK (Software Development Kit) da plataforma. essas funções limpam a memória se os especialistas falharem durante o tempo de execução.

 

 



