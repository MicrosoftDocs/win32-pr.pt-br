---
title: Ciclo de vida da instância de virtualização
description: Visão geral do ciclo de vida de uma instância de virtualização ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499066"
---
# <a name="virtualization-instance-lifecycle"></a><span data-ttu-id="65d7e-103">Ciclo de vida da instância de virtualização</span><span class="sxs-lookup"><span data-stu-id="65d7e-103">Virtualization Instance Lifecycle</span></span>

<span data-ttu-id="65d7e-104">O aplicativo do provedor mantém uma ou mais instâncias de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-104">The provider application maintains one or more virtualization instances.</span></span>  <span data-ttu-id="65d7e-105">Cada instância de virtualização passa por quatro estágios em seu ciclo de vida:</span><span class="sxs-lookup"><span data-stu-id="65d7e-105">Each virtualization instance goes through four stages in its lifecycle:</span></span>

1. <span data-ttu-id="65d7e-106">Criação</span><span class="sxs-lookup"><span data-stu-id="65d7e-106">Creation</span></span>
2. <span data-ttu-id="65d7e-107">Inicialização</span><span class="sxs-lookup"><span data-stu-id="65d7e-107">Startup</span></span>
3. <span data-ttu-id="65d7e-108">Runtime</span><span class="sxs-lookup"><span data-stu-id="65d7e-108">Runtime</span></span>
4. <span data-ttu-id="65d7e-109">Desligar</span><span class="sxs-lookup"><span data-stu-id="65d7e-109">Shutdown</span></span>

<span data-ttu-id="65d7e-110">Observe que, depois de desligar uma instância de virtualização, o provedor não precisa recriá-la para reutilizá-la.</span><span class="sxs-lookup"><span data-stu-id="65d7e-110">Note that after shutting down a virtualization instance the provider does not need to re-create it to reuse it.</span></span>  <span data-ttu-id="65d7e-111">Ele pode simplesmente iniciá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="65d7e-111">It can simply start it up again.</span></span>

> <span data-ttu-id="65d7e-112">**Observação**: Esta seção mostra exemplos de APIs ProjFS.</span><span class="sxs-lookup"><span data-stu-id="65d7e-112">**Note**: This section shows examples of ProjFS APIs.</span></span>  <span data-ttu-id="65d7e-113">Cada exemplo destina-se a ilustrar o uso básico da API.</span><span class="sxs-lookup"><span data-stu-id="65d7e-113">Each example is meant to illustrate basic API usage.</span></span>  <span data-ttu-id="65d7e-114">Para obter a documentação das opções não utilizadas nesses exemplos, consulte a [referência da API do ProjFS](/windows/desktop/api/_projfs).</span><span class="sxs-lookup"><span data-stu-id="65d7e-114">For documentation of options unused in these examples please consult the [ProjFS API reference](/windows/desktop/api/_projfs).</span></span>

## <a name="creating-a-virtualization-root"></a><span data-ttu-id="65d7e-115">Criando uma raiz de virtualização</span><span class="sxs-lookup"><span data-stu-id="65d7e-115">Creating a virtualization root</span></span>

<span data-ttu-id="65d7e-116">Antes que um provedor possa iniciar a instância de virtualização que irá projetar itens no sistema de arquivos local, ele deve criar a raiz de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-116">Before a provider can start up the virtualization instance that will project items into the local file system, it must create the virtualization root.</span></span>  <span data-ttu-id="65d7e-117">A raiz de virtualização é o diretório no qual o provedor projeta uma árvore de diretórios e arquivos.</span><span class="sxs-lookup"><span data-stu-id="65d7e-117">The virtualization root is the directory under which the provider projects a tree of directories and files.</span></span>

<span data-ttu-id="65d7e-118">Para criar uma raiz de virtualização, o provedor deve:</span><span class="sxs-lookup"><span data-stu-id="65d7e-118">To create a virtualization root the provider must:</span></span>

1. <span data-ttu-id="65d7e-119">Crie um diretório para servir como a raiz de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-119">Create a directory to serve as the virtualization root.</span></span>

    <span data-ttu-id="65d7e-120">O provedor cria um diretório para servir como a raiz de virtualização usando, por exemplo, **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span><span class="sxs-lookup"><span data-stu-id="65d7e-120">The provider creates a directory to serve as the virtualization root using, for example **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span></span>

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="65d7e-121">Crie uma ID de instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-121">Create a virtualization instance ID.</span></span>

    <span data-ttu-id="65d7e-122">Cada instância de virtualização tem uma ID exclusiva chamada de _ID de instância de virtualização_.</span><span class="sxs-lookup"><span data-stu-id="65d7e-122">Every virtualization instance has a unique ID called the _virtualization instance ID_.</span></span>  <span data-ttu-id="65d7e-123">O sistema usa esse valor para identificar a qual instância de virtualização seu conteúdo está associado.</span><span class="sxs-lookup"><span data-stu-id="65d7e-123">The system uses this value to identify which virtualization instance its contents are associated to.</span></span>

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="65d7e-124">Marque o novo diretório como a raiz de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-124">Mark the new directory as the virtualization root.</span></span>

    <span data-ttu-id="65d7e-125">O provedor chama **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** para marcar o novo diretório como a raiz de virtualização e atribuí-lo à instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-125">The provider calls **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** to mark the new directory as the virtualization root and assign it to the virtualization instance.</span></span>

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

