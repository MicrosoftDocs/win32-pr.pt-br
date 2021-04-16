---
title: Gerenciando o tempo de vida de um objeto
description: Saiba como gerenciar os métodos AddRef e Release para controlar o tempo de vida de um objeto.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104566145"
---
# <a name="managing-the-lifetime-of-an-object"></a><span data-ttu-id="9a963-103">Gerenciando o tempo de vida de um objeto</span><span class="sxs-lookup"><span data-stu-id="9a963-103">Managing the Lifetime of an Object</span></span>

<span data-ttu-id="9a963-104">Há uma regra para interfaces COM que ainda não mencionamos.</span><span class="sxs-lookup"><span data-stu-id="9a963-104">There is a rule for COM interfaces that we have not yet mentioned.</span></span> <span data-ttu-id="9a963-105">Cada interface COM deve herdar, direta ou indiretamente, de uma interface chamada [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="9a963-105">Every COM interface must inherit, directly or indirectly, from an interface named [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="9a963-106">Essa interface fornece alguns recursos de linha de base para os quais todos os objetos COM devem dar suporte.</span><span class="sxs-lookup"><span data-stu-id="9a963-106">This interface provides some baseline capabilities that all COM objects must support.</span></span>

<span data-ttu-id="9a963-107">A interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) define três métodos:</span><span class="sxs-lookup"><span data-stu-id="9a963-107">The [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface defines three methods:</span></span>

-   <span data-ttu-id="9a963-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="9a963-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
-   [<span data-ttu-id="9a963-109">**AddRef**</span><span class="sxs-lookup"><span data-stu-id="9a963-109">**AddRef**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [<span data-ttu-id="9a963-110">**Versão**</span><span class="sxs-lookup"><span data-stu-id="9a963-110">**Release**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

<span data-ttu-id="9a963-111">O método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) permite que um programa consulte os recursos do objeto em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="9a963-111">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method enables a program to query the capabilities of the object at run time.</span></span> <span data-ttu-id="9a963-112">Vamos falar mais sobre isso no próximo tópico, [solicitando um objeto para uma interface](asking-an-object-for-an-interface.md).</span><span class="sxs-lookup"><span data-stu-id="9a963-112">We'll say more about that in the next topic, [Asking an Object for an Interface](asking-an-object-for-an-interface.md).</span></span> <span data-ttu-id="9a963-113">Os métodos [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) são usados para controlar o tempo de vida de um objeto.</span><span class="sxs-lookup"><span data-stu-id="9a963-113">The [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are used to control the lifetime of an object.</span></span> <span data-ttu-id="9a963-114">Este é o assunto deste tópico.</span><span class="sxs-lookup"><span data-stu-id="9a963-114">This is the subject of this topic.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="9a963-115">Contagem de referência</span><span class="sxs-lookup"><span data-stu-id="9a963-115">Reference Counting</span></span>

<span data-ttu-id="9a963-116">Independentemente do que mais um programa possa fazer, em algum momento ele alocará e liberará recursos.</span><span class="sxs-lookup"><span data-stu-id="9a963-116">Whatever else a program might do, at some point it will allocate and free resources.</span></span> <span data-ttu-id="9a963-117">A alocação de um recurso é fácil.</span><span class="sxs-lookup"><span data-stu-id="9a963-117">Allocating a resource is easy.</span></span> <span data-ttu-id="9a963-118">Saber quando liberar o recurso é difícil, especialmente se o tempo de vida do recurso se estender além do escopo atual.</span><span class="sxs-lookup"><span data-stu-id="9a963-118">Knowing when to free the resource is hard, especially if the lifetime of the resource extends beyond the current scope.</span></span> <span data-ttu-id="9a963-119">Esse problema não é exclusivo do COM.</span><span class="sxs-lookup"><span data-stu-id="9a963-119">This problem is not unique to COM.</span></span> <span data-ttu-id="9a963-120">Qualquer programa que aloca memória de heap deve resolver o mesmo problema.</span><span class="sxs-lookup"><span data-stu-id="9a963-120">Any program that allocates heap memory must solve the same problem.</span></span> <span data-ttu-id="9a963-121">Por exemplo, o C++ usa destruidores automáticos, enquanto C# e Java usam coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="9a963-121">For example, C++ uses automatic destructors, while C# and Java use garbage collection.</span></span> <span data-ttu-id="9a963-122">COM usa uma abordagem chamada *contagem de referência*.</span><span class="sxs-lookup"><span data-stu-id="9a963-122">COM uses an approach called *reference counting*.</span></span>

<span data-ttu-id="9a963-123">Cada objeto COM mantém uma contagem interna.</span><span class="sxs-lookup"><span data-stu-id="9a963-123">Every COM object maintains an internal count.</span></span> <span data-ttu-id="9a963-124">Isso é conhecido como a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="9a963-124">This is known as the reference count.</span></span> <span data-ttu-id="9a963-125">A contagem de referência acompanha Quantas referências ao objeto estão ativas no momento.</span><span class="sxs-lookup"><span data-stu-id="9a963-125">The reference count tracks how many references to the object are currently active.</span></span> <span data-ttu-id="9a963-126">Quando o número de referências cai para zero, o objeto se exclui.</span><span class="sxs-lookup"><span data-stu-id="9a963-126">When the number of references drops to zero, the object deletes itself.</span></span> <span data-ttu-id="9a963-127">A última parte vale a pena repetir: o objeto se exclui.</span><span class="sxs-lookup"><span data-stu-id="9a963-127">The last part is worth repeating: The object deletes itself.</span></span> <span data-ttu-id="9a963-128">O programa nunca exclui explicitamente o objeto.</span><span class="sxs-lookup"><span data-stu-id="9a963-128">The program never explicitly deletes the object.</span></span>

<span data-ttu-id="9a963-129">Aqui estão as regras para a contagem de referência:</span><span class="sxs-lookup"><span data-stu-id="9a963-129">Here are the rules for reference counting:</span></span>

-   <span data-ttu-id="9a963-130">Quando o objeto é criado pela primeira vez, sua contagem de referência é 1.</span><span class="sxs-lookup"><span data-stu-id="9a963-130">When the object is first created, its reference count is 1.</span></span> <span data-ttu-id="9a963-131">Neste ponto, o programa tem um único ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="9a963-131">At this point, the program has a single pointer to the object.</span></span>
-   <span data-ttu-id="9a963-132">O programa pode criar uma nova referência duplicando (copiando) o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="9a963-132">The program can create a new reference by duplicating (copying) the pointer.</span></span> <span data-ttu-id="9a963-133">Ao copiar o ponteiro, você deve chamar o método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) do objeto.</span><span class="sxs-lookup"><span data-stu-id="9a963-133">When you copy the pointer, you must call the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method of the object.</span></span> <span data-ttu-id="9a963-134">Esse método incrementa a contagem de referência em uma.</span><span class="sxs-lookup"><span data-stu-id="9a963-134">This method increments the reference count by one.</span></span>
-   <span data-ttu-id="9a963-135">Quando você terminar de usar um ponteiro para o objeto, deverá chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="9a963-135">When you are finished using a pointer to the object, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="9a963-136">O método **Release** decrementa a contagem de referência em uma.</span><span class="sxs-lookup"><span data-stu-id="9a963-136">The **Release** method decrements the reference count by one.</span></span> <span data-ttu-id="9a963-137">Ele também invalida o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="9a963-137">It also invalidates the pointer.</span></span> <span data-ttu-id="9a963-138">Não use o ponteiro novamente depois de chamar a **versão**.</span><span class="sxs-lookup"><span data-stu-id="9a963-138">Do not use the pointer again after you call **Release**.</span></span> <span data-ttu-id="9a963-139">(Se você tiver outros ponteiros para o mesmo objeto, poderá continuar a usar esses ponteiros.)</span><span class="sxs-lookup"><span data-stu-id="9a963-139">(If you have other pointers to the same object, you can continue to use those pointers.)</span></span>
-   <span data-ttu-id="9a963-140">Quando você tiver chamado [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) com cada ponteiro, a contagem de referência de objeto do objeto chegará a zero e o objeto se excluirá.</span><span class="sxs-lookup"><span data-stu-id="9a963-140">When you have called [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with every pointer, the object reference count of the object reaches zero, and the object deletes itself.</span></span>

<span data-ttu-id="9a963-141">O diagrama a seguir mostra um caso simples, mas típico.</span><span class="sxs-lookup"><span data-stu-id="9a963-141">The following diagram shows a simple but typical case.</span></span>

![Diagrama que mostra um caso simples de contagem de referência.](images/com04.png)

<span data-ttu-id="9a963-143">O programa cria um objeto e armazena um ponteiro (*p*) para o objeto.</span><span class="sxs-lookup"><span data-stu-id="9a963-143">The program creates an object and stores a pointer (*p*) to the object.</span></span> <span data-ttu-id="9a963-144">Neste ponto, a contagem de referência é 1.</span><span class="sxs-lookup"><span data-stu-id="9a963-144">At this point, the reference count is 1.</span></span> <span data-ttu-id="9a963-145">Quando o programa for concluído usando o ponteiro, ele chamará [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="9a963-145">When the program is finished using the pointer, it calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="9a963-146">A contagem de referência é diminuída para zero e o objeto se exclui.</span><span class="sxs-lookup"><span data-stu-id="9a963-146">The reference count is decremented to zero, and the object deletes itself.</span></span> <span data-ttu-id="9a963-147">Agora, *p* é inválido.</span><span class="sxs-lookup"><span data-stu-id="9a963-147">Now *p* is invalid.</span></span> <span data-ttu-id="9a963-148">É um erro usar *p* para qualquer chamada de método adicional.</span><span class="sxs-lookup"><span data-stu-id="9a963-148">It is an error to use *p* for any further method calls.</span></span>

<span data-ttu-id="9a963-149">O próximo diagrama mostra um exemplo mais complexo.</span><span class="sxs-lookup"><span data-stu-id="9a963-149">The next diagram shows a more complex example.</span></span>

![ilustração que mostra a contagem de referência](images/com05.png)

<span data-ttu-id="9a963-151">Aqui, o programa cria um objeto e armazena o ponteiro *p*, como antes.</span><span class="sxs-lookup"><span data-stu-id="9a963-151">Here, the program creates an object and stores the pointer *p*, as before.</span></span> <span data-ttu-id="9a963-152">Em seguida, o programa copia *p* para uma nova variável, *p*.</span><span class="sxs-lookup"><span data-stu-id="9a963-152">Next, the program copies *p* to a new variable, *q*.</span></span> <span data-ttu-id="9a963-153">Neste ponto, o programa deve chamar [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para incrementar a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="9a963-153">At this point, the program must call [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) to increment the reference count.</span></span> <span data-ttu-id="9a963-154">A contagem de referência agora é 2, e há dois ponteiros válidos para o objeto.</span><span class="sxs-lookup"><span data-stu-id="9a963-154">The reference count is now 2, and there are two valid pointers to the object.</span></span> <span data-ttu-id="9a963-155">Agora suponha que o programa termine de usar *p*.</span><span class="sxs-lookup"><span data-stu-id="9a963-155">Now suppose that the program is finished using *p*.</span></span> <span data-ttu-id="9a963-156">O programa chama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), a contagem de referência vai para 1 e *p* não é mais válida.</span><span class="sxs-lookup"><span data-stu-id="9a963-156">The program calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), the reference count goes to 1, and *p* is no longer valid.</span></span> <span data-ttu-id="9a963-157">No entanto, *p* ainda é válido.</span><span class="sxs-lookup"><span data-stu-id="9a963-157">However, *q* is still valid.</span></span> <span data-ttu-id="9a963-158">Posteriormente, o programa terminará de usar *q*.</span><span class="sxs-lookup"><span data-stu-id="9a963-158">Later, the program finishes using *q*.</span></span> <span data-ttu-id="9a963-159">Portanto, ele chama **Release** novamente.</span><span class="sxs-lookup"><span data-stu-id="9a963-159">Therefore, it calls **Release** again.</span></span> <span data-ttu-id="9a963-160">A contagem de referência vai para zero e o objeto se exclui.</span><span class="sxs-lookup"><span data-stu-id="9a963-160">The reference count goes to zero, and the object deletes itself.</span></span>

<span data-ttu-id="9a963-161">Você deve estar imaginando por que o programa copiaria *p*.</span><span class="sxs-lookup"><span data-stu-id="9a963-161">You might wonder why the program would copy *p*.</span></span> <span data-ttu-id="9a963-162">Há dois motivos principais: primeiro, você pode desejar armazenar o ponteiro em uma estrutura de dados, como uma lista.</span><span class="sxs-lookup"><span data-stu-id="9a963-162">There are two main reasons: First, you might want to store the pointer in a data structure, such as a list.</span></span> <span data-ttu-id="9a963-163">Em segundo lugar, talvez você queira manter o ponteiro além do escopo atual da variável original.</span><span class="sxs-lookup"><span data-stu-id="9a963-163">Second, you might want to keep the pointer beyond the current scope of the original variable.</span></span> <span data-ttu-id="9a963-164">Portanto, você o copiaria para uma nova variável com um escopo maior.</span><span class="sxs-lookup"><span data-stu-id="9a963-164">Therefore, you would copy it to a new variable with wider scope.</span></span>

<span data-ttu-id="9a963-165">Uma vantagem da contagem de referência é que você pode compartilhar ponteiros entre diferentes seções de código, sem os vários caminhos de código que coordenam para excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="9a963-165">One advantage of reference counting is that you can share pointers across different sections of code, without the various code paths coordinating to delete the object.</span></span> <span data-ttu-id="9a963-166">Em vez disso, cada caminho de código simplesmente chama [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando o caminho do código é feito usando o objeto.</span><span class="sxs-lookup"><span data-stu-id="9a963-166">Instead, each code path merely calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when that code path is done using the object.</span></span> <span data-ttu-id="9a963-167">O objeto lida com a exclusão no horário correto.</span><span class="sxs-lookup"><span data-stu-id="9a963-167">The object handles deleting itself at the correct time.</span></span>

## <a name="example"></a><span data-ttu-id="9a963-168">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9a963-168">Example</span></span>

<span data-ttu-id="9a963-169">Aqui está o código do [exemplo da caixa de diálogo abrir](example--the-open-dialog-box.md) novamente.</span><span class="sxs-lookup"><span data-stu-id="9a963-169">Here is the code from the [Open dialog box example](example--the-open-dialog-box.md) again.</span></span>

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

<span data-ttu-id="9a963-170">A contagem de referência ocorre em dois locais neste código.</span><span class="sxs-lookup"><span data-stu-id="9a963-170">Reference counting occurs in two places in this code.</span></span> <span data-ttu-id="9a963-171">Primeiro, se o programa criar com êxito o objeto de caixa de diálogo de item comum, ele deverá chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) no ponteiro *pFileOpen* .</span><span class="sxs-lookup"><span data-stu-id="9a963-171">First, if program successfully creates the Common Item Dialog object, it must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pFileOpen* pointer.</span></span>

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

<span data-ttu-id="9a963-172">Em segundo lugar, quando o método [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) retorna um ponteiro para a interface [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , o programa deve chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) no ponteiro *pItem* .</span><span class="sxs-lookup"><span data-stu-id="9a963-172">Second, when the [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method returns a pointer to the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, the program must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pItem* pointer.</span></span>

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

<span data-ttu-id="9a963-173">Observe que em ambos os casos, a chamada de [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) é a última coisa que acontece antes que o ponteiro saia do escopo.</span><span class="sxs-lookup"><span data-stu-id="9a963-173">Notice that in both cases, the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call is the last thing that happens before the pointer goes out of scope.</span></span> <span data-ttu-id="9a963-174">Observe também que a **versão** é chamada somente depois de testar o **HRESULT** para obter êxito.</span><span class="sxs-lookup"><span data-stu-id="9a963-174">Also notice that **Release** is called only after you test the **HRESULT** for success.</span></span> <span data-ttu-id="9a963-175">Por exemplo, se a chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) falhar, o ponteiro *pFileOpen* não será válido.</span><span class="sxs-lookup"><span data-stu-id="9a963-175">For example, if the call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails, the *pFileOpen* pointer is not valid.</span></span> <span data-ttu-id="9a963-176">Portanto, seria um erro para chamar **Release** no ponteiro.</span><span class="sxs-lookup"><span data-stu-id="9a963-176">Therefore, it would be an error to call **Release** on the pointer.</span></span>

## <a name="next"></a><span data-ttu-id="9a963-177">Avançar</span><span class="sxs-lookup"><span data-stu-id="9a963-177">Next</span></span>

[<span data-ttu-id="9a963-178">Solicitando um objeto para uma interface</span><span class="sxs-lookup"><span data-stu-id="9a963-178">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)