---
description: A classe CMsgThread Fornece suporte para um thread de trabalho para o qual as solicitações podem ser postadas de forma assíncrona, em vez de enviadas diretamente.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: Classe CMsg
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: 36d5110cbeda8cbf19c97c3f83ca1431a2cd28c5a07fa70c09e51877e0906a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016244"
---
# <a name="cmsg-class"></a>Classe CMsg

A classe [**CMsgThread**](cmsgthread.md) fornece suporte para um thread de trabalho para o qual as solicitações podem ser postadas de forma assíncrona, em vez de enviadas diretamente. A classe [**CAMThread**](camthread.md) fornece um thread de trabalho para o qual podem ser enviadas solicitações únicas. Somente um cliente pode fazer uma solicitação por vez, e o cliente é bloqueado até que o thread de trabalho tenha concluído a solicitação. Por outro lado, a classe **CMsgThread** fornece um thread de trabalho para o qual qualquer número de solicitações pode ser lançada. As solicitações (na forma de um `CMsg` objeto) são enfileiradas e executadas em ordem, de forma assíncrona. Nenhum valor de resposta ou retorno é recebido.



| Membros de dados              | Descrição                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | Sinalizador de parâmetro para o código de solicitação.                                                                                                                                               |
| lpParam                   | Dados exigidos pelo thread de trabalho como valores de parâmetro ou retorno. Esses dados não devem ser baseados em pilha, pois serão referenciados algum tempo após a conclusão da operação de enfileiramento. |
| pEvent                    | Objeto de evento que um thread de trabalho pode sinalizar para indicar a conclusão da operação.                                                                                         |
| uMsg                      | O código de solicitação que é definido pelo cliente da classe thread e compreendido pela função de thread de trabalho substituída.                                                           |
| Funções de membro          | Descrição                                                                                                                                                                       |
| [**CMsg**](cmsg-cmsg.md) | Constrói um objeto [**CMsg**](cmsg-cmsg.md) .                                                                                                                                    |



 

 

 



