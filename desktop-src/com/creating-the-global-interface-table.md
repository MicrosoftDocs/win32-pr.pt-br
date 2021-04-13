---
title: Criando a tabela de interface global
description: Criando a tabela de interface global
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366785"
---
# <a name="creating-the-global-interface-table"></a><span data-ttu-id="d75c3-103">Criando a tabela de interface global</span><span class="sxs-lookup"><span data-stu-id="d75c3-103">Creating the Global Interface Table</span></span>

<span data-ttu-id="d75c3-104">Use a chamada a seguir para criar o objeto de tabela de interface global e obter um ponteiro para [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span><span class="sxs-lookup"><span data-stu-id="d75c3-104">Use the following call to create the global interface table object and get a pointer to [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span></span>

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> <span data-ttu-id="d75c3-105">Ao criar o objeto de tabela de interface global usando a chamada anterior, é necessário vincular à biblioteca UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="d75c3-105">When creating the global interface table object using the preceding call, it is necessary to link to the library uuid.lib.</span></span> <span data-ttu-id="d75c3-106">Isso resolverá os símbolos externos CLSID \_ StdGlobalInterfaceTable e IID \_ IGlobalInterfaceTable.</span><span class="sxs-lookup"><span data-stu-id="d75c3-106">This will resolve the external symbols CLSID\_StdGlobalInterfaceTable and IID\_IGlobalInterfaceTable.</span></span>

 

<span data-ttu-id="d75c3-107">Há uma única instância da tabela de interface global por processo, portanto, todas as chamadas para essa função em um processo retornam a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="d75c3-107">There is a single instance of the global interface table per process, so all calls to this function in a process return the same instance.</span></span>

<span data-ttu-id="d75c3-108">Após a chamada para a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , registre a interface do apartamento na qual ela reside com uma chamada para o método [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) .</span><span class="sxs-lookup"><span data-stu-id="d75c3-108">After the call to the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, register the interface from the apartment in which it resides with a call to the [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) method.</span></span> <span data-ttu-id="d75c3-109">Esse método fornece um cookie que identifica a interface e sua localização.</span><span class="sxs-lookup"><span data-stu-id="d75c3-109">This method supplies a cookie that identifies the interface and its location.</span></span> <span data-ttu-id="d75c3-110">Um apartamento que procura um ponteiro para essa interface, em seguida, chama o método [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) com esse cookie e a implementação, em seguida, fornece um ponteiro de interface para o apartamento de chamada.</span><span class="sxs-lookup"><span data-stu-id="d75c3-110">An apartment seeking a pointer to this interface then calls the [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) method with this cookie, and the implementation then supplies an interface pointer to the calling apartment.</span></span> <span data-ttu-id="d75c3-111">Para revogar o registro global da interface, qualquer Apartment pode chamar o método [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .</span><span class="sxs-lookup"><span data-stu-id="d75c3-111">To revoke the interface's global registration, any apartment can call the [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) method.</span></span>

<span data-ttu-id="d75c3-112">Um exemplo simples de uso de [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) seria quando você deseja passar um ponteiro de interface em um objeto em um STA (single-threaded apartment) para um thread de trabalho em outro apartamento.</span><span class="sxs-lookup"><span data-stu-id="d75c3-112">A simple example of using [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) would be when you want to pass an interface pointer on an object in a single-threaded apartment (STA) to a worker thread in another apartment.</span></span> <span data-ttu-id="d75c3-113">Em vez de ter que empacotá-lo em um fluxo e passar o fluxo para o thread de trabalho como um parâmetro de thread, o **IGlobalInterfaceTable** permite que você passe um cookie.</span><span class="sxs-lookup"><span data-stu-id="d75c3-113">Rather than having to marshal it into a stream and pass the stream to the worker thread as a thread parameter, **IGlobalInterfaceTable** allows you simply to pass a cookie.</span></span>

<span data-ttu-id="d75c3-114">Ao registrar a interface na tabela de interface global, você obtém um cookie que pode ser usado em vez de passar o ponteiro real (sempre que você precisa passar o ponteiro), para um parâmetro sem método que vai para outro apartamento (como um parâmetro para [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) até [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) ou para a memória em processo acessível fora do seu apartamento.</span><span class="sxs-lookup"><span data-stu-id="d75c3-114">When you register the interface in the global interface table, you get a cookie that you can use instead of passing the actual pointer (whenever you need to pass the pointer), either to a nonmethod parameter that is going to another apartment (as a parameter to [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) through [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) or to in-process memory accessible outside your apartment.</span></span>

<span data-ttu-id="d75c3-115">É necessário ter cuidado porque o uso de interfaces globais coloca a carga extra sobre o programador de gerenciar problemas, como condições de corrida e exclusão mútua, que estão associados ao acesso ao estado global de vários threads simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="d75c3-115">Care is required because using global interfaces places the extra burden on the programmer of managing problems such as race conditions and mutual exclusion, which are associated with accessing global state from multiple threads simultaneously.</span></span>

<span data-ttu-id="d75c3-116">COM fornece uma implementação padrão da interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="d75c3-116">COM provides a standard implementation of the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="d75c3-117">É altamente recomendável que você use essa implementação padrão porque ela fornece uma funcionalidade completa de thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d75c3-117">It is highly recommended that you use this standard implementation because it provides complete thread-safe functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d75c3-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d75c3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d75c3-119">Quando usar a tabela de interface global</span><span class="sxs-lookup"><span data-stu-id="d75c3-119">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 