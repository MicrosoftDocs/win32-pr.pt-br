---
title: Solicitando um objeto para uma interface
description: Solicitando um objeto para uma interface
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007557"
---
# <a name="asking-an-object-for-an-interface"></a><span data-ttu-id="3b3a4-103">Solicitando um objeto para uma interface</span><span class="sxs-lookup"><span data-stu-id="3b3a4-103">Asking an Object for an Interface</span></span>

<span data-ttu-id="3b3a4-104">Vimos anteriormente que um objeto pode implementar mais de uma interface.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-104">We saw earlier that an object can implement more than one interface.</span></span> <span data-ttu-id="3b3a4-105">O objeto de caixa de diálogo de item comum é um exemplo do mundo real disso.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-105">The Common Item Dialog object is a real-world example of this.</span></span> <span data-ttu-id="3b3a4-106">Para dar suporte aos usos mais comuns, o objeto implementa a interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="3b3a4-106">To support the most typical uses, the object implements the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span> <span data-ttu-id="3b3a4-107">Essa interface define métodos básicos para exibir a caixa de diálogo e obter informações sobre o arquivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-107">This interface defines basic methods for displaying the dialog box and getting information about the selected file.</span></span> <span data-ttu-id="3b3a4-108">No entanto, para uso mais avançado, o objeto também implementa uma interface chamada [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize).</span><span class="sxs-lookup"><span data-stu-id="3b3a4-108">For more advanced use, however, the object also implements an interface named [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize).</span></span> <span data-ttu-id="3b3a4-109">Um programa pode usar essa interface para personalizar a aparência e o comportamento da caixa de diálogo, adicionando novos controles de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-109">A program can use this interface to customize the appearance and behavior of the dialog box, by adding new UI controls.</span></span>

<span data-ttu-id="3b3a4-110">Lembre-se de que cada interface COM deve herdar, direta ou indiretamente, da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3b3a4-110">Recall that every COM interface must inherit, directly or indirectly, from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3b3a4-111">O diagrama a seguir mostra a herança do objeto de caixa de diálogo de item comum.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-111">The following diagram shows the inheritance of the Common Item Dialog object.</span></span>

![diagrama que mostra interfaces expostas pelo objeto de caixa de diálogo de item comum](images/com06.png)

