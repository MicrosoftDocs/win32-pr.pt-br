---
description: O conteúdo dos anúncios do roteador IPv6 é automaticamente derivado das rotas publicadas na tabela de roteamento. As rotas não publicadas são usadas para roteamento, mas são ignoradas durante a construção de anúncios de roteador.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Anúncios de roteador IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786151"
---
# <a name="ipv6-router-advertisements"></a>Anúncios de roteador IPv6

O conteúdo dos anúncios do roteador IPv6 é automaticamente derivado das rotas publicadas na tabela de roteamento. As rotas não publicadas são usadas para roteamento, mas são ignoradas durante a construção de anúncios de roteador.

Os anúncios de roteador para IPv6 sempre contêm uma opção de endereço de camada de link de origem e uma opção de MTU. O valor da opção de MTU é obtido da MTU de link atual da interface de envio. Esse valor pode ser alterado com o comando IPv6 IFC MTU.

O anúncio de roteador tem apenas um tempo de vida de roteador diferente de zero se houver uma rota padrão publicada. Uma rota padrão é uma rota para o prefixo de comprimento zero.

As rotas no link publicadas resultam em opções de informações de prefixo em anúncios de roteador. Se o prefixo on-link tiver 64 bits, a opção informações de prefixo terá o L e um conjunto de bits e os hosts que o receberão configurarão endereços.

Uma interface que envia anúncios de roteador também configurará automaticamente os endereços para si mesmo, com base nas opções de informações de prefixo que ele envia.

É recomendável um tempo de vida de não envelhecimento finito em todas as rotas publicadas (por exemplo, 30 minutos). Se você decidir cancelar uma rota, poderá alterar a rota para ter um tempo de vida de envelhecimento. A rota dará vida ao curso de vários anúncios de roteador e desaparecerá do roteador e de quaisquer hosts que recebam os anúncios do roteador.

As rotas que os hosts encontram por meio da idade de anúncios do roteador e não são publicadas. Os endereços autoconfigurados da idade de anúncios do roteador também.

 

 



