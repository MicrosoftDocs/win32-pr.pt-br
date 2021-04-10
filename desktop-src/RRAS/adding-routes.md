---
title: Adicionando rotas
description: Depois que um cliente tiver descoberto uma rota, o cliente poderá adicionar essa rota à tabela de roteamento chamando a função RtmAddNextHop.
ms.assetid: d72c8a84-3eac-4c5d-84af-8edc7b41f0b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276e523f78de99efb981c5ecaf2f33bd2df3d154
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292347"
---
# <a name="adding-routes"></a>Adicionando rotas

Depois que um cliente tiver descoberto uma rota, o cliente poderá adicionar essa rota à tabela de roteamento chamando a função [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop) .

Um cliente pode remover rotas da tabela de roteamento chamando a função [**RtmDeleteRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest) .

Para obter um exemplo de código que mostra como usar essas funções, consulte [Adicionar e atualizar rotas usando o RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).

 

 




