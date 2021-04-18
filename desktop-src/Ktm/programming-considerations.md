---
description: 'Saiba mais sobre: considerações de programação para escrever gerenciadores de recursos'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Considerações de programação para escrever gerenciadores de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760175"
---
# <a name="programming-considerations-for-writing-resource-managers"></a>Considerações de programação para escrever gerenciadores de recursos

Ao usar a API do kernel Transaction Manager para adicionar suporte de transação aos seus aplicativos, considere o seguinte:

-   Ao escrever seu próprio Gerenciador de recursos, você deve ter um bom conhecimento prático de técnicas e protocolos de gerenciamento de transações.
-   Se você não gravar os gerenciadores de recursos corretamente, poderá corromper seus próprios dados com operações de recuperação manipuladas incorretamente. Você também pode fixar a parte final do log de transações e preencher o sistema de arquivos com logs de transações.
-   Se a política de tamanho do log não estiver definida para impedir que o log aumente de tamanho, o Gerenciador de recursos não interromperá as transações. O Gerenciador de recursos deve parar de atualizar o sistema para que ele não satura os recursos do sistema de arquivos.
-   Os gerenciadores de recursos devem usar ACLs (listas de controle de acesso) para controlar o acesso aos arquivos de log; caso contrário, são possíveis ataques de negação de serviço.
-   Qualquer participante do Gerenciador de recursos ou de transação que armazena em cache os dados devem se inscrever para notificações de pré-preparação. Quando uma notificação de pré-preparação é recebida, você deve liberar todos os dados para que os gerenciadores de recursos downstream possam se inscrever antes da fase de preparação. Qualquer trabalho adicional nessa transação não deve ser armazenado em cache.
-   Não feche um identificador de inscrição enquanto a transação ainda estiver ativa; Isso fará com que a transação seja revertida.

 

 



