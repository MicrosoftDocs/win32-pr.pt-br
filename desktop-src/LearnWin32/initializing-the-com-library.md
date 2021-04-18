---
title: Inicializando a biblioteca COM
description: Inicializando a biblioteca COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105780622"
---
# <a name="initializing-the-com-library"></a><span data-ttu-id="b6123-103">Inicializando a biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="b6123-103">Initializing the COM Library</span></span>

<span data-ttu-id="b6123-104">Qualquer programa do Windows que usa COM deve inicializar a biblioteca COM chamando a função [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="b6123-104">Any Windows program that uses COM must initialize the COM library by calling the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> <span data-ttu-id="b6123-105">Cada thread que usa uma interface COM deve fazer uma chamada separada para essa função.</span><span class="sxs-lookup"><span data-stu-id="b6123-105">Each thread that uses a COM interface must make a separate call to this function.</span></span> <span data-ttu-id="b6123-106">**CoInitializeEx** tem a seguinte assinatura:</span><span class="sxs-lookup"><span data-stu-id="b6123-106">**CoInitializeEx** has the following signature:</span></span>


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



<span data-ttu-id="b6123-107">O primeiro parâmetro é reservado e deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b6123-107">The first parameter is reserved and must be **NULL**.</span></span> <span data-ttu-id="b6123-108">O segundo parâmetro especifica o modelo de Threading que o programa usará.</span><span class="sxs-lookup"><span data-stu-id="b6123-108">The second parameter specifies the threading model that your program will use.</span></span> <span data-ttu-id="b6123-109">O COM dá suporte a dois modelos de Threading diferentes, *Apartment Threaded* e *multithread*.</span><span class="sxs-lookup"><span data-stu-id="b6123-109">COM supports two different threading models, *apartment threaded* and *multithreaded*.</span></span> <span data-ttu-id="b6123-110">Se você especificar segmentação de apartamento, você está fazendo as seguintes garantias:</span><span class="sxs-lookup"><span data-stu-id="b6123-110">If you specify apartment threading, you are making the following guarantees:</span></span>

-   <span data-ttu-id="b6123-111">Você vai acessar cada objeto COM de um único thread; Você não compartilhará ponteiros de interface COM entre vários threads.</span><span class="sxs-lookup"><span data-stu-id="b6123-111">You will access each COM object from a single thread; you will not share COM interface pointers between multiple threads.</span></span>
-   <span data-ttu-id="b6123-112">O thread terá um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b6123-112">The thread will have a message loop.</span></span> <span data-ttu-id="b6123-113">(Consulte [as mensagens de janela](window-messages.md) no módulo 1.)</span><span class="sxs-lookup"><span data-stu-id="b6123-113">(See [Window Messages](window-messages.md) in Module 1.)</span></span>

<span data-ttu-id="b6123-114">Se uma dessas restrições não for verdadeira, use o modelo multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="b6123-114">If either of these constraints is not true, use the multithreaded model.</span></span> <span data-ttu-id="b6123-115">Para especificar o modelo de Threading, defina um dos sinalizadores a seguir no parâmetro *dwCoInit* .</span><span class="sxs-lookup"><span data-stu-id="b6123-115">To specify the threading model, set one of the following flags in the *dwCoInit* parameter.</span></span>



| <span data-ttu-id="b6123-116">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="b6123-116">Flag</span></span>                          | <span data-ttu-id="b6123-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6123-117">Description</span></span>         |
|-------------------------------|---------------------|
| <span data-ttu-id="b6123-118">**APARTMENTTHREADED de coinicialização \_**</span><span class="sxs-lookup"><span data-stu-id="b6123-118">**COINIT\_APARTMENTTHREADED**</span></span> | <span data-ttu-id="b6123-119">Apartment Threaded.</span><span class="sxs-lookup"><span data-stu-id="b6123-119">Apartment threaded.</span></span> |
| <span data-ttu-id="b6123-120">**coinit \_ multi-threaded**</span><span class="sxs-lookup"><span data-stu-id="b6123-120">**COINIT\_MULTITHREADED**</span></span>     | <span data-ttu-id="b6123-121">Multithread.</span><span class="sxs-lookup"><span data-stu-id="b6123-121">Multithreaded.</span></span>      |



 

<span data-ttu-id="b6123-122">Você deve definir exatamente um desses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="b6123-122">You must set exactly one of these flags.</span></span> <span data-ttu-id="b6123-123">Geralmente, um thread que cria uma janela deve usar o sinalizador **coinit \_ APARTMENTTHREADED** e outros threads devem usar o **coinit \_ multi-threaded**.</span><span class="sxs-lookup"><span data-stu-id="b6123-123">Generally, a thread that creates a window should use the **COINIT\_APARTMENTTHREADED** flag, and other threads should use **COINIT\_MULTITHREADED**.</span></span> <span data-ttu-id="b6123-124">No entanto, alguns componentes COM exigem um modelo de Threading específico.</span><span class="sxs-lookup"><span data-stu-id="b6123-124">However, some COM components require a particular threading model.</span></span> <span data-ttu-id="b6123-125">A documentação do MSDN deve informá-lo quando esse for o caso.</span><span class="sxs-lookup"><span data-stu-id="b6123-125">The MSDN documentation should tell you when that is the case.</span></span>

> [!Note]  
> <span data-ttu-id="b6123-126">Na verdade, mesmo que você especifique o Threading Apartment, ainda é possível compartilhar interfaces entre threads, usando uma técnica chamada *marshaling*.</span><span class="sxs-lookup"><span data-stu-id="b6123-126">Actually, even if you specify apartment threading, it is still possible to share interfaces between threads, by using a technique called *marshaling*.</span></span> <span data-ttu-id="b6123-127">O marshaling está além do escopo deste módulo.</span><span class="sxs-lookup"><span data-stu-id="b6123-127">Marshaling is beyond the scope of this module.</span></span> <span data-ttu-id="b6123-128">O ponto importante é que, com o Threading Apartment, você nunca deve simplesmente copiar um ponteiro de interface para outro thread.</span><span class="sxs-lookup"><span data-stu-id="b6123-128">The important point is that with apartment threading, you must never simply copy an interface pointer to another thread.</span></span> <span data-ttu-id="b6123-129">Para obter mais informações sobre os modelos de Threading COM, consulte [Processes, threads e Apartments](/windows/desktop/com/processes--threads--and-apartments).</span><span class="sxs-lookup"><span data-stu-id="b6123-129">For more information about the COM threading models, see [Processes, Threads, and Apartments](/windows/desktop/com/processes--threads--and-apartments).</span></span>

 

<span data-ttu-id="b6123-130">Além dos sinalizadores já mencionados, é uma boa ideia definir o sinalizador de **\_ desabilitar \_ OLE1DDE do coinit** no parâmetro *dwCoInit* .</span><span class="sxs-lookup"><span data-stu-id="b6123-130">In addition to the flags already mentioned, it is a good idea to set the **COINIT\_DISABLE\_OLE1DDE** flag in the *dwCoInit* parameter.</span></span> <span data-ttu-id="b6123-131">A definição desse sinalizador evita alguma sobrecarga associada ao OLE (vinculação e inserção de objetos) 1,0, uma tecnologia obsoleta.</span><span class="sxs-lookup"><span data-stu-id="b6123-131">Setting this flag avoids some overhead associated with Object Linking and Embedding (OLE) 1.0, an obsolete technology.</span></span>

<span data-ttu-id="b6123-132">Veja como você deve inicializar COM para Threading Apartment:</span><span class="sxs-lookup"><span data-stu-id="b6123-132">Here is how you would initialize COM for apartment threading:</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



<span data-ttu-id="b6123-133">O tipo de retorno **HRESULT** contém um erro ou código de êxito.</span><span class="sxs-lookup"><span data-stu-id="b6123-133">The **HRESULT** return type contains an error or success code.</span></span> <span data-ttu-id="b6123-134">Veremos o tratamento de erros COM na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="b6123-134">We'll look at COM error handling in the next section.</span></span>

## <a name="uninitializing-the-com-library"></a><span data-ttu-id="b6123-135">Cancelando a inicialização da biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="b6123-135">Uninitializing the COM Library</span></span>

<span data-ttu-id="b6123-136">Para cada chamada bem-sucedida para [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), você deve chamar [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) antes de o thread sair.</span><span class="sxs-lookup"><span data-stu-id="b6123-136">For every successful call to [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), you must call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) before the thread exits.</span></span> <span data-ttu-id="b6123-137">Essa função não usa parâmetros e não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b6123-137">This function takes no parameters and has no return value.</span></span>


```C++
CoUninitialize();
```



## <a name="next"></a><span data-ttu-id="b6123-138">Avançar</span><span class="sxs-lookup"><span data-stu-id="b6123-138">Next</span></span>

[<span data-ttu-id="b6123-139">Códigos de erro em COM</span><span class="sxs-lookup"><span data-stu-id="b6123-139">Error Codes in COM</span></span>](error-codes-in-com.md)

 

 