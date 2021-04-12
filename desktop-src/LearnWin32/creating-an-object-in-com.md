---
title: Criando um objeto em COM
description: Para usar uma interface COM, seu programa primeiro cria uma instância de um objeto que implementa essa interface.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365924"
---
# <a name="creating-an-object-in-com"></a><span data-ttu-id="5e169-103">Criando um objeto em COM</span><span class="sxs-lookup"><span data-stu-id="5e169-103">Creating an Object in COM</span></span>

<span data-ttu-id="5e169-104">Depois que um thread inicializa a biblioteca COM, é seguro que o thread use interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="5e169-104">After a thread has initialized the COM library, it is safe for the thread to use COM interfaces.</span></span> <span data-ttu-id="5e169-105">Para usar uma interface COM, seu programa primeiro cria uma instância de um objeto que implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="5e169-105">To use a COM interface, your program first creates an instance of an object that implements that interface.</span></span>

<span data-ttu-id="5e169-106">Em geral, há duas maneiras de criar um objeto COM:</span><span class="sxs-lookup"><span data-stu-id="5e169-106">In general, there are two ways to create a COM object:</span></span>

-   <span data-ttu-id="5e169-107">O módulo que implementa o objeto pode fornecer uma função projetada especificamente para criar instâncias desse objeto.</span><span class="sxs-lookup"><span data-stu-id="5e169-107">The module that implements the object might provide a function specifically designed to create instances of that object.</span></span>
-   <span data-ttu-id="5e169-108">Como alternativa, COM fornece uma função de criação genérica chamada [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="5e169-108">Alternatively, COM provides a generic creation function named [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="5e169-109">Por exemplo, pegue o objeto hipotético `Shape` do tópico [o que é uma interface com?](what-is-a-com-interface-.md).</span><span class="sxs-lookup"><span data-stu-id="5e169-109">For example, take the hypothetical `Shape` object from the topic [What Is a COM Interface?](what-is-a-com-interface-.md).</span></span> <span data-ttu-id="5e169-110">Nesse exemplo, o `Shape` objeto implementa uma interface chamada `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="5e169-110">In that example, the `Shape` object implements an interface named `IDrawable`.</span></span> <span data-ttu-id="5e169-111">A biblioteca de gráficos que implementa o `Shape` objeto pode exportar uma função com a assinatura a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e169-111">The graphics library that implements the `Shape` object might export a function with the following signature.</span></span>


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



<span data-ttu-id="5e169-112">Dada essa função, você pode criar um novo `Shape` objeto da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5e169-112">Given this function, you could create a new `Shape` object as follows.</span></span>


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="5e169-113">O parâmetro *ppShape* é do tipo ponteiro para ponteiro para `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="5e169-113">The *ppShape* parameter is of type pointer-to-pointer-to-`IDrawable`.</span></span> <span data-ttu-id="5e169-114">Se você ainda não viu esse padrão antes, a dupla indireção pode ser enigmático.</span><span class="sxs-lookup"><span data-stu-id="5e169-114">If you have not seen this pattern before, the double indirection might be puzzling.</span></span>

<span data-ttu-id="5e169-115">Considere os requisitos da `CreateShape` função.</span><span class="sxs-lookup"><span data-stu-id="5e169-115">Consider the requirements of the `CreateShape` function.</span></span> <span data-ttu-id="5e169-116">A função deve dar um `IDrawable` ponteiro de volta ao chamador.</span><span class="sxs-lookup"><span data-stu-id="5e169-116">The function must give an `IDrawable` pointer back to the caller.</span></span> <span data-ttu-id="5e169-117">Mas o valor de retorno da função já é usado para o código de erro/êxito.</span><span class="sxs-lookup"><span data-stu-id="5e169-117">But the function's return value is already used for the error/success code.</span></span> <span data-ttu-id="5e169-118">Portanto, o ponteiro deve ser retornado por meio de um argumento para a função.</span><span class="sxs-lookup"><span data-stu-id="5e169-118">Therefore, the pointer must be returned through an argument to the function.</span></span> <span data-ttu-id="5e169-119">O chamador passará uma variável do tipo `IDrawable*` para a função e a função substituirá essa variável por um novo `IDrawable` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="5e169-119">The caller will pass a variable of type `IDrawable*` to the function, and the function will overwrite this variable with a new `IDrawable` pointer.</span></span> <span data-ttu-id="5e169-120">No C++, há apenas duas maneiras de uma função substituir um valor de parâmetro: passagem por referência ou passagem por endereço.</span><span class="sxs-lookup"><span data-stu-id="5e169-120">In C++, there are only two ways for a function to overwrite a parameter value: pass by reference, or pass by address.</span></span> <span data-ttu-id="5e169-121">COM usa o segundo, passagem por endereço.</span><span class="sxs-lookup"><span data-stu-id="5e169-121">COM uses the latter, pass-by-address.</span></span> <span data-ttu-id="5e169-122">E o endereço de um ponteiro é um ponteiro para ponteiro, portanto, o tipo de parâmetro deve ser `IDrawable**` .</span><span class="sxs-lookup"><span data-stu-id="5e169-122">And the address of a pointer is a pointer-to-a-pointer, so the parameter type must be `IDrawable**`.</span></span>

<span data-ttu-id="5e169-123">Aqui está um diagrama para ajudar a visualizar o que está acontecendo.</span><span class="sxs-lookup"><span data-stu-id="5e169-123">Here is a diagram to help visualize what's going on.</span></span>

![diagrama que mostra o indireção de ponteiro duplo](images/com03.png)

<span data-ttu-id="5e169-125">A `CreateShape` função usa o endereço de *pShape* ( `&pShape` ) para gravar um novo valor de ponteiro em *pShape*.</span><span class="sxs-lookup"><span data-stu-id="5e169-125">The `CreateShape` function uses the address of *pShape* (`&pShape`) to write a new pointer value to *pShape*.</span></span>

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a><span data-ttu-id="5e169-126">CoCreateInstance: uma maneira genérica de criar objetos</span><span class="sxs-lookup"><span data-stu-id="5e169-126">CoCreateInstance: A Generic Way to Create Objects</span></span>

<span data-ttu-id="5e169-127">A função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fornece um mecanismo genérico para a criação de objetos.</span><span class="sxs-lookup"><span data-stu-id="5e169-127">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function provides a generic mechanism for creating objects.</span></span> <span data-ttu-id="5e169-128">Para entender **CoCreateInstance**, tenha em mente que dois objetos com podem implementar a mesma interface e um objeto pode implementar duas ou mais interfaces.</span><span class="sxs-lookup"><span data-stu-id="5e169-128">To understand **CoCreateInstance**, keep in mind that two COM objects can implement the same interface, and one object can implement two or more interfaces.</span></span> <span data-ttu-id="5e169-129">Assim, uma função genérica que cria objetos precisa de duas informações.</span><span class="sxs-lookup"><span data-stu-id="5e169-129">Thus, a generic function that creates objects needs two pieces of information.</span></span>

-   <span data-ttu-id="5e169-130">Qual objeto criar.</span><span class="sxs-lookup"><span data-stu-id="5e169-130">Which object to create.</span></span>
-   <span data-ttu-id="5e169-131">Qual interface deve ser obtida do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e169-131">Which interface to get from the object.</span></span>

<span data-ttu-id="5e169-132">Mas como podemos indicar essas informações quando chamamos a função?</span><span class="sxs-lookup"><span data-stu-id="5e169-132">But how do we indicate this information when we call the function?</span></span> <span data-ttu-id="5e169-133">No COM, um objeto ou uma interface é identificado atribuindo-o um número de 128 bits, chamado de GUID ( *identificador global exclusivo* ).</span><span class="sxs-lookup"><span data-stu-id="5e169-133">In COM, an object or an interface is identified by assigning it a 128-bit number, called a *globally unique identifier* (GUID).</span></span> <span data-ttu-id="5e169-134">Os GUIDs são gerados de forma a torná-los efetivamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="5e169-134">GUIDs are generated in a way that makes them effectively unique.</span></span> <span data-ttu-id="5e169-135">Os GUIDs são uma solução para o problema de como criar identificadores exclusivos sem uma autoridade de registro central.</span><span class="sxs-lookup"><span data-stu-id="5e169-135">GUIDs are a solution to the problem of how to create unique identifiers without a central registration authority.</span></span> <span data-ttu-id="5e169-136">Os GUIDs são, às vezes, chamados de UUIDs ( *identificadores universalmente exclusivos* ).</span><span class="sxs-lookup"><span data-stu-id="5e169-136">GUIDs are sometimes called *universally unique identifiers* (UUIDs).</span></span> <span data-ttu-id="5e169-137">Antes do COM, eles eram usados em DCE/RPC (chamada de procedimento remoto/ambiente de computação distribuído).</span><span class="sxs-lookup"><span data-stu-id="5e169-137">Prior to COM, they were used in DCE/RPC (Distributed Computing Environment/Remote Procedure Call).</span></span> <span data-ttu-id="5e169-138">Existem vários algoritmos para criar novos GUIDs.</span><span class="sxs-lookup"><span data-stu-id="5e169-138">Several algorithms exist for creating new GUIDs.</span></span> <span data-ttu-id="5e169-139">Nem todos esses algoritmos garantem estritamente a exclusividade, mas a probabilidade de criar acidentalmente o mesmo valor de GUID duas vezes é extremamente pequena – efetivamente zero.</span><span class="sxs-lookup"><span data-stu-id="5e169-139">Not all of these algorithms strictly guarantee uniqueness, but the probability of accidentally creating the same GUID value twice is extremely small—effectively zero.</span></span> <span data-ttu-id="5e169-140">GUIDs podem ser usados para identificar qualquer tipo de entidade, não apenas objetos e interfaces.</span><span class="sxs-lookup"><span data-stu-id="5e169-140">GUIDs can be used to identify any sort of entity, not just objects and interfaces.</span></span> <span data-ttu-id="5e169-141">No entanto, esse é o único uso que se refere a nós neste módulo.</span><span class="sxs-lookup"><span data-stu-id="5e169-141">However, that is the only use that concerns us in this module.</span></span>

<span data-ttu-id="5e169-142">Por exemplo, a `Shapes` biblioteca pode declarar duas constantes de GUID:</span><span class="sxs-lookup"><span data-stu-id="5e169-142">For example, the `Shapes` library might declare two GUID constants:</span></span>


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



<span data-ttu-id="5e169-143">(Você pode assumir que os valores numéricos reais de 128 bits para essas constantes estão definidos em outro lugar.) A **\_ forma de CLSID** de constante identifica o `Shape` objeto, enquanto **o \_ IDrawable de IID** constante identifica a `IDrawable` interface.</span><span class="sxs-lookup"><span data-stu-id="5e169-143">(You can assume that the actual 128-bit numeric values for these constants are defined elsewhere.) The constant **CLSID\_Shape** identifies the `Shape` object, while the constant **IID\_IDrawable** identifies the `IDrawable` interface.</span></span> <span data-ttu-id="5e169-144">O prefixo "CLSID" significa *identificador de classe* e o *IID* de prefixo significa *identificador de interface*.</span><span class="sxs-lookup"><span data-stu-id="5e169-144">The prefix "CLSID" stands for *class identifier*, and the prefix *IID* stands for *interface identifier*.</span></span> <span data-ttu-id="5e169-145">Essas são convenções de nomenclatura padrão no COM.</span><span class="sxs-lookup"><span data-stu-id="5e169-145">These are standard naming conventions in COM.</span></span>

<span data-ttu-id="5e169-146">Considerando esses valores, você criaria uma nova `Shape` instância da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5e169-146">Given these values, you would create a new `Shape` instance as follows:</span></span>


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="5e169-147">A função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) tem cinco parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5e169-147">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function has five parameters.</span></span> <span data-ttu-id="5e169-148">O primeiro e o quarto parâmetros são o identificador de classe e o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="5e169-148">The first and fourth parameters are the class identifier and interface identifier.</span></span> <span data-ttu-id="5e169-149">Na verdade, esses parâmetros informam a função "criar o objeto Shape e me dar um ponteiro para a interface IDrawable".</span><span class="sxs-lookup"><span data-stu-id="5e169-149">In effect, these parameters tell the function, "Create the Shape object, and give me a pointer to the IDrawable interface."</span></span>

<span data-ttu-id="5e169-150">Defina o segundo parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5e169-150">Set the second parameter to **NULL**.</span></span> <span data-ttu-id="5e169-151">(Para obter mais informações sobre o significado desse parâmetro, consulte o tópico [agregação](/windows/desktop/com/aggregation) na documentação com.) O terceiro parâmetro usa um conjunto de sinalizadores cujo principal objetivo é especificar o *contexto de execução* para o objeto.</span><span class="sxs-lookup"><span data-stu-id="5e169-151">(For more information about the meaning of this parameter, see the topic [Aggregation](/windows/desktop/com/aggregation) in the COM documentation.) The third parameter takes a set of flags whose main purpose is to specify the *execution context* for the object.</span></span> <span data-ttu-id="5e169-152">O contexto de execução especifica se o objeto é executado no mesmo processo que o aplicativo; em um processo diferente no mesmo computador; ou em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="5e169-152">The execution context specifies whether the object runs in the same process as the application; in a different process on the same computer; or on a remote computer.</span></span> <span data-ttu-id="5e169-153">A tabela a seguir mostra os valores mais comuns para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5e169-153">The following table shows the most common values for this parameter.</span></span>



| <span data-ttu-id="5e169-154">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="5e169-154">Flag</span></span>                       | <span data-ttu-id="5e169-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e169-155">Description</span></span>                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e169-156">**\_servidor CLSCTX InProc \_**</span><span class="sxs-lookup"><span data-stu-id="5e169-156">**CLSCTX\_INPROC\_SERVER**</span></span> | <span data-ttu-id="5e169-157">Mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="5e169-157">Same process.</span></span>                                                                                                                                                      |
| <span data-ttu-id="5e169-158">**\_servidor local \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="5e169-158">**CLSCTX\_LOCAL\_SERVER**</span></span>  | <span data-ttu-id="5e169-159">Processo diferente, o mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="5e169-159">Different process, same computer.</span></span>                                                                                                                                  |
| <span data-ttu-id="5e169-160">**\_servidor remoto \_ CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="5e169-160">**CLSCTX\_REMOTE\_SERVER**</span></span> | <span data-ttu-id="5e169-161">Computador diferente.</span><span class="sxs-lookup"><span data-stu-id="5e169-161">Different computer.</span></span>                                                                                                                                                |
| <span data-ttu-id="5e169-162">**CLSCTX \_ tudo**</span><span class="sxs-lookup"><span data-stu-id="5e169-162">**CLSCTX\_ALL**</span></span>            | <span data-ttu-id="5e169-163">Use a opção mais eficiente para a qual o objeto dá suporte.</span><span class="sxs-lookup"><span data-stu-id="5e169-163">Use the most efficient option that the object supports.</span></span> <span data-ttu-id="5e169-164">(A classificação, da mais eficiente ao menos eficiente, é: em processo, fora do processo e entre computadores.)</span><span class="sxs-lookup"><span data-stu-id="5e169-164">(The ranking, from most efficient to least efficient, is: in-process, out-of-process, and cross-computer.)</span></span> |



 

<span data-ttu-id="5e169-165">A documentação de um componente específico pode informar a qual contexto de execução o objeto dá suporte.</span><span class="sxs-lookup"><span data-stu-id="5e169-165">The documentation for a particular component might tell you which execution context the object supports.</span></span> <span data-ttu-id="5e169-166">Caso contrário, use **CLSCTX \_ All**.</span><span class="sxs-lookup"><span data-stu-id="5e169-166">If not, use **CLSCTX\_ALL**.</span></span> <span data-ttu-id="5e169-167">Se você solicitar um contexto de execução ao qual o objeto não oferece suporte, a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retornará o código de erro **REGDB \_ E \_ CLASSNOTREG**.</span><span class="sxs-lookup"><span data-stu-id="5e169-167">If you request an execution context that the object does not support, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function returns the error code **REGDB\_E\_CLASSNOTREG**.</span></span> <span data-ttu-id="5e169-168">Esse código de erro também pode indicar que o CLSID não corresponde a nenhum componente registrado no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e169-168">This error code can also indicate that the CLSID does not correspond to any component registered on the user's computer.</span></span>

<span data-ttu-id="5e169-169">O quinto parâmetro para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) recebe um ponteiro para a interface.</span><span class="sxs-lookup"><span data-stu-id="5e169-169">The fifth parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) receives a pointer to the interface.</span></span> <span data-ttu-id="5e169-170">Como **CoCreateInstance** é um mecanismo genérico, esse parâmetro não pode ser fortemente tipado.</span><span class="sxs-lookup"><span data-stu-id="5e169-170">Because **CoCreateInstance** is a generic mechanism, this parameter cannot be strongly typed.</span></span> <span data-ttu-id="5e169-171">Em vez disso, o tipo de dados é **void \* \*** e o chamador deve forçar o endereço do ponteiro para um **tipo \* \* void** .</span><span class="sxs-lookup"><span data-stu-id="5e169-171">Instead, the data type is **void\*\***, and the caller must coerce the address of the pointer to a **void\*\*** type.</span></span> <span data-ttu-id="5e169-172">Essa é a finalidade da **\_ conversão de reinterpretação** no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="5e169-172">That is the purpose of the **reinterpret\_cast** in the previous example.</span></span>

