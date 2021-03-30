---
title: Benefícios do armazenamento estruturado
description: O COM fornece um conjunto de serviços coletivamente chamado de armazenamento estruturado.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Strctd de armazenamento estruturado STG, benefícios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635138"
---
# <a name="benefits-of-structured-storage"></a><span data-ttu-id="57fa1-104">Benefícios do armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="57fa1-104">Benefits of Structured Storage</span></span>

<span data-ttu-id="57fa1-105">O COM fornece um conjunto de serviços coletivamente chamado de armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="57fa1-105">COM provides a set of services collectively called structured storage.</span></span> <span data-ttu-id="57fa1-106">Entre os benefícios desses serviços está a redução das penalidades de desempenho e a sobrecarga associada ao armazenamento de objetos separados em um arquivo simples.</span><span class="sxs-lookup"><span data-stu-id="57fa1-106">Among the benefits of these services is the reduction of performance penalties and overhead associated with storing separate objects in a flat file.</span></span> <span data-ttu-id="57fa1-107">Em vez de um arquivo simples, o COM armazena os objetos separados em um único arquivo estruturado, que consiste em dois elementos principais: objetos de armazenamento e objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="57fa1-107">Instead of a flat file, COM stores the separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="57fa1-108">Juntos, eles funcionam como um sistema de arquivos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="57fa1-108">Together, they function like a file system within a file.</span></span>

<span data-ttu-id="57fa1-109">O armazenamento estruturado resolve problemas de desempenho, eliminando a necessidade de reescrever totalmente um arquivo no armazenamento sempre que um novo objeto for adicionado a um arquivo composto ou um objeto existente aumentar de tamanho.</span><span class="sxs-lookup"><span data-stu-id="57fa1-109">Structured storage solves performance problems by eliminating the need to totally rewrite a file to storage whenever a new object is added to a compound file, or an existing object increases in size.</span></span> <span data-ttu-id="57fa1-110">Os novos dados são gravados no próximo local disponível no armazenamento permanente, e o objeto de armazenamento atualiza a tabela de ponteiros que ele mantém para rastrear os locais de seus objetos de armazenamento e objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="57fa1-110">The new data is written to the next available location in permanent storage, and the storage object updates the table of pointers it maintains to track the locations of its storage objects and stream objects.</span></span> <span data-ttu-id="57fa1-111">Ao mesmo tempo, o armazenamento estruturado permite que os usuários finais interajam e gerenciem um arquivo composto como se fosse um único arquivo em vez de uma hierarquia aninhada de objetos separados.</span><span class="sxs-lookup"><span data-stu-id="57fa1-111">At the same time, structured storage enables end users to interact and manage a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

<span data-ttu-id="57fa1-112">O armazenamento estruturado também tem outros benefícios:</span><span class="sxs-lookup"><span data-stu-id="57fa1-112">Structured storage also has other benefits:</span></span>

-   <span data-ttu-id="57fa1-113">**Acesso incremental**.</span><span class="sxs-lookup"><span data-stu-id="57fa1-113">**Incremental access**.</span></span> <span data-ttu-id="57fa1-114">Se um usuário precisar de acesso a um objeto em um arquivo composto, o usuário poderá carregar e salvar apenas esse objeto, em vez de todo o arquivo.</span><span class="sxs-lookup"><span data-stu-id="57fa1-114">If a user needs access to an object within a compound file, the user can load and save only that object, rather than the entire file.</span></span>
-   <span data-ttu-id="57fa1-115">**Uso múltiplo**.</span><span class="sxs-lookup"><span data-stu-id="57fa1-115">**Multiple use**.</span></span> <span data-ttu-id="57fa1-116">Mais de um usuário final ou aplicativo pode ler e gravar informações simultaneamente no mesmo arquivo composto.</span><span class="sxs-lookup"><span data-stu-id="57fa1-116">More than one end user or application can concurrently read and write information in the same compound file.</span></span>
-   <span data-ttu-id="57fa1-117">**Processamento de transações**.</span><span class="sxs-lookup"><span data-stu-id="57fa1-117">**Transaction processing**.</span></span> <span data-ttu-id="57fa1-118">Os usuários podem ler ou gravar em arquivos compostos COM no modo transacionado, em que as alterações feitas no arquivo são armazenadas em buffer e podem ser subseqüentemente confirmadas no arquivo ou invertidas.</span><span class="sxs-lookup"><span data-stu-id="57fa1-118">Users can read or write to COM compound files in transacted mode, where changes made to the file are buffered and can subsequently either be committed to the file or reversed.</span></span>
-   <span data-ttu-id="57fa1-119">**Economia de memória insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="57fa1-119">**Low-memory saves**.</span></span> <span data-ttu-id="57fa1-120">O armazenamento estruturado fornece recursos para salvar arquivos em situações de baixa memória.</span><span class="sxs-lookup"><span data-stu-id="57fa1-120">Structured storage provides facilities for saving files in low-memory situations.</span></span>

 

 




