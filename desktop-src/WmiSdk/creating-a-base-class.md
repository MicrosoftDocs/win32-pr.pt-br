---
description: A maneira recomendada para criar uma nova classe base WMI para um provedor WMI é em um arquivo formato MOF (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Criando uma classe base WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922598"
---
# <a name="creating-a-wmi-base-class"></a><span data-ttu-id="3805a-103">Criando uma classe base WMI</span><span class="sxs-lookup"><span data-stu-id="3805a-103">Creating a WMI Base Class</span></span>

<span data-ttu-id="3805a-104">A maneira recomendada para criar uma nova classe base WMI para um provedor WMI é em um arquivo formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3805a-104">The recommended way to create a new WMI base class for a WMI provider is in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="3805a-105">Você também pode criar uma classe base usando a [API com para o WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="3805a-105">You can also create a base class using the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="3805a-106">Embora você possa criar uma classe base ou derivada no script, sem que um provedor forneça dados para a classe e suas subclasses, a classe não é útil.</span><span class="sxs-lookup"><span data-stu-id="3805a-106">While you can create a base or derived class in script, without a provider supplying data to the class and its subclasses, the class is not useful.</span></span>

<span data-ttu-id="3805a-107">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="3805a-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="3805a-108">Criando uma classe base usando o MOF</span><span class="sxs-lookup"><span data-stu-id="3805a-108">Creating a Base Class Using MOF</span></span>](#creating-a-base-class-using-mof)
-   [<span data-ttu-id="3805a-109">Criando uma classe base com C++</span><span class="sxs-lookup"><span data-stu-id="3805a-109">Creating a Base Class with C++</span></span>](#creating-a-base-class-with-c)
-   [<span data-ttu-id="3805a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3805a-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-base-class-using-mof"></a><span data-ttu-id="3805a-111">Criando uma classe base usando o MOF</span><span class="sxs-lookup"><span data-stu-id="3805a-111">Creating a Base Class Using MOF</span></span>

<span data-ttu-id="3805a-112">As classes WMI geralmente dependem da herança.</span><span class="sxs-lookup"><span data-stu-id="3805a-112">WMI classes usually rely on inheritance.</span></span> <span data-ttu-id="3805a-113">Antes de criar uma classe base, verifique as classes de modelo CIM (CIM) disponíveis na[DMTF](https://www.dmtf.org/)(Distributed Management Task Force).</span><span class="sxs-lookup"><span data-stu-id="3805a-113">Before creating a base class, check the Common Information Model (CIM) classes available from the Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span></span>

<span data-ttu-id="3805a-114">Se muitas classes derivadas usarem as mesmas propriedades, coloque essas propriedades e métodos em sua classe base.</span><span class="sxs-lookup"><span data-stu-id="3805a-114">If many derived classes will use the same properties, put these properties and methods in your base class.</span></span> <span data-ttu-id="3805a-115">O número máximo de propriedades que você pode definir em uma classe WMI é 1024.</span><span class="sxs-lookup"><span data-stu-id="3805a-115">The maximum number of properties you can define in a WMI class is 1024.</span></span>

<span data-ttu-id="3805a-116">Ao criar uma classe base, observe a seguinte lista de diretrizes para nomes de classe:</span><span class="sxs-lookup"><span data-stu-id="3805a-116">When creating a base class, observe the following list of guidelines for class names:</span></span>

-   <span data-ttu-id="3805a-117">Use letras maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3805a-117">Use both uppercase and lowercase letters.</span></span>
-   <span data-ttu-id="3805a-118">Inicie um nome de classe com uma letra.</span><span class="sxs-lookup"><span data-stu-id="3805a-118">Begin a class name with a letter.</span></span>
-   <span data-ttu-id="3805a-119">Não use um sublinhado à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="3805a-119">Do not use either a leading or trailing underscore.</span></span>
-   <span data-ttu-id="3805a-120">Defina todos os caracteres restantes como letras, dígitos ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="3805a-120">Define all remaining characters as letters, digits, or underscores.</span></span>
-   <span data-ttu-id="3805a-121">Use uma Convenção de nomenclatura consistente.</span><span class="sxs-lookup"><span data-stu-id="3805a-121">Use a consistent naming convention.</span></span>

    <span data-ttu-id="3805a-122">Embora não seja necessário, uma boa Convenção de nomenclatura para uma classe é dois componentes Unidos por um sublinhado.</span><span class="sxs-lookup"><span data-stu-id="3805a-122">While not necessary, a good naming convention for a class is two components joined by an underscore.</span></span> <span data-ttu-id="3805a-123">Quando possível, um nome de fornecedor deve criar a primeira metade do nome e um nome de classe descritivo deve ser a segunda parte.</span><span class="sxs-lookup"><span data-stu-id="3805a-123">When possible, a vendor name should make up the first half of the name, and a descriptive class name should be the second part.</span></span>

> [!Note]  
> <span data-ttu-id="3805a-124">Classes não podem ser alteradas durante a execução de provedores.</span><span class="sxs-lookup"><span data-stu-id="3805a-124">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="3805a-125">Você deve interromper a atividade, alterar a classe e reiniciar o serviço de gerenciamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="3805a-125">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="3805a-126">Atualmente, não é possível detectar uma alteração de classe.</span><span class="sxs-lookup"><span data-stu-id="3805a-126">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="3805a-127">No MOF, crie uma classe base, nomeando-a com a palavra-chave **Class** , mas não indicando uma classe pai.</span><span class="sxs-lookup"><span data-stu-id="3805a-127">In MOF, create a base class by naming it with the **class** keyword, but not indicating a parent class.</span></span>

<span data-ttu-id="3805a-128">**Para criar uma classe base usando o código MOF**</span><span class="sxs-lookup"><span data-stu-id="3805a-128">**To create a base class using MOF code**</span></span>

1.  <span data-ttu-id="3805a-129">Use a palavra-chave **Class** com o nome da nova classe, seguida por um par de chaves e um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="3805a-129">Use the **class** keyword with the name of the new class, followed by a pair of curly braces and a semicolon.</span></span> <span data-ttu-id="3805a-130">Adicione Propriedades e métodos para a classe entre as chaves.</span><span class="sxs-lookup"><span data-stu-id="3805a-130">Add properties and methods for the class between the curly braces.</span></span> <span data-ttu-id="3805a-131">O exemplo de código a seguir é fornecido.</span><span class="sxs-lookup"><span data-stu-id="3805a-131">The following code example is provided.</span></span>

    <span data-ttu-id="3805a-132">O exemplo de código a seguir mostra como uma classe base deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="3805a-132">The following code example shows how a base class should be defined.</span></span>

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    <span data-ttu-id="3805a-133">O exemplo de código a seguir mostra uma definição incorreta de uma classe base.</span><span class="sxs-lookup"><span data-stu-id="3805a-133">The following code example shows an incorrect definition of a base class.</span></span>

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  <span data-ttu-id="3805a-134">Adicione qualquer [*qualificador*](gloss-q.md) de classe antes da palavra-chave class para modificar a maneira como a classe é usada.</span><span class="sxs-lookup"><span data-stu-id="3805a-134">Add any class [*qualifiers*](gloss-q.md) before the class keyword to modify the way the class is used.</span></span> <span data-ttu-id="3805a-135">Coloque os qualificadores entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="3805a-135">Place the qualifiers between square brackets.</span></span> <span data-ttu-id="3805a-136">Para obter mais informações sobre qualificadores para modificar classes, consulte [qualificadores WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="3805a-136">For more information about qualifiers for modifying classes, see [WMI Qualifiers](wmi-qualifiers.md).</span></span> <span data-ttu-id="3805a-137">Use o qualificador **abstract** para indicar que você não pode criar uma instância dessa classe diretamente.</span><span class="sxs-lookup"><span data-stu-id="3805a-137">Use the **Abstract** qualifier to indicate that you cannot create an instance of this class directly.</span></span> <span data-ttu-id="3805a-138">Classes abstratas são geralmente usadas para definir propriedades ou métodos que serão usados por várias classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="3805a-138">Abstract classes are often used to define properties or methods that will be used by several derived classes.</span></span> <span data-ttu-id="3805a-139">Para obter mais informações, consulte [criando uma classe derivada](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="3805a-139">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

    <span data-ttu-id="3805a-140">O exemplo de código a seguir define a classe como abstrata e define o provedor que fornecerá os dados.</span><span class="sxs-lookup"><span data-stu-id="3805a-140">The following code example defines the class as abstract and defines the provider that will supply the data.</span></span> <span data-ttu-id="3805a-141">O [*tipo*](gloss-f.md) de qualificador **ToSubClass** indica que as informações no qualificador de **provedor** são herdadas por classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="3805a-141">The **ToSubClass** qualifier [*flavor*](gloss-f.md) indicates that the information in the **Provider** qualifier is inherited by derived classes.</span></span>

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  <span data-ttu-id="3805a-142">Adicione as propriedades e os métodos para a classe dentro de colchetes antes do nome da propriedade ou do método.</span><span class="sxs-lookup"><span data-stu-id="3805a-142">Add the properties and methods for the class inside square brackets before the property or method name.</span></span> <span data-ttu-id="3805a-143">Para obter mais informações, consulte [adicionando uma propriedade](adding-a-property.md) e [criando um método](creating-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3805a-143">For more information, see [Adding a Property](adding-a-property.md) and [Creating a Method](creating-a-method.md).</span></span> <span data-ttu-id="3805a-144">Você pode modificar essas propriedades e métodos usando qualificadores MOF.</span><span class="sxs-lookup"><span data-stu-id="3805a-144">You can modify these properties and methods using MOF qualifiers.</span></span> <span data-ttu-id="3805a-145">Para obter mais informações, consulte [adicionando um qualificador](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="3805a-145">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

    <span data-ttu-id="3805a-146">O exemplo de código a seguir mostra como modificar propriedades e métodos com qualificadores MOF.</span><span class="sxs-lookup"><span data-stu-id="3805a-146">The following code example shows how to modify properties and methods with MOF qualifiers.</span></span>

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  <span data-ttu-id="3805a-147">Salve o arquivo MOF com uma extensão. mof.</span><span class="sxs-lookup"><span data-stu-id="3805a-147">Save the MOF file with an extension of .mof.</span></span>
5.  <span data-ttu-id="3805a-148">Registre a classe com WMI executando [**Mofcomp.exe**](mofcomp.md) no arquivo.</span><span class="sxs-lookup"><span data-stu-id="3805a-148">Register the class with WMI by running [**Mofcomp.exe**](mofcomp.md) on the file.</span></span>

    <span data-ttu-id="3805a-149">**mofcomp.exe** *newmof. mof*</span><span class="sxs-lookup"><span data-stu-id="3805a-149">**mofcomp.exe** *newmof.mof*</span></span>

    <span data-ttu-id="3805a-150">Se você não usar a opção **-N** ou o \# [**namespace pragma**](pragma-namespace.md) do comando de pré-processador para especificar um namespace, as classes MOF compiladas serão armazenadas no \\ namespace root padrão no repositório.</span><span class="sxs-lookup"><span data-stu-id="3805a-150">If you do not use the **-N** switch or the preprocessor command \#[**pragma namespace**](pragma-namespace.md) to specify a namespace, the compiled MOF classes will be stored in the root\\default namespace in the repository.</span></span> <span data-ttu-id="3805a-151">Para obter mais informações, consulte [**Mofcomp**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="3805a-151">For more information, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="3805a-152">O exemplo de código a seguir combina os exemplos de código MOF discutidos no procedimento anterior e mostra como criar uma classe base no \\ namespace raiz cimv2 usando o MOF.</span><span class="sxs-lookup"><span data-stu-id="3805a-152">The following code example combines the MOF code examples discussed in the previous procedure and shows how to create a base class in the root\\cimv2 namespace using MOF.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

<span data-ttu-id="3805a-153">Para obter mais informações, consulte [criando uma classe derivada](creating-a-derived-class.md) para obter um exemplo de uma classe dinâmica derivada desta classe base.</span><span class="sxs-lookup"><span data-stu-id="3805a-153">For more information, see [Creating a Derived Class](creating-a-derived-class.md) for an example of a dynamic class derived from this base class.</span></span>

## <a name="creating-a-base-class-with-c"></a><span data-ttu-id="3805a-154">Criando uma classe base com C++</span><span class="sxs-lookup"><span data-stu-id="3805a-154">Creating a Base Class with C++</span></span>

<span data-ttu-id="3805a-155">Criar uma classe base usando a API do WMI é principalmente uma série de comandos Put que definem a classe e registram a classe com o WMI.</span><span class="sxs-lookup"><span data-stu-id="3805a-155">Creating a base class using the WMI API is mainly a series of Put commands that define the class and register the class with WMI.</span></span> <span data-ttu-id="3805a-156">A principal finalidade dessa API é permitir que aplicativos cliente criem classes base.</span><span class="sxs-lookup"><span data-stu-id="3805a-156">The main purpose of this API is to enable client applications to create base classes.</span></span> <span data-ttu-id="3805a-157">No entanto, você também pode fazer com que um provedor Use essa API para criar uma classe base.</span><span class="sxs-lookup"><span data-stu-id="3805a-157">However, you can also have a provider use this API to create a base class.</span></span> <span data-ttu-id="3805a-158">Por exemplo, se você acreditar que o código MOF para seu provedor não será instalado corretamente, você poderá instruir seu provedor para criar automaticamente as classes corretas no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="3805a-158">For example, if you believe that the MOF code for your provider will not be installed properly, you can instruct your provider to automatically create the correct classes in the WMI repository.</span></span> <span data-ttu-id="3805a-159">Para obter mais informações sobre provedores, consulte [escrevendo um provedor de classe](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3805a-159">For more information about providers, see [Writing a Class Provider](writing-a-class-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="3805a-160">Classes não podem ser alteradas durante a execução de provedores.</span><span class="sxs-lookup"><span data-stu-id="3805a-160">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="3805a-161">Você deve interromper a atividade, alterar a classe e reiniciar o serviço de gerenciamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="3805a-161">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="3805a-162">Atualmente, não é possível detectar uma alteração de classe.</span><span class="sxs-lookup"><span data-stu-id="3805a-162">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="3805a-163">O código requer a seguinte referência para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="3805a-163">The code requires the following reference to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="3805a-164">Você pode criar uma nova classe base programaticamente usando a [API com para o WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="3805a-164">You can create a new base class programmatically using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="3805a-165">**Para criar uma nova classe base com a API do WMI**</span><span class="sxs-lookup"><span data-stu-id="3805a-165">**To create a new base class with the WMI API**</span></span>

1.  <span data-ttu-id="3805a-166">Recupere uma definição para a nova classe chamando o método [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) com o parâmetro *strObjectPath* definido como um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="3805a-166">Retrieve a definition for the new class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method with the *strObjectPath* parameter set to a **null** value.</span></span>

    <span data-ttu-id="3805a-167">O exemplo de código a seguir mostra como recuperar uma definição para uma nova classe.</span><span class="sxs-lookup"><span data-stu-id="3805a-167">The following code example shows how to retrieve a definition for a new class.</span></span>

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  <span data-ttu-id="3805a-168">Estabeleça um nome para a classe definindo a propriedade do sistema de **\_ \_ classe** com uma chamada para o método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="3805a-168">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="3805a-169">O exemplo de código a seguir mostra como nomear a classe definindo a propriedade do sistema de **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="3805a-169">The following code example shows how to name the class by setting the **\_\_CLASS** system property.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  <span data-ttu-id="3805a-170">Crie a propriedade ou propriedades de chave chamando [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="3805a-170">Create the key property or properties by calling [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="3805a-171">O exemplo de código a seguir descreve como criar a propriedade [**index**](swbemrefreshableitem-index.md) , que é rotulada como uma propriedade de chave na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="3805a-171">The following code example describes how to create the [**Index**](swbemrefreshableitem-index.md) property, which is labeled as a key property in Step 4.</span></span>

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  <span data-ttu-id="3805a-172">Anexe o qualificador padrão da [**chave**](standard-qualifiers.md) à propriedade de chave chamando primeiro o método [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) e, em seguida, o método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="3805a-172">Attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property by first calling the [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) method and then the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="3805a-173">O exemplo de código a seguir mostra como anexar o qualificador de [**chave**](standard-qualifiers.md) padrão à propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="3805a-173">The following code example shows how to attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property.</span></span>

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  <span data-ttu-id="3805a-174">Crie outras propriedades da classe com [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="3805a-174">Create other properties of the class with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="3805a-175">O exemplo de código a seguir descreve como criar propriedades adicionais.</span><span class="sxs-lookup"><span data-stu-id="3805a-175">The following code example describes how to create additional properties.</span></span>

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  <span data-ttu-id="3805a-176">Registre a nova classe chamando [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="3805a-176">Register the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="3805a-177">Como não é possível definir chaves e índices depois de registrar uma nova classe, verifique se você definiu todas as suas propriedades antes de chamar [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="3805a-177">Because you cannot define keys and indices after you register a new class, ensure that you have defined all of your properties before calling [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="3805a-178">O exemplo de código a seguir descreve como registrar uma nova classe.</span><span class="sxs-lookup"><span data-stu-id="3805a-178">The following code example describes how to register a new class.</span></span>

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

<span data-ttu-id="3805a-179">O exemplo de código a seguir combina os exemplos de código discutidos no procedimento anterior e mostra como criar uma classe base usando a API do WMI.</span><span class="sxs-lookup"><span data-stu-id="3805a-179">The following code example combines the code examples discussed in the previous procedure and shows how to create a base class using the WMI API.</span></span>


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="3805a-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3805a-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3805a-181">Criando uma classe</span><span class="sxs-lookup"><span data-stu-id="3805a-181">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



