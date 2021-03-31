---
title: Solucionando problemas de conexões com a Internet
description: Nesse cenário, um usuário está tentando navegar até www.msn.com usando o protocolo HTTPS, mas não consegue se conectar. Você pode usar o netsh e o Monitor de Rede para coletar e exibir rastreamentos a fim de ajudar a determinar por que a conexão falhou.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822516"
---
# <a name="troubleshooting-internet-connections"></a>Solucionando problemas de conexões com a Internet

Nesse cenário, um usuário está tentando navegar até www.msn.com usando o protocolo HTTPS, mas não consegue se conectar. Você pode usar o netsh e o Monitor de Rede para coletar e exibir rastreamentos a fim de ajudar a determinar por que a conexão falhou.

Primeiro, você pode usar o netsh para iniciar um rastreamento. Digitando **netsh trace iniciar cenário = InternetClient TraceFile = MSN. etl** inicia o rastreamento para todos os provedores habilitados no cenário InternetClient, salvando os resultados em um arquivo chamado MSN. etl. Depois de usar um navegador da Web para tentar acessar o www.msn.com, digitar **netsh trace stop** termina e correlaciona o arquivo de rastreamento.

Em seguida, você pode abrir o arquivo MSN. etl em Monitor de Rede. Os eventos são agrupados por ID de atividade no painel esquerdo. Usando a descrição do filtro **. Contains ("MSN")** mostrará somente os eventos que incluem a cadeia de caracteres "MSN" em sua descrição de protocolo.

![Solucionando problemas de conexões de Internet usando o monitor de rede (1)](images/internetclient1.png)

Em seguida, você pode examinar os eventos no resumo do quadro para identificar um evento que é relevante. Depois de selecionar o evento, clique com o botão direito do mouse e aponte para localizar conversas e clique em UTEvent para selecionar a conversa no nível de UTEvent.

![Solucionando problemas de conexões de Internet usando o monitor de rede (2)](images/internetclient2.png)

A atividade normalizada associada no painel esquerdo é realçada, nesse caso, UTEvent ActivityId 397.

![Solucionando problemas de conexões de Internet usando o monitor de rede (3)](images/internetclient3.png)

Usando Monitor de Rede para exibir e filtrar as informações de rastreamento, o número de eventos a serem examinados foi reduzido de 1989 para 96.

 

 




