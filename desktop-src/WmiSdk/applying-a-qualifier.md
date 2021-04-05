---
description: Como muitas outras técnicas no formato MOF (MOF), a aplicação de um qualificador ao seu código é um processo relativamente simples.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Aplicando um qualificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663581"
---
# <a name="applying-a-qualifier"></a><span data-ttu-id="1c73c-103">Aplicando um qualificador</span><span class="sxs-lookup"><span data-stu-id="1c73c-103">Applying a Qualifier</span></span>

<span data-ttu-id="1c73c-104">Como muitas outras técnicas no formato MOF (MOF), a aplicação de um qualificador ao seu código é um processo relativamente simples.</span><span class="sxs-lookup"><span data-stu-id="1c73c-104">Like many other techniques in Managed Object Format (MOF), applying a qualifier to your code is a relatively simple process.</span></span>

<span data-ttu-id="1c73c-105">Os únicos desafios reais são as seguintes restrições nas convenções de nomenclatura que o WMI impõe:</span><span class="sxs-lookup"><span data-stu-id="1c73c-105">The only real challenges are the following restrictions in naming conventions that WMI enforces:</span></span>

-   <span data-ttu-id="1c73c-106">Um qualificador pode descrever uma classe, instância, propriedade, método ou parâmetro de método.</span><span class="sxs-lookup"><span data-stu-id="1c73c-106">A qualifier can describe a class, instance, property, method, or method parameter.</span></span>
-   <span data-ttu-id="1c73c-107">Os nomes de qualificador não podem ter sublinhados à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="1c73c-107">Qualifier names cannot have either leading or trailing underscores.</span></span>
-   <span data-ttu-id="1c73c-108">Um nome de qualificador não pode começar com um dígito.</span><span class="sxs-lookup"><span data-stu-id="1c73c-108">A qualifier name cannot begin with a digit.</span></span>
-   <span data-ttu-id="1c73c-109">Um nome de qualificador não pode conter caracteres especiais, como & \* @!</span><span class="sxs-lookup"><span data-stu-id="1c73c-109">A qualifier name cannot contain special characters such as & \* @ !</span></span><span data-ttu-id="1c73c-110"> ~ \\ /.</span><span class="sxs-lookup"><span data-stu-id="1c73c-110"> ~ \\ /.</span></span>
-   <span data-ttu-id="1c73c-111">Todos os nomes de qualificador não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1c73c-111">All qualifier names are case-insensitive.</span></span>
-   <span data-ttu-id="1c73c-112">Você não pode redefinir os qualificadores WMI padrão ou quaisquer qualificadores descritos na especificação CIM DMTF.</span><span class="sxs-lookup"><span data-stu-id="1c73c-112">You cannot redefine the standard WMI qualifiers or any qualifiers described in the DMTF CIM specification.</span></span>
-   <span data-ttu-id="1c73c-113">Os tipos de qualificador não são declarados explicitamente.</span><span class="sxs-lookup"><span data-stu-id="1c73c-113">Qualifier types are not explicitly declared.</span></span>

    <span data-ttu-id="1c73c-114">Se você não declarar um tipo de qualificador, o WMI assumirá o tipo como booliano com um valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="1c73c-114">If you do not declare a qualifier type, WMI assumes the type as Boolean with a value of **TRUE**.</span></span> <span data-ttu-id="1c73c-115">Caso contrário, o WMI digitará os qualificadores com base nos valores do qualificador que você declarar.</span><span class="sxs-lookup"><span data-stu-id="1c73c-115">Otherwise, WMI types qualifiers based on the qualifier values you declare.</span></span>

-   <span data-ttu-id="1c73c-116">Ao criar seus próprios qualificadores, você deve prefixar o nome do esquema para o nome do qualificador.</span><span class="sxs-lookup"><span data-stu-id="1c73c-116">When creating your own qualifiers, you should prefix your schema name to your qualifier name.</span></span>

    <span data-ttu-id="1c73c-117">A finalidade dessa regra é evitar confusão com novos qualificadores.</span><span class="sxs-lookup"><span data-stu-id="1c73c-117">The purpose of this rule is to avoid confusion with new qualifiers.</span></span>

-   <span data-ttu-id="1c73c-118">Você pode criar matrizes homogêneos de qualificadores.</span><span class="sxs-lookup"><span data-stu-id="1c73c-118">You can create homogeneous arrays of qualifiers.</span></span>

    <span data-ttu-id="1c73c-119">O exemplo de código a seguir mostra como as matrizes de qualificador são especificadas com chaves que envolvem os valores.</span><span class="sxs-lookup"><span data-stu-id="1c73c-119">The following code example shows how qualifier arrays are specified with curly braces that surround the values.</span></span>

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   <span data-ttu-id="1c73c-120">O WMI não oferece suporte a tipos de automação não listados na referência, como VT \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="1c73c-120">WMI does not support automation types not listed in the reference, such as VT\_NULL.</span></span> <span data-ttu-id="1c73c-121">Para obter mais informações, consulte [MOF Data Types](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="1c73c-121">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

<span data-ttu-id="1c73c-122">O procedimento a seguir ajuda você a usar o C++ para adicionar um qualificador a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="1c73c-122">The following procedure helps you to use C++ to add a qualifier to a property.</span></span>

<span data-ttu-id="1c73c-123">**Para aplicar um qualificador usando C++**</span><span class="sxs-lookup"><span data-stu-id="1c73c-123">**To apply a qualifier using C++**</span></span>

-   <span data-ttu-id="1c73c-124">Aplique o qualificador com uma chamada para o método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="1c73c-124">Apply the qualifier with a call to the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="1c73c-125">Você pode usar outros métodos de [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) para recuperar ou excluir qualificadores existentes.</span><span class="sxs-lookup"><span data-stu-id="1c73c-125">You can use other methods of [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) to retrieve or delete existing qualifiers.</span></span>

<span data-ttu-id="1c73c-126">O procedimento a seguir ajuda a aplicar um qualificador em arquivos MOF.</span><span class="sxs-lookup"><span data-stu-id="1c73c-126">The following procedure helps you to apply a qualifier in MOF files.</span></span>

<span data-ttu-id="1c73c-127">**Para descrever uma palavra-chave ou um identificador com um qualificador usando o MOF**</span><span class="sxs-lookup"><span data-stu-id="1c73c-127">**To describe a keyword or identifier with a qualifier using MOF**</span></span>

-   <span data-ttu-id="1c73c-128">Coloque um qualificador entre colchetes antes da palavra-chave ou do identificador descrito pelo qualificador.</span><span class="sxs-lookup"><span data-stu-id="1c73c-128">Place a qualifier in brackets before the keyword or identifier described by the qualifier.</span></span>

    <span data-ttu-id="1c73c-129">O exemplo de código a seguir mostra como os qualificadores são usados.</span><span class="sxs-lookup"><span data-stu-id="1c73c-129">The following code example shows how qualifiers are used.</span></span>

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    <span data-ttu-id="1c73c-130">O exemplo a seguir descreve o posicionamento apropriado dos qualificadores.</span><span class="sxs-lookup"><span data-stu-id="1c73c-130">The following example describes the proper placement of qualifiers.</span></span>

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



