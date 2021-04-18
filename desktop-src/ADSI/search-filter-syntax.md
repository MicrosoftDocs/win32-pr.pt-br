---
title: Sintaxe do filtro de pesquisa
description: Os filtros de pesquisa permitem que você defina critérios de pesquisa e forneça pesquisas mais eficientes e eficazes.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- ADSI de sintaxe de filtro de pesquisa
- consultas, sintaxe de filtro de pesquisa
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105762841"
---
# <a name="search-filter-syntax"></a><span data-ttu-id="c3a33-105">Sintaxe do filtro de pesquisa</span><span class="sxs-lookup"><span data-stu-id="c3a33-105">Search Filter Syntax</span></span>

<span data-ttu-id="c3a33-106">Os filtros de pesquisa permitem que você defina critérios de pesquisa e forneça pesquisas mais eficientes e eficazes.</span><span class="sxs-lookup"><span data-stu-id="c3a33-106">Search filters enable you to define search criteria and provide more efficient and effective searches.</span></span>

<span data-ttu-id="c3a33-107">A ADSI dá suporte aos filtros de pesquisa LDAP, conforme definido em RFC2254.</span><span class="sxs-lookup"><span data-stu-id="c3a33-107">ADSI supports the LDAP search filters as defined in RFC2254.</span></span> <span data-ttu-id="c3a33-108">Esses filtros de pesquisa são representados por cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3a33-108">These search filters are represented by Unicode strings.</span></span> <span data-ttu-id="c3a33-109">A tabela a seguir lista alguns exemplos de filtros de pesquisa LDAP.</span><span class="sxs-lookup"><span data-stu-id="c3a33-109">The following table lists some examples of LDAP search filters.</span></span>



| <span data-ttu-id="c3a33-110">Filtro de pesquisa</span><span class="sxs-lookup"><span data-stu-id="c3a33-110">Search filter</span></span>                                                               | <span data-ttu-id="c3a33-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3a33-111">Description</span></span>                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c3a33-112">"(objectClass = \* )"</span><span class="sxs-lookup"><span data-stu-id="c3a33-112">"(objectClass=\*)"</span></span>                                                          | <span data-ttu-id="c3a33-113">Todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="c3a33-113">All objects.</span></span>                                               |
| <span data-ttu-id="c3a33-114">"(& (objectCategory = Person) (objectClass = user) (! ( CN = Andy))) "</span><span class="sxs-lookup"><span data-stu-id="c3a33-114">"(&(objectCategory=person)(objectClass=user)(!(cn=andy)))"</span></span>                  | <span data-ttu-id="c3a33-115">Todos os objetos de usuário, mas "Andy".</span><span class="sxs-lookup"><span data-stu-id="c3a33-115">All user objects but "andy".</span></span>                               |
| <span data-ttu-id="c3a33-116">"(SN = SM \* )"</span><span class="sxs-lookup"><span data-stu-id="c3a33-116">"(sn=sm\*)"</span></span>                                                                 | <span data-ttu-id="c3a33-117">Todos os objetos com um sobrenome que começa com "SM".</span><span class="sxs-lookup"><span data-stu-id="c3a33-117">All objects with a surname that starts with "sm".</span></span>          |
| <span data-ttu-id="c3a33-118">"(& (objectCategory = Person) (objectClass = Contact) ( \| (SN = Smith) (SN = Johnson))"</span><span class="sxs-lookup"><span data-stu-id="c3a33-118">"(&(objectCategory=person)(objectClass=contact)(\|(sn=Smith)(sn=Johnson)))"</span></span> | <span data-ttu-id="c3a33-119">Todos os contatos com um sobrenome igual a "Smith" ou "Johnson".</span><span class="sxs-lookup"><span data-stu-id="c3a33-119">All contacts with a surname equal to "Smith" or "Johnson".</span></span> |



 

<span data-ttu-id="c3a33-120">Esses filtros de pesquisa usam um dos formatos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3a33-120">These search filters use one of the following formats.</span></span>


```C++
<filter>=(<attribute><operator><value>)
```



<span data-ttu-id="c3a33-121">ou</span><span class="sxs-lookup"><span data-stu-id="c3a33-121">or</span></span>


