---
title: Diferenças entre MIDL e MkTypLib
description: Diferenças entre MIDL e MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL e ODL, diferenças entre MIDL e MkTypLib
- MIDL MkTypLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006159"
---
# <a name="differences-between-midl-and-mktyplib"></a><span data-ttu-id="0033a-105">Diferenças entre MIDL e MkTypLib</span><span class="sxs-lookup"><span data-stu-id="0033a-105">Differences Between MIDL and MkTypLib</span></span>

> [!Note]  
> <span data-ttu-id="0033a-106">A ferramenta de Mktyplib.exe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="0033a-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="0033a-107">Em vez disso, use o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="0033a-107">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="0033a-108">Há algumas áreas-chave em que o compilador MIDL difere de MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="0033a-108">There are a few key areas in which the MIDL compiler differs from MkTypLib.</span></span> <span data-ttu-id="0033a-109">A maioria dessas diferenças surge porque MIDL é orientado mais em direção C-Syntax do que MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="0033a-109">Most of these differences arise because MIDL is oriented more toward C-syntax than MkTypLib.</span></span>

<span data-ttu-id="0033a-110">Em geral, você desejará usar a sintaxe MIDL em seus arquivos IDL.</span><span class="sxs-lookup"><span data-stu-id="0033a-110">In general, you will want to use the MIDL syntax in your IDL files.</span></span> <span data-ttu-id="0033a-111">No entanto, se você precisar compilar um arquivo ODL existente ou manter a compatibilidade com o MkTypLib, use a opção de compilador de MIDL [**/mktyplib203**](-mktyplib203.md) para forçar o MIDL a se comportar como Mkktyplib.exe, versão 2, 3.</span><span class="sxs-lookup"><span data-stu-id="0033a-111">However, if you need to compile an existing ODL file, or otherwise maintain compatibility with MkTypLib, use the [**/mktyplib203**](-mktyplib203.md) MIDL compiler option to force MIDL to behave like Mkktyplib.exe, version 2.03.</span></span> <span data-ttu-id="0033a-112">(Esta é a última versão da ferramenta MkTypLib.) Especificamente, a opção **/mktyplib203** resolve essas diferenças:</span><span class="sxs-lookup"><span data-stu-id="0033a-112">(This is the last release of the MkTypLib tool.) Specifically, the **/mktyplib203** option resolves these differences:</span></span>

