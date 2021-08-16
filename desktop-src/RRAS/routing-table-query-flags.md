---
title: Sinalizadores de consulta de tabela de roteamento
description: Use essas constantes para consultas de tabela de roteador.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Sinalizadores de consulta de tabela de roteamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 307dd91e9b3d248e5b2b69869ee1e7d14ae17834f7fe57d9e136da16ba3f6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787444"
---
# <a name="routing-table-query-flags"></a>Sinalizadores de consulta de tabela de roteamento

Use essas constantes para consultas de tabela de roteador.



| Constante              | Valor      | Descrição                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| RTM \_ MATCH \_ NONE      | 0x00000000 | Corresponde a nenhum dos critérios; todas as rotas para o destino são retornadas. |
| RTM \_ MATCH \_ OWNER     | 0x00000001 | Corresponde às rotas com o mesmo proprietário.                                            |
| RTM \_ MATCH \_ NEIGHBOUR | 0x00000002 | Corresponde às rotas com o mesmo vizinho.                                     |
| RTM \_ MATCH \_ PREF      | 0x00000004 | Corresponde a rotas que têm a mesma preferência.                              |
| RTM \_ MATCH \_ NEXTHOP   | 0x00000008 | Corresponde às rotas que têm o mesmo próximo salto.                                |
| INTERFACE DE \_ COMBINAÇÃO RTM \_ | 0x00000010 | Corresponde às rotas que estão na mesma interface.                             |
| RTM \_ MATCH \_ FULL      | 0x0000FFFF | Corresponde a rotas com todos os critérios.                                          |
| RTM \_ BEST \_ PROTOCOL   | 0          | Retorna uma rota, independentemente de qual protocolo a possui.                      |
| RTM \_ THIS \_ PROTOCOL   | ~0         | Retorna a melhor rota para o protocolo de chamada.                           |



 

 

 




