---
description: A criação de uma classe derivada no WMI é muito semelhante à criação de uma classe base. Assim como com uma classe base, você deve primeiro definir a classe derivada e, em seguida, registrar a classe derivada com o WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Criando uma classe derivada de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785929"
---
# <a name="creating-a-wmi-derived-class"></a><span data-ttu-id="06516-104">Criando uma classe derivada de WMI</span><span class="sxs-lookup"><span data-stu-id="06516-104">Creating a WMI Derived Class</span></span>

<span data-ttu-id="06516-105">A criação de uma classe derivada no WMI é muito semelhante à criação de uma classe base.</span><span class="sxs-lookup"><span data-stu-id="06516-105">Creating a derived class in WMI is very similar to creating a base class.</span></span> <span data-ttu-id="06516-106">Assim como com uma classe base, você deve primeiro definir a classe derivada e, em seguida, registrar a classe derivada com o WMI.</span><span class="sxs-lookup"><span data-stu-id="06516-106">As with a base class, you must first define the derived class and then register the derived class with WMI.</span></span> <span data-ttu-id="06516-107">A principal diferença é que você deve primeiro localizar a classe pai da qual deseja derivar.</span><span class="sxs-lookup"><span data-stu-id="06516-107">The main difference is that you must first locate the parent class from which you wish to derive.</span></span> <span data-ttu-id="06516-108">Para obter mais informações, consulte [escrevendo um provedor de classe](writing-a-class-provider.md) e [escrevendo um provedor de instância](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06516-108">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>

<span data-ttu-id="06516-109">A maneira recomendada para criar classes para um provedor é em arquivos formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="06516-109">The recommended way to create classes for a provider is in Managed Object Format (MOF) files.</span></span> <span data-ttu-id="06516-110">Várias classes derivadas que estão relacionadas entre si devem ser agrupadas em um arquivo MOF, juntamente com quaisquer classes base das quais derivam Propriedades ou métodos.</span><span class="sxs-lookup"><span data-stu-id="06516-110">Several derived classes that are related to each other should be grouped into a MOF file, along with any base classes from which they derive properties or methods.</span></span> <span data-ttu-id="06516-111">Se você posicionar cada classe em um arquivo MOF separado, cada arquivo deverá ser compilado antes que o provedor possa funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="06516-111">If you place each class in a separate MOF file then each file must be compiled before the provider can work properly.</span></span>

<span data-ttu-id="06516-112">Depois de criar sua classe, você deve excluir todas as instâncias da sua classe antes de poder executar qualquer uma das seguintes atividades em sua classe derivada:</span><span class="sxs-lookup"><span data-stu-id="06516-112">After you create your class, you must delete all instances of your class before you can perform any of the following activities on your derived class:</span></span>

-   <span data-ttu-id="06516-113">Altere a classe pai da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="06516-113">Change the parent class of your derived class.</span></span>
-   <span data-ttu-id="06516-114">Adicionar ou remover propriedades.</span><span class="sxs-lookup"><span data-stu-id="06516-114">Add or remove properties.</span></span>
-   <span data-ttu-id="06516-115">Alterar tipos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="06516-115">Change property types.</span></span>
-   <span data-ttu-id="06516-116">Adicionar ou remover qualificadores **indexados** ou de [**chave**](key-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="06516-116">Add or remove [**Key**](key-qualifier.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="06516-117">Adicionar ou remover qualificadores [**singleton**](standard-wmi-qualifiers.md), **dinâmico** ou [**abstrato**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="06516-117">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

> [!Note]  
> <span data-ttu-id="06516-118">Para adicionar, remover ou modificar uma propriedade ou um qualificador, chame [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) ou [**SWbemObject. \_ Put**](swbemobject-put-.md) e defina o parâmetro Flag como "modo forçado".</span><span class="sxs-lookup"><span data-stu-id="06516-118">To add, remove, or modify a property or qualifier, call [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) or [**SWbemObject.Put\_**](swbemobject-put-.md) and set the flag parameter to "force mode".</span></span> <span data-ttu-id="06516-119">O qualificador [**abstrato**](standard-qualifiers.md) só poderá ser usado se a classe pai for abstrata.</span><span class="sxs-lookup"><span data-stu-id="06516-119">The [**Abstract**](standard-qualifiers.md) qualifier can be used only if the parent class is abstract.</span></span>

 

<span data-ttu-id="06516-120">Quando você declarar sua classe derivada, observe as seguintes regras e restrições:</span><span class="sxs-lookup"><span data-stu-id="06516-120">When you declare your derived class, observe the following rules and restrictions:</span></span>

-   <span data-ttu-id="06516-121">A classe pai da classe derivada já deve existir.</span><span class="sxs-lookup"><span data-stu-id="06516-121">The parent class of the derived class must already exist.</span></span>

    <span data-ttu-id="06516-122">A declaração da classe pai pode aparecer no mesmo arquivo MOF que a classe derivada ou em um arquivo diferente.</span><span class="sxs-lookup"><span data-stu-id="06516-122">The declaration of the parent class can appear in the same MOF file as the derived class or in a different file.</span></span> <span data-ttu-id="06516-123">Se a classe pai for desconhecida, o compilador gerará um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="06516-123">If the parent class is unknown, the compiler generates a run-time error.</span></span>

-   <span data-ttu-id="06516-124">Uma classe derivada pode ter apenas uma única classe pai.</span><span class="sxs-lookup"><span data-stu-id="06516-124">A derived class can have only a single parent class.</span></span>

    <span data-ttu-id="06516-125">O WMI não dá suporte a várias heranças.</span><span class="sxs-lookup"><span data-stu-id="06516-125">WMI does not support multiple inheritance.</span></span> <span data-ttu-id="06516-126">No entanto, uma classe pai pode ter muitas classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="06516-126">However, a parent class can have many derived classes.</span></span>

-   <span data-ttu-id="06516-127">Você pode definir índices para classes derivadas, mas o WMI não usa esses índices.</span><span class="sxs-lookup"><span data-stu-id="06516-127">You can define indices for derived classes, but WMI does not use these indices.</span></span>

    <span data-ttu-id="06516-128">Portanto, a especificação de um índice em uma classe derivada não melhora o desempenho de consultas para instâncias da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="06516-128">Therefore, specifying an index on a derived class does not improve the performance of queries for instances of the derived class.</span></span> <span data-ttu-id="06516-129">Você pode melhorar o desempenho de uma consulta em uma classe derivada especificando propriedades indexadas para a classe pai da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="06516-129">You can improve the performance of a query on a derived class by specifying indexed properties for the parent class of the derived class.</span></span>

-   <span data-ttu-id="06516-130">As definições de classe derivada podem ser mais complexas e podem incluir recursos como aliases, qualificadores e tipos de qualificador.</span><span class="sxs-lookup"><span data-stu-id="06516-130">Derived class definitions can be more complex, and can include such features as aliases, qualifiers, and qualifier flavors.</span></span>

    <span data-ttu-id="06516-131">Para obter mais informações, consulte [criando um alias](creating-an-alias.md) e [adicionando um qualificador](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="06516-131">For more information, see [Creating an Alias](creating-an-alias.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

-   <span data-ttu-id="06516-132">Se você quiser alterar um qualificador, alterar o valor padrão de uma propriedade de classe base ou digitar com mais rigidez uma propriedade de referência ou de objeto incorporado de uma classe base, você deve declarar a classe base inteira novamente.</span><span class="sxs-lookup"><span data-stu-id="06516-132">If you wish to change a qualifier, change the default value of a base class property, or more strongly type a reference or embedded object property of a base class, you must declare the entire base class again.</span></span>
-   <span data-ttu-id="06516-133">O número máximo de propriedades que você pode definir em uma classe WMI é 1024.</span><span class="sxs-lookup"><span data-stu-id="06516-133">The maximum number of properties you can define in a WMI class is 1024.</span></span>

> [!Note]  
> <span data-ttu-id="06516-134">Classes não podem ser alteradas durante a execução de provedores.</span><span class="sxs-lookup"><span data-stu-id="06516-134">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="06516-135">Você deve interromper a atividade, alterar a classe e reiniciar o serviço de gerenciamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="06516-135">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="06516-136">Atualmente, não é possível detectar uma alteração de classe.</span><span class="sxs-lookup"><span data-stu-id="06516-136">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="06516-137">Assim como acontece com a classe base, o uso mais comum dessa técnica será por aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="06516-137">As with the base class, the most common use of this technique will be by client applications.</span></span> <span data-ttu-id="06516-138">No entanto, um provedor também pode criar uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="06516-138">However, a provider can also create a derived class.</span></span> <span data-ttu-id="06516-139">Para obter mais informações, consulte [criando uma classe base](creating-a-base-class.md) e [gravando um provedor de classe](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06516-139">For more information, see [Creating a Base Class](creating-a-base-class.md) and [Writing a Class Provider](writing-a-class-provider.md).</span></span>

<span data-ttu-id="06516-140">O exemplo de código neste tópico requer que a seguinte \# instrução include seja compilada corretamente.</span><span class="sxs-lookup"><span data-stu-id="06516-140">The code example in this topic requires the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="06516-141">O procedimento a seguir descreve como criar uma classe derivada usando C++.</span><span class="sxs-lookup"><span data-stu-id="06516-141">The following procedure describes how to create a derived class using C++.</span></span>

<span data-ttu-id="06516-142">**Para criar uma classe derivada usando C++**</span><span class="sxs-lookup"><span data-stu-id="06516-142">**To create a derived class using C++**</span></span>

1.  <span data-ttu-id="06516-143">Localize a classe base com uma chamada para [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="06516-143">Locate the base class with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

    <span data-ttu-id="06516-144">O exemplo de código a seguir mostra como localizar a classe base de exemplo.</span><span class="sxs-lookup"><span data-stu-id="06516-144">The following code example shows how to locate the Example base class.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="06516-145">Crie um objeto derivado da classe base com uma chamada para [**IWbemClassObject:: SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span><span class="sxs-lookup"><span data-stu-id="06516-145">Create a derived object from the base class with a call to [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span></span>

    <span data-ttu-id="06516-146">O exemplo de código a seguir mostra como criar um objeto de classe derivada.</span><span class="sxs-lookup"><span data-stu-id="06516-146">The following code example shows how to create a derived class object.</span></span>

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  <span data-ttu-id="06516-147">Estabeleça um nome para a classe definindo a propriedade do sistema de **\_ \_ classe** com uma chamada para o método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="06516-147">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="06516-148">O exemplo de código a seguir mostra como atribuir um nome à classe derivada.</span><span class="sxs-lookup"><span data-stu-id="06516-148">The following code example shows how to assign a name to the derived class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="06516-149">Crie propriedades adicionais com [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="06516-149">Create additional properties with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="06516-150">O exemplo de código a seguir mostra como criar propriedades adicionais.</span><span class="sxs-lookup"><span data-stu-id="06516-150">The following code example shows how to create additional properties.</span></span>

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  <span data-ttu-id="06516-151">Salve a nova classe chamando [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="06516-151">Save the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="06516-152">O exemplo de código a seguir mostra como salvar a nova classe derivada.</span><span class="sxs-lookup"><span data-stu-id="06516-152">The following code example shows how to save the new derived class.</span></span>

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

<span data-ttu-id="06516-153">O exemplo de código a seguir combina os exemplos de código discutidos no procedimento anterior para descrever como criar uma classe derivada usando a API do WMI.</span><span class="sxs-lookup"><span data-stu-id="06516-153">The following code example combines the code examples discussed in the previous procedure to describe how to create a derived class using the WMI API.</span></span>


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



<span data-ttu-id="06516-154">O procedimento a seguir descreve como definir uma classe derivada usando o código MOF.</span><span class="sxs-lookup"><span data-stu-id="06516-154">The following procedure describes how to define a derived class using MOF code.</span></span>

<span data-ttu-id="06516-155">**Para definir uma classe derivada usando o código MOF**</span><span class="sxs-lookup"><span data-stu-id="06516-155">**To define a derived class using MOF code**</span></span>

1.  <span data-ttu-id="06516-156">Defina a classe derivada com a palavra-chave **Class** , seguida pelo nome da classe derivada e o nome da classe pai separada por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="06516-156">Define your derived class with the **Class** keyword, followed by the name of your derived class, and the name of the parent class separated by a colon.</span></span>

    <span data-ttu-id="06516-157">O exemplo de código a seguir descreve uma implementação de uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="06516-157">The following code example describes an implementation of a derived class.</span></span>

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  <span data-ttu-id="06516-158">Ao concluir, compile seu código MOF com o compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="06516-158">When complete, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="06516-159">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="06516-159">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06516-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06516-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06516-161">Criando uma classe</span><span class="sxs-lookup"><span data-stu-id="06516-161">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