-   <span data-ttu-id="0033a-113">sintaxe de typedef para tipos de dados complexos</span><span class="sxs-lookup"><span data-stu-id="0033a-113">typedef syntax for complex data types</span></span>

    <span data-ttu-id="0033a-114">No MkTypLib, ambas as definições a seguir geram um \_ registro TKIND para "este \_ struct" na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="0033a-114">In MkTypLib, both of the following definitions generate a TKIND\_RECORD for "this\_struct" in the type library.</span></span> <span data-ttu-id="0033a-115">A marca " \_ tag struct" é opcional e, se usada, não aparecerá na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="0033a-115">The tag "struct\_tag" is optional and, if used, will not show up in the type library.</span></span>

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    <span data-ttu-id="0033a-116">Se uma marca opcional estiver ausente, MIDL irá gerá-la, adicionando efetivamente uma marca à definição fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0033a-116">If an optional tag is missing, MIDL will generate it, effectively adding a tag to the definition supplied by the user.</span></span> <span data-ttu-id="0033a-117">Como a primeira definição tem uma marca, MIDL gerará um \_ registro TKIND para "This \_ struct" e um \_ alias TKIND para "This \_ struct" (definindo "This \_ struct" como um alias para " \_ tag struct").</span><span class="sxs-lookup"><span data-stu-id="0033a-117">Since the first definition has a tag, MIDL will generate a TKIND\_RECORD for "this\_struct" and a TKIND\_ALIAS for "this\_struct" (defining "this\_struct" as an alias for "struct\_tag").</span></span> <span data-ttu-id="0033a-118">Como a marca está ausente na segunda definição, MIDL gerará um registro TKIND \_ para um nome desconfigurado, interno ao MIDL, que não é significativo para o usuário e um alias TKIND \_ para "essa \_ struct".</span><span class="sxs-lookup"><span data-stu-id="0033a-118">Because the tag is missing in the second definition, MIDL will generate a TKIND\_RECORD for a mangled name, internal to MIDL, that is not meaningful to the user and a TKIND\_ALIAS for "that\_struct".</span></span>

    <span data-ttu-id="0033a-119">Isso tem possíveis implicações para os navegadores de biblioteca de tipos que simplesmente mostram o nome de um registro em sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0033a-119">This has potential implications for type library browsers that simply show the name of a record in their user interface.</span></span> <span data-ttu-id="0033a-120">Se você espera que um \_ registro TKIND tenha um nome real, nomes não reconhecíveis podem aparecer na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0033a-120">If you expect a TKIND\_RECORD to have a real name, unrecognizable names could appear in the user interface.</span></span> <span data-ttu-id="0033a-121">Esse comportamento também se aplica às definições de [**União**](union.md) e [**Enumeração**](enum.md) , com o compilador MIDL gerando \_ uniões TKIND e \_ enumerações TKIND, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0033a-121">This behavior also applies to [**union**](union.md) and [**enum**](enum.md) definitions, with the MIDL compiler generating TKIND\_UNIONs and TKIND\_ENUMs, respectively.</span></span>

    <span data-ttu-id="0033a-122">MIDL também permite definições de [**struct**](struct.md), [**Union**](union.md)e [**enum**](enum.md) em estilo C.</span><span class="sxs-lookup"><span data-stu-id="0033a-122">MIDL also allows C-style [**struct**](struct.md), [**union**](union.md), and [**enum**](enum.md) definitions.</span></span> <span data-ttu-id="0033a-123">Por exemplo, a seguinte definição é válida no MIDL:</span><span class="sxs-lookup"><span data-stu-id="0033a-123">For example, the following definition is legal in MIDL:</span></span>

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   <span data-ttu-id="0033a-124">Tipos de dados boolianos</span><span class="sxs-lookup"><span data-stu-id="0033a-124">Boolean data types</span></span>

    <span data-ttu-id="0033a-125">Em MkTypLib, o tipo de base [**booliano**](boolean.md) e o tipo de dados MkTypLib bool são equivalentes a VT \_ bool, que é mapeado para \_ booliano de Variant e que é definido como um [**curto**](short.md).</span><span class="sxs-lookup"><span data-stu-id="0033a-125">In MkTypLib, the [**Boolean**](boolean.md) base type and the MkTypLib data type BOOL equate to VT\_BOOL, which maps to VARIANT\_BOOL, and which is defined as a [**short**](short.md).</span></span> <span data-ttu-id="0033a-126">No MIDL, o tipo base **booliano** é equivalente a VT \_ UI1, que é definido como um [**Char não assinado**](unsigned.md), e o tipo de dados bool é definido como um [**longo**](long.md).</span><span class="sxs-lookup"><span data-stu-id="0033a-126">In MIDL, the **Boolean** base type is equivalent to VT\_UI1, which is defined as an [**unsigned char**](unsigned.md), and the BOOL data type is defined as a [**long**](long.md).</span></span> <span data-ttu-id="0033a-127">Isso leva a dificuldades se você misturar a sintaxe IDL e a sintaxe ODL no mesmo arquivo enquanto ainda estiver tentando manter a compatibilidade com o MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="0033a-127">This leads to difficulties if you mix IDL syntax and ODL syntax in the same file while still trying to maintain compatibility with MkTypLib.</span></span> <span data-ttu-id="0033a-128">Como os tipos de dados são tamanhos diferentes, o código de marshaling não corresponderá ao que está descrito nas informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="0033a-128">Because the data types are different sizes, the marshaling code will not match what is described in the type information.</span></span> <span data-ttu-id="0033a-129">Se você quiser um VT \_ bool em sua biblioteca de tipos, deverá usar o \_ tipo de dados BOOL de variante.</span><span class="sxs-lookup"><span data-stu-id="0033a-129">If you want a VT\_BOOL in your type library, you should use the VARIANT\_BOOL data type.</span></span>

