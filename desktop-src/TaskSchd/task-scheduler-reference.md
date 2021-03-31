---
title: Referência de Agendador de Tarefas
description: Esta seção descreve as APIs, os objetos de script e o esquema XML fornecidos pelo Agendador de Tarefas.
ms.assetid: e3b5a1e1-4d18-44b7-aaa6-ebec11892bec
keywords:
- Agendador de Tarefas Agendador de Tarefas, referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb22306266054b8ec19a90f188c43e5eb7e4393b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635921"
---
# <a name="task-scheduler-reference"></a><span data-ttu-id="2d30b-104">Referência de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2d30b-104">Task Scheduler Reference</span></span>

<span data-ttu-id="2d30b-105">Esta seção descreve as APIs, os objetos de script e o esquema XML fornecidos pelo Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="2d30b-105">This section describes the APIs, scripting objects, and XML schema that are provided by the Task Scheduler.</span></span>

<span data-ttu-id="2d30b-106">Os tópicos de API incluem uma descrição da API, a sintaxe da declaração da API, comentários que descrevem condições especiais para a API e um bloco de requisitos que descreve qual plataforma, arquivos de cabeçalho e bibliotecas são necessários.</span><span class="sxs-lookup"><span data-stu-id="2d30b-106">API topics include a description of the API, the declaration syntax of the API, remarks that describe special conditions for the API, and a requirements block that describes what platform, header files, and libraries are required.</span></span>

<span data-ttu-id="2d30b-107">Os tópicos de objeto de script incluem uma descrição do objeto, a sintaxe da declaração do objeto, comentários que descrevem condições especiais para o objeto e um bloco de requisitos que descreve quais plataformas e bibliotecas de tipos são necessárias.</span><span class="sxs-lookup"><span data-stu-id="2d30b-107">Scripting object topics include a description of the object, the declaration syntax of the object, remarks that describe special conditions for the object, and a requirements block that describes what platform and type libraries are required.</span></span>

<span data-ttu-id="2d30b-108">Os tópicos de esquema XML incluem uma descrição das informações de elemento, pai, filho e atributo, e comentários que descrevem condições especiais.</span><span class="sxs-lookup"><span data-stu-id="2d30b-108">XML schema topics include a description of the element, parent, child, and attribute information, and remarks that describe special conditions.</span></span>



| <span data-ttu-id="2d30b-109">Consulte</span><span class="sxs-lookup"><span data-stu-id="2d30b-109">See</span></span>                                                                                          | <span data-ttu-id="2d30b-110">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="2d30b-110">For information on</span></span>                                                                                                                            |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d30b-111">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2d30b-111">Task Scheduler Objects</span></span>](task-scheduler-objects.md)                                         | <span data-ttu-id="2d30b-112">Objetos de script e seus métodos e propriedades.</span><span class="sxs-lookup"><span data-stu-id="2d30b-112">Scripting objects and their methods and properties.</span></span>                                                                                           |
| [<span data-ttu-id="2d30b-113">Interfaces Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2d30b-113">Task Scheduler Interfaces</span></span>](task-scheduler-interfaces.md)                                   | <span data-ttu-id="2d30b-114">Interfaces e seus métodos e propriedades.</span><span class="sxs-lookup"><span data-stu-id="2d30b-114">Interfaces and their methods and properties.</span></span>                                                                                                  |
| [<span data-ttu-id="2d30b-115">Estruturas de Agendador de Tarefas e uniões</span><span class="sxs-lookup"><span data-stu-id="2d30b-115">Task Scheduler Structures and Unions</span></span>](task-scheduler-structures-and-unions.md)             | <span data-ttu-id="2d30b-116">Estruturas e uniões.</span><span class="sxs-lookup"><span data-stu-id="2d30b-116">Structures and unions.</span></span>                                                                                                                        |
| [<span data-ttu-id="2d30b-117">Agendador de Tarefas tipos enumerados</span><span class="sxs-lookup"><span data-stu-id="2d30b-117">Task Scheduler Enumerated Types</span></span>](task-scheduler-enumerated-types.md)                       | <span data-ttu-id="2d30b-118">Constantes definidas por enumeradores.</span><span class="sxs-lookup"><span data-stu-id="2d30b-118">Constants defined by enumerators.</span></span>                                                                                                             |
| [<span data-ttu-id="2d30b-119">Esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2d30b-119">Task Scheduler Schema</span></span>](task-scheduler-schema.md)                                           | <span data-ttu-id="2d30b-120">Elementos, tipos simples, tipos complexos e grupos de atributos definidos pelo esquema.</span><span class="sxs-lookup"><span data-stu-id="2d30b-120">Elements, simple types, complex types, and attribute groups defined by the schema.</span></span>                                                            |
| [<span data-ttu-id="2d30b-121">Agendador de Tarefas constantes de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="2d30b-121">Task Scheduler Error and Success Constants</span></span>](task-scheduler-error-and-success-constants.md) | <span data-ttu-id="2d30b-122">Constantes Error e Success retornadas por Agendador de Tarefas APIs.</span><span class="sxs-lookup"><span data-stu-id="2d30b-122">Error and success constants returned by Task Scheduler APIs.</span></span>                                                                                  |
| [<span data-ttu-id="2d30b-123">**Schtasks.exe**</span><span class="sxs-lookup"><span data-stu-id="2d30b-123">**Schtasks.exe**</span></span>](schtasks.md)                                                             | <span data-ttu-id="2d30b-124">A ferramenta de linha de comando Schtasks.exe que é usada para criar, excluir, consultar, alterar, executar e finalizar tarefas agendadas em um computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="2d30b-124">The Schtasks.exe command line tool that is used to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2d30b-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d30b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d30b-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="2d30b-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




