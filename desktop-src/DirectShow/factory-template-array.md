---
description: Matriz de modelo de fábrica
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Matriz de modelo de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088804"
---
# <a name="factory-template-array"></a><span data-ttu-id="6246b-103">Matriz de modelo de fábrica</span><span class="sxs-lookup"><span data-stu-id="6246b-103">Factory Template Array</span></span>

<span data-ttu-id="6246b-104">O modelo de fábrica contém as seguintes variáveis de membro público:</span><span class="sxs-lookup"><span data-stu-id="6246b-104">The factory template contains the following public member variables:</span></span>

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

<span data-ttu-id="6246b-105">Os dois ponteiros de função, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) e [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md), usam as seguintes definições de tipo:</span><span class="sxs-lookup"><span data-stu-id="6246b-105">The two function pointers, [**m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) and [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md), use the following type definitions:</span></span>

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

<span data-ttu-id="6246b-106">A primeira é a função de instanciação para o componente.</span><span class="sxs-lookup"><span data-stu-id="6246b-106">The first is the instantiation function for the component.</span></span> <span data-ttu-id="6246b-107">A segunda é uma função de inicialização opcional.</span><span class="sxs-lookup"><span data-stu-id="6246b-107">The second is an optional initialization function.</span></span> <span data-ttu-id="6246b-108">Se você fornecer uma função de inicialização, ela será chamada de dentro da função de ponto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="6246b-108">If you provide an initialization function, it is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="6246b-109">(A função de ponto de entrada de DLL é discutida posteriormente neste artigo.)</span><span class="sxs-lookup"><span data-stu-id="6246b-109">(The DLL entry-point function is discussed later in this article.)</span></span>

<span data-ttu-id="6246b-110">Suponha que você esteja criando uma DLL que contém um componente chamado CMyComponent, que herda de [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="6246b-110">Suppose you are creating a DLL that contains a component named CMyComponent, which inherits from [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="6246b-111">Você deve fornecer os seguintes itens em sua DLL:</span><span class="sxs-lookup"><span data-stu-id="6246b-111">You must provide the following items in your DLL:</span></span>

-   <span data-ttu-id="6246b-112">A função de inicialização, um método público que retorna uma nova instância de CMyComponent.</span><span class="sxs-lookup"><span data-stu-id="6246b-112">The initialization function, a public method that returns a new instance of CMyComponent.</span></span>
-   <span data-ttu-id="6246b-113">Uma matriz global de modelos de fábrica, chamados de *modelos de g \_ .*</span><span class="sxs-lookup"><span data-stu-id="6246b-113">A global array of factory templates, named *g\_Templates.*</span></span> <span data-ttu-id="6246b-114">Essa matriz contém o modelo de fábrica para CMyComponent.</span><span class="sxs-lookup"><span data-stu-id="6246b-114">This array contains the factory template for CMyComponent.</span></span>
-   <span data-ttu-id="6246b-115">Uma variável global chamada *g \_ cTemplates* que especifica o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="6246b-115">A global variable named *g\_cTemplates* that specifies the size of the array.</span></span>

<span data-ttu-id="6246b-116">O exemplo a seguir mostra como declarar esses itens:</span><span class="sxs-lookup"><span data-stu-id="6246b-116">The following example shows how to declare these items:</span></span>


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



<span data-ttu-id="6246b-117">O `CreateInstance` método chama o construtor de classe e retorna um ponteiro para a nova instância de classe.</span><span class="sxs-lookup"><span data-stu-id="6246b-117">The `CreateInstance` method calls the class constructor and returns a pointer to the new class instance.</span></span> <span data-ttu-id="6246b-118">O parâmetro *punk* é um ponteiro para o [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)de agregação.</span><span class="sxs-lookup"><span data-stu-id="6246b-118">The parameter *pUnk* is a pointer to the aggregating [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="6246b-119">Você pode simplesmente passar esse parâmetro para o construtor de classe.</span><span class="sxs-lookup"><span data-stu-id="6246b-119">You can simply pass this parameter to the class constructor.</span></span> <span data-ttu-id="6246b-120">O parâmetro *PHR* é um ponteiro para um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="6246b-120">The parameter *pHr* is a pointer to an HRESULT value.</span></span> <span data-ttu-id="6246b-121">O construtor de classe define isso como um valor apropriado, mas se o Construtor falhar, defina o valor como E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6246b-121">The class constructor sets this to an appropriate value, but if the constructor fails, set the value to E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="6246b-122">A macro de [**nome**](name.md) gera uma cadeia de caracteres em compilações de depuração, mas é resolvida como **NULL** em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="6246b-122">The [**NAME**](name.md) macro generates a string in debug builds but resolves to **NULL** in retail builds.</span></span> <span data-ttu-id="6246b-123">Ele é usado neste exemplo para dar ao componente um nome que aparece nos logs de depuração, mas não ocupa memória na versão final.</span><span class="sxs-lookup"><span data-stu-id="6246b-123">It is used in this example to give the component a name that appears in debug logs but does not occupy memory in the final version.</span></span>

<span data-ttu-id="6246b-124">O `CreateInstance` método pode ter qualquer nome, porque a fábrica de classes refere-se ao ponteiro de função no modelo de fábrica.</span><span class="sxs-lookup"><span data-stu-id="6246b-124">The `CreateInstance` method can have any name, because the class factory refers to the function pointer in the factory template.</span></span> <span data-ttu-id="6246b-125">No entanto, os *\_ modelos g* e *g \_ cTemplates* são variáveis globais que a fábrica de classes espera encontrar, portanto, eles devem ter exatamente esses nomes.</span><span class="sxs-lookup"><span data-stu-id="6246b-125">However, *g\_Templates* and *g\_cTemplates* are global variables that the class factory expects to find, so they must have exactly those names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6246b-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6246b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6246b-127">Como criar uma DLL de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="6246b-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
