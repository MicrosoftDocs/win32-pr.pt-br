---
description: Para criar um método WMI, defina os parâmetros de entrada e saída para o método.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Criando um método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171453"
---
# <a name="creating-a-wmi-method"></a><span data-ttu-id="e1bc8-103">Criando um método WMI</span><span class="sxs-lookup"><span data-stu-id="e1bc8-103">Creating a WMI Method</span></span>

<span data-ttu-id="e1bc8-104">Para criar um método WMI, defina os parâmetros de entrada e saída para o método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-104">To create a WMI method, define the input and output parameters for the method.</span></span> <span data-ttu-id="e1bc8-105">Os parâmetros de entrada e saída são representados por um [**\_ \_ parâmetro**](--parameters.md)especial de classe do sistema WMI.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-105">The input and output parameters are represented by a special WMI system class [**\_\_PARAMETERS**](--parameters.md).</span></span> <span data-ttu-id="e1bc8-106">Para obter mais informações, consulte [chamando um método](calling-a-method.md) e [escrevendo um provedor de método](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e1bc8-106">For more information, see [Calling a Method](calling-a-method.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="e1bc8-107">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="e1bc8-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="e1bc8-108">Criando um método de classe WMI no MOF</span><span class="sxs-lookup"><span data-stu-id="e1bc8-108">Creating a WMI Class Method in MOF</span></span>](#creating-a-wmi-class-method-in-mof)
-   [<span data-ttu-id="e1bc8-109">Criando um método de classe WMI em C++</span><span class="sxs-lookup"><span data-stu-id="e1bc8-109">Creating a WMI Class Method in C++</span></span>](#creating-a-wmi-class-method-in-c)
-   [<span data-ttu-id="e1bc8-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1bc8-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a><span data-ttu-id="e1bc8-111">Criando um método de classe WMI no MOF</span><span class="sxs-lookup"><span data-stu-id="e1bc8-111">Creating a WMI Class Method in MOF</span></span>

<span data-ttu-id="e1bc8-112">No WMI, os métodos de provedor geralmente são ações distintas relacionadas ao objeto que a classe representa.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-112">In WMI, provider methods are generally distinct actions related to the object that the class represents.</span></span> <span data-ttu-id="e1bc8-113">Em vez de alterar o valor de uma propriedade para executar uma ação, um método deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-113">Rather than change the value of a property to execute an action, a method should be created.</span></span> <span data-ttu-id="e1bc8-114">Por exemplo, você pode habilitar ou desabilitar um centro de informações de rede (NIC) que é representado pelo [**Win32 \_ adaptador**](/windows/desktop/CIMWin32Prov/win32-networkadapter) usando os métodos [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) e [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) .</span><span class="sxs-lookup"><span data-stu-id="e1bc8-114">For example, you can enable or disable a network information center (NIC) that is represented by [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) by using the [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) and [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) methods.</span></span> <span data-ttu-id="e1bc8-115">Embora essas ações possam ser representadas como uma propriedade de leitura/gravação, o design recomendado é criar um método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-115">While these actions can be represented as a read/write property, the recommended design is to create a method.</span></span> <span data-ttu-id="e1bc8-116">Como alternativa, se você quiser tornar um Estado ou valor visível para a classe, a abordagem recomendada é criar uma propriedade de leitura/gravação em vez de um método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-116">Alternatively, if you want to make a state or value visible for the class, then the recommended approach is to create a read/write property rather than a method.</span></span> <span data-ttu-id="e1bc8-117">No **Win32 \_ adaptador**, a propriedade **netativad** torna o estado do adaptador visível, mas as alterações entre os Estados são executadas pelos métodos **Enable** ou **Disable** .</span><span class="sxs-lookup"><span data-stu-id="e1bc8-117">In **Win32\_NetworkAdapter**, the **NetEnabled** property makes the state of the adapter visible but changes between states are executed by the **Enable** or **Disable** methods.</span></span>

<span data-ttu-id="e1bc8-118">Declarações de classe podem incluir a declaração de um ou mais métodos.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-118">Class declarations can include the declaration of one or more methods.</span></span> <span data-ttu-id="e1bc8-119">Você pode optar por herdar os métodos de uma classe pai ou implementar suas próprias.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-119">You can either choose to inherit the methods of a parent class, or implement your own.</span></span> <span data-ttu-id="e1bc8-120">Se você optar por implementar seus próprios métodos, deverá declarar o método e marcar o método com marcas de qualificador específicas.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-120">If you choose to implement your own methods, you must declare the method and mark the method with specific qualifier tags.</span></span>

<span data-ttu-id="e1bc8-121">O procedimento a seguir descreve como declarar um método em uma classe que não herda de uma classe base.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-121">The following procedure describes how to declare a method in a class that does not inherit from a base class.</span></span>

<span data-ttu-id="e1bc8-122">**Para declarar um método**</span><span class="sxs-lookup"><span data-stu-id="e1bc8-122">**To declare a method**</span></span>

1.  <span data-ttu-id="e1bc8-123">Defina o nome do seu método entre as chaves de uma declaração de classe, seguida por quaisquer qualificadores.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-123">Define the name of your method between the curly braces of a class declaration, followed by any qualifiers.</span></span>

    <span data-ttu-id="e1bc8-124">O exemplo de código a seguir descreve a sintaxe de um método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-124">The following code example describes the syntax for a method.</span></span>

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  <span data-ttu-id="e1bc8-125">Quando terminar, insira seu código de formato MOF (MOF) no repositório WMI com uma chamada para o compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-125">When finished, insert your Managed Object Format (MOF) code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="e1bc8-126">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e1bc8-126">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="e1bc8-127">A lista a seguir define os elementos da declaração do método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-127">The following list defines the elements of the method declaration.</span></span>

<dl> <dt>

<span data-ttu-id="e1bc8-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Operador**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="e1bc8-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>
</dt> <dd>

<span data-ttu-id="e1bc8-129">Vincula um provedor específico à sua descrição de classe.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-129">Links a specific provider to your class description.</span></span> <span data-ttu-id="e1bc8-130">O valor do qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) é o nome do provedor, que informa ao WMI onde o código que dá suporte ao seu método reside.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-130">The value of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is the name of the provider, which tells WMI where the code that supports your method resides.</span></span> <span data-ttu-id="e1bc8-131">Um provedor também deve marcar com o qualificador **dinâmico** qualquer classe que tenha instâncias dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-131">A provider should also mark with the **Dynamic** qualifier any class that has dynamic instances.</span></span> <span data-ttu-id="e1bc8-132">Por outro lado, não use o qualificador **dinâmico** para marcar uma classe que contém uma instância estática com métodos **implementados** .</span><span class="sxs-lookup"><span data-stu-id="e1bc8-132">In contrast, do not use the **Dynamic** qualifier to mark a class that contains a static instance with **Implemented** methods.</span></span>

</dd> <dt>

<span data-ttu-id="e1bc8-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementado**</span><span class="sxs-lookup"><span data-stu-id="e1bc8-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="e1bc8-134">Declara que você implementará um método, em vez de herdar a implementação do método da classe pai.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-134">Declares that you will implement a method, rather than inherit the method implementation from the parent class.</span></span> <span data-ttu-id="e1bc8-135">Por padrão, o WMI propaga a implementação da classe pai para uma classe derivada, a menos que a classe derivada forneça uma implementação.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-135">By default, WMI propagates the implementation of the parent class to a derived class unless the derived class provides an implementation.</span></span> <span data-ttu-id="e1bc8-136">Omitir o qualificador **implementado** indica que o método não tem nenhuma implementação nessa classe.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-136">Omitting the **Implemented** qualifier indicates that the method has no implementation in that class.</span></span> <span data-ttu-id="e1bc8-137">Se você redeclarar um método sem o qualificador **implementado** , o WMI ainda pressupõe que você não vai implementar esse método e invoca a implementação do método de classe pai quando chamado.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-137">If you redeclare a method without the **Implemented** qualifier, WMI still assumes that you are not going to implement that method, and invokes the parent class method implementation when called.</span></span> <span data-ttu-id="e1bc8-138">Dessa forma, a redeclaração de um método em uma classe derivada sem anexar o qualificador **implementado** é útil somente quando você adiciona ou remove um qualificador de ou para o método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-138">As such, redeclaring a method in a derived class without attaching the **Implemented** qualifier is useful only when you add or remove a qualifier to or from the method.</span></span>

</dd> <dt>

<span data-ttu-id="e1bc8-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span><span class="sxs-lookup"><span data-stu-id="e1bc8-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span></span>
</dt> <dd>

<span data-ttu-id="e1bc8-140">Descreve o valor que o método retorna.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-140">Describes what value the method returns.</span></span> <span data-ttu-id="e1bc8-141">O valor de retorno para um método deve ser um objeto booliano, numérico, **Char**, **cadeia de caracteres**, [DateTime](datetime.md)ou esquema.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-141">The return value for a method must be a Boolean, numeric, **CHAR**, **STRING**, [DATETIME](datetime.md), or schema object.</span></span> <span data-ttu-id="e1bc8-142">Você também pode declarar o tipo de retorno como [void](void.md), indicando que o método não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-142">You can also declare the return type as [VOID](void.md), indicating that the method returns nothing.</span></span> <span data-ttu-id="e1bc8-143">No entanto, você não pode declarar uma matriz como um tipo de valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-143">However, you cannot declare an array as a return value type.</span></span>

</dd> <dt>

<span data-ttu-id="e1bc8-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span><span class="sxs-lookup"><span data-stu-id="e1bc8-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span></span>
</dt> <dd>

<span data-ttu-id="e1bc8-145">Define o nome do método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-145">Defines the name of the method.</span></span> <span data-ttu-id="e1bc8-146">Cada método deve ter um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-146">Every method must have a unique name.</span></span> <span data-ttu-id="e1bc8-147">O WMI não permite que dois métodos com o mesmo nome e assinaturas diferentes existam em uma classe ou em uma hierarquia de classe.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-147">WMI does not allow two methods with the same name and different signatures to exist in one class or within a class hierarchy.</span></span> <span data-ttu-id="e1bc8-148">Como tal, você também não pode sobrecarregar um método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-148">As such, you also cannot overload a method.</span></span>

</dd> <dt>

<span data-ttu-id="e1bc8-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="e1bc8-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span></span>
</dt> <dd>

<span data-ttu-id="e1bc8-150">Contém qualificadores que descrevem se um parâmetro é um parâmetro de entrada, um parâmetro de saída ou ambos.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-150">Contains qualifiers that describe if a parameter is an input parameter, output parameter, or both.</span></span> <span data-ttu-id="e1bc8-151">Não use o mesmo nome de parâmetro mais de uma vez como um parâmetro de entrada ou mais de uma vez como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-151">Do not use the same parameter name more than one time as an input parameter or more than one time as an output parameter.</span></span> <span data-ttu-id="e1bc8-152">Se o mesmo nome de parâmetro aparecer com os qualificadores [**in**](standard-qualifiers.md) e **out** , a funcionalidade será conceitualmente a mesma que usar os qualificadores **in** e **out** em um único parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-152">If the same parameter name appears with both the [**In**](standard-qualifiers.md) and an **Out** qualifiers, the functionality is conceptually the same as using the **In**, **Out** qualifiers on a single parameter.</span></span> <span data-ttu-id="e1bc8-153">No entanto, ao usar declarações separadas, os parâmetros de entrada e saída devem ser exatamente os mesmos em todos os outros aspectos, incluindo o número e o tipo de qualificadores de [**ID**](standard-wmi-qualifiers.md) , e o qualificador deve ser o mesmo e declarado explicitamente para ambos.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-153">However, when using separate declarations, the input and output parameters must be exactly the same in all other respects, including the number and type of [**ID**](standard-wmi-qualifiers.md) qualifiers, and the qualifier must be the same and explicitly declared for both.</span></span> <span data-ttu-id="e1bc8-154">É altamente recomendável usar os qualificadores **in** e **out** dentro de uma declaração de parâmetro único.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-154">It is strongly recommended to use the **In**, **Out** qualifiers within a single parameter declaration.</span></span>

</dd> <dt>

<span data-ttu-id="e1bc8-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span><span class="sxs-lookup"><span data-stu-id="e1bc8-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="e1bc8-156">Contém o qualificador de [**ID**](standard-wmi-qualifiers.md) que identifica exclusivamente a posição de cada parâmetro na sequência de parâmetros no método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-156">Contains the [**ID**](standard-wmi-qualifiers.md) qualifier that uniquely identifies the position of each parameter within the sequence of parameters in the method.</span></span> <span data-ttu-id="e1bc8-157">Por padrão, o compilador MOF marca automaticamente os parâmetros com um qualificador de **ID** .</span><span class="sxs-lookup"><span data-stu-id="e1bc8-157">By default, the MOF compiler automatically marks parameters with an **ID** qualifier.</span></span> <span data-ttu-id="e1bc8-158">O compilador marca o primeiro parâmetro com um valor de 0 (zero), o segundo parâmetro com um valor de 1 (um) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-158">The compiler marks the first parameter with a value of 0 (zero), the second parameter a value of 1 (one), and so on.</span></span> <span data-ttu-id="e1bc8-159">Se necessário, você pode declarar explicitamente a sequência de ID em seu código MOF.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-159">If necessary, you can explicitly state the ID sequence in your MOF code.</span></span>

</dd> <dt>

<span data-ttu-id="e1bc8-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span><span class="sxs-lookup"><span data-stu-id="e1bc8-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span></span>
</dt> <dd>

<span data-ttu-id="e1bc8-161">Descreve o tipo de dados que o método pode aceitar.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-161">Describes what data type the method can accept.</span></span> <span data-ttu-id="e1bc8-162">Você pode definir um tipo de parâmetro como qualquer valor de dados MOF, incluindo uma matriz, objeto de esquema ou referência.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-162">You can define a parameter type as any MOF data value, including an array, schema object, or reference.</span></span> <span data-ttu-id="e1bc8-163">Ao usar uma matriz como parâmetro, use a matriz como desassociada ou com um tamanho explícito.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-163">When using an array as a parameter, use the array as unbound or with an explicit size.</span></span>

</dd> <dt>

<span data-ttu-id="e1bc8-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span><span class="sxs-lookup"><span data-stu-id="e1bc8-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span></span>
</dt> <dd>

<span data-ttu-id="e1bc8-165">Contém o nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-165">Contains the name of the parameter.</span></span> <span data-ttu-id="e1bc8-166">Você também pode optar por definir o valor padrão do parâmetro neste ponto.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-166">You can also choose to define the default value of the parameter at this point.</span></span> <span data-ttu-id="e1bc8-167">Os parâmetros sem valores iniciais permanecem não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-167">Parameters lacking initial values remain unassigned.</span></span>

</dd> </dl>

<span data-ttu-id="e1bc8-168">O exemplo de código a seguir descreve a lista de parâmetros e qualificadores.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-168">The following code example describes parameter listing and qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

<span data-ttu-id="e1bc8-169">O exemplo de código a seguir descreve como usar uma matriz em um parâmetro do MOF.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-169">The following code example describes how to use an array in a MOF parameter.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

<span data-ttu-id="e1bc8-170">O exemplo de código a seguir descreve como usar um objeto de esquema como um valor de parâmetro e de retorno.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-170">The following code example describes using a schema object as both a parameter and return value.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

<span data-ttu-id="e1bc8-171">O exemplo de código a seguir descreve como incluir duas referências: uma para uma instância da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e outra para uma instância de um tipo de objeto desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-171">The following code example describes how to include two references: one to an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and the other to an instance of an unknown object type.</span></span>

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a><span data-ttu-id="e1bc8-172">Criando um método de classe WMI em C++</span><span class="sxs-lookup"><span data-stu-id="e1bc8-172">Creating a WMI Class Method in C++</span></span>

<span data-ttu-id="e1bc8-173">O procedimento a seguir descreve como criar um método de classe WMI programaticamente.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-173">The following procedure describes how to create a WMI class method programmatically.</span></span>

<span data-ttu-id="e1bc8-174">**Para criar um método de classe WMI programaticamente**</span><span class="sxs-lookup"><span data-stu-id="e1bc8-174">**To create a WMI class method programmatically**</span></span>

1.  <span data-ttu-id="e1bc8-175">Crie a classe à qual o método pertencerá.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-175">Create the class to which the method will belong.</span></span>

    <span data-ttu-id="e1bc8-176">Você deve primeiro ter uma classe para posicionar o método no antes de criar o método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-176">You must first have a class to place the method in before you create the method.</span></span>

2.  <span data-ttu-id="e1bc8-177">Recupere duas classes filhas da classe System [**\_ \_ Parameters**](--parameters.md) usando [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="e1bc8-177">Retrieve two child classes of the [**\_\_PARAMETERS**](--parameters.md) system class using either [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="e1bc8-178">Use a primeira classe filho para descrever os parâmetros in e a segunda para descrever os parâmetros out.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-178">Use the first child class to describe the in-parameters, and the second to describe the out-parameters.</span></span> <span data-ttu-id="e1bc8-179">Se necessário, você pode executar uma única recuperação seguida de uma chamada para o método [**IWbemClassObject:: clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .</span><span class="sxs-lookup"><span data-stu-id="e1bc8-179">If necessary, you can perform a single retrieval followed by a call to the [**IWbemClassObject::Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

3.  <span data-ttu-id="e1bc8-180">Escreva os parâmetros in na primeira classe e os parâmetros out para a segunda classe, usando uma ou mais chamadas para [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="e1bc8-180">Write the in-parameters to the first class, and the out-parameters to the second class, using one or more calls to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="e1bc8-181">Ao descrever os parâmetros para um método, observe as seguintes regras e restrições:</span><span class="sxs-lookup"><span data-stu-id="e1bc8-181">When describing parameters to a method, observe the following rules and restrictions:</span></span>

    -   <span data-ttu-id="e1bc8-182">Trate os \[ parâmetros in e out \] como entradas separadas, um no objeto que contém os parâmetros in e um no objeto que contém os parâmetros out.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-182">Treat the \[in, out\] parameters as separate entries, one in the object that contains the in-parameters and one in the object that contains the out-parameters.</span></span>
    -   <span data-ttu-id="e1bc8-183">Além dos \[ qualificadores de saída, \] os qualificadores restantes devem ser exatamente iguais.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-183">Other than the \[in, out\] qualifiers, the remaining qualifiers must be exactly the same.</span></span>
    -   <span data-ttu-id="e1bc8-184">Especifique os qualificadores de [**ID**](standard-wmi-qualifiers.md) , começando em 0 (zero), um para cada parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-184">Specify the [**ID**](standard-wmi-qualifiers.md) qualifiers, starting at 0 (zero), one for each parameter.</span></span>

        <span data-ttu-id="e1bc8-185">A ordem dos parâmetros de entrada ou saída é estabelecida pelo valor do qualificador de [**ID**](standard-wmi-qualifiers.md) em cada parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-185">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="e1bc8-186">Todos os argumentos de entrada devem preceder quaisquer argumentos de saída.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-186">All input arguments must precede any output arguments.</span></span> <span data-ttu-id="e1bc8-187">Alterar a ordem dos parâmetros de entrada e saída do método ao atualizar um provedor de métodos existente pode fazer com que os aplicativos que chamam o método falhem.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-187">Changing the order of method input and output parameters when updating an existing method provider can cause applications that call the method to fail.</span></span> <span data-ttu-id="e1bc8-188">Adicione novos parâmetros de entrada ao final dos parâmetros existentes em vez de inseri-los na sequência que já está estabelecida.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-188">Add new input parameters at the end of the existing parameters rather than inserting them in the sequence that is already established.</span></span>

        <span data-ttu-id="e1bc8-189">Certifique-se de não deixar nenhuma lacuna na sequência de qualificador de [**ID**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="e1bc8-189">Make sure to leave no gaps in the [**ID**](standard-wmi-qualifiers.md) qualifier sequence.</span></span>

    -   <span data-ttu-id="e1bc8-190">Coloque o valor de retorno na classe out-Parameters como uma propriedade chamada **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-190">Place the return value in the out-parameters class as a property named **ReturnValue**.</span></span>

        <span data-ttu-id="e1bc8-191">Isso identifica a propriedade como o valor de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-191">This identifies the property as the return value of the method.</span></span> <span data-ttu-id="e1bc8-192">O tipo CIM dessa propriedade é o tipo de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-192">The CIM type of this property is the return type of the method.</span></span> <span data-ttu-id="e1bc8-193">Se o método tiver um tipo de retorno de void, não terá uma propriedade **ReturnValue** .</span><span class="sxs-lookup"><span data-stu-id="e1bc8-193">If the method has a return type of void, then do not have a **ReturnValue** property at all.</span></span> <span data-ttu-id="e1bc8-194">Além disso, a propriedade **ReturnValue** não pode ter um qualificador de [**ID**](standard-wmi-qualifiers.md) como os argumentos do método.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-194">Also, the **ReturnValue** property cannot have an [**ID**](standard-wmi-qualifiers.md) qualifier like the arguments of the method.</span></span> <span data-ttu-id="e1bc8-195">A atribuição de um qualificador de **ID** à propriedade **ReturnValue** produz um erro de WMI.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-195">Assigning an **ID** qualifier to the **ReturnValue** property produces a WMI error.</span></span>

    -   <span data-ttu-id="e1bc8-196">Expresse todos os valores de parâmetro padrão para a propriedade na classe.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-196">Express any default parameter values for the property in the class.</span></span>

4.  <span data-ttu-id="e1bc8-197">Coloque os dois objetos de [**\_ \_ parâmetros**](--parameters.md) na classe pai com uma chamada para [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="e1bc8-197">Place both [**\_\_PARAMETERS**](--parameters.md) objects into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

    <span data-ttu-id="e1bc8-198">Uma única chamada para [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) pode posicionar os dois objetos de [**\_ \_ parâmetros**](--parameters.md) na classe.</span><span class="sxs-lookup"><span data-stu-id="e1bc8-198">A single call to [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) can place both [**\_\_PARAMETERS**](--parameters.md) objects into the class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1bc8-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1bc8-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1bc8-200">Criando uma classe</span><span class="sxs-lookup"><span data-stu-id="e1bc8-200">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 
