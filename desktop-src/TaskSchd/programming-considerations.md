---
title: Considerações sobre programação (Agendador de Tarefas)
description: Ao desenvolver aplicativos que usam o Agendador de Tarefas 1,0, tenha em mente os seguintes problemas de programação. Seu aplicativo deve garantir que o serviço de Agendador de Tarefas esteja em execução antes de tentar fazer qualquer chamada usando a API Agendador de Tarefas. Ao recuperar cadeias de caracteres, certifique-se de chamar CoTaskMemFree para liberar cada cadeia de caracteres depois que ela não for mais necessária. Ao recuperar matrizes de cadeias de caracteres, certifique-se de primeiro lançar cada cadeia de caracteres na matriz e, em seguida, liberar a própria matriz. Ao criar ou modificar um item de trabalho, incluindo gatilhos associados a um item de trabalho, certifique-se de chamar IPersistFile Save para salvar o item de trabalho em disco. Depois de usar qualquer uma das interfaces fornecidas pela API de Agendador de Tarefas, certifique-se de chamar a versão IUnknown para liberar a interface. Há suporte para IUnknown em cada objeto de Agendador de Tarefas.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- Iniciando Agendador de Tarefas
- considerações sobre programação Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105780582"
---
# <a name="programming-considerations-task-scheduler"></a><span data-ttu-id="e7b3c-107">Considerações sobre programação (Agendador de Tarefas)</span><span class="sxs-lookup"><span data-stu-id="e7b3c-107">Programming Considerations (Task Scheduler)</span></span>

<span data-ttu-id="e7b3c-108">Ao desenvolver aplicativos que usam o Agendador de Tarefas 1,0, tenha em mente os seguintes problemas de programação.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-108">When developing applications that use the Task Scheduler 1.0, keep the following programming issues in mind.</span></span>

-   <span data-ttu-id="e7b3c-109">Seu aplicativo deve garantir que o serviço de Agendador de Tarefas esteja em execução antes de tentar fazer qualquer chamada usando a API Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-109">Your application must ensure the Task Scheduler service is running before attempting to make any calls using the Task Scheduler API.</span></span>
-   <span data-ttu-id="e7b3c-110">Ao recuperar cadeias de caracteres, certifique-se de chamar [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar cada cadeia de caracteres depois que ela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-110">When retrieving strings, make sure that you call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release each string after it is no longer needed.</span></span> <span data-ttu-id="e7b3c-111">Ao recuperar matrizes de cadeias de caracteres, certifique-se de primeiro lançar cada cadeia de caracteres na matriz e, em seguida, liberar a própria matriz.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-111">When retrieving arrays of strings, make sure you first release each string in the array and then release the array itself.</span></span>
-   <span data-ttu-id="e7b3c-112">Ao criar ou modificar um item de trabalho, incluindo gatilhos associados a um item de trabalho, certifique-se de chamar [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para salvar o item de trabalho em disco.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-112">When creating or modifying a work item, including triggers associated with a work item, make sure you call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the work item to disk.</span></span>
-   <span data-ttu-id="e7b3c-113">Depois de usar qualquer uma das interfaces fornecidas pela API de Agendador de Tarefas, certifique-se de chamar [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-113">After using any of the interfaces that are provided by the Task Scheduler API, make sure you call [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the interface.</span></span> <span data-ttu-id="e7b3c-114">Há suporte para [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) em cada objeto de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is supported by each Task Scheduler object.</span></span>

<span data-ttu-id="e7b3c-115">A seção usando da documentação do Agendador de Tarefas fornece inúmeros exemplos que seguem essas diretrizes.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-115">The Using section of the Task Scheduler documentation provides numerous examples that follow these guidelines.</span></span> <span data-ttu-id="e7b3c-116">A tabela a seguir fornece saltos para alguns desses exemplos.</span><span class="sxs-lookup"><span data-stu-id="e7b3c-116">The table below provides jumps to some of these examples.</span></span>

| <span data-ttu-id="e7b3c-117">Para um exemplo de</span><span class="sxs-lookup"><span data-stu-id="e7b3c-117">For an example of</span></span>         | <span data-ttu-id="e7b3c-118">Consulte</span><span class="sxs-lookup"><span data-stu-id="e7b3c-118">See</span></span>                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b3c-119">Liberando cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="e7b3c-119">Releasing strings</span></span>         | [<span data-ttu-id="e7b3c-120">Recuperando exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="e7b3c-120">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="e7b3c-121">Salvando itens de trabalho em disco</span><span class="sxs-lookup"><span data-stu-id="e7b3c-121">Saving work items to disk</span></span> | [<span data-ttu-id="e7b3c-122">Definindo exemplos de propriedade de item de trabalho</span><span class="sxs-lookup"><span data-stu-id="e7b3c-122">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |
| <span data-ttu-id="e7b3c-123">Liberando interfaces</span><span class="sxs-lookup"><span data-stu-id="e7b3c-123">Releasing interfaces</span></span>      | [<span data-ttu-id="e7b3c-124">Criando uma tarefa usando o exemplo NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="e7b3c-124">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |



 

 

 