```C++
(<operator><filter1><filter2>)
```



<span data-ttu-id="c3a33-122">Os filtros de pesquisa do ADSI são usados de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="c3a33-122">The ADSI search filters are used in two ways.</span></span> <span data-ttu-id="c3a33-123">Eles formam uma parte do dialeto LDAP para enviar consultas por meio do provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c3a33-123">They form a part of the LDAP dialect for submitting queries through the OLE DB provider.</span></span> <span data-ttu-id="c3a33-124">Eles também são usados com a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="c3a33-124">They are also used with the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

## <a name="operators"></a><span data-ttu-id="c3a33-125">Operadores</span><span class="sxs-lookup"><span data-stu-id="c3a33-125">Operators</span></span>

<span data-ttu-id="c3a33-126">A tabela a seguir lista os operadores de filtro de pesquisa usados com frequência.</span><span class="sxs-lookup"><span data-stu-id="c3a33-126">The following table lists frequently used search filter operators.</span></span>



| <span data-ttu-id="c3a33-127">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="c3a33-127">Logical operator</span></span> | <span data-ttu-id="c3a33-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3a33-128">Description</span></span>                                |
|------------------|--------------------------------------------|
| =                | <span data-ttu-id="c3a33-129">Igual a</span><span class="sxs-lookup"><span data-stu-id="c3a33-129">Equal to</span></span>                                   |
| ~=               | <span data-ttu-id="c3a33-130">Aproximadamente igual a</span><span class="sxs-lookup"><span data-stu-id="c3a33-130">Approximately equal to</span></span>                     |
| <=            | <span data-ttu-id="c3a33-131">Modo lexicográfico menor ou igual a</span><span class="sxs-lookup"><span data-stu-id="c3a33-131">Lexicographically less than or equal to</span></span>    |
| >=            | <span data-ttu-id="c3a33-132">Modo lexicográfico maior ou igual a</span><span class="sxs-lookup"><span data-stu-id="c3a33-132">Lexicographically greater than or equal to</span></span> |
| &                | <span data-ttu-id="c3a33-133">AND</span><span class="sxs-lookup"><span data-stu-id="c3a33-133">AND</span></span>                                        |
| \|               | <span data-ttu-id="c3a33-134">OU</span><span class="sxs-lookup"><span data-stu-id="c3a33-134">OR</span></span>                                         |
| <span data-ttu-id="c3a33-135">!</span><span class="sxs-lookup"><span data-stu-id="c3a33-135">!</span></span>                | <span data-ttu-id="c3a33-136">NOT</span><span class="sxs-lookup"><span data-stu-id="c3a33-136">NOT</span></span>                                        |



 

<span data-ttu-id="c3a33-137">Além dos operadores acima, o LDAP define dois OIDs (identificadores de objeto de regra) correspondentes que podem ser usados para executar comparações de valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="c3a33-137">In addition to the operators above, LDAP defines two matching rule object identifiers (OIDs) that can be used to perform bitwise comparisons of numeric values.</span></span> <span data-ttu-id="c3a33-138">As regras de correspondência têm a seguinte sintaxe.</span><span class="sxs-lookup"><span data-stu-id="c3a33-138">Matching rules have the following syntax.</span></span>


```C++
<attribute name>:<matching rule OID>:=<value>
```



<span data-ttu-id="c3a33-139">" &lt; nome do atributo &gt; " é o **lDAPDisplayName** do atributo, " &lt; OID da regra &gt; " é o OID da regra de correspondência e " &lt; valor &gt; " é o valor a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="c3a33-139">"&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute, "&lt;rule OID&gt;" is the OID for the matching rule, and "&lt;value&gt;" is the value to use for comparison.</span></span> <span data-ttu-id="c3a33-140">Lembre-se de que os espaços não podem ser usados nesta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c3a33-140">Be aware that spaces cannot be used in this string.</span></span> <span data-ttu-id="c3a33-141">" &lt; Value &gt; " deve ser um número decimal; ele não pode ser um número hexadecimal ou um nome de constante, como a **\_ segurança de tipo de grupo ADS \_ \_ \_ habilitada**.</span><span class="sxs-lookup"><span data-stu-id="c3a33-141">"&lt;value&gt;" must be a decimal number; it cannot be a hexadecimal number or a constant name such as **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**.</span></span> <span data-ttu-id="c3a33-142">Para obter mais informações sobre os atributos de Active Directory disponíveis, consulte [todos os atributos](/windows/desktop/ADSchema/attributes-all).</span><span class="sxs-lookup"><span data-stu-id="c3a33-142">For more information about the available Active Directory attributes, see [All Attributes](/windows/desktop/ADSchema/attributes-all).</span></span>

