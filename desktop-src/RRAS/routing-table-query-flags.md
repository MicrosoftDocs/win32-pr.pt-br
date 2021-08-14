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
| correspondência de RTM \_ \_ None      | 0x00000000 | Corresponde a nenhum dos critérios; todas as rotas para o destino são retornadas. |
| \_proprietário da correspondência RTM \_     | 0x00000001 | Corresponde a rotas com o mesmo proprietário.                                            |
| \_vizinho de correspondência RTM \_ | 0x00000002 | Faz a correspondência de rotas com o mesmo vizinho.                                     |
| \_correspondência RTM \_ pref      | 0x00000004 | Faz a correspondência de rotas que têm a mesma preferência.                              |
| \_NEXTHOP de correspondência RTM \_   | 0x00000008 | Faz a correspondência de rotas que têm o mesmo salto seguinte.                                |
| \_interface de correspondência RTM \_ | 0x00000010 | Faz a correspondência de rotas que estão na mesma interface.                             |
| \_correspondência RTM \_ completa      | 0x0000FFFF | Faz a correspondência de rotas com todos os critérios.                                          |
| \_melhor \_ protocolo RTM   | 0          | Retorna uma rota independentemente de qual protocolo possui.                      |
| RTM \_ este \_ protocolo   | ~0         | Retorna a melhor rota para o protocolo de chamada.                           |



 

 

 




