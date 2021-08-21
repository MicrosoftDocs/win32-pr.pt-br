---
title: Inserindo o estado passivo
description: Inserindo o estado passivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a0a3a93b0ff0bd1c16701c82f271847ee435375112a8e7a03120155928fe1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736850"
---
# <a name="entering-the-passive-state"></a>Inserindo o estado passivo

O fechamento do objeto força um objeto inserido ou vinculado ao estado passivo. Normalmente, ele é iniciado na interface do usuário do aplicativo do servidor OLE, como quando o usuário seleciona o comando Fechar Arquivo. Nesse caso, o aplicativo de servidor OLE notifica o contêiner, que libera sua contagem de referência no objeto . Quando todas as referências ao objeto foram liberadas, o objeto pode ser liberado. Quando todos os objetos foram liberados, o aplicativo de servidor OLE pode ser encerrado com segurança.

Um aplicativo de contêiner também pode iniciar o fechamento do objeto. Para fechar um objeto, o contêiner libera sua contagem de referência depois de concluir uma operação de salvar opcional. Você pode criar contêineres para liberar objetos quando eles estão sendo desativados após uma sessão de ativação in-loco, permitindo que o usuário clique fora do objeto sem perder a sessão de edição ativa.

 

 




