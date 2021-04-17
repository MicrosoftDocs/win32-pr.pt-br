---
title: Métodos de propriedade de interface
description: Muitas interfaces ADSI são projetadas para dar suporte à automação e, portanto, são interfaces duplas, pois dão suporte ao acesso de cliente por meio de interfaces IUnknown e IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade de interface
- ADSI de ADSI, referência, métodos de propriedade explicados
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105811234"
---
# <a name="interface-property-methods"></a><span data-ttu-id="20373-105">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="20373-105">Interface Property Methods</span></span>

<span data-ttu-id="20373-106">Muitas interfaces ADSI são projetadas para dar suporte à automação e, portanto, são interfaces duplas, pois dão suporte ao acesso de cliente por meio de interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="20373-106">Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span> <span data-ttu-id="20373-107">Clientes não de automação, como aqueles escritos em C/C++, resolvem a invocação de método diretamente, usando o método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e chamam o método diretamente.</span><span class="sxs-lookup"><span data-stu-id="20373-107">Non-Automation clients, such as those written in C/C++, resolve method invocation directly, using the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, and call the method directly.</span></span> <span data-ttu-id="20373-108">Clientes de automação, também conhecidos como clientes com limite de nome, como aqueles escritos em Visual Basic, ou Visual Basic Scripting Edition (VBScript), devem resolver indiretamente a invocação de método usando o método [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) .</span><span class="sxs-lookup"><span data-stu-id="20373-108">Automation clients, also known as name-bound clients, such as those written in Visual Basic, or Visual Basic Scripting Edition (VBScript), must resolve method invocation indirectly using the [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) method.</span></span>

<span data-ttu-id="20373-109">Uma interface ADSI com suporte a automação define métodos de propriedade para recuperar e modificar propriedades de um objeto que implementa a interface.</span><span class="sxs-lookup"><span data-stu-id="20373-109">An ADSI interface supporting Automation defines property methods for retrieving and modifying properties of an object implementing the interface.</span></span> <span data-ttu-id="20373-110">Os métodos Property têm nomes que têm **Get** \_ e **Put** precedidos \_ para os nomes de propriedade apropriados, por exemplo, **Get \_ User** e **Put \_ Name**.</span><span class="sxs-lookup"><span data-stu-id="20373-110">The property methods have names that have **get**\_ and **put**\_ prepended to the appropriate property names, for example, **get\_User** and **put\_Name**.</span></span>

<span data-ttu-id="20373-111">Cada **método \_ Get** usa um único parâmetro como saída.</span><span class="sxs-lookup"><span data-stu-id="20373-111">Each **get\_** method takes a single parameter as output.</span></span> <span data-ttu-id="20373-112">Esse parâmetro é um endereço alocado por método de uma variável do tipo de dados Property.</span><span class="sxs-lookup"><span data-stu-id="20373-112">This parameter is a method-allocated address of a variable of the property data type.</span></span> <span data-ttu-id="20373-113">No retorno, essa variável assume o valor atual da propriedade solicitada.</span><span class="sxs-lookup"><span data-stu-id="20373-113">On return, this variable assumes the current value of the requested property.</span></span> <span data-ttu-id="20373-114">O chamador deve liberar a memória alocada da variável quando a propriedade não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="20373-114">The caller must release the allocated memory of the variable when the property is no longer required.</span></span>

<span data-ttu-id="20373-115">Cada **método \_ Put** usa um único parâmetro como entrada para o tipo de dados da propriedade correspondente.</span><span class="sxs-lookup"><span data-stu-id="20373-115">Each **put\_** method takes a single parameter as input for the data type of the corresponding property.</span></span> <span data-ttu-id="20373-116">O parâmetro contém um novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="20373-116">The parameter holds a new value of the property.</span></span>

<span data-ttu-id="20373-117">O exemplo de código a seguir mostra a invocação dos métodos de propriedade que seguem o procedimento habitual para chamar a função de membro de um objeto.</span><span class="sxs-lookup"><span data-stu-id="20373-117">The following code example shows the invocation of the property methods that follow the usual procedure to call the member function of an object.</span></span>


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



<span data-ttu-id="20373-118">O exemplo de código a seguir mostra a invocação dos métodos de propriedade em clientes de automação, que podem ser um pouco diferentes.</span><span class="sxs-lookup"><span data-stu-id="20373-118">The following code example shows the invocation of the property methods in automation clients, which can be somewhat different.</span></span> <span data-ttu-id="20373-119">Por exemplo, Visual Basic usa a notação de ponto.</span><span class="sxs-lookup"><span data-stu-id="20373-119">For example, Visual Basic uses dot notation.</span></span>


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



<span data-ttu-id="20373-120">Todos os parâmetros e tipos de retorno devem ser daqueles que o tipo de dados VARIANT define.</span><span class="sxs-lookup"><span data-stu-id="20373-120">All parameters and return types must be of those that the VARIANT data type defines.</span></span> <span data-ttu-id="20373-121">Todos os métodos em uma interface dupla retornam um valor HRESULT para indicar êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="20373-121">All methods on a dual interface return an HRESULT value to indicate success or failure.</span></span>

<span data-ttu-id="20373-122">Para obter mais informações sobre como obter e definir propriedades em objetos ADSI, consulte [cache de propriedades](property-cache-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="20373-122">For more information about getting and setting properties on ADSI objects, see [Property Cache](property-cache-interfaces.md).</span></span>

 

 