<span data-ttu-id="c3a33-143">A tabela a seguir lista os OIDs de regra de correspondência implementados pelo LDAP.</span><span class="sxs-lookup"><span data-stu-id="c3a33-143">The following table lists the matching rule OIDs implemented by LDAP.</span></span>



| <span data-ttu-id="c3a33-144">OID da regra de correspondência</span><span class="sxs-lookup"><span data-stu-id="c3a33-144">Matching rule OID</span></span>       | <span data-ttu-id="c3a33-145">Identificador de cadeia de caracteres (de Ntldap. h)</span><span class="sxs-lookup"><span data-stu-id="c3a33-145">String identifier (from Ntldap.h)</span></span>   | <span data-ttu-id="c3a33-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3a33-146">Description</span></span>                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a33-147">1.2.840.113556.1.4.803</span><span class="sxs-lookup"><span data-stu-id="c3a33-147">1.2.840.113556.1.4.803</span></span>  | <span data-ttu-id="c3a33-148">**\_ \_ \_ bit de regra de correspondência LDAP \_ e**</span><span class="sxs-lookup"><span data-stu-id="c3a33-148">**LDAP\_MATCHING\_RULE\_BIT\_AND**</span></span>  | <span data-ttu-id="c3a33-149">Uma correspondência será encontrada somente se todos os bits do atributo corresponderem ao valor.</span><span class="sxs-lookup"><span data-stu-id="c3a33-149">A match is found only if all bits from the attribute match the value.</span></span> <span data-ttu-id="c3a33-150">Essa regra é equivalente a um operador **and** bit a bit.</span><span class="sxs-lookup"><span data-stu-id="c3a33-150">This rule is equivalent to a bitwise **AND** operator.</span></span>                                                                  |
| <span data-ttu-id="c3a33-151">1.2.840.113556.1.4.804</span><span class="sxs-lookup"><span data-stu-id="c3a33-151">1.2.840.113556.1.4.804</span></span>  | <span data-ttu-id="c3a33-152">**\_ \_ \_ bit de regra de correspondência LDAP \_ ou**</span><span class="sxs-lookup"><span data-stu-id="c3a33-152">**LDAP\_MATCHING\_RULE\_BIT\_OR**</span></span>   | <span data-ttu-id="c3a33-153">Uma correspondência será encontrada se qualquer um dos bits do atributo corresponder ao valor.</span><span class="sxs-lookup"><span data-stu-id="c3a33-153">A match is found if any bits from the attribute match the value.</span></span> <span data-ttu-id="c3a33-154">Essa regra é equivalente a **um operador OR**</span><span class="sxs-lookup"><span data-stu-id="c3a33-154">This rule is equivalent to a bitwise **OR** operator.</span></span>                                                                        |
| <span data-ttu-id="c3a33-155">1.2.840.113556.1.4.1941</span><span class="sxs-lookup"><span data-stu-id="c3a33-155">1.2.840.113556.1.4.1941</span></span> | <span data-ttu-id="c3a33-156">**\_ \_ regra de correspondência LDAP \_ na \_ cadeia**</span><span class="sxs-lookup"><span data-stu-id="c3a33-156">**LDAP\_MATCHING\_RULE\_IN\_CHAIN**</span></span> | <span data-ttu-id="c3a33-157">Essa regra é limitada a filtros que se aplicam ao DN.</span><span class="sxs-lookup"><span data-stu-id="c3a33-157">This rule is limited to filters that apply to the DN.</span></span> <span data-ttu-id="c3a33-158">Esse é um operador de correspondência "estendida" especial que percorre a cadeia de ancestrais em objetos até a raiz até encontrar uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="c3a33-158">This is a special "extended" match operator that walks the chain of ancestry in objects all the way to the root until it finds a match.</span></span> |



 

