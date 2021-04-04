---
title: Sinalizadores de consulta de tabela de roteamento
description: Use essas constantes para consultas de tabela de roteador.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Sinalizadores de consulta de tabela de roteamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823073"
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



 

 

 




