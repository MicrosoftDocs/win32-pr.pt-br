---
title: Como a arquitetura do Gerenciador de Tabelas de Roteamento se encaixa
description: A ilustração a seguir mostra a relação entre os diferentes componentes de um roteador.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1637eed71a89a6de4fa7dad6a4fea4a5918366f69ee05a490824699605a117a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791344"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a>Como a arquitetura do Gerenciador de Tabelas de Roteamento se encaixa

A ilustração a seguir mostra a relação entre os diferentes componentes de um roteador.

![relação entre componentes do roteador](images/rtsrvarch.png)

Quando o roteador é inicializado, o serviço de gerenciador de roteador é iniciado, bem como um ou mais protocolos de roteamento. Os protocolos de roteamento são associados às várias interfaces no roteador. O gerenciador de roteador também inicia o gerenciador de tabela de roteamento.

A ilustração a seguir mostra a relação entre clientes e os diferentes componentes do gerenciador de tabela de roteamento.

![relação entre clientes e componentes do gerenciador de tabela de roteamento](images/rtmentrel.png)

O gerenciador de roteador inicia uma ou mais instâncias do gerenciador de tabela de roteamento. Quando várias instâncias do gerenciador de tabela de roteamento são iniciadas, o roteador foi configurado para atuar como um ou mais roteadores virtuais. Cada instância do gerenciador de tabela de roteamento possui uma ou mais interfaces; cada interface só pode ser de propriedade de uma instância do gerenciador de tabela de roteamento.

Cada instância do gerenciador de tabela de roteamento é independente das outras; nenhuma informação é trocada entre as instâncias.

Cada instância do gerenciador de tabela de roteamento contém uma ou mais tabelas de roteamento. Cada tabela de roteamento está associada a uma família de endereços.

Cada tabela de roteamento contém uma ou mais exibições. Neste exemplo, a tabela de roteamento é mostrada com uma exibição unicast e multicast. Cada exibição é um subconjunto da tabela de roteamento.

A ilustração a seguir mostra a relação entre clientes e várias instâncias do gerenciador de tabelas de roteamento, tabelas de roteamento e exibições.

![clientes de relacionamento, gerenciador de tabela de roteamento, tabelas de roteamento, exibições](images/multrtabrel.png)

Uma instância do cliente pode se registrar várias vezes com uma instância do gerenciador de tabela de roteamento – uma vez por família de endereços. Um cliente pode se registrar em cada instância do gerenciador de tabela de roteamento.

A ilustração a seguir mostra como as entradas da tabela de roteamento estão relacionadas. Para obter mais informações sobre entradas de tabela de roteamento, consulte [Entradas de tabela de roteamento](routing-table-entries.md).

![relação entre entradas da tabela de roteamento](images/nexthop.png)

A tabela de roteamento contém destinos. Cada destino está relacionado a uma ou mais rotas. Cada rota tem zero, um ou mais ponteiros para os próximos saltos associados à rota. Cada ponteiro refere-se ao próximo salto real na lista de próximos saltos. Cada cliente que se registra com o gerenciador de tabela de roteamento cria uma lista de próximos saltos que o cliente possui.

As rotas só podem conter ponteiros para a lista de próximo salto associada ao cliente que possui a rota.

 

 




