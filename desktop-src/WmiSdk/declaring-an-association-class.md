---
description: Uma classe de associação é um tipo especial de classe que define uma relação entre duas outras classes.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Declarando uma classe de associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011508"
---
# <a name="declaring-an-association-class"></a><span data-ttu-id="f39be-103">Declarando uma classe de associação</span><span class="sxs-lookup"><span data-stu-id="f39be-103">Declaring an Association Class</span></span>

<span data-ttu-id="f39be-104">Uma classe de associação é um tipo especial de classe que define uma relação entre duas outras classes.</span><span class="sxs-lookup"><span data-stu-id="f39be-104">An association class is a special type of class that defines a relationship between two other classes.</span></span>

<span data-ttu-id="f39be-105">O procedimento a seguir descreve como criar uma classe de associação usando o código MOF.</span><span class="sxs-lookup"><span data-stu-id="f39be-105">The following procedure describes how to create an association class using MOF code.</span></span>

<span data-ttu-id="f39be-106">**Para criar uma classe de associação usando código MOF**</span><span class="sxs-lookup"><span data-stu-id="f39be-106">**To create an association class using MOF code**</span></span>

1.  <span data-ttu-id="f39be-107">Atribua o qualificador de **Associação** à sua classe.</span><span class="sxs-lookup"><span data-stu-id="f39be-107">Assign the **Association** qualifier to your class.</span></span>

    <span data-ttu-id="f39be-108">Embora seja possível criar uma classe com referências a objetos ou classes, usar o qualificador de **Associação** não apenas torna claro que sua classe é uma classe de associação, mas, como prática recomendada, garante que sua classe funcione totalmente como uma classe de associação.</span><span class="sxs-lookup"><span data-stu-id="f39be-108">Although it is possible to create a class with references to objects or classes, using the **Association** qualifier not only makes it clear that your class is an association class, but, as a best practice, ensures that your class fully functions as an association class.</span></span>

2.  <span data-ttu-id="f39be-109">Crie duas referências dentro da classe que descreve as duas instâncias de objeto que você deseja associar em conjunto usando o tipo **ref** .</span><span class="sxs-lookup"><span data-stu-id="f39be-109">Create two references within the class describing the two object instances you wish to associate together using the **ref** type.</span></span>

    <span data-ttu-id="f39be-110">As referências associam os dois objetos na associação, contendo caminhos aos objetos.</span><span class="sxs-lookup"><span data-stu-id="f39be-110">The references bind the two objects in the association by containing paths to the objects.</span></span> <span data-ttu-id="f39be-111">Embora não seja necessário, use as propriedades de referência como propriedades de chave também.</span><span class="sxs-lookup"><span data-stu-id="f39be-111">Although not required, use the reference properties as key properties as well.</span></span>

    <span data-ttu-id="f39be-112">Embora você possa criar referências totalmente qualificadas ou relativas a namespace, o WMI tem apenas suporte limitado para referências de namespace cruzado.</span><span class="sxs-lookup"><span data-stu-id="f39be-112">Although you can create fully qualified or namespace-relative references, WMI has only limited support for cross-namespace references.</span></span> <span data-ttu-id="f39be-113">Especificamente, somente objetos definidos estaticamente podem referenciar uns aos outros nos limites do namespace; os objetos com suporte dinâmico não podem fazer referência uns aos outros.</span><span class="sxs-lookup"><span data-stu-id="f39be-113">Specifically, only statically defined objects can reference each other across namespace boundaries; dynamically supported objects cannot reference each other.</span></span>

    <span data-ttu-id="f39be-114">Se necessário, use os qualificadores **HasClassRef** e **Classref** em conjunto com o tipo de referência de **objeto** para fazer referência a uma classe.</span><span class="sxs-lookup"><span data-stu-id="f39be-114">If necessary, use the **HasClassRef** and **Classref** qualifiers in conjunction with the **object ref** type to reference a class.</span></span>

    <span data-ttu-id="f39be-115">O WMI dá suporte a um ponto de referência **ref** a uma instância, e a outra referência de **objeto** aponta para uma classe.</span><span class="sxs-lookup"><span data-stu-id="f39be-115">WMI supports having one **ref** reference point to an instance, and the other **object** reference point to a class.</span></span> <span data-ttu-id="f39be-116">Nesse caso, sua classe de associação descreveria uma associação que associa instâncias a classes.</span><span class="sxs-lookup"><span data-stu-id="f39be-116">In this case, your association class would describe an association that binds instances to classes.</span></span>

    <span data-ttu-id="f39be-117">O exemplo de código a seguir descreve a sintaxe para usar **HasClassRef** e **Classref** com um tipo de **objeto** .</span><span class="sxs-lookup"><span data-stu-id="f39be-117">The following code example describes the syntax for using **HasClassRef** and **Classref** with an **object** type.</span></span>

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    <span data-ttu-id="f39be-118">No exemplo anterior, a referência **ep1** pode apontar para as definições de classe da classe **myEndpoint** ou da classe **OtherContainer** .</span><span class="sxs-lookup"><span data-stu-id="f39be-118">In the previous example, the **ep1** reference can point to the class definitions for either the **MyEndpoint** class or the **OtherContainer** class.</span></span> <span data-ttu-id="f39be-119">Observe que, embora você deva digitar de tipo fraco a classe de referência, não é possível digitar fracamente o qualificador **Classref** ; Isso reduziria severamente a eficiência do mecanismo de consulta do WMI.</span><span class="sxs-lookup"><span data-stu-id="f39be-119">Note that while you must weakly type the reference class, you cannot weakly type the **Classref** qualifier itself; doing so would severely reduce the efficiency of the WMI query engine.</span></span> <span data-ttu-id="f39be-120">A digitação fraca é criar uma referência que possa conter qualquer tipo de dados usando a palavra-chave **Object** e o tipo de dados **ref** .</span><span class="sxs-lookup"><span data-stu-id="f39be-120">Weak typing is creating a reference that can contain any data type by using the **object** keyword and **ref** data type.</span></span> <span data-ttu-id="f39be-121">Para usar o **HasClassRef** com êxito, você deve definir os tipos de qualificador relevantes para propagar para todas as instâncias e subclasses.</span><span class="sxs-lookup"><span data-stu-id="f39be-121">To successfully use **HasClassRef**, you must set the relevant qualifier flavors to propagate to all instances and subclasses.</span></span>

