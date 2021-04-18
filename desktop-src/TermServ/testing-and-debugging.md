---
title: Teste e depuração
description: Há um \ 0034; Echo \ 0034; ouvinte que é implementado pelo cliente de Conexão de Área de Trabalho Remota (RDC), que está sempre presente e escutando conexões de entrada.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754163"
---
# <a name="testing-and-debugging"></a>Teste e depuração

Há um ouvinte de "eco" que é implementado pelo cliente de Conexão de Área de Trabalho Remota (RDC), que está sempre presente e escutando conexões de entrada. Ao gravar o lado do servidor de um módulo de canal virtual dinâmico (DVC), como um teste rápido, você pode abrir um ponto de extremidade chamado "ECHO". Qualquer gravação em um canal que é instanciado desse ponto de extremidade resultará no recebimento dos mesmos dados.

Você pode usar essa técnica para testar uma implementação de e/s (entrada/saída) do módulo do lado do servidor, para medir o tempo de resposta para um plug-in de cliente Conexão de Área de Trabalho Remota (RDC) ou para medir o atraso de rede para o cliente Conexão de Área de Trabalho Remota (RDC). Não há nenhuma limitação na quantidade de dados que podem ser enviados por esse canal.

 

 




