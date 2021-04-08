---
title: Inserindo o estado passivo
description: Inserindo o estado passivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822950"
---
# <a name="entering-the-passive-state"></a>Inserindo o estado passivo

O fechamento do objeto força um objeto incorporado ou vinculado ao estado passivo. Normalmente, ele é iniciado a partir da interface do usuário do aplicativo de servidor OLE, como quando o usuário seleciona o comando File Close. Nesse caso, o aplicativo de servidor OLE notifica o contêiner, que libera sua contagem de referência no objeto. Quando todas as referências ao objeto forem liberadas, o objeto poderá ser liberado. Quando todos os objetos forem liberados, o aplicativo do servidor OLE poderá ser encerrado com segurança.

Um aplicativo de contêiner também pode iniciar o fechamento do objeto. Para fechar um objeto, o contêiner libera sua contagem de referência depois de concluir uma operação de salvamento opcional. Você pode criar contêineres para liberar objetos quando eles estiverem sendo desativados após uma sessão de ativação in-loco, permitindo que o usuário clique fora do objeto sem perder a sessão de edição ativa.

 

 