<span data-ttu-id="5e169-173">É crucial verificar o valor de retorno de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="5e169-173">It is crucial to check the return value of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="5e169-174">Se a função retornar um código de erro, o ponteiro de interface COM é inválido e a tentativa de desreferenciá-lo pode fazer com que o programa falhe.</span><span class="sxs-lookup"><span data-stu-id="5e169-174">If the function returns an error code, the COM interface pointer is invalid, and attempting to dereference it can cause your program to crash.</span></span>

<span data-ttu-id="5e169-175">Internamente, a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa várias técnicas para criar um objeto.</span><span class="sxs-lookup"><span data-stu-id="5e169-175">Internally, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function uses various techniques to create an object.</span></span> <span data-ttu-id="5e169-176">No caso mais simples, ele pesquisa o identificador de classe no registro.</span><span class="sxs-lookup"><span data-stu-id="5e169-176">In the simplest case, it looks up the class identifier in the registry.</span></span> <span data-ttu-id="5e169-177">A entrada do registro aponta para uma DLL ou EXE que implementa o objeto.</span><span class="sxs-lookup"><span data-stu-id="5e169-177">The registry entry points to a DLL or EXE that implements the object.</span></span> <span data-ttu-id="5e169-178">**CoCreateInstance** também pode usar informações de um catálogo com+ ou de um manifesto lado a lado (SXS).</span><span class="sxs-lookup"><span data-stu-id="5e169-178">**CoCreateInstance** can also use information from a COM+ catalog or a side-by-side (SxS) manifest.</span></span> <span data-ttu-id="5e169-179">Independentemente, os detalhes são transparentes para o chamador.</span><span class="sxs-lookup"><span data-stu-id="5e169-179">Regardless, the details are transparent to the caller.</span></span> <span data-ttu-id="5e169-180">Para obter mais informações sobre os detalhes internos de **CoCreateInstance**, consulte [clientes e servidores com](/windows/desktop/com/com-clients-and-servers).</span><span class="sxs-lookup"><span data-stu-id="5e169-180">For more information about the internal details of **CoCreateInstance**, see [COM Clients and Servers](/windows/desktop/com/com-clients-and-servers).</span></span>

<span data-ttu-id="5e169-181">O `Shapes` exemplo que estamos usando é um pouco forçado, então agora vamos voltar a um exemplo do mundo real de com em ação: exibindo a caixa de diálogo **abrir** para o usuário selecionar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e169-181">The `Shapes` example that we have been using is somewhat contrived, so now let's turn to a real-world example of COM in action: displaying the **Open** dialog box for the user to select a file.</span></span>

## <a name="next"></a><span data-ttu-id="5e169-182">Avançar</span><span class="sxs-lookup"><span data-stu-id="5e169-182">Next</span></span>

[<span data-ttu-id="5e169-183">Exemplo: a caixa de diálogo abrir</span><span class="sxs-lookup"><span data-stu-id="5e169-183">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)

 

 