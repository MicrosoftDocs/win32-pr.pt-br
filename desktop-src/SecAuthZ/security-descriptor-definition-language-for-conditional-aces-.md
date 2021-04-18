---
description: Uma ACE (entrada de controle de acesso condicional) permite que uma condição de acesso seja avaliada quando uma verificação de acesso é executada. A linguagem de definição do descritor de segurança (SDDL) fornece a sintaxe para definir ACEs condicionais em um formato de cadeia de caracteres.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Linguagem de definição do descritor de segurança para ACEs condicionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501976"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a><span data-ttu-id="3346a-104">Linguagem de definição do descritor de segurança para ACEs condicionais</span><span class="sxs-lookup"><span data-stu-id="3346a-104">Security Descriptor Definition Language for Conditional ACEs</span></span>

<span data-ttu-id="3346a-105">Uma ACE ( [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) condicional) permite que uma condição de acesso seja avaliada quando uma verificação de acesso é executada.</span><span class="sxs-lookup"><span data-stu-id="3346a-105">A conditional [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) allows an access condition to be evaluated when an access check is performed.</span></span> <span data-ttu-id="3346a-106">A linguagem de definição do descritor de segurança (SDDL) fornece a sintaxe para definir ACEs condicionais em um formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3346a-106">The security descriptor definition language (SDDL) provides syntax for defining conditional ACEs in a string format.</span></span>

