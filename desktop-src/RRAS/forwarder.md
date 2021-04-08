---
title: Encaminhador de
description: O encaminhador é o componente de modo kernel do roteador que é responsável por encaminhar dados de uma interface de roteador para as outras.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005566"
---
# <a name="forwarder"></a>Encaminhador de

O encaminhador é o componente de modo kernel do roteador que é responsável por encaminhar dados de uma interface de roteador para as outras. O encaminhador também decide se um pacote é destinado para entrega local, se ele é destinado a ser encaminhado de outra interface ou ambos.

Há dois encaminhadores em modo kernel: unicast e multicast.

O Gerenciador de roteador obtém as melhores rotas para todos os destinos do Gerenciador de tabela de roteamento. Essas rotas são passadas para o encaminhador unicast. O encaminhador unicast usa essas rotas para executar o encaminhamento real de dados unicast. Dessa maneira, o encaminhador unicast mantém um cache das melhores rotas na exibição unicast da tabela de roteamento.

O Gerenciador de grupos de multicast usa informações da exibição multicast da tabela de roteamento para adicionar entradas de encaminhamento de multicast ao encaminhador de multicast.

 

 




