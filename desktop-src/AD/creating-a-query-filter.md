---
title: Criando um filtro de consulta
description: Um filtro de consulta instrui Active Directory Domain Services localizar dados em uma sintaxe de consulta LDAP. Todas as tecnologias de acesso a dados especificadas listadas no tópico escolhendo a tecnologia de pesquisa dão suporte à sintaxe de consulta LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, criando um filtro de consulta
- filtros de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822161"
---
# <a name="creating-a-query-filter"></a><span data-ttu-id="ba18b-106">Criando um filtro de consulta</span><span class="sxs-lookup"><span data-stu-id="ba18b-106">Creating a Query Filter</span></span>

<span data-ttu-id="ba18b-107">Um filtro de consulta instrui Active Directory Domain Services localizar dados em uma sintaxe de consulta LDAP.</span><span class="sxs-lookup"><span data-stu-id="ba18b-107">A query filter instructs Active Directory Domain Services to find data in an LDAP query syntax.</span></span> <span data-ttu-id="ba18b-108">Todas as tecnologias de acesso a dados especificadas listadas no tópico [escolhendo a tecnologia de pesquisa](choosing-the-search-technology.md) dão suporte à sintaxe de consulta LDAP.</span><span class="sxs-lookup"><span data-stu-id="ba18b-108">All the specified data access technologies listed in the [Choosing the Search Technology](choosing-the-search-technology.md) topic support LDAP query syntax.</span></span>

<span data-ttu-id="ba18b-109">A sintaxe de consulta LDAP é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="ba18b-109">The LDAP query syntax is as follows:</span></span>


```C++
<expression><expression>...
```



<span data-ttu-id="ba18b-110">Um filtro pode conter uma ou mais expressões.</span><span class="sxs-lookup"><span data-stu-id="ba18b-110">A filter can contain one, or more, expressions.</span></span> <span data-ttu-id="ba18b-111">Uma expressão tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="ba18b-111">An expression has the following form:</span></span>


```C++
(<logicaloperator><comparison><comparison...>)
```



<span data-ttu-id="ba18b-112">em que " &lt; LogicalOperator &gt; " é um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="ba18b-112">where "&lt;logicaloperator&gt;" is one of the following.</span></span>



| <span data-ttu-id="ba18b-113">Operador</span><span class="sxs-lookup"><span data-stu-id="ba18b-113">Operator</span></span>        | <span data-ttu-id="ba18b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba18b-114">Description</span></span>                |
|-----------------|----------------------------|
| <span data-ttu-id="ba18b-115">"\|"</span><span class="sxs-lookup"><span data-stu-id="ba18b-115">"\|"</span></span><br/> | <span data-ttu-id="ba18b-116">**Or** lógico</span><span class="sxs-lookup"><span data-stu-id="ba18b-116">Logical **OR**</span></span><br/>  |
| <span data-ttu-id="ba18b-117">"&"</span><span class="sxs-lookup"><span data-stu-id="ba18b-117">"&"</span></span><br/>  | <span data-ttu-id="ba18b-118">**And** lógico</span><span class="sxs-lookup"><span data-stu-id="ba18b-118">Logical **AND**</span></span><br/> |
| <span data-ttu-id="ba18b-119">"!"</span><span class="sxs-lookup"><span data-stu-id="ba18b-119">"!"</span></span><br/>  | <span data-ttu-id="ba18b-120">**Não** lógico</span><span class="sxs-lookup"><span data-stu-id="ba18b-120">Logical **NOT**</span></span><br/> |



 

<span data-ttu-id="ba18b-121">e " &lt; Comparison &gt; " é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ba18b-121">and "&lt;comparison&gt;" is the following:</span></span>


```C++
(<attribute><operator><value>)
```



<span data-ttu-id="ba18b-122">onde " &lt; Attribute &gt; " é o **lDAPDisplayName** do atributo a ser avaliado, " &lt; Value &gt; " é o valor a ser comparado e " &lt; Operator &gt; " é um dos operadores de comparação a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba18b-122">where "&lt;attribute&gt;" is the **lDAPDisplayName** of the attribute to evaluate, "&lt;value&gt;" is the value to compare against, and "&lt;operator&gt;" is one of the following comparison operators.</span></span>



