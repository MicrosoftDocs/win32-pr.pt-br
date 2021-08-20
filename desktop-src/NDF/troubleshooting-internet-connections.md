---
title: Solução de problemas de conexões com a Internet
description: Nesse cenário, um usuário está tentando navegar até o www.msn.com usando o protocolo https, mas não consegue se conectar. Você pode usar Netsh e Monitor de Rede coletar e exibir rastreamentos para ajudar a determinar por que a conexão falhou.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fadeefe0413a5a6be5d3ec7f5676ef346e21bc1f4b9e4c3cca026b54d761784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133381"
---
# <a name="troubleshooting-internet-connections"></a>Solução de problemas de conexões com a Internet

Nesse cenário, um usuário está tentando navegar até o www.msn.com usando o protocolo https, mas não consegue se conectar. Você pode usar Netsh e Monitor de Rede coletar e exibir rastreamentos para ajudar a determinar por que a conexão falhou.

Primeiro, você pode usar netsh para iniciar um rastreamento. Digitando cenário de início de rastreamento **netsh = InternetClient tracefile=msn.etl** inicia o rastreamento para todos os provedores habilitados no cenário InternetClient, salvando os resultados em um arquivo chamado msn.etl. Depois de usar um navegador da Web para tentar alcançar www.msn.com, digitar **netsh trace stop** termina e correlaciona o arquivo de rastreamento.

Em seguida, você pode abrir o arquivo msn.etl no Monitor de Rede. Os eventos são agrupados por ID de atividade no painel esquerdo. O uso do **filtro description.contains("msn")** mostrará apenas os eventos que incluem a cadeia de caracteres "msn" na descrição do protocolo.

![solução de problemas de conexões com a Internet usando o monitor de rede (1)](images/internetclient1.png)

Em seguida, você pode revisar os eventos no resumo do quadro para identificar um evento que parece relevante. Depois de selecionar o evento, clique com o botão direito do mouse e aponte para Encontrar Conversas e clique em UTEvent para selecionar a conversa no nível UTEvent.

![solução de problemas de conexões com a Internet usando o monitor de rede (2)](images/internetclient2.png)

A atividade normalizada associada no painel esquerdo é realçada, nesse caso, UTEvent ActivityID 397.

![solução de problemas de conexões com a Internet usando o monitor de rede (3)](images/internetclient3.png)

Usando o Monitor de Rede para exibir e filtrar as informações de rastreamento, o número de eventos a examinar foi reduzido de 1989 para 96.

 

 




