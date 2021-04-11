---
description: Terminologia usada para descrever o NTFS Transacional (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glossário do TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171500"
---
# <a name="txf-glossary"></a><span data-ttu-id="8bb30-103">Glossário do TxF</span><span class="sxs-lookup"><span data-stu-id="8bb30-103">TxF Glossary</span></span>

<dl> <dt>

<span data-ttu-id="8bb30-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**ininterrupta**</span><span class="sxs-lookup"><span data-stu-id="8bb30-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**availability**</span></span>
</dt> <dd>

<span data-ttu-id="8bb30-105">Disponibilidade significa que um Gerenciador de recursos anulará as transações mesmo que isso interrompa a consistência para que o sistema possa continuar a fazer um novo trabalho.</span><span class="sxs-lookup"><span data-stu-id="8bb30-105">Availability means that a resource manager will abort transactions even if that would break consistency so that the system can continue to do new work.</span></span> <span data-ttu-id="8bb30-106">O Gerenciador de recursos padrão força a disponibilidade no volume do sistema.</span><span class="sxs-lookup"><span data-stu-id="8bb30-106">The default resource manager forces availability on the system volume.</span></span> <span data-ttu-id="8bb30-107">Por exemplo, se o log de transações estiver cheio, o novo espaço de log de transações não poderá ser adicionado e uma transação mais antiga que seria anulada exigirá que um resultado seja entregue de um Gerenciador de recursos superior para que uma transação distribuída seja concluída, o Gerenciador de recursos não aguardará o Gerenciador de transações superior e anulará essa transação, mesmo que possa interromper a consistência.</span><span class="sxs-lookup"><span data-stu-id="8bb30-107">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will not wait for the superior transaction manager and abort that transaction even though that potentially breaks consistency.</span></span>

</dd> <dt>

<span data-ttu-id="8bb30-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**verificação**</span><span class="sxs-lookup"><span data-stu-id="8bb30-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**consistency**</span></span>
</dt> <dd>

<span data-ttu-id="8bb30-109">Consistência significa que um Gerenciador de recursos falhará em novas transações se não puder fazer o progresso.</span><span class="sxs-lookup"><span data-stu-id="8bb30-109">Consistency means that a resource manager will fail new transactions if it cannot make forward progress.</span></span> <span data-ttu-id="8bb30-110">Por exemplo, se o log de transações estiver cheio, o novo espaço de log de transações não poderá ser adicionado e uma transação mais antiga que seria anulada exigirá a entrega de um resultado de um Gerenciador de recursos superior para que uma transação distribuída seja concluída, o Gerenciador de recursos aguardará esse resultado.</span><span class="sxs-lookup"><span data-stu-id="8bb30-110">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will wait for that outcome.</span></span>

</dd> <dt>

<span data-ttu-id="8bb30-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversão**</span><span class="sxs-lookup"><span data-stu-id="8bb30-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**</span></span>
</dt> <dd>

<span data-ttu-id="8bb30-112">Um miniversão é uma versão de um arquivo que um gravador transacionado cria durante uma transação.</span><span class="sxs-lookup"><span data-stu-id="8bb30-112">A miniversion is a version of a file that a transacted writer creates during a transaction.</span></span> <span data-ttu-id="8bb30-113">O miniversão pode ser aberto posteriormente na transação com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8bb30-113">The miniversion can be opened later in the transaction with read-only access.</span></span>

</dd> <dt>

<span data-ttu-id="8bb30-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**leitor transacionado**</span><span class="sxs-lookup"><span data-stu-id="8bb30-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transacted reader**</span></span>
</dt> <dd>

<span data-ttu-id="8bb30-115">Um leitor transacionado é um identificador de arquivo transacionado aberto com qualquer permissão que faça parte do acesso de leitura genérico, mas que não faz parte do acesso de gravação genérico.</span><span class="sxs-lookup"><span data-stu-id="8bb30-115">A transacted reader is a transacted file handle opened with any permission that is a part of generic read access, but is not part of generic write access.</span></span>

</dd> <dt>

<span data-ttu-id="8bb30-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**gravador transacionado**</span><span class="sxs-lookup"><span data-stu-id="8bb30-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**transacted writer**</span></span>
</dt> <dd>

<span data-ttu-id="8bb30-117">Um gravador transacionado é um identificador de arquivo transacionado aberto com qualquer permissão que não faça parte do acesso de leitura genérico, mas que faz parte do acesso de gravação genérico.</span><span class="sxs-lookup"><span data-stu-id="8bb30-117">A transacted writer is a transacted file handle opened with any permission that is not part of generic read access, but is part of generic write access.</span></span>

</dd> </dl>

 

 