| <span data-ttu-id="ba18b-123">Operador</span><span class="sxs-lookup"><span data-stu-id="ba18b-123">Operator</span></span>           | <span data-ttu-id="ba18b-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba18b-124">Description</span></span>                         |
|--------------------|-------------------------------------|
| <span data-ttu-id="ba18b-125">"="</span><span class="sxs-lookup"><span data-stu-id="ba18b-125">"="</span></span><br/>     | <span data-ttu-id="ba18b-126">É igual a</span><span class="sxs-lookup"><span data-stu-id="ba18b-126">Equals</span></span><br/>                   |
| <span data-ttu-id="ba18b-127">"~="</span><span class="sxs-lookup"><span data-stu-id="ba18b-127">"~="</span></span><br/>    | <span data-ttu-id="ba18b-128">Aproximadamente é igual a</span><span class="sxs-lookup"><span data-stu-id="ba18b-128">Approximately equals</span></span><br/>     |
| <span data-ttu-id="ba18b-129">"<="</span><span class="sxs-lookup"><span data-stu-id="ba18b-129">"<="</span></span><br/> | <span data-ttu-id="ba18b-130">Menor ou igual a</span><span class="sxs-lookup"><span data-stu-id="ba18b-130">Less than or equal to</span></span><br/>    |
| <span data-ttu-id="ba18b-131">">="</span><span class="sxs-lookup"><span data-stu-id="ba18b-131">">="</span></span><br/> | <span data-ttu-id="ba18b-132">Maior ou igual a</span><span class="sxs-lookup"><span data-stu-id="ba18b-132">Greater than or equal to</span></span><br/> |



 

<span data-ttu-id="ba18b-133">Além disso, dependendo da sintaxe do atributo, o " &lt; valor &gt; " pode conter o símbolo curinga (" \* ").</span><span class="sxs-lookup"><span data-stu-id="ba18b-133">In addition, depending on the attribute syntax, the "&lt;value&gt;" may contain the wildcard symbol ("\*").</span></span> <span data-ttu-id="ba18b-134">Um " &lt; valor &gt; " que contém apenas um caractere curinga verificará a existência de qualquer valor em " &lt; Attribute &gt; ".</span><span class="sxs-lookup"><span data-stu-id="ba18b-134">A "&lt;value&gt;" that contains only a wildcard will check for the existence of any value in "&lt;attribute&gt;".</span></span> <span data-ttu-id="ba18b-135">Se nenhum valor for definido para " &lt; Attribute &gt; ", o teste falhará.</span><span class="sxs-lookup"><span data-stu-id="ba18b-135">If no value is set for "&lt;attribute&gt;", the test will fail.</span></span>

<span data-ttu-id="ba18b-136">Se qualquer um dos seguintes caracteres especiais precisar aparecer no filtro de consulta como literais, eles deverão ser substituídos pela sequência de escape listada.</span><span class="sxs-lookup"><span data-stu-id="ba18b-136">If any of the following special characters must appear in the query filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="ba18b-137">Caractere ASCII</span><span class="sxs-lookup"><span data-stu-id="ba18b-137">ASCII character</span></span>    | <span data-ttu-id="ba18b-138">Sequência de escape substituída</span><span class="sxs-lookup"><span data-stu-id="ba18b-138">Escape sequence substitute</span></span> |
|--------------------|----------------------------|
| \*<br/>      | <span data-ttu-id="ba18b-139">" \\ 2a"</span><span class="sxs-lookup"><span data-stu-id="ba18b-139">"\\2a"</span></span><br/>          |
| <span data-ttu-id="ba18b-140">(</span><span class="sxs-lookup"><span data-stu-id="ba18b-140">(</span></span><br/>       | <span data-ttu-id="ba18b-141">" \\ 28"</span><span class="sxs-lookup"><span data-stu-id="ba18b-141">"\\28"</span></span><br/>          |
| <span data-ttu-id="ba18b-142">)</span><span class="sxs-lookup"><span data-stu-id="ba18b-142">)</span></span><br/>       | <span data-ttu-id="ba18b-143">" \\ 29"</span><span class="sxs-lookup"><span data-stu-id="ba18b-143">"\\29"</span></span><br/>          |
| \\<br/>      | <span data-ttu-id="ba18b-144">" \\ 5C"</span><span class="sxs-lookup"><span data-stu-id="ba18b-144">"\\5c"</span></span><br/>          |
| <span data-ttu-id="ba18b-145">**NUL**</span><span class="sxs-lookup"><span data-stu-id="ba18b-145">**NUL**</span></span><br/> | <span data-ttu-id="ba18b-146">" \\ 00"</span><span class="sxs-lookup"><span data-stu-id="ba18b-146">"\\00"</span></span><br/>          |



 

