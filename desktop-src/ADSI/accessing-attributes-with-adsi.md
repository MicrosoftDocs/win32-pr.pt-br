---
title: Acessando atributos com ADSI
description: Os métodos IADs. Get e IADs. GetEx são usados para recuperar valores de atributo nomeados.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Atributos, acessando com ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105749124"
---
# <a name="accessing-attributes-with-adsi"></a><span data-ttu-id="bc202-104">Acessando atributos com ADSI</span><span class="sxs-lookup"><span data-stu-id="bc202-104">Accessing Attributes with ADSI</span></span>

<span data-ttu-id="bc202-105">Os métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) são usados para recuperar valores de atributo nomeados.</span><span class="sxs-lookup"><span data-stu-id="bc202-105">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods are used to retrieve named attribute values.</span></span> <span data-ttu-id="bc202-106">Os dois métodos retornam um valor de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="bc202-106">Both methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) value.</span></span> <span data-ttu-id="bc202-107">Esses métodos estão disponíveis apenas para diretórios que dão suporte a um esquema.</span><span class="sxs-lookup"><span data-stu-id="bc202-107">These methods are available only for directories that support a schema.</span></span> <span data-ttu-id="bc202-108">Ao acessar objetos em um diretório sem um esquema, as interfaces [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) devem ser usadas para manipular valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="bc202-108">When accessing objects in a directory without a schema, the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces must be used to manipulate attribute values.</span></span>

<span data-ttu-id="bc202-109">Os métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) retornam uma [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) que pode ou não ser uma matriz **Variant** , dependendo do número de valores retornados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="bc202-109">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) which may, or may not, be a **VARIANT** array depending on the number of values returned by the server.</span></span> <span data-ttu-id="bc202-110">Por exemplo, se apenas um valor for retornado do servidor, independentemente de ser um atributo único ou com vários valores, o método retornará uma única **variante**.</span><span class="sxs-lookup"><span data-stu-id="bc202-110">For example, if only one value is returned from the server, regardless of whether it is a single or multi-valued attribute, the method returns a single **VARIANT**.</span></span> <span data-ttu-id="bc202-111">Por outro lado, se vários valores forem retornados, uma matriz **Variant** será retornada.</span><span class="sxs-lookup"><span data-stu-id="bc202-111">Conversely, if multiple values are returned, a **VARIANT** array is returned.</span></span> <span data-ttu-id="bc202-112">Se uma **matriz Variant** for retornada, o membro **VT** da estrutura **Variant** conterá os sinalizadores **VT \_ Variant/vbVariant** e **VT \_ array/VBArray** .</span><span class="sxs-lookup"><span data-stu-id="bc202-112">If a **VARIANT** array is returned, the **vt** member of the **VARIANT** structure contains the **VT\_VARIANT/vbVariant** and **VT\_ARRAY/vbArray** flags.</span></span>

<span data-ttu-id="bc202-113">Os métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) também podem retornar um objeto com usando a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="bc202-113">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods can also return a COM object using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="bc202-114">Nesse caso, o membro **VT** da estrutura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contém o sinalizador de **\_ expedição/vbObject do VT** .</span><span class="sxs-lookup"><span data-stu-id="bc202-114">In this case, the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure contains the **VT\_DISPATCH/vbObject** flag.</span></span> <span data-ttu-id="bc202-115">Para acessar o objeto COM, chame o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) na interface **IDispatch** para obter a interface desejada.</span><span class="sxs-lookup"><span data-stu-id="bc202-115">To access the COM object, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the **IDispatch** interface to obtain the desired interface.</span></span>

<span data-ttu-id="bc202-116">Outro tipo de dados retornado pelos métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) são dados binários.</span><span class="sxs-lookup"><span data-stu-id="bc202-116">Another data type returned by the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods is binary data.</span></span> <span data-ttu-id="bc202-117">Nesse caso, os dados são fornecidos como uma matriz contígua de bytes e o membro **VT** da estrutura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) conterá os sinalizadores **VT \_ UI1/vbByte** e **VT \_ array/VBArray** .</span><span class="sxs-lookup"><span data-stu-id="bc202-117">In this case, the data is supplied as a contiguous array of bytes and the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure will contain the **VT\_UI1/vbByte** and **VT\_ARRAY/vbArray** flags.</span></span>

