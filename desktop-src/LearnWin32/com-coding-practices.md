---
title: Práticas de codificação COM
description: Este tópico descreve maneiras de tornar seu código COM mais eficiente e robusto.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104084962"
---
# <a name="com-coding-practices"></a><span data-ttu-id="89b51-103">Práticas de codificação COM</span><span class="sxs-lookup"><span data-stu-id="89b51-103">COM Coding Practices</span></span>

<span data-ttu-id="89b51-104">Este tópico descreve maneiras de tornar seu código COM mais eficiente e robusto.</span><span class="sxs-lookup"><span data-stu-id="89b51-104">This topic describes ways to make your COM code more effective and robust.</span></span>

-   [<span data-ttu-id="89b51-105">O \_ \_ operador uuidof</span><span class="sxs-lookup"><span data-stu-id="89b51-105">The \_\_uuidof Operator</span></span>](/windows)
-   [<span data-ttu-id="89b51-106">A \_ macro IID PPV \_ args</span><span class="sxs-lookup"><span data-stu-id="89b51-106">The IID\_PPV\_ARGS Macro</span></span>](/windows)
-   [<span data-ttu-id="89b51-107">O padrão SafeRelease</span><span class="sxs-lookup"><span data-stu-id="89b51-107">The SafeRelease Pattern</span></span>](#the-saferelease-pattern)
-   [<span data-ttu-id="89b51-108">Ponteiros inteligentes COM</span><span class="sxs-lookup"><span data-stu-id="89b51-108">COM Smart Pointers</span></span>](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a><span data-ttu-id="89b51-109">O \_ \_ operador uuidof</span><span class="sxs-lookup"><span data-stu-id="89b51-109">The \_\_uuidof Operator</span></span>

<span data-ttu-id="89b51-110">Ao compilar seu programa, você pode obter erros de vinculador semelhantes ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="89b51-110">When you build your program, you might get linker errors similar to the following:</span></span>

`unresolved external symbol "struct _GUID const IID_IDrawable"`

<span data-ttu-id="89b51-111">Esse erro significa que uma constante GUID foi declarada com ligação externa (**externa**) e o vinculador não pôde localizar a definição da constante.</span><span class="sxs-lookup"><span data-stu-id="89b51-111">This error means that a GUID constant was declared with external linkage (**extern**), and the linker could not find the definition of the constant.</span></span> <span data-ttu-id="89b51-112">O valor de uma constante de GUID geralmente é exportado de um arquivo de biblioteca estático.</span><span class="sxs-lookup"><span data-stu-id="89b51-112">The value of a GUID constant is usually exported from a static library file.</span></span> <span data-ttu-id="89b51-113">Se você estiver usando Microsoft Visual C++, poderá evitar a necessidade de vincular uma biblioteca estática usando o operador **\_ \_ uuidof** .</span><span class="sxs-lookup"><span data-stu-id="89b51-113">If you are using Microsoft Visual C++, you can avoid the need to link a static library by using the **\_\_uuidof** operator.</span></span> <span data-ttu-id="89b51-114">Esse operador é uma extensão de idioma da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="89b51-114">This operator is a Microsoft language extension.</span></span> <span data-ttu-id="89b51-115">Ele retorna um valor GUID de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="89b51-115">It returns a GUID value from an expression.</span></span> <span data-ttu-id="89b51-116">A expressão pode ser um nome de tipo de interface, um nome de classe ou um ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="89b51-116">The expression can be an interface type name, a class name, or an interface pointer.</span></span> <span data-ttu-id="89b51-117">Usando o **\_ \_ uuidof**, você pode criar o objeto de caixa de diálogo de item comum da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="89b51-117">Using **\_\_uuidof**, you can create the Common Item Dialog object as follows:</span></span>


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



<span data-ttu-id="89b51-118">O compilador extrai o valor de GUID do cabeçalho, portanto, nenhuma exportação de biblioteca é necessária.</span><span class="sxs-lookup"><span data-stu-id="89b51-118">The compiler extracts the GUID value from the header, so no library export is necessary.</span></span>

> [!Note]  
> <span data-ttu-id="89b51-119">O valor de GUID é associado ao nome do tipo declarando `__declspec(uuid( ... ))` no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="89b51-119">The GUID value is associated with the type name by declaring `__declspec(uuid( ... ))` in the header.</span></span> <span data-ttu-id="89b51-120">Para obter mais informações, consulte a documentação do **\_ \_ declspec** na documentação do Visual C++.</span><span class="sxs-lookup"><span data-stu-id="89b51-120">For more information, see the documentation for **\_\_declspec** in the Visual C++ documentation.</span></span>

 

## <a name="the-iid_ppv_args-macro"></a><span data-ttu-id="89b51-121">A \_ macro IID PPV \_ args</span><span class="sxs-lookup"><span data-stu-id="89b51-121">The IID\_PPV\_ARGS Macro</span></span>

<span data-ttu-id="89b51-122">Vimos que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) exigem a coerção do parâmetro final para um tipo **void \* \*** .</span><span class="sxs-lookup"><span data-stu-id="89b51-122">We saw that both [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) require coercing the final parameter to a **void\*\*** type.</span></span> <span data-ttu-id="89b51-123">Isso cria o potencial para uma incompatibilidade de tipo.</span><span class="sxs-lookup"><span data-stu-id="89b51-123">This creates the potential for a type mismatch.</span></span> <span data-ttu-id="89b51-124">Considere o fragmento de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="89b51-124">Consider the following code fragment:</span></span>


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



<span data-ttu-id="89b51-125">Esse código solicita a interface [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , mas passa um ponteiro [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="89b51-125">This code asks for the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface, but passes in an [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer.</span></span> <span data-ttu-id="89b51-126">A expressão de **\_ conversão de reinterpretação** evita o sistema de tipos C++, portanto, o compilador não capturará esse erro.</span><span class="sxs-lookup"><span data-stu-id="89b51-126">The **reinterpret\_cast** expression circumvents the C++ type system, so the compiler will not catch this error.</span></span> <span data-ttu-id="89b51-127">Na melhor das hipóteses, se o objeto não implementar a interface solicitada, a chamada simplesmente falhará.</span><span class="sxs-lookup"><span data-stu-id="89b51-127">In the best case, if the object does not implement the requested interface, the call simply fails.</span></span> <span data-ttu-id="89b51-128">Na pior das hipóteses, a função é bem sucedido e você tem um ponteiro incompatível.</span><span class="sxs-lookup"><span data-stu-id="89b51-128">In the worst case, the function succeeds and you have a mismatched pointer.</span></span> <span data-ttu-id="89b51-129">Em outras palavras, o tipo de ponteiro não corresponde à vtable real na memória.</span><span class="sxs-lookup"><span data-stu-id="89b51-129">In other words, the pointer type does not match the actual vtable in memory.</span></span> <span data-ttu-id="89b51-130">Como você pode imaginar, nada bom pode acontecer nesse ponto.</span><span class="sxs-lookup"><span data-stu-id="89b51-130">As you can imagine, nothing good can happen at that point.</span></span>

> [!Note]  
> <span data-ttu-id="89b51-131">Uma *vtable* (tabela de método virtual) é uma tabela de ponteiros de função.</span><span class="sxs-lookup"><span data-stu-id="89b51-131">A *vtable* (virtual method table) is a table of function pointers.</span></span> <span data-ttu-id="89b51-132">A vtable é como o COM associa uma chamada de método à sua implementação em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="89b51-132">The vtable is how COM binds a method call to its implementation at run time.</span></span> <span data-ttu-id="89b51-133">Não coincidentemente, as vtables são como a maioria dos compiladores C++ implementam métodos virtuais.</span><span class="sxs-lookup"><span data-stu-id="89b51-133">Not coincidentally, vtables are how most C++ compilers implement virtual methods.</span></span>

 

<span data-ttu-id="89b51-134">A macro [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) ajuda a evitar essa classe de erro.</span><span class="sxs-lookup"><span data-stu-id="89b51-134">The [**IID\_PPV\_ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) macro helps to avoid this class of error.</span></span> <span data-ttu-id="89b51-135">Para usar essa macro, substitua o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="89b51-135">To use this macro, replace the following code:</span></span>


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



<span data-ttu-id="89b51-136">por este:</span><span class="sxs-lookup"><span data-stu-id="89b51-136">with this:</span></span>


```C++
IID_PPV_ARGS(&pFileOpen)
```



<span data-ttu-id="89b51-137">A macro é inserida automaticamente `__uuidof(IFileOpenDialog)` para o identificador de interface, portanto, é garantido que ela corresponda ao tipo de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="89b51-137">The macro automatically inserts `__uuidof(IFileOpenDialog)` for the interface identifier, so it is guaranteed to match the pointer type.</span></span> <span data-ttu-id="89b51-138">Este é o código modificado (e correto):</span><span class="sxs-lookup"><span data-stu-id="89b51-138">Here is the modified (and correct) code:</span></span>


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



<span data-ttu-id="89b51-139">Você pode usar a mesma macro com [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="89b51-139">You can use the same macro with [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a><span data-ttu-id="89b51-140">O padrão SafeRelease</span><span class="sxs-lookup"><span data-stu-id="89b51-140">The SafeRelease Pattern</span></span>

<span data-ttu-id="89b51-141">A contagem de referência é uma das coisas na programação que é basicamente fácil, mas também é entediante, o que torna mais fácil ficar errado.</span><span class="sxs-lookup"><span data-stu-id="89b51-141">Reference counting is one of those things in programming that is basically easy, but is also tedious, which makes it easy to get wrong.</span></span> <span data-ttu-id="89b51-142">Os erros típicos incluem:</span><span class="sxs-lookup"><span data-stu-id="89b51-142">Typical errors include:</span></span>

-   <span data-ttu-id="89b51-143">Falha ao liberar um ponteiro de interface quando você terminar de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="89b51-143">Failing to release an interface pointer when you are done using it.</span></span> <span data-ttu-id="89b51-144">Essa classe de bug fará com que o programa vazasse memória e outros recursos, porque os objetos não são destruídos.</span><span class="sxs-lookup"><span data-stu-id="89b51-144">This class of bug will cause your program to leak memory and other resources, because objects are not destroyed.</span></span>
-   <span data-ttu-id="89b51-145">Chamando a [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) com um ponteiro inválido.</span><span class="sxs-lookup"><span data-stu-id="89b51-145">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with an invalid pointer.</span></span> <span data-ttu-id="89b51-146">Por exemplo, esse erro pode ocorrer se o objeto nunca foi criado.</span><span class="sxs-lookup"><span data-stu-id="89b51-146">For example, this error can happen if the object was never created.</span></span> <span data-ttu-id="89b51-147">Essa categoria de bug provavelmente causará falha no seu programa.</span><span class="sxs-lookup"><span data-stu-id="89b51-147">This category of bug will probably cause your program to crash.</span></span>
-   <span data-ttu-id="89b51-148">A desreferência de um ponteiro de interface após a [**liberação**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) é chamada.</span><span class="sxs-lookup"><span data-stu-id="89b51-148">Dereferencing an interface pointer after [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) is called.</span></span> <span data-ttu-id="89b51-149">Esse bug pode fazer com que o programa falhe.</span><span class="sxs-lookup"><span data-stu-id="89b51-149">This bug may cause your program to crash.</span></span> <span data-ttu-id="89b51-150">Pior, pode fazer com que seu programa falhe em um momento aleatório, o que dificulta o rastreamento do erro original.</span><span class="sxs-lookup"><span data-stu-id="89b51-150">Worse, it may cause your program to crash at a random later time, making it hard to track down the original error.</span></span>

<span data-ttu-id="89b51-151">Uma maneira de evitar esses bugs é chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) por meio de uma função que libera com segurança o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="89b51-151">One way to avoid these bugs is to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) through a function that safely releases the pointer.</span></span> <span data-ttu-id="89b51-152">O código a seguir mostra uma função que faz isso:</span><span class="sxs-lookup"><span data-stu-id="89b51-152">The following code shows a function that does this:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



<span data-ttu-id="89b51-153">Essa função usa um ponteiro de interface COM como um parâmetro e faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="89b51-153">This function takes a COM interface pointer as a parameter and does the following:</span></span>

1.  <span data-ttu-id="89b51-154">Verifica se o ponteiro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="89b51-154">Checks whether the pointer is **NULL**.</span></span>
2.  <span data-ttu-id="89b51-155">Chama a [**versão**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se o ponteiro não for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="89b51-155">Calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) if the pointer is not **NULL**.</span></span>
3.  <span data-ttu-id="89b51-156">Define o ponteiro como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="89b51-156">Sets the pointer to **NULL**.</span></span>

<span data-ttu-id="89b51-157">Aqui está um exemplo de como usar `SafeRelease` :</span><span class="sxs-lookup"><span data-stu-id="89b51-157">Here is an example of how to use `SafeRelease`:</span></span>


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



<span data-ttu-id="89b51-158">Se [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) for executado com sucesso, a chamada para `SafeRelease` liberar o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="89b51-158">If [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) succeeds, the call to `SafeRelease` releases the pointer.</span></span> <span data-ttu-id="89b51-159">Se **CoCreateInstance** falhar, *PFileOpen* permanecerá **nulo**.</span><span class="sxs-lookup"><span data-stu-id="89b51-159">If **CoCreateInstance** fails, *pFileOpen* remains **NULL**.</span></span> <span data-ttu-id="89b51-160">A `SafeRelease` função verifica isso e ignora a chamada para [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="89b51-160">The `SafeRelease` function checks for this and skips the call to [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span>

<span data-ttu-id="89b51-161">Também é seguro chamar `SafeRelease` mais de uma vez no mesmo ponteiro, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="89b51-161">It is also safe to call `SafeRelease` more than once on the same pointer, as shown here:</span></span>


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a><span data-ttu-id="89b51-162">Ponteiros inteligentes COM</span><span class="sxs-lookup"><span data-stu-id="89b51-162">COM Smart Pointers</span></span>

<span data-ttu-id="89b51-163">A `SafeRelease` função é útil, mas exige que você se lembre de duas coisas:</span><span class="sxs-lookup"><span data-stu-id="89b51-163">The `SafeRelease` function is useful, but it requires you to remember two things:</span></span>

-   <span data-ttu-id="89b51-164">Inicializar cada ponteiro de interface como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="89b51-164">Initialize every interface pointer to **NULL**.</span></span>
-   <span data-ttu-id="89b51-165">Chame `SafeRelease` antes de cada ponteiro sair do escopo.</span><span class="sxs-lookup"><span data-stu-id="89b51-165">Call `SafeRelease` before each pointer goes out of scope.</span></span>

<span data-ttu-id="89b51-166">Como programador de C++, você provavelmente está pensando que não deve ter que se lembrar dessas coisas.</span><span class="sxs-lookup"><span data-stu-id="89b51-166">As a C++ programmer, you are probably thinking that you shouldn't have to remember either of these things.</span></span> <span data-ttu-id="89b51-167">Afinal, é por isso que o C++ tem construtores e destruidores.</span><span class="sxs-lookup"><span data-stu-id="89b51-167">After all, that's why C++ has constructors and destructors.</span></span> <span data-ttu-id="89b51-168">Seria interessante ter uma classe que encapsulasse o ponteiro de interface subjacente, inicializando e liberando automaticamente o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="89b51-168">It would be nice to have a class that wraps the underlying interface pointer and automatically initializes and releases the pointer.</span></span> <span data-ttu-id="89b51-169">Em outras palavras, queremos algo assim:</span><span class="sxs-lookup"><span data-stu-id="89b51-169">In other words, we want something like this:</span></span>


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



<span data-ttu-id="89b51-170">A definição de classe mostrada aqui está incompleta e não pode ser usada como mostrado.</span><span class="sxs-lookup"><span data-stu-id="89b51-170">The class definition shown here is incomplete, and is not usable as shown.</span></span> <span data-ttu-id="89b51-171">No mínimo, você precisaria definir um construtor de cópia, um operador de atribuição e uma maneira de acessar o ponteiro COM subjacente.</span><span class="sxs-lookup"><span data-stu-id="89b51-171">At a minimum, you would need to define a copy constructor, an assignment operator, and a way to access the underlying COM pointer.</span></span> <span data-ttu-id="89b51-172">Felizmente, você não precisa fazer nenhum trabalho, porque Microsoft Visual Studio já fornece uma classe de ponteiro inteligente como parte do Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="89b51-172">Fortunately, you don't need to do any of this work, because Microsoft Visual Studio already provides a smart pointer class as part of the Active Template Library (ATL).</span></span>

<span data-ttu-id="89b51-173">A classe de ponteiro inteligente ATL é denominada **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="89b51-173">The ATL smart pointer class is named **CComPtr**.</span></span> <span data-ttu-id="89b51-174">(Há também uma classe **CComQIPtr** , que não é discutida aqui.) Aqui está o exemplo de [caixa de diálogo aberta](example--the-open-dialog-box.md) reescrito para usar **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="89b51-174">(There is also a **CComQIPtr** class, which is not discussed here.) Here is the [Open Dialog Box](example--the-open-dialog-box.md) example rewritten to use **CComPtr**.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="89b51-175">A principal diferença entre esse código e o exemplo original é que essa versão não chama explicitamente [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="89b51-175">The main difference between this code and the original example is that this version does not explicitly call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="89b51-176">Quando a instância **CComPtr** sai do escopo, o destruidor chama **Release** no ponteiro subjacente.</span><span class="sxs-lookup"><span data-stu-id="89b51-176">When the **CComPtr** instance goes out of scope, the destructor calls **Release** on the underlying pointer.</span></span>

<span data-ttu-id="89b51-177">**CComPtr** é um modelo de classe.</span><span class="sxs-lookup"><span data-stu-id="89b51-177">**CComPtr** is a class template.</span></span> <span data-ttu-id="89b51-178">O argumento de modelo é o tipo de interface COM.</span><span class="sxs-lookup"><span data-stu-id="89b51-178">The template argument is the COM interface type.</span></span> <span data-ttu-id="89b51-179">Internamente, **CComPtr** mantém um ponteiro desse tipo.</span><span class="sxs-lookup"><span data-stu-id="89b51-179">Internally, **CComPtr** holds a pointer of that type.</span></span> <span data-ttu-id="89b51-180">**CComPtr** substitui **Operator-> ()** e **operador& ()** para que a classe atue como o ponteiro subjacente.</span><span class="sxs-lookup"><span data-stu-id="89b51-180">**CComPtr** overrides **operator->()** and **operator&()** so that the class acts like the underlying pointer.</span></span> <span data-ttu-id="89b51-181">Por exemplo, o código a seguir é equivalente a chamar o método **IFileOpenDialog:: show** diretamente:</span><span class="sxs-lookup"><span data-stu-id="89b51-181">For example, the following code is equivalent to calling the **IFileOpenDialog::Show** method directly:</span></span>


```C++
hr = pFileOpen->Show(NULL);
```



<span data-ttu-id="89b51-182">**CComPtr** também define um método **CComPtr:: CoCreateInstance** , que chama a função com [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com alguns valores de parâmetro padrão.</span><span class="sxs-lookup"><span data-stu-id="89b51-182">**CComPtr** also defines a **CComPtr::CoCreateInstance** method, which calls the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function with some default parameter values.</span></span> <span data-ttu-id="89b51-183">O único parâmetro necessário é o identificador de classe, como mostra o exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="89b51-183">The only required parameter is the class identifier, as the next example shows:</span></span>


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



<span data-ttu-id="89b51-184">O método **CComPtr:: CoCreateInstance** é fornecido puramente como uma conveniência; Você ainda pode chamar a função de [**COCREATEINSTANCE**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com, se preferir.</span><span class="sxs-lookup"><span data-stu-id="89b51-184">The **CComPtr::CoCreateInstance** method is provided purely as a convenience; you can still call the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, if you prefer.</span></span>

## <a name="next"></a><span data-ttu-id="89b51-185">Avançar</span><span class="sxs-lookup"><span data-stu-id="89b51-185">Next</span></span>

[<span data-ttu-id="89b51-186">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="89b51-186">Error Handling in COM</span></span>](error-handling-in-com.md)

 

 