3.  <span data-ttu-id="f39be-122">Crie outras propriedades conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f39be-122">Create any other properties as necessary.</span></span>

    <span data-ttu-id="f39be-123">O exemplo de código a seguir mostra que o WMI atualmente não dá suporte a classes de associação com menos ou mais de duas propriedades de referência.</span><span class="sxs-lookup"><span data-stu-id="f39be-123">The following code example shows that WMI does not currently support association classes having less or more than two reference properties.</span></span>

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  <span data-ttu-id="f39be-124">Quando terminar, compile seu código MOF com o compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="f39be-124">When finished, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="f39be-125">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="f39be-125">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="f39be-126">O exemplo de código na etapa 3 define a classe de associação **MyAssocClass** .</span><span class="sxs-lookup"><span data-stu-id="f39be-126">The code example in Step 3 defines the **MyAssocClass** association class.</span></span> <span data-ttu-id="f39be-127">A classe **MyAssocClass** define uma relação entre **ClassX** e **classe**.</span><span class="sxs-lookup"><span data-stu-id="f39be-127">The **MyAssocClass** class defines a relationship between **ClassX** and **ClassY**.</span></span> <span data-ttu-id="f39be-128">As propriedades **PathToClassX** e **PathToClassY** contêm caminhos de objeto para as instâncias das classes a serem associadas.</span><span class="sxs-lookup"><span data-stu-id="f39be-128">The **PathToClassX** and **PathToClassY** properties contain object paths to the instances of the classes to be associated.</span></span> <span data-ttu-id="f39be-129">A palavra-chave **ToInstance** é um dos vários sinalizadores de tipo que o WMI define para fornecer informações sobre o uso de um qualificador.</span><span class="sxs-lookup"><span data-stu-id="f39be-129">The keyword **ToInstance** is one of several flavor flags that WMI defines to provide information about the use of a qualifier.</span></span> <span data-ttu-id="f39be-130">A palavra-chave **ToInstance** indica que o WMI deve propagar o qualificador de **Associação** para todas as instâncias da classe de associação.</span><span class="sxs-lookup"><span data-stu-id="f39be-130">The **ToInstance** keyword indicates that WMI should propagate the **Association** qualifier to all instances of the association class.</span></span> <span data-ttu-id="f39be-131">Ao marcar esse qualificador de instância, o software cliente pode determinar que uma instância pertence a uma classe de associação, sem precisar recuperar a definição de classe para procurar o qualificador de **Associação** .</span><span class="sxs-lookup"><span data-stu-id="f39be-131">By checking this instance qualifier, the client software can determine that an instance belongs to an association class, without having to retrieve the class definition to look for the **Association** qualifier.</span></span> <span data-ttu-id="f39be-132">Para obter mais informações, consulte [descrevendo um qualificador com um tipo de qualificador](describing-a-qualifier-with-a-qualifier-flavor.md) e [referências](references.md).</span><span class="sxs-lookup"><span data-stu-id="f39be-132">For more information, see [Describing a Qualifier With a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md) and [References](references.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f39be-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f39be-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f39be-134">Criando classes formato MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="f39be-134">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



