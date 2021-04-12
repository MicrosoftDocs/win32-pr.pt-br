---
title: Tipos de notificações
description: Tipos de notificações
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364273"
---
# <a name="types-of-notifications"></a>Tipos de notificações

As notificações se enquadram em três grupos: documento composto, dados e exibição. Um objeto envia notificações de documento composto em resposta a ser renomeado, salvo, fechado ou, no caso de um link, tendo sua origem de link renomeada. Como você deve esperar, os objetos enviam notificações de dados em resposta a alterações em seus dados e enviamos notificações de exibição em resposta às alterações em sua apresentação. Os aplicativos de contêiner devem ser registrados separadamente para cada um desses tipos de notificação, mas todos podem ser tratados por um único coletor de consultoria.

Todos os contêineres, o manipulador de objeto e o objeto vinculado são registrados para notificações de documento composto. O contêiner típico também se registra para exibir notificações. As notificações de dados geralmente são enviadas para o objeto vinculado e o manipulador de objetos. Um contêiner de propósito especial, como um que renderiza os dados em si, pode se beneficiar do recebimento de notificações de dados em vez de exibir notificações. Por exemplo, um contêiner de gráfico incorporado com um link para uma tabela pode se registrar para notificações de dados. Como uma alteração na tabela afeta o gráfico, o recebimento de uma notificação de dados direcionaria o contêiner para obter os novos dados tabulares.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Notificações](notifications.md)
</dt> </dl>

 

 