<span data-ttu-id="ba18b-147">Além disso, dados binários arbitrários podem ser representados usando a sintaxe da sequência de escape codificando cada byte de dados binários com a barra invertida seguida de dois dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="ba18b-147">In addition, arbitrary binary data may be represented using the escape sequence syntax by encoding each byte of binary data with the backslash followed by two hexadecimal digits.</span></span> <span data-ttu-id="ba18b-148">Por exemplo, o valor de quatro bytes 0x00000004 é codificado como " \\ 00 \\ 00 \\ 00 \\ 04" em uma cadeia de caracteres de filtro.</span><span class="sxs-lookup"><span data-stu-id="ba18b-148">For example, the four-byte value 0x00000004 is encoded as "\\00\\00\\00\\04" in a filter string.</span></span>

## <a name="examples"></a><span data-ttu-id="ba18b-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ba18b-149">Examples</span></span>

<span data-ttu-id="ba18b-150">A cadeia de caracteres de consulta a seguir pesquisará todos os objetos do tipo "computador".</span><span class="sxs-lookup"><span data-stu-id="ba18b-150">The following query string will search for all objects of type "computer".</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="ba18b-151">A cadeia de caracteres de consulta a seguir pesquisará todos os objetos do tipo "computador" com um nome que começa com "desktop".</span><span class="sxs-lookup"><span data-stu-id="ba18b-151">The following query string will search for all objects of type "computer" with a name that begins with "desktop".</span></span>


```C++
(&(objectCategory=computer)(name=desktop*))
```



<span data-ttu-id="ba18b-152">A cadeia de caracteres de consulta a seguir pesquisará todos os objetos do tipo "computador" com um nome que comece com "desktop" ou um nome que comece com "Notebook".</span><span class="sxs-lookup"><span data-stu-id="ba18b-152">The following query string will search for all objects of type "computer" with a name that begins with "desktop" or a name that begins with "notebook".</span></span>


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



<span data-ttu-id="ba18b-153">A cadeia de caracteres de consulta a seguir pesquisará todos os objetos do tipo "usuário" que têm um número de telefone residencial.</span><span class="sxs-lookup"><span data-stu-id="ba18b-153">The following query string will search for all objects of type "user" that have a home phone number.</span></span>


```C++
(&(objectCategory=user)(homePhone=*))
```



<span data-ttu-id="ba18b-154">Para obter mais informações sobre cadeias de caracteres de filtro de consulta e exemplos de uso, consulte:</span><span class="sxs-lookup"><span data-stu-id="ba18b-154">For more information about query filter strings, and usage examples, see:</span></span>

-   [<span data-ttu-id="ba18b-155">Localizando objetos por classe</span><span class="sxs-lookup"><span data-stu-id="ba18b-155">Finding Objects by Class</span></span>](finding-objects-by-class.md)
-   [<span data-ttu-id="ba18b-156">Localizando objetos por nome</span><span class="sxs-lookup"><span data-stu-id="ba18b-156">Finding Objects by Name</span></span>](finding-objects-by-name.md)
-   [<span data-ttu-id="ba18b-157">Localizando uma lista de atributos a serem consultados</span><span class="sxs-lookup"><span data-stu-id="ba18b-157">Finding a List of Attributes To Query</span></span>](finding-a-list-of-attributes-to-query.md)
-   [<span data-ttu-id="ba18b-158">Verificando a sintaxe do filtro de consulta</span><span class="sxs-lookup"><span data-stu-id="ba18b-158">Checking the Query Filter Syntax</span></span>](checking-the-query-filter-syntax.md)
-   [<span data-ttu-id="ba18b-159">Como especificar valores de comparação</span><span class="sxs-lookup"><span data-stu-id="ba18b-159">How to Specify Comparison Values</span></span>](how-to-specify-comparison-values.md)

 

 





