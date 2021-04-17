---
description: Este tópico descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funções de DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105748797"
---
# <a name="dll-functions"></a><span data-ttu-id="50638-103">Funções de DLL</span><span class="sxs-lookup"><span data-stu-id="50638-103">DLL Functions</span></span>

<span data-ttu-id="50638-104">Este tópico descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="50638-104">This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span>

<span data-ttu-id="50638-105">Uma DLL deve implementar as seguintes funções para que possam ser registradas, canceladas e carregadas na memória.</span><span class="sxs-lookup"><span data-stu-id="50638-105">A DLL must implement the following functions so that it can be registered, unregistered, and loaded into memory.</span></span>

-   <span data-ttu-id="50638-106">[*DllMain*](/windows/desktop/Dlls/dllmain): o ponto de entrada de dll.</span><span class="sxs-lookup"><span data-stu-id="50638-106">[*DllMain*](/windows/desktop/Dlls/dllmain): The DLL entry point.</span></span> <span data-ttu-id="50638-107">O nome *DllMain* é um espaço reservado para o nome da função definida pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="50638-107">The name *DllMain* is a placeholder for the library-defined function name.</span></span> <span data-ttu-id="50638-108">A implementação do DirectShow usa o nome **DllEntryPoint**.</span><span class="sxs-lookup"><span data-stu-id="50638-108">The DirectShow implementation uses the name **DllEntryPoint**.</span></span> <span data-ttu-id="50638-109">Para obter mais informações, consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="50638-109">For more information, see the Platform SDK.</span></span>
-   <span data-ttu-id="50638-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): cria uma instância de fábrica de classes.</span><span class="sxs-lookup"><span data-stu-id="50638-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): Creates a class factory instance.</span></span> <span data-ttu-id="50638-111">Descrito nas seções anteriores.</span><span class="sxs-lookup"><span data-stu-id="50638-111">Described in the previous sections.</span></span>
-   <span data-ttu-id="50638-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): consulta se a dll pode ser descarregada com segurança.</span><span class="sxs-lookup"><span data-stu-id="50638-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): Queries whether the DLL can safely be unloaded.</span></span>
-   <span data-ttu-id="50638-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): cria entradas de registro para a dll.</span><span class="sxs-lookup"><span data-stu-id="50638-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): Creates registry entries for the DLL.</span></span>
-   <span data-ttu-id="50638-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): remove entradas do registro para a dll.</span><span class="sxs-lookup"><span data-stu-id="50638-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): Removes registry entries for the DLL.</span></span>

<span data-ttu-id="50638-115">Desses, os três primeiros são implementados pelo DirectShow.</span><span class="sxs-lookup"><span data-stu-id="50638-115">Of these, the first three are implemented by DirectShow.</span></span> <span data-ttu-id="50638-116">Se o modelo de fábrica fornecer uma função de inicialização na variável de membro [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) , essa função será chamada de dentro da função de ponto de entrada de dll.</span><span class="sxs-lookup"><span data-stu-id="50638-116">If your factory template provides an initialization function in the [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md) member variable, that function is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="50638-117">Para obter mais informações sobre quando o sistema chama a função de ponto de entrada de DLL, consulte [*DllMain*](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="50638-117">For more information on when the system calls the DLL entry-point function, see [*DllMain*](/windows/desktop/Dlls/dllmain).</span></span>

<span data-ttu-id="50638-118">Você deve implementar [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), mas o DirectShow fornece uma função chamada [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) que faz o trabalho necessário.</span><span class="sxs-lookup"><span data-stu-id="50638-118">You must implement [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), but DirectShow provides a function named [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) that does the necessary work.</span></span> <span data-ttu-id="50638-119">O componente pode simplesmente encapsular essa função, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="50638-119">Your component can simply wrap this function, as shown in the following example:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



<span data-ttu-id="50638-120">No entanto, dentro de [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) , você pode personalizar o processo de registro conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="50638-120">However, within [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) you can customize the registration process as needed.</span></span> <span data-ttu-id="50638-121">Se sua DLL contiver um filtro, talvez seja necessário fazer algum trabalho adicional.</span><span class="sxs-lookup"><span data-stu-id="50638-121">If your DLL contains a filter, you might need to do some additional work.</span></span> <span data-ttu-id="50638-122">Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="50638-122">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

<span data-ttu-id="50638-123">No arquivo de definição de módulo (. def), exporte todas as funções de DLL, exceto a função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="50638-123">In your module-definition (.def) file, export all the DLL functions except for the entry-point function.</span></span> <span data-ttu-id="50638-124">Este é um arquivo. def de exemplo:</span><span class="sxs-lookup"><span data-stu-id="50638-124">The following is an example .def file:</span></span>


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



<span data-ttu-id="50638-125">Você pode registrar a DLL usando o utilitário Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="50638-125">You can register the DLL using the Regsvr32.exe utility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50638-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50638-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50638-127">Como criar uma DLL de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="50638-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