-   <span data-ttu-id="0033a-130">Definições de GUID em arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0033a-130">GUID definitions in header files</span></span>

    <span data-ttu-id="0033a-131">No MkTypLib, os GUIDs são definidos no arquivo de cabeçalho com uma macro que pode ser compilada condicionalmente para gerar uma predefinição de GUID ou um GUID instanciado.</span><span class="sxs-lookup"><span data-stu-id="0033a-131">In MkTypLib, GUIDs are defined in the header file with a macro that can be conditionally compiled to generate either a GUID predefinition or an instantiated GUID.</span></span> <span data-ttu-id="0033a-132">O MIDL normalmente coloca as predefinições de GUID em seus arquivos de cabeçalho gerados e instanciações GUID somente no arquivo gerado pelo comutador [**/IID nomedearquivo**](-iid.md) .</span><span class="sxs-lookup"><span data-stu-id="0033a-132">MIDL normally puts GUID predefinitions in its generated header files and GUID instantiations only in the file generated by the [**/iid**](-iid.md) switch.</span></span>

<span data-ttu-id="0033a-133">As seguintes diferenças no comportamento não podem ser resolvidas usando a opção [**/mktyplib203**](-mktyplib203.md) :</span><span class="sxs-lookup"><span data-stu-id="0033a-133">The following differences in behavior cannot be resolved by using the [**/mktyplib203**](-mktyplib203.md) switch:</span></span>

-   <span data-ttu-id="0033a-134">Diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="0033a-134">Case sensitivity</span></span>

    <span data-ttu-id="0033a-135">MIDL diferencia maiúsculas de minúsculas, automação OLE não é.</span><span class="sxs-lookup"><span data-stu-id="0033a-135">MIDL is case sensitive, OLE Automation is not.</span></span>

-   <span data-ttu-id="0033a-136">Escopo de símbolos em uma declaração de enumeração</span><span class="sxs-lookup"><span data-stu-id="0033a-136">Scope of symbols in an enum declaration</span></span>

    <span data-ttu-id="0033a-137">No MkTypLib, o escopo de símbolos em um enum é local.</span><span class="sxs-lookup"><span data-stu-id="0033a-137">In MkTypLib the scope of symbols in an enum is local.</span></span> <span data-ttu-id="0033a-138">No MIDL, o escopo dos símbolos em uma enumeração é global, pois ele está em C. Por exemplo, o código a seguir será compilado em MkTypLib, mas irá gerar um erro de nome duplicado no MIDL:</span><span class="sxs-lookup"><span data-stu-id="0033a-138">In MIDL, the scope of symbols in an enum is global, as it is in C. For example, the following code will compile in MkTypLib, but will generate a duplicate name error in MIDL:</span></span>

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   <span data-ttu-id="0033a-139">Escopo do atributo público</span><span class="sxs-lookup"><span data-stu-id="0033a-139">Scope of public attribute</span></span>

    <span data-ttu-id="0033a-140">Se você aplicar o atributo [**Public**](public.md) a um bloco de interface, MkTypLib tratará cada typedef dentro desse bloco de interface como público.</span><span class="sxs-lookup"><span data-stu-id="0033a-140">If you apply the [**public**](public.md) attribute to an interface block, MkTypLib treats every typedef inside that interface block as public.</span></span> <span data-ttu-id="0033a-141">MIDL requer que você aplique explicitamente o atributo **Public** a esses TYPEDEFs que você deseja público.</span><span class="sxs-lookup"><span data-stu-id="0033a-141">MIDL requires that you explicitly apply the **public** attribute to those typedefs that you want public.</span></span>

