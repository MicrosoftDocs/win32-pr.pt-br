---
description: Um objeto consiste em um cabeçalho padrão e atributos específicos de objeto. Como todos os objetos têm a mesma estrutura, há um Gerenciador de objetos único no Windows que mantém todos os objetos.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Gerenciador de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922224"
---
# <a name="object-manager"></a><span data-ttu-id="05e42-104">Gerenciador de objetos</span><span class="sxs-lookup"><span data-stu-id="05e42-104">Object Manager</span></span>

<span data-ttu-id="05e42-105">Um objeto consiste em um cabeçalho padrão e atributos específicos de objeto.</span><span class="sxs-lookup"><span data-stu-id="05e42-105">An object consists of a standard header and object-specific attributes.</span></span> <span data-ttu-id="05e42-106">Como todos os objetos têm a mesma estrutura, há um Gerenciador de objetos único no Windows que mantém todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="05e42-106">Because all objects have the same structure, there is a single object manager in Windows that maintains all objects.</span></span>

<span data-ttu-id="05e42-107">O cabeçalho do objeto inclui itens como o nome do objeto, para que outros processos possam referenciar o objeto por nome e um descritor de segurança, para que o Gerenciador de objetos possa controlar quais processos acessam o recurso do sistema.</span><span class="sxs-lookup"><span data-stu-id="05e42-107">The object header includes items such as the object name, so that other processes can reference the object by name, and a security descriptor, so that the object manager can control which processes access the system resource.</span></span>

<span data-ttu-id="05e42-108">As tarefas que o Gerenciador de objetos executa incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="05e42-108">The tasks that the object manager performs include the following:</span></span>

-   <span data-ttu-id="05e42-109">Criando objetos</span><span class="sxs-lookup"><span data-stu-id="05e42-109">Creating objects</span></span>
-   <span data-ttu-id="05e42-110">Verificando se um processo tem o direito de usar o objeto</span><span class="sxs-lookup"><span data-stu-id="05e42-110">Verifying that a process has the right to use the object</span></span>
-   <span data-ttu-id="05e42-111">Criando identificadores de objeto e retornando-os para o chamador</span><span class="sxs-lookup"><span data-stu-id="05e42-111">Creating object handles and returning them to the caller</span></span>
-   <span data-ttu-id="05e42-112">Mantendo cotas de recursos</span><span class="sxs-lookup"><span data-stu-id="05e42-112">Maintaining resource quotas</span></span>
-   <span data-ttu-id="05e42-113">Criando identificadores duplicados</span><span class="sxs-lookup"><span data-stu-id="05e42-113">Creating duplicate handles</span></span>
-   <span data-ttu-id="05e42-114">Identificadores de fechamento para objetos</span><span class="sxs-lookup"><span data-stu-id="05e42-114">Closing handles to objects</span></span>

 

 



