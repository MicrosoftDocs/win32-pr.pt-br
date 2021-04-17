---
description: Um processo filho pode herdar identificadores de seu processo pai. Um identificador herdado é válido somente no contexto do processo filho. Para habilitar um processo filho para herdar identificadores abertos de seu processo pai, use as etapas a seguir.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Manipular herança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755774"
---
# <a name="handle-inheritance"></a><span data-ttu-id="34aea-105">Manipular herança</span><span class="sxs-lookup"><span data-stu-id="34aea-105">Handle Inheritance</span></span>

<span data-ttu-id="34aea-106">Um processo filho pode herdar identificadores de seu processo pai.</span><span class="sxs-lookup"><span data-stu-id="34aea-106">A child process can inherit handles from its parent process.</span></span> <span data-ttu-id="34aea-107">Um identificador herdado é válido somente no contexto do processo filho.</span><span class="sxs-lookup"><span data-stu-id="34aea-107">An inherited handle is valid only in the context of the child process.</span></span> <span data-ttu-id="34aea-108">Para habilitar um processo filho para herdar identificadores abertos de seu processo pai, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="34aea-108">To enable a child process to inherit open handles from its parent process, use the following steps.</span></span>

1.  <span data-ttu-id="34aea-109">Crie o identificador com o membro **bInheritHandle** da estrutura [**de \_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="34aea-109">Create the handle with the **bInheritHandle** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure set to **TRUE**.</span></span>
2.  <span data-ttu-id="34aea-110">Crie o processo filho usando a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , com o parâmetro *BInheritHandles* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="34aea-110">Create the child process using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, with the *bInheritHandles* parameter set to **TRUE**.</span></span>

<span data-ttu-id="34aea-111">A função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) duplica um identificador a ser usado no processo atual ou em outro processo.</span><span class="sxs-lookup"><span data-stu-id="34aea-111">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function duplicates a handle to be used in the current process or in another process.</span></span> <span data-ttu-id="34aea-112">Se um aplicativo duplicar um de seus identificadores para outro processo, o identificador duplicado será válido somente no contexto do outro processo.</span><span class="sxs-lookup"><span data-stu-id="34aea-112">If an application duplicates one of its handles for another process, the duplicated handle is valid only in the context of the other process.</span></span>

<span data-ttu-id="34aea-113">Um identificador duplicado ou herdado é um valor exclusivo, mas se refere ao mesmo objeto que o identificador original.</span><span class="sxs-lookup"><span data-stu-id="34aea-113">A duplicated or inherited handle is a unique value, but it refers to the same object as the original handle.</span></span> <span data-ttu-id="34aea-114">Os processos podem herdar ou duplicar identificadores para os seguintes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="34aea-114">Processes can inherit or duplicate handles to the following types of objects:</span></span>

-   <span data-ttu-id="34aea-115">Token de acesso</span><span class="sxs-lookup"><span data-stu-id="34aea-115">Access Token</span></span>
-   <span data-ttu-id="34aea-116">Dispositivo de comunicações</span><span class="sxs-lookup"><span data-stu-id="34aea-116">Communications device</span></span>
-   <span data-ttu-id="34aea-117">Entrada do console</span><span class="sxs-lookup"><span data-stu-id="34aea-117">Console input</span></span>
-   <span data-ttu-id="34aea-118">Buffer da tela do console</span><span class="sxs-lookup"><span data-stu-id="34aea-118">Console screen buffer</span></span>
-   <span data-ttu-id="34aea-119">Área de trabalho</span><span class="sxs-lookup"><span data-stu-id="34aea-119">Desktop</span></span>
-   <span data-ttu-id="34aea-120">Diretório</span><span class="sxs-lookup"><span data-stu-id="34aea-120">Directory</span></span>
-   <span data-ttu-id="34aea-121">Evento</span><span class="sxs-lookup"><span data-stu-id="34aea-121">Event</span></span>
-   <span data-ttu-id="34aea-122">Arquivo</span><span class="sxs-lookup"><span data-stu-id="34aea-122">File</span></span>
-   <span data-ttu-id="34aea-123">Mapeamento de arquivo</span><span class="sxs-lookup"><span data-stu-id="34aea-123">File mapping</span></span>
-   <span data-ttu-id="34aea-124">Trabalho</span><span class="sxs-lookup"><span data-stu-id="34aea-124">Job</span></span>
-   <span data-ttu-id="34aea-125">Recepção</span><span class="sxs-lookup"><span data-stu-id="34aea-125">Mailslot</span></span>
-   <span data-ttu-id="34aea-126">Mutex</span><span class="sxs-lookup"><span data-stu-id="34aea-126">Mutex</span></span>
-   <span data-ttu-id="34aea-127">Pipe</span><span class="sxs-lookup"><span data-stu-id="34aea-127">Pipe</span></span>
-   <span data-ttu-id="34aea-128">Processar</span><span class="sxs-lookup"><span data-stu-id="34aea-128">Process</span></span>
-   <span data-ttu-id="34aea-129">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="34aea-129">Registry key</span></span>
-   <span data-ttu-id="34aea-130">Sinal</span><span class="sxs-lookup"><span data-stu-id="34aea-130">Semaphore</span></span>
-   <span data-ttu-id="34aea-131">Soquete</span><span class="sxs-lookup"><span data-stu-id="34aea-131">Socket</span></span>
-   <span data-ttu-id="34aea-132">Thread</span><span class="sxs-lookup"><span data-stu-id="34aea-132">Thread</span></span>
-   <span data-ttu-id="34aea-133">Temporizador</span><span class="sxs-lookup"><span data-stu-id="34aea-133">Timer</span></span>
-   <span data-ttu-id="34aea-134">Estação de janela</span><span class="sxs-lookup"><span data-stu-id="34aea-134">Window station</span></span>

<span data-ttu-id="34aea-135">Todos os outros objetos são privados ao processo que os criou; seus identificadores de objeto não podem ser duplicados ou herdados.</span><span class="sxs-lookup"><span data-stu-id="34aea-135">All other objects are private to the process that created them; their object handles cannot be duplicated or inherited.</span></span>

<span data-ttu-id="34aea-136">Para obter mais informações, consulte [Herança](/windows/desktop/ProcThread/inheritance).</span><span class="sxs-lookup"><span data-stu-id="34aea-136">For more information, see [Inheritance](/windows/desktop/ProcThread/inheritance).</span></span>

 

 
