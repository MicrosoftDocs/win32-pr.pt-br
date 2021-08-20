---
title: Encaminhador de
description: O encaminhador é o componente de modo kernel do roteador que é responsável por encaminhar dados de uma interface de roteador para as outras.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5011d340b444c9d0be5b26ee5449f041bb7419fd4a52f8a983ce2b85d9b106f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674016"
---
# <a name="forwarder"></a>Encaminhador de

O encaminhador é o componente de modo kernel do roteador que é responsável por encaminhar dados de uma interface de roteador para as outras. O encaminhador também decide se um pacote é destinado para entrega local, se ele é destinado a ser encaminhado de outra interface ou ambos.

Há dois encaminhadores em modo kernel: unicast e multicast.

O Gerenciador de roteador obtém as melhores rotas para todos os destinos do Gerenciador de tabela de roteamento. Essas rotas são passadas para o encaminhador unicast. O encaminhador unicast usa essas rotas para executar o encaminhamento real de dados unicast. Dessa maneira, o encaminhador unicast mantém um cache das melhores rotas na exibição unicast da tabela de roteamento.

O Gerenciador de grupos de multicast usa informações da exibição multicast da tabela de roteamento para adicionar entradas de encaminhamento de multicast ao encaminhador de multicast.

 

 




