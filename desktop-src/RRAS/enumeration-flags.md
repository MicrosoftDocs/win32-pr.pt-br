---
title: Sinalizadores de enumeração
description: Sinalizadores de enumeração
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumeração
- Sinalizadores de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916281"
---
# <a name="enumeration-flags"></a>Sinalizadores de enumeração



| Constante               | Valor      | Descrição                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_início da enumeração do RTM \_       | 0x00000000 | Enumere rotas ou destinos começando em 0/0.                                                                                                         |
| \_Enumeração RTM \_ Next        | 0x00000001 | Enumere rotas ou destinos começando no comprimento de endereço/máscara especificado (como 10/8). A enumeração continua no final da tabela de roteamento. |
| \_intervalo de enumeração de RTM \_       | 0x00000002 | Enumere rotas ou destinos na subárvore especificada especificada pelo comprimento de endereço/máscara (como 10/8).                                            |
| \_ \_ todos os \_ dests enum de RTM  | 0x00000000 | Retornar todos os destinos.                                                                                                                                  |
| todos \_ os \_ dests de enumeração do RTM \_  | 0x01000000 | Retornar somente os destinos que o cliente possui.                                                                                                      |
| \_ \_ todas as rotas de enumeração do RTM \_ | 0x00000000 | Retornar todas as rotas.                                                                                                                                        |
| \_rotas de enumeração do RTM \_ \_ | 0x00010000 | Retornar somente as rotas que o cliente possui.                                                                                                            |



 

 

 