<span data-ttu-id="c3a33-159">O exemplo de cadeia de caracteres de consulta a seguir procura objetos de grupo que têm o sinalizador de **\_ segurança de tipo de grupo ADS \_ \_ \_ habilitado** definido.</span><span class="sxs-lookup"><span data-stu-id="c3a33-159">The following example query string searches for group objects that have the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag set.</span></span> <span data-ttu-id="c3a33-160">Lembre-se de que o valor decimal do **\_ tipo de grupo ADS \_ \_ segurança \_ habilitado** (0x80000000 = 2147483648) é usado para o valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="c3a33-160">Be aware that the decimal value of **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) is used for the comparison value.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



<span data-ttu-id="c3a33-161">A **\_ regra de correspondência LDAP \_ \_ na \_ cadeia** é um OID de regra de correspondência projetado para fornecer um método para pesquisar o ancestrais de um objeto.</span><span class="sxs-lookup"><span data-stu-id="c3a33-161">The **LDAP\_MATCHING\_RULE\_IN\_CHAIN** is a matching rule OID that is designed to provide a method to look up the ancestry of an object.</span></span> <span data-ttu-id="c3a33-162">Muitos aplicativos que usam o AD e o AD LDS geralmente funcionam com dados hierárquicos, que são ordenados por relações pai-filho.</span><span class="sxs-lookup"><span data-stu-id="c3a33-162">Many applications using AD and AD LDS usually work with hierarchical data, which is ordered by parent-child relationships.</span></span> <span data-ttu-id="c3a33-163">Anteriormente, os aplicativos executaram a expansão de grupo transitiva para descobrir a associação de grupo, que usava muita largura de banda de rede; os aplicativos precisavam fazer várias viagens de ida e volta para descobrir se um objeto ficou "na cadeia" se um link for percorrido até o final.</span><span class="sxs-lookup"><span data-stu-id="c3a33-163">Previously, applications performed transitive group expansion to figure out group membership, which used too much network bandwidth; applications needed to make multiple roundtrips to figure out if an object fell "in the chain" if a link is traversed through to the end.</span></span>

<span data-ttu-id="c3a33-164">Um exemplo de tal consulta é um projetado para verificar se um usuário "Usuário1" é membro do grupo "grupo1".</span><span class="sxs-lookup"><span data-stu-id="c3a33-164">An example of such a query is one designed to check if a user "user1" is a member of group "group1".</span></span> <span data-ttu-id="c3a33-165">Você definiria a base para o DN de usuário `(cn=user1, cn=users, dc=x)` e o escopo como e `base` usará a consulta a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3a33-165">You would set the base to the user DN `(cn=user1, cn=users, dc=x)` and the scope to `base`, and use the following query.</span></span>


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



<span data-ttu-id="c3a33-166">Da mesma forma, para localizar todos os grupos dos quais "Usuário1" é um membro, defina a base como o DN do contêiner de grupos; por exemplo `(OU=groupsOU, dc=x)` , e o escopo para `subtree` , e use o filtro a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3a33-166">Similarly, to find all the groups that "user1" is a member of, set the base to the groups container DN; for example `(OU=groupsOU, dc=x)` and the scope to `subtree`, and use the following filter.</span></span>


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



<span data-ttu-id="c3a33-167">Observe que, ao usar a **\_ \_ regra de correspondência LDAP \_ na \_ cadeia**, o escopo não é limitado — pode ser `base` , `one-level` ou `subtree` .</span><span class="sxs-lookup"><span data-stu-id="c3a33-167">Note that when using **LDAP\_MATCHING\_RULE\_IN\_CHAIN**, scope is not limited—it can be `base`, `one-level`, or `subtree`.</span></span> <span data-ttu-id="c3a33-168">Algumas dessas consultas em subárvores podem ser mais intensivas no processador, como links de caça com um alto Fan-out; ou seja, listando todos os grupos dos quais um usuário é membro.</span><span class="sxs-lookup"><span data-stu-id="c3a33-168">Some such queries on subtrees may be more processor intensive, such as chasing links with a high fan-out; that is, listing all the groups that a user is a member of.</span></span> <span data-ttu-id="c3a33-169">Pesquisas ineficientes registrarão as mensagens de log de eventos apropriadas, assim como com qualquer outro tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="c3a33-169">Inefficient searches will log appropriate event log messages, as with any other type of query.</span></span>