<span data-ttu-id="65d7e-126">O provedor só precisa criar a raiz de virtualização uma vez para cada instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-126">The provider only needs to create the virtualization root once for each virtualization instance.</span></span>  <span data-ttu-id="65d7e-127">Depois que uma raiz tiver sido criada, sua instância associada poderá ser iniciada repetidamente e interrompida sem recriar a raiz.</span><span class="sxs-lookup"><span data-stu-id="65d7e-127">Once a root has been created, its associated instance can be repeatedly started and stopped without recreating the root.</span></span>

## <a name="starting-a-virtualization-instance"></a><span data-ttu-id="65d7e-128">Iniciando uma instância de virtualização</span><span class="sxs-lookup"><span data-stu-id="65d7e-128">Starting a virtualization instance</span></span>

<span data-ttu-id="65d7e-129">Depois que a raiz de virtualização tiver sido criada, o provedor deverá iniciar a instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-129">Once the virtualization root has been created the provider must start the virtualization instance.</span></span>  <span data-ttu-id="65d7e-130">Isso sinaliza ProjFS que o provedor está pronto para receber retornos de chamada e fornecer dados.</span><span class="sxs-lookup"><span data-stu-id="65d7e-130">This signals ProjFS that the provider is ready to receive callbacks and provide data.</span></span>

<span data-ttu-id="65d7e-131">Para iniciar a instância de virtualização, o provedor deve:</span><span class="sxs-lookup"><span data-stu-id="65d7e-131">To start the virtualization instance the provider must:</span></span>

1. <span data-ttu-id="65d7e-132">Configure a tabela de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="65d7e-132">Set up the callback table.</span></span>

    <span data-ttu-id="65d7e-133">O ProjFS se comunica com o provedor invocando rotinas de retorno de chamada implementadas pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="65d7e-133">ProjFS communicates with the provider by invoking callback routines implemented by the provider.</span></span>  <span data-ttu-id="65d7e-134">O provedor popula um struct [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) com ponteiros para suas rotinas de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="65d7e-134">The provider populates a [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct with pointers to its callback routines.</span></span>

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. <span data-ttu-id="65d7e-135">Inicie a instância.</span><span class="sxs-lookup"><span data-stu-id="65d7e-135">Start the instance.</span></span>

    <span data-ttu-id="65d7e-136">O provedor chama **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** para iniciar a instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-136">The provider calls **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** to start the virtualization instance.</span></span>

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    <span data-ttu-id="65d7e-137">O parâmetro _instanceHandle_ do **PrjStartVirtualizing** retorna um identificador para a instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-137">**PrjStartVirtualizing**'s _instanceHandle_ parameter returns a handle to the virtualization instance.</span></span>  <span data-ttu-id="65d7e-138">O provedor usa esse identificador ao chamar outras APIs ProjFS.</span><span class="sxs-lookup"><span data-stu-id="65d7e-138">The provider uses this handle when calling other ProjFS APIs.</span></span>

## <a name="virtualization-instance-runtime"></a><span data-ttu-id="65d7e-139">Tempo de execução da instância de virtualização</span><span class="sxs-lookup"><span data-stu-id="65d7e-139">Virtualization instance runtime</span></span>

<span data-ttu-id="65d7e-140">Depois que a chamada para **PrjStartVirtualizing** retorna, ProjFS invocará as rotinas de retorno de chamada do provedor em resposta às operações do sistema de arquivos na instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-140">Once the call to **PrjStartVirtualizing** returns, ProjFS will invoke the provider's callback routines in response to file system operations in the virtualization instance.</span></span>  <span data-ttu-id="65d7e-141">Para obter informações sobre como o provedor pode lidar com várias operações do sistema de arquivos, consulte as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="65d7e-141">For information on how the provider can handle various file system operations, refer to the following sections:</span></span>

* [<span data-ttu-id="65d7e-142">Enumerar arquivos e diretórios</span><span class="sxs-lookup"><span data-stu-id="65d7e-142">Enumerating Files and Directories</span></span>](enumerating-files-and-directories.md)
* [<span data-ttu-id="65d7e-143">Fornecer dados de arquivo</span><span class="sxs-lookup"><span data-stu-id="65d7e-143">Providing File Data</span></span>](providing-file-data.md)
* [<span data-ttu-id="65d7e-144">Notificações de operação do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="65d7e-144">File System Operation Notifications</span></span>](file-system-operation-notifications.md)
* [<span data-ttu-id="65d7e-145">Manipulando alterações de exibição</span><span class="sxs-lookup"><span data-stu-id="65d7e-145">Handling View Changes</span></span>](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a><span data-ttu-id="65d7e-146">Desligando uma instância de virtualização</span><span class="sxs-lookup"><span data-stu-id="65d7e-146">Shutting down a virtualization instance</span></span>

<span data-ttu-id="65d7e-147">Para sinalizar ProjFS que o provedor deseja parar de receber retornos de chamada e fornecer dados, o provedor deve parar a instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="65d7e-147">To signal ProjFS that the provider wants to stop receiving callbacks and providing data, the provider must stop the virtualization instance.</span></span>  <span data-ttu-id="65d7e-148">Para fazer isso, o provedor chama **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passando o identificador para a instância de virtualização recebida da chamada para **PrjStartVirtualizing**.</span><span class="sxs-lookup"><span data-stu-id="65d7e-148">To do this the provider calls **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passing it the handle to the virtualization instance that it received from the call to **PrjStartVirtualizing**.</span></span>

```C++
PrjStopVirtualizing(instanceHandle);
```

<span data-ttu-id="65d7e-149">Observe que até que essa chamada retorne, ProjFS pode continuar invocando as rotinas de retorno de chamada do provedor.</span><span class="sxs-lookup"><span data-stu-id="65d7e-149">Note that until this call returns, ProjFS may continue to invoke the provider's callback routines.</span></span>