<span data-ttu-id="3b3a4-113">Como você pode ver no diagrama, o ancestral direto de [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) é a interface [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) , que por sua vez herda [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span><span class="sxs-lookup"><span data-stu-id="3b3a4-113">As you can see from the diagram, the direct ancestor of [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) is the [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface, which in turn inherits [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="3b3a4-114">À medida que você passa a cadeia de herança de **IFileOpenDialog** para **IModalWindow**, as interfaces definem a funcionalidade de janela cada vez mais generalizada.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-114">As you go up the inheritance chain from **IFileOpenDialog** to **IModalWindow**, the interfaces define increasingly generalized window functionality.</span></span> <span data-ttu-id="3b3a4-115">Por fim, a interface **IModalWindow** herda [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="3b3a4-115">Finally, the **IModalWindow** interface inherits [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="3b3a4-116">O objeto de caixa de diálogo de item comum também implementa [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), que existe em uma cadeia de herança separada.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-116">The Common Item Dialog object also implements [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), which exists in a separate inheritance chain.</span></span>

<span data-ttu-id="3b3a4-117">Agora suponha que você tenha um ponteiro para a interface [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="3b3a4-117">Now suppose that you have a pointer to the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span> <span data-ttu-id="3b3a4-118">Como você obteria um ponteiro para a interface [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ?</span><span class="sxs-lookup"><span data-stu-id="3b3a4-118">How would you get a pointer to the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface?</span></span>

![diagrama que mostra dois ponteiros de interface para interfaces no mesmo objeto](images/com07.png)

<span data-ttu-id="3b3a4-120">Simplesmente converter o ponteiro [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) para um ponteiro [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) não funcionará.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-120">Simply casting the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer to an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer will not work.</span></span> <span data-ttu-id="3b3a4-121">Não há uma maneira confiável de "conversão cruzada" em uma hierarquia de herança, sem alguma forma de RTTI (informações de tipo em tempo de execução), que é um recurso dependente de linguagem.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-121">There is no reliable way to "cross cast" across an inheritance hierarchy, without some form of run-time type information (RTTI), which is a highly language-dependent feature.</span></span>

<span data-ttu-id="3b3a4-122">A abordagem COM é *pedir* ao objeto que lhe dê um ponteiro [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , usando a primeira interface como um canal no objeto.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-122">The COM approach is to *ask* the object to give you an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer, using the first interface as a conduit into the object.</span></span> <span data-ttu-id="3b3a4-123">Isso é feito chamando o método [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do primeiro ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-123">This is done by calling the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method from the first interface pointer.</span></span> <span data-ttu-id="3b3a4-124">Você pode considerar **QueryInterface** como uma versão independente de idioma da palavra-chave **Dynamic \_ Cast** em C++.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-124">You can think of **QueryInterface** as a language-independent version of the **dynamic\_cast** keyword in C++.</span></span>

<span data-ttu-id="3b3a4-125">O método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) tem a seguinte assinatura:</span><span class="sxs-lookup"><span data-stu-id="3b3a4-125">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method has the following signature:</span></span>

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

<span data-ttu-id="3b3a4-126">Com base no que você já conhece sobre [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), talvez seja possível adivinhar o funcionamento de [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="3b3a4-126">Based on what you already know about [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), you might be able to guess how [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) works.</span></span>

-   <span data-ttu-id="3b3a4-127">O parâmetro *riid* é o GUID que identifica a interface que você está solicitando.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-127">The *riid* parameter is the GUID that identifies the interface you are asking for.</span></span> <span data-ttu-id="3b3a4-128">O tipo de dados **REFIID** é um **typedef** para `const GUID&` .</span><span class="sxs-lookup"><span data-stu-id="3b3a4-128">The data type **REFIID** is a **typedef** for `const GUID&`.</span></span> <span data-ttu-id="3b3a4-129">Observe que o CLSID (identificador de classe) não é necessário, pois o objeto já foi criado.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-129">Notice that the class identifier (CLSID) is not required, because the object has already been created.</span></span> <span data-ttu-id="3b3a4-130">Somente o identificador de interface é necessário.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-130">Only the interface identifier is necessary.</span></span>
-   <span data-ttu-id="3b3a4-131">O parâmetro *ppvObject* recebe um ponteiro para a interface.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-131">The *ppvObject* parameter receives a pointer to the interface.</span></span> <span data-ttu-id="3b3a4-132">O tipo de dados desse parâmetro é **void \* \***, pelo mesmo motivo que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa este tipo de dados: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pode ser usado para consultar qualquer interface com, portanto, o parâmetro não pode ser fortemente tipado.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-132">The data type of this parameter is **void\*\***, for the same reason that [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses this data type: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) can be used to query for any COM interface, so the parameter cannot be strongly typed.</span></span>

<span data-ttu-id="3b3a4-133">Aqui está como você chamaria [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) :</span><span class="sxs-lookup"><span data-stu-id="3b3a4-133">Here is how you would call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer:</span></span>


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="3b3a4-134">Como sempre, verifique o valor de retorno **HRESULT** , caso o método falhe.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-134">As always, check the **HRESULT** return value, in case the method fails.</span></span> <span data-ttu-id="3b3a4-135">Se o método tiver sucesso, você deverá chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) quando terminar de usar o ponteiro, conforme descrito em [Gerenciando o tempo de vida de um objeto](managing-the-lifetime-of-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="3b3a4-135">If the method succeeds, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when you are done using the pointer, as described in [Managing the Lifetime of an Object](managing-the-lifetime-of-an-object.md).</span></span>

## <a name="next"></a><span data-ttu-id="3b3a4-136">Avançar</span><span class="sxs-lookup"><span data-stu-id="3b3a4-136">Next</span></span>

[<span data-ttu-id="3b3a4-137">Alocação de memória em COM</span><span class="sxs-lookup"><span data-stu-id="3b3a4-137">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)

 

 