-   <span data-ttu-id="0033a-142">Ordem de pesquisa do importlib</span><span class="sxs-lookup"><span data-stu-id="0033a-142">Importlib search order</span></span>

    <span data-ttu-id="0033a-143">Se você importar mais de uma biblioteca de tipos e se essas bibliotecas contiverem referências duplicadas, o MkTypLib resolverá isso usando a primeira referência que encontrar.</span><span class="sxs-lookup"><span data-stu-id="0033a-143">If you import more than one type library, and if these libraries contain duplicate references, MkTypLib resolves this by using the first reference that it finds.</span></span> <span data-ttu-id="0033a-144">MIDL usará a última referência que encontrar.</span><span class="sxs-lookup"><span data-stu-id="0033a-144">MIDL will use the last reference that it finds.</span></span> <span data-ttu-id="0033a-145">Por exemplo, considerando a seguinte sintaxe ODL, a biblioteca C usará o typedef MOO da biblioteca A se você compilar com MkTypLib e o typedef MOO da biblioteca B se você compilar with MIDL:</span><span class="sxs-lookup"><span data-stu-id="0033a-145">For example, given the following ODL syntax, library C will use the MOO typedef from library A if you compile with MkTypLib, and the MOO typedef from library B if you compile with MIDL:</span></span>

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    <span data-ttu-id="0033a-146">A solução alternativa apropriada para isso é qualificar cada referência desse tipo com o nome da biblioteca de importação correto, desta forma:</span><span class="sxs-lookup"><span data-stu-id="0033a-146">The appropriate workaround for this is to qualify each such reference with the correct import library name, like this:</span></span>

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   <span data-ttu-id="0033a-147">Tipo de dados VOID não reconhecido</span><span class="sxs-lookup"><span data-stu-id="0033a-147">VOID data type not recognized</span></span>

    <span data-ttu-id="0033a-148">MIDL reconhece o tipo de dados [**void**](void.md) em linguagem C e não reconhece o tipo de dados void de automação OLE.</span><span class="sxs-lookup"><span data-stu-id="0033a-148">MIDL recognizes the C-language [**void**](void.md) data type and does not recognize the OLE Automation VOID data type.</span></span> <span data-ttu-id="0033a-149">Se você tiver um arquivo ODL que usa VOID, coloque essa definição na parte superior do arquivo:</span><span class="sxs-lookup"><span data-stu-id="0033a-149">If you have an ODL file that uses VOID, place this definition at the top of the file:</span></span>

    ``` syntax
#define VOID void
    ```

-   <span data-ttu-id="0033a-150">Notação exponencial</span><span class="sxs-lookup"><span data-stu-id="0033a-150">Exponential notation</span></span>

    <span data-ttu-id="0033a-151">MIDL requer que os valores expressos na notação exponencial sejam contidos entre aspas.</span><span class="sxs-lookup"><span data-stu-id="0033a-151">MIDL requires that values expressed in exponential notation be contained within quotation marks.</span></span> <span data-ttu-id="0033a-152">Por exemplo, "-2,5 E + 3"</span><span class="sxs-lookup"><span data-stu-id="0033a-152">For example, "-2.5E+3"</span></span>

-   <span data-ttu-id="0033a-153">Valores e constantes LCID</span><span class="sxs-lookup"><span data-stu-id="0033a-153">LCID values and constants</span></span>

    <span data-ttu-id="0033a-154">Normalmente, o MIDL não considera o LCID ao analisar arquivos.</span><span class="sxs-lookup"><span data-stu-id="0033a-154">Normally MIDL does not consider the LCID when parsing files.</span></span> <span data-ttu-id="0033a-155">Para forçar esse comportamento para um valor, ou se você precisar usar notação específica de localidade ao definir uma constante, coloque o valor ou a constante entre aspas.</span><span class="sxs-lookup"><span data-stu-id="0033a-155">To force this behavior for a value, or if you need to use locale-specific notation when defining a constant, enclose the value or constant in quotation marks.</span></span>

<span data-ttu-id="0033a-156">Para obter mais informações, consulte [**/mktyplib203**](-mktyplib203.md), [**/IID nomedearquivo**](-iid.md)e [empacotamento de tipos de dados OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="0033a-156">For more information, see [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md), and [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




