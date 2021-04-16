---
title: Delegação e representação
description: Em cenários de cliente/servidor, é comum que um servidor Chame outro servidor para realizar alguma tarefa em nome de um cliente. A situação em que um servidor recebe a autoridade para agir em nome de um cliente é chamada de delegação.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104566828"
---
# <a name="delegation-and-impersonation"></a>Delegação e representação

Em cenários de cliente/servidor, é comum que um servidor Chame outro servidor para realizar alguma tarefa em nome de um cliente. A situação em que um servidor recebe a autoridade para agir em nome de um cliente é chamada de *delegação*.

Do ponto de vista da segurança, dois problemas surgem em relação à delegação:

-   O que o servidor deve ter permissão para fazer ao agir em nome do cliente?
-   Qual identidade é apresentada pelo servidor quando ele chama outros servidores em nome de um cliente?

Para lidar com esses problemas, o COM fornece a funcionalidade a seguir. O cliente pode definir um *nível de representação* que determina até que ponto o servidor será capaz de atuar como o cliente. Se o cliente conceder autoridade suficiente ao servidor, o servidor poderá *representar* (fingir ser) o cliente. Ao representar o cliente, o servidor recebe acesso apenas a esses objetos ou recursos que o cliente tem permissão para usar. O servidor, agindo como um cliente, também pode habilitar o *encobrimento* para mascarar sua própria identidade e projetar a identidade do cliente em chamadas para outros componentes com.

![Diagrama que mostra como o servidor que atua como o cliente pode habilitar o encobrimento.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Considere o cenário ilustrado pela figura anterior, em que a e B são processos em um computador diferente de C. processar uma chamada B e B chama C. o cliente A define o nível de representação. B define o recurso de encobrimento. Se um definir um nível de representação que permita A representação, B poderá representar um ao chamar C em nome. A identidade que é apresentada para o processo C será A identidade de uma identidade ou de B, dependendo se o encobrimento foi habilitado por B. Se o encobrimento estiver habilitado, a identidade apresentada ao processo C será a de um. Se o encobrimento não estiver habilitado, a identidade de B será apresentada a C.

Para mais informações, consulte os seguintes tópicos:

-   [Representação](impersonation.md)
-   [Níveis de representação](impersonation-levels.md)
-   [Encobrimento](cloaking.md)

 

 