## <a name="wildcards"></a><span data-ttu-id="c3a33-170">Curingas</span><span class="sxs-lookup"><span data-stu-id="c3a33-170">Wildcards</span></span>

<span data-ttu-id="c3a33-171">Você também pode adicionar curingas e condições a um filtro de pesquisa LDAP.</span><span class="sxs-lookup"><span data-stu-id="c3a33-171">You can also add wildcards and conditions to an LDAP search filter.</span></span> <span data-ttu-id="c3a33-172">Os exemplos a seguir mostram subcadeias de caracteres que podem ser usadas para pesquisar o diretório.</span><span class="sxs-lookup"><span data-stu-id="c3a33-172">The following examples show substrings that can be used to search the directory.</span></span>

<span data-ttu-id="c3a33-173">Obter todas as entradas:</span><span class="sxs-lookup"><span data-stu-id="c3a33-173">Get all entries:</span></span>


```C++
(objectClass=*)
```



<span data-ttu-id="c3a33-174">Obter entradas contendo "Bob" em algum lugar no nome comum:</span><span class="sxs-lookup"><span data-stu-id="c3a33-174">Get entries containing "bob" somewhere in the common name:</span></span>


```C++
(cn=*bob*)
```



<span data-ttu-id="c3a33-175">Obter entradas com um nome comum maior ou igual a "Bob":</span><span class="sxs-lookup"><span data-stu-id="c3a33-175">Get entries with a common name greater than or equal to "bob":</span></span>


```C++
(cn>='bob')
```



<span data-ttu-id="c3a33-176">Obter todos os usuários com um atributo de email:</span><span class="sxs-lookup"><span data-stu-id="c3a33-176">Get all users with an email attribute:</span></span>


```C++
(&(objectClass=user)(email=*))
```



<span data-ttu-id="c3a33-177">Obter todas as entradas de usuário com um atributo de email e um sobrenome igual a "Smith":</span><span class="sxs-lookup"><span data-stu-id="c3a33-177">Get all user entries with an email attribute and a surname equal to "smith":</span></span>


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



<span data-ttu-id="c3a33-178">Obtenha todas as entradas de usuário com um nome comum que comece com "Andy", "Steve" ou "Margaret":</span><span class="sxs-lookup"><span data-stu-id="c3a33-178">Get all user entries with a common name that starts with "andy", "steve", or "margaret":</span></span>


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



<span data-ttu-id="c3a33-179">Obter todas as entradas sem um atributo de email:</span><span class="sxs-lookup"><span data-stu-id="c3a33-179">Get all entries without an email attribute:</span></span>


```C++
(!(email=*))
```



