---
description: Você pode declarar uma instância básica de uma classe no serviço de gerenciamento do Windows usando formato MOF (MOF). Você também pode substituir os valores padrão de uma instância. Para obter mais informações, consulte Definindo um valor de propriedade de instância.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Criando uma instância usando o MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782752"
---
# <a name="creating-an-instance-using-mof"></a><span data-ttu-id="af4d8-105">Criando uma instância usando o MOF</span><span class="sxs-lookup"><span data-stu-id="af4d8-105">Creating an Instance Using MOF</span></span>

<span data-ttu-id="af4d8-106">Você pode declarar uma instância básica de uma classe no serviço de gerenciamento do Windows usando formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="af4d8-106">You can declare a basic instance of a class in the Windows Management service using Managed Object Format (MOF).</span></span> <span data-ttu-id="af4d8-107">Você também pode substituir os valores padrão de uma instância.</span><span class="sxs-lookup"><span data-stu-id="af4d8-107">You can also override the default values for an instance.</span></span> <span data-ttu-id="af4d8-108">Para obter mais informações, consulte [definindo um valor de propriedade de instância](#setting-an-instance-property-value).</span><span class="sxs-lookup"><span data-stu-id="af4d8-108">For more information, see [Setting an Instance Property Value](#setting-an-instance-property-value).</span></span>

<span data-ttu-id="af4d8-109">O procedimento a seguir descreve como declarar uma instância básica de uma classe usando o código MOF.</span><span class="sxs-lookup"><span data-stu-id="af4d8-109">The following procedure describes how to declare a basic instance of a class using MOF code.</span></span>

<span data-ttu-id="af4d8-110">**Para declarar uma instância básica de uma classe usando código MOF**</span><span class="sxs-lookup"><span data-stu-id="af4d8-110">**To declare a basic instance of a class using MOF code**</span></span>

1.  <span data-ttu-id="af4d8-111">Use a **instância de** palavras-chave seguida pelo nome da classe, chaves e um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="af4d8-111">Use the **Instance of** keywords followed by the class name, curly braces, and a semicolon.</span></span>

    <span data-ttu-id="af4d8-112">O exemplo de código a seguir mostra como declarar uma instância de uma classe.</span><span class="sxs-lookup"><span data-stu-id="af4d8-112">The following code example shows how to declare an instance of a class.</span></span>

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  <span data-ttu-id="af4d8-113">Quando terminar, insira o código MOF no repositório WMI usando o compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="af4d8-113">When finished, insert your MOF code into the WMI repository using the MOF compiler.</span></span>

    <span data-ttu-id="af4d8-114">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="af4d8-114">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="af4d8-115">Uma instância de uma classe inclui todas as propriedades da classe.</span><span class="sxs-lookup"><span data-stu-id="af4d8-115">An instance of a class includes all of the properties of the class.</span></span> <span data-ttu-id="af4d8-116">Se a classe for uma classe derivada, as instâncias incluem as propriedades que pertencem a todas as classes mais altas na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="af4d8-116">If the class is a derived class, instances include the properties belonging to all of the classes higher in the hierarchy.</span></span> <span data-ttu-id="af4d8-117">Cada classe da qual uma instância é criada tem uma ou mais propriedades de chave.</span><span class="sxs-lookup"><span data-stu-id="af4d8-117">Each class that an instance is created from has one or more key properties.</span></span> <span data-ttu-id="af4d8-118">Você não pode criar uma instância com mais de 256 chaves.</span><span class="sxs-lookup"><span data-stu-id="af4d8-118">You cannot create an instance with more than 256 keys.</span></span>

## <a name="setting-an-instance-property-value"></a><span data-ttu-id="af4d8-119">Definindo um valor de propriedade de instância</span><span class="sxs-lookup"><span data-stu-id="af4d8-119">Setting an Instance Property Value</span></span>

<span data-ttu-id="af4d8-120">Como o WMI digita Propriedades de tipos, você não pode modificar os tipos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="af4d8-120">Because WMI strongly types properties, you cannot modify property types.</span></span> <span data-ttu-id="af4d8-121">No entanto, você pode definir valores de propriedade em instâncias.</span><span class="sxs-lookup"><span data-stu-id="af4d8-121">You can, however, set property values in instances.</span></span> <span data-ttu-id="af4d8-122">Quando uma classe atribui um valor padrão a uma propriedade, o WMI atribui o valor padrão a cada instância.</span><span class="sxs-lookup"><span data-stu-id="af4d8-122">When a class assigns a default value to a property, WMI assigns the default value to each instance.</span></span> <span data-ttu-id="af4d8-123">Você pode substituir esse valor em sua declaração de instância.</span><span class="sxs-lookup"><span data-stu-id="af4d8-123">You can override this value in your instance declaration.</span></span>

<span data-ttu-id="af4d8-124">O procedimento a seguir descreve como definir um valor de propriedade ou substituir um valor padrão usando o código MOF.</span><span class="sxs-lookup"><span data-stu-id="af4d8-124">The following procedure describes how to set a property value or overwrite a default value using MOF code.</span></span>

<span data-ttu-id="af4d8-125">**Para definir um valor de propriedade ou substituir um valor padrão usando o código MOF**</span><span class="sxs-lookup"><span data-stu-id="af4d8-125">**To set a property value or overwrite a default value using MOF code**</span></span>

1.  <span data-ttu-id="af4d8-126">Coloque uma instrução de atribuição entre as chaves da declaração da instância.</span><span class="sxs-lookup"><span data-stu-id="af4d8-126">Place an assignment statement between the curly braces of the instance declaration.</span></span>

    <span data-ttu-id="af4d8-127">O exemplo de código a seguir mostra como definir um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="af4d8-127">The following code example shows how to set a property value.</span></span>

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    <span data-ttu-id="af4d8-128">O WMI não exige que você defina qualquer propriedade durante a criação da instância.</span><span class="sxs-lookup"><span data-stu-id="af4d8-128">WMI does not require that you set any property during instance creation.</span></span> <span data-ttu-id="af4d8-129">A exceção é qualquer propriedade marcada com o qualificador de [**chave**](key-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="af4d8-129">The exception is any property marked with the [**Key**](key-qualifier.md) qualifier.</span></span> <span data-ttu-id="af4d8-130">Como o WMI usa propriedades de chave para identificar instâncias exclusivamente, você deve definir todas as propriedades de chave conforme as encontrar.</span><span class="sxs-lookup"><span data-stu-id="af4d8-130">Because WMI uses key properties to uniquely identify instances, you must set all key properties as you encounter them.</span></span> <span data-ttu-id="af4d8-131">Por outro lado, você não deve definir uma propriedade do sistema em uma declaração de instância.</span><span class="sxs-lookup"><span data-stu-id="af4d8-131">In contrast, you must not set a system property in an instance declaration.</span></span> <span data-ttu-id="af4d8-132">Em vez disso, o WMI atribui os valores apropriados a uma propriedade do sistema quando necessário.</span><span class="sxs-lookup"><span data-stu-id="af4d8-132">Instead, WMI assigns the appropriate values to a system property when necessary.</span></span>

2.  <span data-ttu-id="af4d8-133">Quando terminar, insira o código MOF no repositório WMI com uma chamada para o compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="af4d8-133">When finished, insert your MOF code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="af4d8-134">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="af4d8-134">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="af4d8-135">Os exemplos de código a seguir mostram como uma instância especifica dados para propriedades definidas por uma classe.</span><span class="sxs-lookup"><span data-stu-id="af4d8-135">The following code examples show how an instance specifies data for properties defined by a class.</span></span>

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

<span data-ttu-id="af4d8-136">No exemplo anterior, a classe define três propriedades: uma cadeia de caracteres, um inteiro com sinal de 32 bits e um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="af4d8-136">In the preceding example, the class defines three properties: a character string, a 32-bit signed integer, and a 32-bit unsigned integer.</span></span> <span data-ttu-id="af4d8-137">A instância fornece valores de dados para cada uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="af4d8-137">The instance provides data values for each of these properties.</span></span>

 

 



