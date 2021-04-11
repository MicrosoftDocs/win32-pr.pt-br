---
description: Um caminho de objeto de instância descreve o local de uma instância de uma determinada classe dentro de um namespace específico.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Descrevendo um caminho de objeto de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297058"
---
# <a name="describing-an-instance-object-path"></a><span data-ttu-id="6647b-103">Descrevendo um caminho de objeto de instância</span><span class="sxs-lookup"><span data-stu-id="6647b-103">Describing an Instance Object Path</span></span>

<span data-ttu-id="6647b-104">Um caminho de objeto de instância descreve o local de uma instância de uma determinada classe dentro de um namespace específico.</span><span class="sxs-lookup"><span data-stu-id="6647b-104">An instance object path describes the location of an instance of a given class within a specific namespace.</span></span>

<span data-ttu-id="6647b-105">Você pode ter vários tipos diferentes de caminhos de objeto de instância:</span><span class="sxs-lookup"><span data-stu-id="6647b-105">You can have several different kinds of instance object paths:</span></span>

-   <span data-ttu-id="6647b-106">Completo</span><span class="sxs-lookup"><span data-stu-id="6647b-106">Full</span></span>

    <span data-ttu-id="6647b-107">Um caminho de objeto de instância completo acrescenta o nome e o valor da propriedade de chave para a classe a um caminho de objeto de classe completa.</span><span class="sxs-lookup"><span data-stu-id="6647b-107">A full instance object path appends the name and value of the key property for the class to a full class object path.</span></span>

    <span data-ttu-id="6647b-108">O exemplo a seguir mostra a definição do caminho completo do objeto de instância.</span><span class="sxs-lookup"><span data-stu-id="6647b-108">The following example shows the definition of the full instance object path.</span></span>

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   <span data-ttu-id="6647b-109">Relativo</span><span class="sxs-lookup"><span data-stu-id="6647b-109">Relative</span></span>

    <span data-ttu-id="6647b-110">Um caminho de objeto relativo refere-se a uma instância localizada no namespace atual no servidor atual.</span><span class="sxs-lookup"><span data-stu-id="6647b-110">A relative object path refers to an instance located in the current namespace on the current server.</span></span> <span data-ttu-id="6647b-111">O caminho relativo consiste no nome da classe seguido pelos nomes e valores das propriedades de chave dessa instância.</span><span class="sxs-lookup"><span data-stu-id="6647b-111">The relative path consists of the class name followed by the names and values of the key properties of this instance.</span></span>

    <span data-ttu-id="6647b-112">O exemplo a seguir mostra a definição do caminho do objeto de instância relativo.</span><span class="sxs-lookup"><span data-stu-id="6647b-112">The following example shows the definition of the relative instance object path.</span></span>

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   <span data-ttu-id="6647b-113">Relativo a uma única chave</span><span class="sxs-lookup"><span data-stu-id="6647b-113">Relative with a single key</span></span>

    <span data-ttu-id="6647b-114">Para classes com apenas uma propriedade designada como chave, você pode omitir o nome da propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="6647b-114">For classes with only one property designated as the key, you can omit the name of the key property.</span></span>

    <span data-ttu-id="6647b-115">O exemplo a seguir mostra a definição do caminho do objeto de instância relativo com uma única chave.</span><span class="sxs-lookup"><span data-stu-id="6647b-115">The following example shows the definition of the relative instance object path with a single key.</span></span>

    ``` syntax
    MyClass="e:"
    ```

-   <span data-ttu-id="6647b-116">Relativo a várias chaves</span><span class="sxs-lookup"><span data-stu-id="6647b-116">Relative with multiple keys</span></span>

    <span data-ttu-id="6647b-117">Use uma vírgula para distinguir entre as chaves de uma instância com várias chaves.</span><span class="sxs-lookup"><span data-stu-id="6647b-117">Use a comma to distinguish between the keys of an instance with multiple keys.</span></span>

    <span data-ttu-id="6647b-118">O exemplo a seguir mostra as definições do caminho do objeto de instância relativo com várias chaves.</span><span class="sxs-lookup"><span data-stu-id="6647b-118">The following example shows the definitions of the relative instance object path with multiple keys.</span></span>

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   <span data-ttu-id="6647b-119">Relativo para uma classe singleton</span><span class="sxs-lookup"><span data-stu-id="6647b-119">Relative for a singleton class</span></span>

    <span data-ttu-id="6647b-120">O caminho relativo do objeto para uma classe singleton consiste no nome da classe seguido pela notação "= @".</span><span class="sxs-lookup"><span data-stu-id="6647b-120">The relative object path for a singleton class consists of the class name followed by the "=@" notation.</span></span>

    <span data-ttu-id="6647b-121">O exemplo a seguir mostra a definição do caminho de objeto da instância relativa para uma classe singleton.</span><span class="sxs-lookup"><span data-stu-id="6647b-121">The following example shows the definition of the relative instance object path for a singleton class.</span></span>

    ``` syntax
    MySingletonClass=@
    ```

<span data-ttu-id="6647b-122">O procedimento a seguir descreve como recuperar uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="6647b-122">The following procedure describes how to retrieve a class instance.</span></span>

<span data-ttu-id="6647b-123">**Para recuperar uma instância de classe**</span><span class="sxs-lookup"><span data-stu-id="6647b-123">**To retrieve a class instance**</span></span>

1.  <span data-ttu-id="6647b-124">Inicialize uma cadeia de caracteres que contenha o caminho do objeto com uma chamada para a função [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) .</span><span class="sxs-lookup"><span data-stu-id="6647b-124">Initialize a string that contains the object path with a call to the [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) function.</span></span>
2.  <span data-ttu-id="6647b-125">Inicialize um objeto que receberá a instância.</span><span class="sxs-lookup"><span data-stu-id="6647b-125">Initialize an object that will receive the instance.</span></span>
3.  <span data-ttu-id="6647b-126">Recupere o objeto com uma chamada para [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="6647b-126">Retrieve the object with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="6647b-127">Para usar o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), você deve implementar a interface [**IWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="6647b-127">To use [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), you must implement the [**IWbemSink**](swbemsink.md) interface.</span></span>

<span data-ttu-id="6647b-128">A \# instrução include a seguir é necessária para o código listado posteriormente neste tópico para ser compilado corretamente.</span><span class="sxs-lookup"><span data-stu-id="6647b-128">The following \#include statement is required for the code that is listed later in this topic to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="6647b-129">O exemplo de código a seguir descreve como recuperar uma instância de classe usando um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="6647b-129">The following code example describes how to retrieve a class instance using an object path.</span></span>


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



<span data-ttu-id="6647b-130">Para instâncias de classes que especificam várias propriedades como chave, o WMI não requer nenhuma ordenação específica de propriedades de chave em caminhos de objeto.</span><span class="sxs-lookup"><span data-stu-id="6647b-130">For instances of classes that specify multiple properties as the key, WMI requires no specific ordering of key properties in object paths.</span></span> <span data-ttu-id="6647b-131">Você só precisa especificar o valor de cada uma das propriedades no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6647b-131">You need only specify the value of each of the properties in the object path.</span></span>

<span data-ttu-id="6647b-132">O exemplo de código a seguir descreve duas descrições de chave equivalentes.</span><span class="sxs-lookup"><span data-stu-id="6647b-132">The following code example describes two equivalent key descriptions.</span></span>

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