<span data-ttu-id="3346a-107">O SDDL para uma ACE condicional é o mesmo de qualquer ACE, com a sintaxe da instrução condicional acrescentada ao final da cadeia de caracteres ACE.</span><span class="sxs-lookup"><span data-stu-id="3346a-107">The SDDL for a conditional ACE is the same as for any ACE, with the syntax for the conditional statement appended to the end of the ACE string.</span></span> <span data-ttu-id="3346a-108">Para obter informações sobre SDDL, consulte [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="3346a-108">For information about SDDL, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

<span data-ttu-id="3346a-109">O \# sinal "" é sinônimo de "0" em atributos de recurso.</span><span class="sxs-lookup"><span data-stu-id="3346a-109">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="3346a-110">Por exemplo, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) é equivalente a e interpretado como D:ai (XA; OICI; FA;;; WD; (OctetStringType = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="3346a-110">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

-   [<span data-ttu-id="3346a-111">Formato de cadeia de caracteres da ACE condicional</span><span class="sxs-lookup"><span data-stu-id="3346a-111">Conditional ACE String Format</span></span>](#conditional-ace-string-format)
-   [<span data-ttu-id="3346a-112">Expressões condicionais</span><span class="sxs-lookup"><span data-stu-id="3346a-112">Conditional Expressions</span></span>](#conditional-expressions)
-   [<span data-ttu-id="3346a-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="3346a-113">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="3346a-114">Operadores</span><span class="sxs-lookup"><span data-stu-id="3346a-114">Operators</span></span>](#operators)
-   [<span data-ttu-id="3346a-115">Precedência de operador</span><span class="sxs-lookup"><span data-stu-id="3346a-115">Operator Precedence</span></span>](#operator-precedence)
-   [<span data-ttu-id="3346a-116">Valores desconhecidos</span><span class="sxs-lookup"><span data-stu-id="3346a-116">Unknown Values</span></span>](#unknown-values)
-   [<span data-ttu-id="3346a-117">Avaliação da ACE condicional</span><span class="sxs-lookup"><span data-stu-id="3346a-117">Conditional ACE Evaluation</span></span>](#conditional-ace-evaluation)
-   [<span data-ttu-id="3346a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3346a-118">Examples</span></span>](#examples)
-   [<span data-ttu-id="3346a-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3346a-119">Related topics</span></span>](#related-topics)

## <a name="conditional-ace-string-format"></a><span data-ttu-id="3346a-120">Formato de cadeia de caracteres da ACE condicional</span><span class="sxs-lookup"><span data-stu-id="3346a-120">Conditional ACE String Format</span></span>

<span data-ttu-id="3346a-121">Cada ACE em uma cadeia de caracteres de [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) é colocado entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="3346a-121">Each ACE in a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string is enclosed in parentheses.</span></span> <span data-ttu-id="3346a-122">Os campos da ACE estão na seguinte ordem e são separados por ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="3346a-122">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

<span data-ttu-id="3346a-123">*AceType ***;** _AceFlags_* _;_ *_Direitos_*_;_ *_ObjectGUID_*_;_ *_InheritObjectGuid_*_;_ *_AccountId_*_;(_*_condicionalização_*_)_*</span><span class="sxs-lookup"><span data-stu-id="3346a-123">*AceType\***;**_AceFlags_*_;_*_Rights_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_;(_*_ConditionalExpression_*_)_\*</span></span>

<span data-ttu-id="3346a-124">Os campos são descritos em [cadeias de caracteres Ace](ace-strings.md), com as seguintes exceções.</span><span class="sxs-lookup"><span data-stu-id="3346a-124">The fields are as described in [ACE Strings](ace-strings.md), with the following exceptions.</span></span>

-   <span data-ttu-id="3346a-125">O campo *AceType* pode ser uma das cadeias de caracteres a seguir.</span><span class="sxs-lookup"><span data-stu-id="3346a-125">The *AceType* field can be one of the following strings.</span></span>

    | <span data-ttu-id="3346a-126">ACE tipo String</span><span class="sxs-lookup"><span data-stu-id="3346a-126">ACE type string</span></span> | <span data-ttu-id="3346a-127">Constante em SDDL. h</span><span class="sxs-lookup"><span data-stu-id="3346a-127">Constant in Sddl.h</span></span>                         | <span data-ttu-id="3346a-128">Valor de AceType</span><span class="sxs-lookup"><span data-stu-id="3346a-128">AceType value</span></span>                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | <span data-ttu-id="3346a-129">XA</span><span class="sxs-lookup"><span data-stu-id="3346a-129">"XA"</span></span><br/> | <span data-ttu-id="3346a-130">\_acesso de retorno de chamada SDDL \_ \_ permitido</span><span class="sxs-lookup"><span data-stu-id="3346a-130">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span><br/> | <span data-ttu-id="3346a-131">\_tipo de \_ ACE de retorno de chamada permitido de \_ acesso \_</span><span class="sxs-lookup"><span data-stu-id="3346a-131">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE</span></span><br/> |
    | <span data-ttu-id="3346a-132">XD</span><span class="sxs-lookup"><span data-stu-id="3346a-132">"XD"</span></span><br/> | <span data-ttu-id="3346a-133">\_acesso de retorno de chamada SDDL \_ \_ negado</span><span class="sxs-lookup"><span data-stu-id="3346a-133">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span><br/>  | <span data-ttu-id="3346a-134">tipo de ACE de retorno de \_ chamada negado de acesso \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3346a-134">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE</span></span><br/>  |

    

     

-   <span data-ttu-id="3346a-135">A cadeia de caracteres ACE inclui uma ou mais expressões condicionais, delimitadas por parênteses no final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3346a-135">The ACE string includes one or more conditional expressions, enclosed in parentheses at the end of the string.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="3346a-136">Expressões condicionais</span><span class="sxs-lookup"><span data-stu-id="3346a-136">Conditional Expressions</span></span>

<span data-ttu-id="3346a-137">Uma expressão condicional pode incluir qualquer um dos elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="3346a-137">A conditional expression can include any of the following elements.</span></span>



| <span data-ttu-id="3346a-138">Elemento Expression</span><span class="sxs-lookup"><span data-stu-id="3346a-138">Expression element</span></span>                                                | <span data-ttu-id="3346a-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="3346a-139">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3346a-140">*AttributeName*</span><span class="sxs-lookup"><span data-stu-id="3346a-140">*AttributeName*</span></span><br/>                                        | <span data-ttu-id="3346a-141">Testa se o atributo especificado tem um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3346a-141">Tests whether the specified attribute has a nonzero value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3346a-142">**existe** *AttributeName*</span><span class="sxs-lookup"><span data-stu-id="3346a-142">**exists** *AttributeName*</span></span><br/>                             | <span data-ttu-id="3346a-143">Testa se o atributo especificado existe no contexto do cliente.</span><span class="sxs-lookup"><span data-stu-id="3346a-143">Tests whether the specified attribute exists in the client context.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3346a-144">*Valor* do *operador* *AttributeName*</span><span class="sxs-lookup"><span data-stu-id="3346a-144">*AttributeName* *Operator* *Value*</span></span><br/>                     | <span data-ttu-id="3346a-145">Retorna o resultado da operação especificada.</span><span class="sxs-lookup"><span data-stu-id="3346a-145">Returns the result of the specified operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3346a-146">\* **\|\|** _Condicionalização_ \* condicional</span><span class="sxs-lookup"><span data-stu-id="3346a-146">\*ConditionalExpression\***\|\|**_ConditionalExpression_</span></span><br/> | <span data-ttu-id="3346a-147">Testa se uma das expressões condicionais especificadas é true.</span><span class="sxs-lookup"><span data-stu-id="3346a-147">Tests whether either of the specified conditional expressions is true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3346a-148">*Condicionalização* **&&** *Condicionalização*</span><span class="sxs-lookup"><span data-stu-id="3346a-148">*ConditionalExpression* **&&** *ConditionalExpression*</span></span><br/> | <span data-ttu-id="3346a-149">Testa se ambas as expressões condicionais especificadas são true.</span><span class="sxs-lookup"><span data-stu-id="3346a-149">Tests whether both of the specified conditional expressions are true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3346a-150">**! (**_Conditionalparameters_*_)_*</span><span class="sxs-lookup"><span data-stu-id="3346a-150">**!(**_ConditionalExpression_*_)_*</span></span><br/>                     | <span data-ttu-id="3346a-151">O inverso de uma expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="3346a-151">The inverse of a conditional expression.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3346a-152">**Membro \_ de {**_SidArray_*_}_*</span><span class="sxs-lookup"><span data-stu-id="3346a-152">**Member\_of{**_SidArray_*_}_*</span></span><br/>                         | <span data-ttu-id="3346a-153">Testa se a matriz de [**\_ \_ atributos e Sid**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) do contexto do cliente contém todos os SIDs ( [identificadores de segurança](security-identifiers.md) ) na lista separada por vírgulas especificada por *SidArray*.</span><span class="sxs-lookup"><span data-stu-id="3346a-153">Tests whether the [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) array of the client context contains all of the [Security Identifiers](security-identifiers.md) (SIDs) in the comma-separated list specified by *SidArray*.</span></span><br/> <span data-ttu-id="3346a-154">Para permitir ACEs, um SID de contexto de cliente deve ter o conjunto de atributos **\_ \_ habilitado para grupo se** definido para ser considerado uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="3346a-154">For Allow ACEs, a client context SID must have the **SE\_GROUP\_ENABLED** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="3346a-155">Para Deny ACEs, um SID de contexto de cliente deve ter **o \_ grupo se \_ habilitado** ou **o \_ grupo se \_ usar \_ para \_ negação \_** de atributo definido para ser considerado uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="3346a-155">For Deny ACEs, a client context SID must have either the **SE\_GROUP\_ENABLED** or the **SE\_GROUP\_USE\_FOR\_DENY\_ONLY** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="3346a-156">A matriz *SidArray* pode conter cadeias de caracteres Sid (por exemplo, "S-1-5-6") ou aliases de Sid (por exemplo, "BA"</span><span class="sxs-lookup"><span data-stu-id="3346a-156">The *SidArray* array can contain either SID strings (for example, "S-1-5-6") or SID aliases (for example, "BA"</span></span><br/> |



 

## <a name="attributes"></a><span data-ttu-id="3346a-157">Atributos</span><span class="sxs-lookup"><span data-stu-id="3346a-157">Attributes</span></span>

<span data-ttu-id="3346a-158">Um atributo representa um elemento na matriz [**de \_ \_ \_ informações de atributos de segurança de AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) no contexto do cliente.</span><span class="sxs-lookup"><span data-stu-id="3346a-158">An attribute represents an element in the [**AUTHZ\_SECURITY\_ATTRIBUTES\_INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) array in the client context.</span></span> <span data-ttu-id="3346a-159">Um nome de atributo pode conter qualquer caractere alfanumérico e qualquer um dos caracteres ":", "/", "." e " \_ ".</span><span class="sxs-lookup"><span data-stu-id="3346a-159">An attribute name can contain any alphanumeric characters and any of the characters ":", "/", ".", and "\_".</span></span>

<span data-ttu-id="3346a-160">Um valor de atributo pode ser qualquer um dos tipos a seguir.</span><span class="sxs-lookup"><span data-stu-id="3346a-160">An attribute value can be any of the following types.</span></span>



| <span data-ttu-id="3346a-161">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="3346a-161">Value type</span></span>         | <span data-ttu-id="3346a-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="3346a-162">Description</span></span>                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3346a-163">Integer</span><span class="sxs-lookup"><span data-stu-id="3346a-163">Integer</span></span><br/> | <span data-ttu-id="3346a-164">Um inteiro de 64 bits em notação decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="3346a-164">A 64-bit integer in either decimal or hexadecimal notation.</span></span><br/>                                                                                                                              |
| <span data-ttu-id="3346a-165">String</span><span class="sxs-lookup"><span data-stu-id="3346a-165">String</span></span><br/>  | <span data-ttu-id="3346a-166">Um valor de cadeia de caracteres delimitado por aspas.</span><span class="sxs-lookup"><span data-stu-id="3346a-166">A string value delimited by quotes.</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="3346a-167">SID</span><span class="sxs-lookup"><span data-stu-id="3346a-167">SID</span></span><br/>     | <span data-ttu-id="3346a-168">SID (S-1-1-0) ou SID (BA).</span><span class="sxs-lookup"><span data-stu-id="3346a-168">SID(S-1-1-0) or SID(BA).</span></span> <span data-ttu-id="3346a-169">Deve estar no RHS do membro \_ ou \_ do membro do dispositivo \_ de.</span><span class="sxs-lookup"><span data-stu-id="3346a-169">Has to be on RHS of Member\_of or Device\_Member\_of.</span></span><br/>                                                                                                           |
| <span data-ttu-id="3346a-170">BLOB</span><span class="sxs-lookup"><span data-stu-id="3346a-170">BLOB</span></span><br/>    | <span data-ttu-id="3346a-171">\# seguido por números hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="3346a-171">\# followed by hexadecimal numbers.</span></span> <span data-ttu-id="3346a-172">Se o comprimento dos números for ímpar, o \# será convertido em um 0 para torná-lo par.</span><span class="sxs-lookup"><span data-stu-id="3346a-172">If length of the numbers is odd, then the \# is translated to a 0 to make it even.</span></span> <span data-ttu-id="3346a-173">Além disso, uma \# exibição em outro lugar no valor é convertida em 0.</span><span class="sxs-lookup"><span data-stu-id="3346a-173">Also an \# appearing elsewhere in the value is translated to a 0.</span></span><br/> |



 

## <a name="operators"></a><span data-ttu-id="3346a-174">Operadores</span><span class="sxs-lookup"><span data-stu-id="3346a-174">Operators</span></span>

<span data-ttu-id="3346a-175">Os operadores a seguir são definidos para uso em expressões condicionais para testar os valores de atributos.</span><span class="sxs-lookup"><span data-stu-id="3346a-175">The following operators are defined for use in conditional expressions to test the values of attributes.</span></span> <span data-ttu-id="3346a-176">Todos esses são operadores binários e usados no formulário de *valor* do *operador* *AttributeName* .</span><span class="sxs-lookup"><span data-stu-id="3346a-176">All of these are binary operators and used in the form *AttributeName* *Operator* *Value*.</span></span>



| <span data-ttu-id="3346a-177">Operador</span><span class="sxs-lookup"><span data-stu-id="3346a-177">Operator</span></span>            | <span data-ttu-id="3346a-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="3346a-178">Description</span></span>                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | <span data-ttu-id="3346a-179">Definição convencional.</span><span class="sxs-lookup"><span data-stu-id="3346a-179">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="3346a-180">!=</span><span class="sxs-lookup"><span data-stu-id="3346a-180">!=</span></span><br/>       | <span data-ttu-id="3346a-181">Definição convencional.</span><span class="sxs-lookup"><span data-stu-id="3346a-181">Conventional definition.</span></span><br/>                                                                                      |
| <<br/>     | <span data-ttu-id="3346a-182">Definição convencional.</span><span class="sxs-lookup"><span data-stu-id="3346a-182">Conventional definition.</span></span><br/>                                                                                      |
| <=<br/>    | <span data-ttu-id="3346a-183">Definição convencional.</span><span class="sxs-lookup"><span data-stu-id="3346a-183">Conventional definition.</span></span><br/>                                                                                      |
| ><br/>     | <span data-ttu-id="3346a-184">Definição convencional.</span><span class="sxs-lookup"><span data-stu-id="3346a-184">Conventional definition.</span></span><br/>                                                                                      |
| >=<br/>    | <span data-ttu-id="3346a-185">Definição convencional.</span><span class="sxs-lookup"><span data-stu-id="3346a-185">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="3346a-186">Contém</span><span class="sxs-lookup"><span data-stu-id="3346a-186">Contains</span></span><br/> | <span data-ttu-id="3346a-187">**True** se o valor do atributo especificado for um superconjunto do valor especificado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3346a-187">**TRUE** if the value of the specified attribute is a superset of the specified value; otherwise, **FALSE**.</span></span><br/>  |
| <span data-ttu-id="3346a-188">Qualquer \_ de</span><span class="sxs-lookup"><span data-stu-id="3346a-188">Any\_of</span></span><br/>  | <span data-ttu-id="3346a-189">**True** se o valor especificado for um superconjunto do valor do atributo especificado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3346a-189">**TRUE** if the specified value is a superset of the value of the specified attribute; otherwise, **FALSE**.</span></span> <br/> |



 

<span data-ttu-id="3346a-190">Além disso, os operadores unários existem, member \_ of e Negation (!) são definidos conforme descrito na tabela de expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="3346a-190">In addition, the unary operators Exists, Member\_of, and negation (!) are defined as described in the Conditional Expressions table.</span></span>

<span data-ttu-id="3346a-191">O operador "Contains" deve ser precedido e seguido por um espaço em branco e o operador "Any \_ of" deve ser precedido por um espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="3346a-191">The "Contains" operator must be preceded and followed by white space, and the "Any\_of" operator must be preceded by white space.</span></span>

## <a name="operator-precedence"></a><span data-ttu-id="3346a-192">Precedência de operador</span><span class="sxs-lookup"><span data-stu-id="3346a-192">Operator Precedence</span></span>

<span data-ttu-id="3346a-193">Os operadores são avaliados na seguinte ordem de precedência, com operações de precedência igual sendo avaliadas da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="3346a-193">The operators are evaluated in the following order of precedence, with operations of equal precedence being evaluated from left to right.</span></span>

1.  <span data-ttu-id="3346a-194">Existe, membro \_ de</span><span class="sxs-lookup"><span data-stu-id="3346a-194">Exists, Member\_of</span></span>
2.  <span data-ttu-id="3346a-195">Contém, qualquer um \_ dos</span><span class="sxs-lookup"><span data-stu-id="3346a-195">Contains, Any\_of</span></span>
3.  <span data-ttu-id="3346a-196">= =,! =, <, <=, >, >=</span><span class="sxs-lookup"><span data-stu-id="3346a-196">==, !=, <, <=, >, >=</span></span>
4.  <span data-ttu-id="3346a-197">!</span><span class="sxs-lookup"><span data-stu-id="3346a-197">!</span></span>
5.  &&
6.  \|\|

<span data-ttu-id="3346a-198">Além disso, qualquer parte de uma expressão condicional pode ser colocada entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="3346a-198">In addition, any portion of a conditional expression can be enclosed in parenthesis.</span></span> <span data-ttu-id="3346a-199">As expressões dentro dos parênteses são avaliadas primeiro.</span><span class="sxs-lookup"><span data-stu-id="3346a-199">Expressions within parentheses are evaluated first.</span></span>

## <a name="unknown-values"></a><span data-ttu-id="3346a-200">Valores desconhecidos</span><span class="sxs-lookup"><span data-stu-id="3346a-200">Unknown Values</span></span>

<span data-ttu-id="3346a-201">Os resultados de expressões condicionais às vezes retornam um valor **desconhecido**.</span><span class="sxs-lookup"><span data-stu-id="3346a-201">The results of conditional expressions sometimes return a value of **Unknown**.</span></span> <span data-ttu-id="3346a-202">Por exemplo, qualquer uma das operações relacionais retorna **desconhecido** quando o atributo especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="3346a-202">For example, any of the relational operations return **Unknown** when the specified attribute does not exist.</span></span>

<span data-ttu-id="3346a-203">A tabela a seguir descreve os resultados de uma operação **and** lógica entre duas expressões condicionais, *ConditionalExpression1* e *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="3346a-203">The following table describes the results for a logical **AND** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="3346a-204">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="3346a-204">*ConditionalExpression1*</span></span> | <span data-ttu-id="3346a-205">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="3346a-205">*ConditionalExpression2*</span></span> | <span data-ttu-id="3346a-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="3346a-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|----------------------------------------------------------|
| <span data-ttu-id="3346a-207">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-207">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-208">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-208">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-209">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-209">**TRUE**</span></span><br/>                                      |
| <span data-ttu-id="3346a-210">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-210">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-211">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-211">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-212">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-212">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3346a-213">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-213">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-214">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-214">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-215">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-215">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="3346a-216">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-216">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-217">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-217">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-218">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-218">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3346a-219">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-219">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-220">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-220">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-221">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-221">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3346a-222">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-222">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-223">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-223">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-224">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-224">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3346a-225">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-225">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-226">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-226">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-227">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-227">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="3346a-228">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-228">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-229">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-229">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-230">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-230">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="3346a-231">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-231">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-232">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-232">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-233">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-233">**UNKNOWN**</span></span><br/>                                   |



 

<span data-ttu-id="3346a-234">A tabela a seguir descreve os resultados de uma operação **or** lógica entre duas expressões condicionais, *ConditionalExpression1* e *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="3346a-234">The following table describes the results for a logical **OR** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="3346a-235">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="3346a-235">*ConditionalExpression1*</span></span> | <span data-ttu-id="3346a-236">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="3346a-236">*ConditionalExpression2*</span></span> | <span data-ttu-id="3346a-237">*ConditionalExpression1* \*\*</span><span class="sxs-lookup"><span data-stu-id="3346a-237">*ConditionalExpression1* \*\*</span></span>\|\|<span data-ttu-id="3346a-238">\*\* *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="3346a-238">\*\* *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|------------------------------------------------------------|
| <span data-ttu-id="3346a-239">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-239">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-240">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-240">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-241">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-241">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3346a-242">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-242">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-243">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-243">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-244">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-244">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3346a-245">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-245">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-246">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-246">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-247">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-247">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3346a-248">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-248">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-249">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-249">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-250">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-250">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3346a-251">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-251">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-252">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-252">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-253">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-253">**FALSE**</span></span><br/>                                       |
| <span data-ttu-id="3346a-254">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-254">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-255">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-255">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-256">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-256">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="3346a-257">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-257">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-258">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-258">**TRUE**</span></span><br/>      | <span data-ttu-id="3346a-259">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3346a-259">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="3346a-260">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-260">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-261">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3346a-261">**FALSE**</span></span><br/>     | <span data-ttu-id="3346a-262">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-262">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="3346a-263">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-263">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-264">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-264">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="3346a-265">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3346a-265">**UNKNOWN**</span></span><br/>                                     |



 

<span data-ttu-id="3346a-266">A negação de uma expressão condicional com um valor de **desconhecido** também é **desconhecida**.</span><span class="sxs-lookup"><span data-stu-id="3346a-266">The negation of a conditional expression with a value of **UNKNOWN** is also **UNKNOWN**.</span></span>

## <a name="conditional-ace-evaluation"></a><span data-ttu-id="3346a-267">Avaliação da ACE condicional</span><span class="sxs-lookup"><span data-stu-id="3346a-267">Conditional ACE Evaluation</span></span>

<span data-ttu-id="3346a-268">A tabela a seguir descreve o resultado da verificação de acesso de uma ACE condicional, dependendo da avaliação final da expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="3346a-268">The following table describes the access check result of a conditional ACE depending on the final evaluation of the conditional expression.</span></span>

| <span data-ttu-id="3346a-269">Tipo de ACE</span><span class="sxs-lookup"><span data-stu-id="3346a-269">ACE type</span></span>         | <span data-ttu-id="3346a-270">TRUE</span><span class="sxs-lookup"><span data-stu-id="3346a-270">TRUE</span></span>             | <span data-ttu-id="3346a-271">FALSE</span><span class="sxs-lookup"><span data-stu-id="3346a-271">FALSE</span></span>                 | <span data-ttu-id="3346a-272">DESCONHECIDO</span><span class="sxs-lookup"><span data-stu-id="3346a-272">UNKNOWN</span></span>               |
|------------------|------------------|-----------------------|-----------------------|
| <span data-ttu-id="3346a-273">Allow</span><span class="sxs-lookup"><span data-stu-id="3346a-273">Allow</span></span><br/> | <span data-ttu-id="3346a-274">Allow</span><span class="sxs-lookup"><span data-stu-id="3346a-274">Allow</span></span><br/> | <span data-ttu-id="3346a-275">Ignorar ACE</span><span class="sxs-lookup"><span data-stu-id="3346a-275">Ignore ACE</span></span><br/> | <span data-ttu-id="3346a-276">Ignorar ACE</span><span class="sxs-lookup"><span data-stu-id="3346a-276">Ignore ACE</span></span><br/> |
| <span data-ttu-id="3346a-277">Negar</span><span class="sxs-lookup"><span data-stu-id="3346a-277">Deny</span></span><br/>  | <span data-ttu-id="3346a-278">Negar</span><span class="sxs-lookup"><span data-stu-id="3346a-278">Deny</span></span><br/>  | <span data-ttu-id="3346a-279">Ignorar ACE</span><span class="sxs-lookup"><span data-stu-id="3346a-279">Ignore ACE</span></span><br/> | <span data-ttu-id="3346a-280">Negar</span><span class="sxs-lookup"><span data-stu-id="3346a-280">Deny</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="3346a-281">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3346a-281">Examples</span></span>

<span data-ttu-id="3346a-282">Os exemplos a seguir mostram como as políticas de acesso especificadas são representadas por uma ACE condicional definida usando SDDL.</span><span class="sxs-lookup"><span data-stu-id="3346a-282">The following examples show how the specified access policies are represented by a conditional ACE defined by using SDDL.</span></span>

<dl> <dt>

<span data-ttu-id="3346a-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Regras</span><span class="sxs-lookup"><span data-stu-id="3346a-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="3346a-284">Permitir executar para todos se as duas condições a seguir forem atendidas:</span><span class="sxs-lookup"><span data-stu-id="3346a-284">Allow Execute to Everyone if both of the following conditions are met:</span></span>

-   <span data-ttu-id="3346a-285">Título = PM</span><span class="sxs-lookup"><span data-stu-id="3346a-285">Title = PM</span></span>
-   <span data-ttu-id="3346a-286">Divisão = finanças ou divisão = vendas</span><span class="sxs-lookup"><span data-stu-id="3346a-286">Division = Finance or Division = Sales</span></span>

</dd> <dt>

<span data-ttu-id="3346a-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="3346a-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="3346a-288">D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Finance" \| \| @User.Division = = "Sales")))</span><span class="sxs-lookup"><span data-stu-id="3346a-288">D:(XA; ;FX;;;S-1-1-0; (@User.Title=="PM" && (@User.Division=="Finance" \|\| @User.Division ==" Sales")))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="3346a-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Regras</span><span class="sxs-lookup"><span data-stu-id="3346a-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="3346a-290">Permitir executar se qualquer um dos projetos do usuário se Interseccionar com os projetos do arquivo s.</span><span class="sxs-lookup"><span data-stu-id="3346a-290">Allow execute if any of the user s projects intersect with the file s projects.</span></span>

</dd> <dt>

<span data-ttu-id="3346a-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="3346a-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="3346a-292">D: (XA;; FX;;; S-1-1-0; ( @User.Project Qualquer \_ de @Resource.Project ))</span><span class="sxs-lookup"><span data-stu-id="3346a-292">D:(XA; ;FX;;;S-1-1-0; (@User.Project Any\_of @Resource.Project))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="3346a-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Regras</span><span class="sxs-lookup"><span data-stu-id="3346a-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="3346a-294">Permitir acesso de leitura se o usuário tiver feito logon com um cartão inteligente, for um operador de backup e estiver se conectando de um computador com o BitLocker habilitado.</span><span class="sxs-lookup"><span data-stu-id="3346a-294">Allow read access if the user has logged in with a smart card, is a backup operator, and is connecting from a machine with Bitlocker enabled.</span></span>

</dd> <dt>

<span data-ttu-id="3346a-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="3346a-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="3346a-296">D: (XA;; FR;;; S-1-1-0; (Membro \_ de {Sid (SID de cartão inteligente \_ ), Sid (Bo)}  && @Device.Bitlocker ))</span><span class="sxs-lookup"><span data-stu-id="3346a-296">D:(XA; ;FR;;;S-1-1-0; (Member\_of {SID(Smartcard\_SID), SID(BO)} && @Device.Bitlocker))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="3346a-297">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3346a-297">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3346a-298">[\[MS-DTYP \] : linguagem de descrição do descritor de segurança](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="3346a-298">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

