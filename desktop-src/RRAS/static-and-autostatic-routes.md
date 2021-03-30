---
title: Rotas estáticas e auto-estáticas
description: Normalmente, as rotas para redes remotas são obtidas dinamicamente por meio de protocolos de roteamento.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916553"
---
# <a name="static-and-autostatic-routes"></a>Rotas estáticas e auto-estáticas

Normalmente, as rotas para redes remotas são obtidas dinamicamente por meio de protocolos de roteamento. No entanto, o administrador também pode *propagar* a tabela de roteamento fornecendo rotas manualmente. Essas rotas são conhecidas como *estáticas*. Uma rota estática é associada a uma interface que representa a rede remota. Ao contrário das rotas dinâmicas, as rotas estáticas são retidas mesmo se o roteador for reiniciado ou a interface estiver desabilitada.

Uma rota *autoestática* é obtida por meio de um protocolo de roteamento, mas uma vez obtida se comporta como uma rota estática. O processo para obter rotas autoestáticas é o seguinte: o Gerenciador de roteador IP ou IPX emite uma solicitação que um protocolo de roteamento atualiza as informações de roteamento para uma interface específica. Os resultados da atualização são então convertidos em rotas estáticas. Observe que apenas determinados protocolos de roteamento dão suporte a solicitações para atualizações de rota autoestática.

 

 




