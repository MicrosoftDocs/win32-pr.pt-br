---
description: Você pode criar uma instância em C++ por meio da interface IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Criando e declarando uma instância usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761512"
---
# <a name="creating-and-declaring-an-instance-using-c"></a><span data-ttu-id="47b4d-103">Criando e declarando uma instância usando C++</span><span class="sxs-lookup"><span data-stu-id="47b4d-103">Creating and Declaring an Instance Using C++</span></span>

<span data-ttu-id="47b4d-104">Você pode criar uma instância em C++ por meio da interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="47b4d-104">You can create an instance in C++ through the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="47b4d-105">Os exemplos de código neste tópico exigem a seguinte \# instrução include para serem compiladas corretamente.</span><span class="sxs-lookup"><span data-stu-id="47b4d-105">The code examples in this topic require the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="47b4d-106">O procedimento a seguir descreve como criar uma instância de uma classe existente.</span><span class="sxs-lookup"><span data-stu-id="47b4d-106">The following procedure describes how to create an instance of an existing class.</span></span>

<span data-ttu-id="47b4d-107">**Para criar uma instância de uma classe existente**</span><span class="sxs-lookup"><span data-stu-id="47b4d-107">**To create an instance of an existing class**</span></span>

1.  <span data-ttu-id="47b4d-108">Recupere a definição da classe existente chamando os métodos [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="47b4d-108">Retrieve the definition of the existing class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span>

    <span data-ttu-id="47b4d-109">O exemplo de código a seguir mostra como usar os métodos [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para obter um ponteiro para a interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que fornece acesso à definição de classe.</span><span class="sxs-lookup"><span data-stu-id="47b4d-109">The following code example shows how to use the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to get a pointer to the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface that provides access to the class definition.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="47b4d-110">Crie a nova instância chamando o método [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="47b4d-110">Create the new instance by calling the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

    <span data-ttu-id="47b4d-111">O exemplo de código a seguir mostra como criar uma nova instância e, em seguida, liberar a classe.</span><span class="sxs-lookup"><span data-stu-id="47b4d-111">The following code example shows how to create a new instance and then release the class.</span></span>

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  <span data-ttu-id="47b4d-112">Defina valores para todas as propriedades que não herdam os valores definidos para a classe chamando o método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="47b4d-112">Set values for any properties that do not inherit the values defined for the class by calling the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="47b4d-113">Cada instância de uma classe herda todas as propriedades que são definidas para a classe.</span><span class="sxs-lookup"><span data-stu-id="47b4d-113">Each instance of a class inherits all of the properties that are defined for the class.</span></span> <span data-ttu-id="47b4d-114">No entanto, você pode especificar valores de propriedade diferentes se escolher.</span><span class="sxs-lookup"><span data-stu-id="47b4d-114">However, you can specify different property values if you choose.</span></span>

    <span data-ttu-id="47b4d-115">Se a classe existente tiver uma propriedade de chave, você deverá definir a propriedade como **NULL** ou um valor exclusivo garantido.</span><span class="sxs-lookup"><span data-stu-id="47b4d-115">If the existing class has a key property, you should set the property either to **NULL** or a guaranteed unique value.</span></span> <span data-ttu-id="47b4d-116">Se você definir a chave como **NULL** e a chave for uma cadeia de caracteres, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) ou [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) gerará internamente e atribuirá um GUID à chave.</span><span class="sxs-lookup"><span data-stu-id="47b4d-116">If you set the key to **NULL** and the key is a string, then [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) or [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) internally generates and assigns a GUID to the key.</span></span> <span data-ttu-id="47b4d-117">Dessa forma, especificar **NULL** para uma propriedade de chave permite criar uma instância exclusiva que não substituirá nenhuma instância anterior.</span><span class="sxs-lookup"><span data-stu-id="47b4d-117">This way, specifying **NULL** for a key property lets you create a unique instance that will not overwrite any previous instance.</span></span>

    <span data-ttu-id="47b4d-118">O exemplo de código a seguir mostra como definir o valor da propriedade [**index**](swbemrefreshableitem-index.md) da classe de instância de exemplo.</span><span class="sxs-lookup"><span data-stu-id="47b4d-118">The following code example shows how to set the [**Index**](swbemrefreshableitem-index.md) property value of the example instance class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="47b4d-119">Defina os valores para quaisquer qualificadores relevantes por meio de uma chamada para [**IWbemClassObject:: Getqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span><span class="sxs-lookup"><span data-stu-id="47b4d-119">Set the values for any relevant qualifiers through a call to [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span></span>

    <span data-ttu-id="47b4d-120">O método [**Getqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) retorna um ponteiro para uma interface [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , que usa para acessar os qualificadores para uma classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="47b4d-120">The [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) method returns a pointer to an [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface, which use to access the qualifiers for a class or instance.</span></span> <span data-ttu-id="47b4d-121">Você pode especificar valores diferentes para um qualificador definido para a classe se o tipo de qualificador de classe for **EnableOverride**.</span><span class="sxs-lookup"><span data-stu-id="47b4d-121">You can specify different values for a qualifier defined for the class if the class qualifier flavor is **EnableOverride**.</span></span> <span data-ttu-id="47b4d-122">Você não pode modificar ou excluir um qualificador de classe com o tipo definido como **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="47b4d-122">You cannot modify or delete a class qualifier with the flavor set to **DisableOverride**.</span></span> <span data-ttu-id="47b4d-123">Para obter mais informações, consulte [qualificadores de tipos](qualifier-flavors.md).</span><span class="sxs-lookup"><span data-stu-id="47b4d-123">For more information, see [Qualifier Flavors](qualifier-flavors.md).</span></span>

    <span data-ttu-id="47b4d-124">Como opção, você também pode definir qualificadores adicionais para sua classe de instância.</span><span class="sxs-lookup"><span data-stu-id="47b4d-124">As an option, you can also define additional qualifiers for your instance class.</span></span> <span data-ttu-id="47b4d-125">Você pode definir qualificadores adicionais para a propriedade instância ou instância que não precisam aparecer na declaração de classe.</span><span class="sxs-lookup"><span data-stu-id="47b4d-125">You can define additional qualifiers for the instance or instance property which do not need to appear in the class declaration.</span></span>

5.  <span data-ttu-id="47b4d-126">Salve a instância chamando o método [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="47b4d-126">Save the instance by calling the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method.</span></span>

    <span data-ttu-id="47b4d-127">O WMI salva a instância no namespace WMI atual.</span><span class="sxs-lookup"><span data-stu-id="47b4d-127">WMI saves the instance in the current WMI namespace.</span></span> <span data-ttu-id="47b4d-128">Como tal, o caminho completo da instância depende do namespace, que normalmente é o \\ padrão raiz.</span><span class="sxs-lookup"><span data-stu-id="47b4d-128">As such, the full path of the instance is dependent on the namespace, which is typically root\\default.</span></span> <span data-ttu-id="47b4d-129">Para este exemplo de código, o nome do caminho completo seria \\ \\ . \\ raiz \\ padrão: example. index = "IX100".</span><span class="sxs-lookup"><span data-stu-id="47b4d-129">For this code example, the full path name would be \\\\.\\root\\default:Example.Index="IX100".</span></span>

    <span data-ttu-id="47b4d-130">O exemplo de código a seguir mostra como salvar uma instância do.</span><span class="sxs-lookup"><span data-stu-id="47b4d-130">The following code example shows how to save an instance.</span></span>

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

<span data-ttu-id="47b4d-131">Salvar a instância em bloqueios de WMI reduz várias das propriedades da instância.</span><span class="sxs-lookup"><span data-stu-id="47b4d-131">Saving the instance to WMI locks down several of the properties of the instance.</span></span>

<span data-ttu-id="47b4d-132">Especificamente, você não pode executar nenhuma das seguintes operações por meio da API do WMI depois que existe uma instância dentro da infraestrutura do WMI:</span><span class="sxs-lookup"><span data-stu-id="47b4d-132">Specifically, you cannot perform any of the following operations through the WMI API after an instance exists within the WMI infrastructure:</span></span>

-   <span data-ttu-id="47b4d-133">Altere a classe pai da classe à qual a instância pertence.</span><span class="sxs-lookup"><span data-stu-id="47b4d-133">Change the parent class of the class to which the instance belongs.</span></span>
-   <span data-ttu-id="47b4d-134">Adicionar ou remover propriedades.</span><span class="sxs-lookup"><span data-stu-id="47b4d-134">Add or remove properties.</span></span>
-   <span data-ttu-id="47b4d-135">Alterar tipos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="47b4d-135">Change property types.</span></span>
-   <span data-ttu-id="47b4d-136">Adicionar ou remover qualificadores **indexados** ou de [**chave**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="47b4d-136">Add or remove [**Key**](standard-qualifiers.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="47b4d-137">Adicionar ou remover qualificadores [**singleton**](standard-wmi-qualifiers.md), **dinâmico** ou [**abstrato**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="47b4d-137">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

<span data-ttu-id="47b4d-138">O exemplo de código a seguir combina os exemplos de código discutidos no procedimento anterior para mostrar como criar uma instância usando a API do WMI.</span><span class="sxs-lookup"><span data-stu-id="47b4d-138">The following code example combines the code examples discussed in the previous procedure to show how to create an instance using the WMI API.</span></span>


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



