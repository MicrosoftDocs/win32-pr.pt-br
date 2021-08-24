---
title: Solucionando problemas de conexões de LAN sem fio
description: Nesse cenário, um usuário está tentando se conectar a uma LAN sem fio, mas não consegue se conectar. Você pode usar o netsh e o Monitor de Rede para coletar e exibir rastreamentos a fim de ajudar a determinar por que a conexão falhou.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3749b3e3a45ef68cb33b7d3658ca346dd4c6e0a8ba8ea11626573f4da6edfbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801807"
---
# <a name="troubleshooting-wireless-lan-connections"></a>Solucionando problemas de conexões de LAN sem fio

Nesse cenário, um usuário está tentando se conectar a uma LAN sem fio, mas não consegue se conectar. Você pode usar o netsh e o Monitor de Rede para coletar e exibir rastreamentos a fim de ajudar a determinar por que a conexão falhou.

Primeiro, você pode usar o netsh para iniciar um rastreamento. Digitando **netsh trace iniciar cenário = WLAN TraceFile = wlanwpp. etl** inicia o rastreamento para todos os provedores habilitados no cenário de WLAN, salvando os resultados em um arquivo chamado wlanwpp. etl. Depois de tentar se conectar à LAN sem fio, digitar **netsh trace stop** terminará e correlacionará o arquivo de rastreamento.

Em seguida, você pode abrir o arquivo wlanwpp. etl em Monitor de Rede. Os eventos são agrupados por ID de atividade no painel esquerdo.

![Solucionando problemas de conexões LAN sem fio usando o monitor de rede (1)](images/1wlan.png)

O ETL contém muitos rastreamentos de outros provedores de rede que estão habilitados. Você pode aplicar um filtro para exibir somente os eventos que são relevantes para o provedor de **\_ MicrosoftWindowsWlanAutoConfig de WLAN** .

![Solucionando problemas de conexões LAN sem fio usando o monitor de rede (2)](images/2wlan.png)

Depois que o filtro tiver sido aplicado, você poderá examinar os eventos no resumo do quadro para identificar um evento que pareça relevante. Depois de selecionar o evento, clique com o botão direito do mouse e aponte para localizar conversas e clique em netevent.

![Solucionando problemas de conexões LAN sem fio usando o monitor de rede (3)](images/3wlan.png)

Expandir os itens em uma ID de atividade no painel esquerdo permitirá que você exiba todos os outros provedores relevantes para a tentativa de conexão. Para exibir os eventos de outros provedores, todos os filtros são removidos clicando em **remover** no painel **filtro de exibição** . Os rastreamentos podem ser analisados rolando o resumo do quadro, selecionando eventos adicionais conforme necessário para coletar mais informações. Nesse caso, o painel detalhes do quadro fornece informações de que a falha ocorre devido a uma falha de troca de chave, provavelmente devido ao usuário entrando na chave de passagem incorreta.

 

 




