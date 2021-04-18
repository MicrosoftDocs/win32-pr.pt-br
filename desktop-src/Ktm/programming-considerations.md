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
# <a name="programming-considerations-for-writing-resource-managers"></a><span data-ttu-id="1db04-103">Considerações de programação para escrever gerenciadores de recursos</span><span class="sxs-lookup"><span data-stu-id="1db04-103">Programming Considerations For Writing Resource Managers</span></span>

<span data-ttu-id="1db04-104">Ao usar a API do kernel Transaction Manager para adicionar suporte de transação aos seus aplicativos, considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1db04-104">When using the Kernel Transaction Manager API to add transaction support to your applications, consider the following:</span></span>

-   <span data-ttu-id="1db04-105">Ao escrever seu próprio Gerenciador de recursos, você deve ter um bom conhecimento prático de técnicas e protocolos de gerenciamento de transações.</span><span class="sxs-lookup"><span data-stu-id="1db04-105">When you are writing your own resource manager, you should have a good, working knowledge of transaction management techniques and protocols.</span></span>
-   <span data-ttu-id="1db04-106">Se você não gravar os gerenciadores de recursos corretamente, poderá corromper seus próprios dados com operações de recuperação manipuladas incorretamente.</span><span class="sxs-lookup"><span data-stu-id="1db04-106">If you do not write resource managers correctly, you can corrupt your own data with improperly handled recovery operations.</span></span> <span data-ttu-id="1db04-107">Você também pode fixar a parte final do log de transações e preencher o sistema de arquivos com logs de transações.</span><span class="sxs-lookup"><span data-stu-id="1db04-107">You can also pin the tail of transaction log and fill up your file system with transaction logs.</span></span>
-   <span data-ttu-id="1db04-108">Se a política de tamanho do log não estiver definida para impedir que o log aumente de tamanho, o Gerenciador de recursos não interromperá as transações.</span><span class="sxs-lookup"><span data-stu-id="1db04-108">If your log size policy is not set to prevent the log from increasing in size, your resource manager will not stop transactions.</span></span> <span data-ttu-id="1db04-109">O Gerenciador de recursos deve parar de atualizar o sistema para que ele não satura os recursos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1db04-109">Your resource manager must stop updating the system so it does not overrun the file system resources.</span></span>
-   <span data-ttu-id="1db04-110">Os gerenciadores de recursos devem usar ACLs (listas de controle de acesso) para controlar o acesso aos arquivos de log; caso contrário, são possíveis ataques de negação de serviço.</span><span class="sxs-lookup"><span data-stu-id="1db04-110">Resource managers should use access control lists (ACLs) to control access to the log files; otherwise, denial of service attacks are possible.</span></span>
-   <span data-ttu-id="1db04-111">Qualquer participante do Gerenciador de recursos ou de transação que armazena em cache os dados devem se inscrever para notificações de pré-preparação.</span><span class="sxs-lookup"><span data-stu-id="1db04-111">Any resource manager or transaction participant that caches data must enlist for pre-prepare notifications.</span></span> <span data-ttu-id="1db04-112">Quando uma notificação de pré-preparação é recebida, você deve liberar todos os dados para que os gerenciadores de recursos downstream possam se inscrever antes da fase de preparação.</span><span class="sxs-lookup"><span data-stu-id="1db04-112">When a pre-prepare notification is received, you must flush all your data, so that any downstream resource managers can enlist before the prepare phase.</span></span> <span data-ttu-id="1db04-113">Qualquer trabalho adicional nessa transação não deve ser armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="1db04-113">Any further work in that transaction must not be cached.</span></span>
-   <span data-ttu-id="1db04-114">Não feche um identificador de inscrição enquanto a transação ainda estiver ativa; Isso fará com que a transação seja revertida.</span><span class="sxs-lookup"><span data-stu-id="1db04-114">Do not close an enlistment handle while the transaction is still active; this will cause the transaction to be rolled back.</span></span>

 

 