<span data-ttu-id="c3a33-180">A definição formal do filtro de pesquisa é a seguinte (da [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span><span class="sxs-lookup"><span data-stu-id="c3a33-180">The formal definition of the search filter is as follows (from [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span></span>


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



<span data-ttu-id="c3a33-181">O símbolo &lt; attr &gt; é uma cadeia de caracteres que representa um attributeType.</span><span class="sxs-lookup"><span data-stu-id="c3a33-181">The token &lt;attr&gt; is a string that represents an AttributeType.</span></span> <span data-ttu-id="c3a33-182">O valor do token &lt; &gt; é uma cadeia de caracteres que representa um AttributeValue cujo formato é definido pelo serviço de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="c3a33-182">The token &lt;value&gt; is a string that represents an AttributeValue whose format is defined by the underlying directory service.</span></span>

<span data-ttu-id="c3a33-183">Se um &lt; valor &gt; precisar conter o caractere asterisco ( \* ), parêntese esquerdo (() ou parêntese direito ()), o caractere deverá ser precedido pelo caractere de escape de barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="c3a33-183">If a &lt;value&gt; must contain the asterisk (\*), left parenthesis ((), or right parenthesis ()) character, the character should be preceded by the backslash escape character (\\).</span></span>

## <a name="special-characters"></a><span data-ttu-id="c3a33-184">Caracteres Especiais</span><span class="sxs-lookup"><span data-stu-id="c3a33-184">Special Characters</span></span>

<span data-ttu-id="c3a33-185">Se qualquer um dos seguintes caracteres especiais precisar aparecer no filtro de pesquisa como literais, eles deverão ser substituídos pela sequência de escape listada.</span><span class="sxs-lookup"><span data-stu-id="c3a33-185">If any of the following special characters must appear in the search filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="c3a33-186">Caractere ASCII</span><span class="sxs-lookup"><span data-stu-id="c3a33-186">ASCII character</span></span> | <span data-ttu-id="c3a33-187">Sequência de escape substituída</span><span class="sxs-lookup"><span data-stu-id="c3a33-187">Escape sequence substitute</span></span> |
|-----------------|----------------------------|
| \*              | <span data-ttu-id="c3a33-188">\\2a</span><span class="sxs-lookup"><span data-stu-id="c3a33-188">\\2a</span></span>                       |
| <span data-ttu-id="c3a33-189">(</span><span class="sxs-lookup"><span data-stu-id="c3a33-189">(</span></span>               | <span data-ttu-id="c3a33-190">\\38</span><span class="sxs-lookup"><span data-stu-id="c3a33-190">\\28</span></span>                       |
| <span data-ttu-id="c3a33-191">)</span><span class="sxs-lookup"><span data-stu-id="c3a33-191">)</span></span>               | <span data-ttu-id="c3a33-192">\\29</span><span class="sxs-lookup"><span data-stu-id="c3a33-192">\\29</span></span>                       |
| \\              | <span data-ttu-id="c3a33-193">\\5C</span><span class="sxs-lookup"><span data-stu-id="c3a33-193">\\5c</span></span>                       |
| <span data-ttu-id="c3a33-194">NUL</span><span class="sxs-lookup"><span data-stu-id="c3a33-194">NUL</span></span>             | <span data-ttu-id="c3a33-195">\\00</span><span class="sxs-lookup"><span data-stu-id="c3a33-195">\\00</span></span>                       |
| /               | <span data-ttu-id="c3a33-196">\\2F</span><span class="sxs-lookup"><span data-stu-id="c3a33-196">\\2f</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="c3a33-197">Nos casos em que um conjunto de caracteres MultiByte está sendo usado, as sequências de escape listadas acima devem ser usadas se a pesquisa for executada pelo ADO com o dialeto SQL.</span><span class="sxs-lookup"><span data-stu-id="c3a33-197">In cases where a MultiByte Character Set is being used, the escape sequences listed above must be used if the search is performed by ADO with the SQL dialect.</span></span>

 

<span data-ttu-id="c3a33-198">Além disso, dados binários arbitrários podem ser representados usando a sintaxe da sequência de escape codificando cada byte de dados binários com a barra invertida ( \\ ) seguida de dois dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="c3a33-198">In addition, arbitrary binary data may be represented by using the escape sequence syntax by encoding each byte of binary data with the backslash (\\) followed by two hexadecimal digits.</span></span> <span data-ttu-id="c3a33-199">Por exemplo, o valor de quatro bytes 0x00000004 é codificado como \\ 00 \\ 00 \\ 00 \\ 04 em uma cadeia de caracteres de filtro.</span><span class="sxs-lookup"><span data-stu-id="c3a33-199">For example, the four-byte value 0x00000004 is encoded as \\00\\00\\00\\04 in a filter string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3a33-200">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3a33-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3a33-201">Dialeto LDAP</span><span class="sxs-lookup"><span data-stu-id="c3a33-201">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="c3a33-202">Dialeto SQL</span><span class="sxs-lookup"><span data-stu-id="c3a33-202">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="c3a33-203">Pesquisando com a interface IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="c3a33-203">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="c3a33-204">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="c3a33-204">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="c3a33-205">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="c3a33-205">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 
