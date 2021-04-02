---
description: Uma matriz é uma lista indexada de valores de dados que são do mesmo tipo de dados, que você pode referenciar. Além das matrizes de cadeia de caracteres e numéricas, o MOF oferece suporte a matrizes de objetos e referências inseridas.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Matrizes MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164859"
---
# <a name="mof-arrays"></a><span data-ttu-id="e1aa9-104">Matrizes MOF</span><span class="sxs-lookup"><span data-stu-id="e1aa9-104">MOF Arrays</span></span>

<span data-ttu-id="e1aa9-105">Uma matriz é uma lista indexada de valores de dados que são do mesmo tipo de dados, que você pode referenciar.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-105">An array is an indexed list of data values that are of the same data type, which you can reference.</span></span> <span data-ttu-id="e1aa9-106">Além das matrizes de cadeia de caracteres e numéricas, o MOF oferece suporte a matrizes de objetos e referências inseridas.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-106">In addition to string and numeric arrays, MOF supports arrays of embedded objects and references.</span></span>

<span data-ttu-id="e1aa9-107">As regras a seguir definem uma matriz MOF:</span><span class="sxs-lookup"><span data-stu-id="e1aa9-107">The following rules define a MOF array:</span></span>

-   <span data-ttu-id="e1aa9-108">Colchetes usados após o identificador de propriedade especifique uma matriz em uma definição de classe.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-108">Brackets used after the property identifier specify an array in a class definition.</span></span>

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   <span data-ttu-id="e1aa9-109">Todas as matrizes devem ser unidimensionais.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-109">All arrays must be one-dimensional.</span></span>
-   <span data-ttu-id="e1aa9-110">As matrizes podem ser desassociadas ou ter um tamanho explícito.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-110">Arrays can be unbounded or have an explicit size.</span></span>

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    <span data-ttu-id="e1aa9-111">O WMI implementa matrizes vinculadas e não associadas como estruturas **SafeArray** , o que permite que o WMI varie as dimensões da matriz em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-111">WMI implements bounded and unbounded arrays as **SAFEARRAY** structures, which allows WMI to vary array dimensions at run time.</span></span> <span data-ttu-id="e1aa9-112">Quando você declara uma matriz com um tamanho explícito, o WMI armazena o tamanho como um qualificador e trata o tamanho como o tamanho máximo sugerido.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-112">When you declare an array with an explicit size, WMI stores the size as a qualifier, and treats the size as the suggested maximum size.</span></span> <span data-ttu-id="e1aa9-113">No entanto, o WMI pode expandir o tamanho, se necessário.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-113">However, WMI can expand the size if necessary.</span></span> <span data-ttu-id="e1aa9-114">A alteração do tamanho explícito não tem nenhum efeito sobre os dados reais.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-114">Changing the explicit size has no effect on the actual data.</span></span>

-   <span data-ttu-id="e1aa9-115">As matrizes são inicializadas especificando-se os valores do tipo apropriado em uma lista separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-115">Arrays are initialized by specifying values of the appropriate type in a comma-separated list.</span></span>

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   <span data-ttu-id="e1aa9-116">Uma matriz de referências é declarada como uma matriz de cadeias de caracteres de caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-116">An array of references is declared as an array of object path strings.</span></span>

    <span data-ttu-id="e1aa9-117">Ao declarar uma cadeia de caracteres de caminho de objeto, não coloque o espaço em branco entre os elementos do caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-117">When declaring an object path string, do not place white space between the elements of the object path.</span></span> <span data-ttu-id="e1aa9-118">O exemplo a seguir descreve como declarar uma referência de caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-118">The following example describes how to declare an object path reference.</span></span>

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   <span data-ttu-id="e1aa9-119">Você pode usar uma matriz como um parâmetro para um método, mas não como um valor de retorno para um parâmetro de entrada ou de entrada/saída.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-119">You can use an array as a parameter for a method, but not as a return value for an input or input-output parameter.</span></span>
-   <span data-ttu-id="e1aa9-120">Todos os elementos em uma matriz são criados como valores do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-120">All elements in an array are created as values of the same type.</span></span>

    <span data-ttu-id="e1aa9-121">Se os elementos de uma matriz forem do tipo de **objeto** , você poderá inserir qualquer tipo de objeto na matriz.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-121">If the elements of an array are of the **object** type, then you can place any kind of object in the array.</span></span> <span data-ttu-id="e1aa9-122">Por outro lado, se você declarar um tipo específico de objeto, o WMI permitirá apenas objetos dessa classe ou subclasse na matriz.</span><span class="sxs-lookup"><span data-stu-id="e1aa9-122">On the other hand, if you declare a specific type of object, then WMI allows only objects of that class or subclass in the array.</span></span> <span data-ttu-id="e1aa9-123">Os exemplos a seguir mostram declarações de matriz que incluem o uso do tipo de **objeto** .</span><span class="sxs-lookup"><span data-stu-id="e1aa9-123">The following examples show array declarations that includes using the **object** type.</span></span>

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



