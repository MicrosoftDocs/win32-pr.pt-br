---
title: Rotas estáticas e estáticas
description: Normalmente, as rotas para redes remotas são obtidas dinamicamente por meio de protocolos de roteamento.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0206190c86c75e4e50ce390cf3f084db956671de6efebe21022151879362ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127826"
---
# <a name="static-and-autostatic-routes"></a>Rotas estáticas e estáticas

Normalmente, as rotas para redes remotas são obtidas dinamicamente por meio de protocolos de roteamento. No entanto, o administrador também pode *semear a* tabela de roteamento fornecendo rotas manualmente. Essas rotas são conhecidas como *estáticas.* Uma rota estática é associada a uma interface que representa a rede remota. Ao contrário das rotas dinâmicas, as rotas estáticas são mantidas mesmo que o roteador seja reiniciado ou a interface seja desabilitada.

Uma *rota autoestática* é obtida por meio de um protocolo de roteamento, mas uma vez obtida se comporta como uma rota estática. O processo para obter rotas autoestáticas é o seguinte: o gerenciador de roteador IPX ou IP emite uma solicitação para que um protocolo de roteamento atualize as informações de roteamento para uma interface específica. Os resultados da atualização são convertidos em rotas estáticas. Observe que apenas determinados protocolos de roteamento suportam solicitações de atualizações de rota autoestáticas.

 

 




