---
description: Carregando um grafo a partir de um processo externo
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Carregando um grafo a partir de um processo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570489"
---
# <a name="loading-a-graph-from-an-external-process"></a><span data-ttu-id="f6412-103">Carregando um grafo a partir de um processo externo</span><span class="sxs-lookup"><span data-stu-id="f6412-103">Loading a Graph From an External Process</span></span>

<span data-ttu-id="f6412-104">GraphEdit pode carregar um grafo de filtro criado por um processo externo.</span><span class="sxs-lookup"><span data-stu-id="f6412-104">GraphEdit can load a filter graph created by an external process.</span></span> <span data-ttu-id="f6412-105">Com esse recurso, você pode ver exatamente qual grafo de filtro seu aplicativo cria, com apenas uma quantidade mínima de código adicional em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6412-105">With this feature, you can see exactly what filter graph your application builds, with only a minimal amount of additional code in your application.</span></span>

> [!Note]  
> <span data-ttu-id="f6412-106">Esse recurso requer o Windows 2000, o Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f6412-106">This feature requires Windows 2000, Windows XP, or later.</span></span>

 

> [!Note]  
> <span data-ttu-id="f6412-107">A partir do Windows Vista, você deve registrar proppage.dll para habilitar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f6412-107">Starting in Windows Vista, you must register proppage.dll to enable this feature.</span></span> <span data-ttu-id="f6412-108">Proppage.dll está incluído no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f6412-108">Proppage.dll is included in the Windows SDK.</span></span>

 

<span data-ttu-id="f6412-109">O aplicativo deve registrar a instância do grafo de filtro na corrompidos (tabela de objetos em execução).</span><span class="sxs-lookup"><span data-stu-id="f6412-109">The application must register the filter graph instance in the Running Object Table (ROT).</span></span> <span data-ttu-id="f6412-110">O corrompidos é uma tabela de pesquisa globalmente acessível que controla a execução de objetos.</span><span class="sxs-lookup"><span data-stu-id="f6412-110">The ROT is a globally accessible look-up table that keeps track of running objects.</span></span> <span data-ttu-id="f6412-111">Os objetos são registrados no corrompidos por moniker.</span><span class="sxs-lookup"><span data-stu-id="f6412-111">Objects are registered in the ROT by moniker.</span></span> <span data-ttu-id="f6412-112">Para se conectar ao grafo, o GraphEdit pesquisa o corrompidos em busca de monikers cujo nome de exibição corresponde a um determinado formato:</span><span class="sxs-lookup"><span data-stu-id="f6412-112">To connect to the graph, GraphEdit searches the ROT for monikers whose display name matches a particular format:</span></span>


```C++
!FilterGraph X pid Y
```



<span data-ttu-id="f6412-113">em que *X* é o endereço hexadecimal do Gerenciador de gráfico de filtro, e *Y* é a ID do processo, também em hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="f6412-113">where *X* is the hexadecimal address of the Filter Graph Manager, and *Y* is the process id, also in hexadecimal.</span></span>

<span data-ttu-id="f6412-114">Quando o aplicativo criar primeiro o grafo de filtro, chame a seguinte função:</span><span class="sxs-lookup"><span data-stu-id="f6412-114">When your application first creates the filter graph, call the following function:</span></span>


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



<span data-ttu-id="f6412-115">Essa função cria um moniker e uma nova entrada corrompidos para o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="f6412-115">This function creates a moniker and a new ROT entry for the filter graph.</span></span> <span data-ttu-id="f6412-116">O primeiro parâmetro é um ponteiro para o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="f6412-116">The first parameter is a pointer to the filter graph.</span></span> <span data-ttu-id="f6412-117">O segundo parâmetro recebe um valor que identifica a nova entrada corrompidos.</span><span class="sxs-lookup"><span data-stu-id="f6412-117">The second parameter receives a value that identifies the new ROT entry.</span></span> <span data-ttu-id="f6412-118">Antes que o aplicativo libere o gráfico de filtro, chame a função a seguir para remover a entrada corrompidos.</span><span class="sxs-lookup"><span data-stu-id="f6412-118">Before the application releases the filter graph, call the following function to remove the ROT entry.</span></span> <span data-ttu-id="f6412-119">O parâmetro *pdwRegister* é o identificador retornado pela função AddToRot.</span><span class="sxs-lookup"><span data-stu-id="f6412-119">The *pdwRegister* parameter is the identifier returned by the AddToRot function.</span></span>


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



<span data-ttu-id="f6412-120">O exemplo de código a seguir mostra como chamar essas funções.</span><span class="sxs-lookup"><span data-stu-id="f6412-120">The following code example shows how to call these functions.</span></span> <span data-ttu-id="f6412-121">Neste exemplo, o código que adiciona e remove entradas corrompidos é compilado condicionalmente, para que ela seja incluída somente em compilações de depuração.</span><span class="sxs-lookup"><span data-stu-id="f6412-121">In this example, the code that adds and removes ROT entries is conditionally compiled, so that it is included only in debug builds.</span></span>


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