> [!Note]  
> <span data-ttu-id="bc202-118">O Microsoft Visual Basic, Scripting Edition, só dá suporte a matrizes [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) e **Variant** .</span><span class="sxs-lookup"><span data-stu-id="bc202-118">Microsoft Visual Basic, Scripting Edition only supports [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) and **VARIANT** arrays.</span></span> <span data-ttu-id="bc202-119">Por isso, o VBScript não pode ser usado para ler valores de propriedade binária.</span><span class="sxs-lookup"><span data-stu-id="bc202-119">Because of this, VBScript cannot be used to read binary property values.</span></span>

 

<span data-ttu-id="bc202-120">Muitas interfaces ADSI definem propriedades específicas de interface.</span><span class="sxs-lookup"><span data-stu-id="bc202-120">Many ADSI interfaces define interface-specific properties.</span></span> <span data-ttu-id="bc202-121">Por exemplo, a interface [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) define a propriedade [**Location**](iadscomputer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="bc202-121">For example, the [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface defines the [**Location**](iadscomputer-property-methods.md) property.</span></span> <span data-ttu-id="bc202-122">Essas propriedades definidas pela interface podem conter dados idênticos a um dos atributos nomeados, mas as propriedades são específicas ao tipo de objeto ao qual a interface se refere.</span><span class="sxs-lookup"><span data-stu-id="bc202-122">These interface-defined properties may contain data that is identical to one of the named attributes, but the properties are specific to the type of object the interface refers to.</span></span> <span data-ttu-id="bc202-123">Em idiomas que dão suporte à automação, essas propriedades definidas pela interface podem ser acessadas usando a notação de ponto, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="bc202-123">In languages that support automation, these interface-defined properties can be accessed using the dot notation as shown in the following code example.</span></span>

## <a name="examples"></a><span data-ttu-id="bc202-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc202-124">Examples</span></span>

<span data-ttu-id="bc202-125">O exemplo de código a seguir mostra como acessar a propriedade ADsPath na interface IADs.</span><span class="sxs-lookup"><span data-stu-id="bc202-125">The following code example shows how to access the ADsPath property on the IADs interface.</span></span>


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



<span data-ttu-id="bc202-126">Em linguagens que não são de automação, os métodos de acesso à propriedade devem ser usados para acessar as propriedades definidas pela interface.</span><span class="sxs-lookup"><span data-stu-id="bc202-126">In non-automation languages, the property access methods must be used to access the interface-defined properties.</span></span> <span data-ttu-id="bc202-127">Por exemplo, o método de [**\_ localização IADsComputer:: Get**](iadscomputer-property-methods.md) é usado para recuperar a propriedade **IADsComputer. Location** .</span><span class="sxs-lookup"><span data-stu-id="bc202-127">For example, the [**IADsComputer::get\_Location**](iadscomputer-property-methods.md) method is used to retrieve the **IADsComputer.Location** property.</span></span>

<span data-ttu-id="bc202-128">O exemplo de código C++ a seguir demonstra como usar o método de acesso de propriedade em C++ para recuperar o ADsPath de um usuário.</span><span class="sxs-lookup"><span data-stu-id="bc202-128">The following C++ code example demonstrates how to use the property access method in C++ to retrieve the ADsPath of a user.</span></span>


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



<span data-ttu-id="bc202-129">Para obter mais informações sobre como acessar atributos com ADSI, consulte:</span><span class="sxs-lookup"><span data-stu-id="bc202-129">For more information about accessing attributes with ADSI, see:</span></span>

-   [<span data-ttu-id="bc202-130">O método Get</span><span class="sxs-lookup"><span data-stu-id="bc202-130">The Get Method</span></span>](the-get-method.md)
-   [<span data-ttu-id="bc202-131">O método GetEx</span><span class="sxs-lookup"><span data-stu-id="bc202-131">The GetEx Method</span></span>](the-getex-method.md)
-   [<span data-ttu-id="bc202-132">O método GetInfo</span><span class="sxs-lookup"><span data-stu-id="bc202-132">The GetInfo Method</span></span>](the-getinfo-method.md)
-   [<span data-ttu-id="bc202-133">Otimização usando GetInfoEx</span><span class="sxs-lookup"><span data-stu-id="bc202-133">Optimization Using GetInfoEx</span></span>](optimization-using-getinfoex.md)
-   [<span data-ttu-id="bc202-134">Acessando atributos com a interface IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="bc202-134">Accessing Attributes with the IDirectoryObject Interface</span></span>](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [<span data-ttu-id="bc202-135">Exemplo de código para ler atributos</span><span class="sxs-lookup"><span data-stu-id="bc202-135">Example Code for Reading Attributes</span></span>](example-code-for-reading-attributes.md)

 

 