<span data-ttu-id="f6412-122">Para exibir o gráfico de filtro no GraphEdit, execute o aplicativo e GraphEdit ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="f6412-122">To view the filter graph in GraphEdit, run your application and GraphEdit at the same time.</span></span> <span data-ttu-id="f6412-123">No menu **arquivo** GraphEdit, clique em **conectar ao grafo remoto...** Na caixa de diálogo **conectar ao grafo** , selecione a ID do processo (PID) do seu aplicativo e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6412-123">In the GraphEdit **File** menu, click **Connect to Remote Graph...** In the **Connect To Graph** dialog box, select the process id (pid) of your application and click **OK**.</span></span> <span data-ttu-id="f6412-124">GraphEdit carrega o gráfico de filtro e o exibe.</span><span class="sxs-lookup"><span data-stu-id="f6412-124">GraphEdit loads the filter graph and displays it.</span></span> <span data-ttu-id="f6412-125">Não use nenhum outro recurso do GraphEdit nesse grafo — isso pode causar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="f6412-125">Don't use any other GraphEdit features on this graph—it might cause unexpected results.</span></span> <span data-ttu-id="f6412-126">Por exemplo, não adicione ou remova filtros, ou pare e inicie o grafo.</span><span class="sxs-lookup"><span data-stu-id="f6412-126">For example, don't add or remove filters, or stop and start the graph.</span></span> <span data-ttu-id="f6412-127">Feche o GraphEdit antes de sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6412-127">Close GraphEdit before exiting your application.</span></span>

> [!Note]  
> <span data-ttu-id="f6412-128">Seu aplicativo pode atingir várias declarações quando ele é encerrado.</span><span class="sxs-lookup"><span data-stu-id="f6412-128">Your application might hit various asserts when it exits.</span></span> <span data-ttu-id="f6412-129">Você pode ignorá-los.</span><span class="sxs-lookup"><span data-stu-id="f6412-129">You can ignore these.</span></span>

 

<span data-ttu-id="f6412-130">A ilustração a seguir mostra a caixa de diálogo **conectar ao grafo** .</span><span class="sxs-lookup"><span data-stu-id="f6412-130">The following illustration shows the **Connect To Graph** dialog box.</span></span>

![conectar ao grafo](images/gedit-spy.png)

<span data-ttu-id="f6412-132">Quando o GraphEdit carrega o grafo, ele é executado no contexto do aplicativo de destino.</span><span class="sxs-lookup"><span data-stu-id="f6412-132">When GraphEdit loads the graph, it executes in the context of the target application.</span></span> <span data-ttu-id="f6412-133">Portanto, GraphEdit pode bloquear porque está aguardando o thread.</span><span class="sxs-lookup"><span data-stu-id="f6412-133">Therefore, GraphEdit might block because it is waiting for the thread.</span></span> <span data-ttu-id="f6412-134">Por exemplo, isso pode ocorrer se você estiver percorrendo o código no depurador.</span><span class="sxs-lookup"><span data-stu-id="f6412-134">For example, this can occur if you are stepping through your code in the debugger.</span></span>

<span data-ttu-id="f6412-135">Esse recurso deve ser usado somente em compilações de depuração do seu aplicativo, não compilações de varejo, pois permite que outros aplicativos exibam ou controlem o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="f6412-135">This feature should be used only in debug builds of your application, not retail builds, because it enables other applications to view or control the filter graph.</span></span>

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a><span data-ttu-id="f6412-136">Conectando-se a um grafo remoto na linha de comando</span><span class="sxs-lookup"><span data-stu-id="f6412-136">Connecting to a Remote Graph from the Command Line</span></span>

<span data-ttu-id="f6412-137">O GraphEdit dá suporte a uma opção de linha de comando para carregar automaticamente um grafo remoto na inicialização.</span><span class="sxs-lookup"><span data-stu-id="f6412-137">GraphEdit supports a command-line option to load a remote graph automatically on startup.</span></span> <span data-ttu-id="f6412-138">A sintaxe do é:</span><span class="sxs-lookup"><span data-stu-id="f6412-138">The syntax is:</span></span>


```C++
GraphEdt -a moniker
```



<span data-ttu-id="f6412-139">em que *moniker* é um moniker criado usando a função AddToRot, descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f6412-139">where *moniker* is a moniker created using the AddToRot function, described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6412-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6412-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6412-141">Simulando a criação de gráficos com o GraphEdit</span><span class="sxs-lookup"><span data-stu-id="f6412-141">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



