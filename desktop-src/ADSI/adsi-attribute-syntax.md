---
title: Sintaxe de atributo ADSI
description: Cada atributo no diretório tem uma sintaxe associada. Por exemplo, inteiro, Cadeia de caracteres, numérico e assim por diante. A ADSI define sua própria sintaxe que é mapeada para a sintaxe do diretório nativo. Esta seção descreve os tipos de sintaxes de atributo no ADSI.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- atributos ADSI, sintaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23d58b48b27fa88077f388b47535afd1dbd0a4f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641828"
---
# <a name="adsi-attribute-syntax"></a><span data-ttu-id="70c3f-107">Sintaxe de atributo ADSI</span><span class="sxs-lookup"><span data-stu-id="70c3f-107">ADSI Attribute Syntax</span></span>

<span data-ttu-id="70c3f-108">Cada atributo no diretório tem uma sintaxe associada.</span><span class="sxs-lookup"><span data-stu-id="70c3f-108">Each attribute in the directory has an associated syntax.</span></span> <span data-ttu-id="70c3f-109">Por exemplo, inteiro, Cadeia de caracteres, numérico e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="70c3f-109">For example, integer, string, numeric, and so on.</span></span> <span data-ttu-id="70c3f-110">A ADSI define sua própria sintaxe que é mapeada para a sintaxe do diretório nativo.</span><span class="sxs-lookup"><span data-stu-id="70c3f-110">ADSI defines its own syntax that maps to the native directory syntax.</span></span> <span data-ttu-id="70c3f-111">Esta seção descreve os tipos de sintaxes de atributo no ADSI.</span><span class="sxs-lookup"><span data-stu-id="70c3f-111">This section describes the types of attribute syntaxes in ADSI.</span></span>

## <a name="distinguished-name-string"></a><span data-ttu-id="70c3f-112">Cadeia de caracteres de nome distinto</span><span class="sxs-lookup"><span data-stu-id="70c3f-112">Distinguished Name String</span></span>


```VB
Syntax Type: ADSTYPE_DN_STRING
```



<span data-ttu-id="70c3f-113">O nome distinto é útil para vincular dois objetos juntos.</span><span class="sxs-lookup"><span data-stu-id="70c3f-113">The distinguished name is useful for linking two objects together.</span></span> <span data-ttu-id="70c3f-114">Por exemplo, ele pode criar um link que torna o objeto Alice um gerente do objeto Bob.</span><span class="sxs-lookup"><span data-stu-id="70c3f-114">For example, it can create a link that makes the Alice object a manager of the Bob object.</span></span> <span data-ttu-id="70c3f-115">Se o objeto Alice se mover para um local diferente, o link do gerente entre Alice e Bob será atualizado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="70c3f-115">If the Alice object moves to different place, the manager link between Alice and Bob is updated automatically.</span></span>

<span data-ttu-id="70c3f-116">O nome distinto deve conter um objeto de nome distinto válido.</span><span class="sxs-lookup"><span data-stu-id="70c3f-116">The distinguished name must contain a valid distinguished name object.</span></span> <span data-ttu-id="70c3f-117">Se o nome diferenciado não corresponder a um objeto existente válido, a maioria dos servidores rejeitará a solicitação e retornará um erro de violação de restrição.</span><span class="sxs-lookup"><span data-stu-id="70c3f-117">If the distinguished name does not correspond to a valid existing object, most servers reject the request and return a constraint violation error.</span></span>

<span data-ttu-id="70c3f-118">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="70c3f-118">Examples:</span></span>


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a><span data-ttu-id="70c3f-119">Cadeia de caracteres Exact maiúsculas e maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="70c3f-119">Case Exact String and Case Ignore String</span></span>


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



<span data-ttu-id="70c3f-120">A cadeia exata de maiúsculas e minúsculas é uma cadeia de caracteres que diferencia maiúsculas de minúsculas quando a cadeia de caracteres ignora maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="70c3f-120">Case Exact String is a case-sensitive string while Case Ignore String is a case-insensitive string.</span></span> <span data-ttu-id="70c3f-121">Uma grande porcentagem de atributos no diretório usa essa sintaxe.</span><span class="sxs-lookup"><span data-stu-id="70c3f-121">A large percentage of attributes in the directory use this syntax.</span></span>

> [!Note]  
> <span data-ttu-id="70c3f-122">O diretório pode ou não armazenar isso como uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="70c3f-122">The directory may or may not store this as a Unicode string.</span></span> <span data-ttu-id="70c3f-123">No entanto, a ADSI aceita e retorna cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="70c3f-123">However, ADSI accepts and returns Unicode strings.</span></span>

 

<span data-ttu-id="70c3f-124">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="70c3f-124">Example:</span></span>


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a><span data-ttu-id="70c3f-125">Cadeia de caracteres imprimível</span><span class="sxs-lookup"><span data-stu-id="70c3f-125">Printable String</span></span>


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



<span data-ttu-id="70c3f-126">Essa sintaxe é usada para atributos com valores de cadeia de caracteres em que letras maiúsculas e minúsculas são consideradas desiguais para comparações, por exemplo, "FABRIKAM" e "fabrikam" não correspondem.</span><span class="sxs-lookup"><span data-stu-id="70c3f-126">This syntax is used for attributes with string values where uppercase and lowercase are considered unequal for comparisons, for example, "FABRIKAM" and "Fabrikam" do not match.</span></span> <span data-ttu-id="70c3f-127">A ADSI aceita qualquer conteúdo para uma cadeia de caracteres imprimível; Ele não tenta verificar se eles estão realmente imprimíveis.</span><span class="sxs-lookup"><span data-stu-id="70c3f-127">ADSI accepts any contents for a Printable-String; it does not attempt to verify that they are indeed printable.</span></span>

## <a name="numeric-string"></a><span data-ttu-id="70c3f-128">Cadeia de caracteres numérica</span><span class="sxs-lookup"><span data-stu-id="70c3f-128">Numeric String</span></span>


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



<span data-ttu-id="70c3f-129">Nessa sintaxe, cadeias de caracteres correspondem como em cadeias imprimíveis, exceto que todos os caracteres de espaço são ignorados em comparações.</span><span class="sxs-lookup"><span data-stu-id="70c3f-129">In this syntax, strings match as in Printable String, except that all space characters are ignored in comparisons.</span></span> <span data-ttu-id="70c3f-130">A ADSI não executa a verificação de valor para garantir que somente numerais e espaços apareçam em valores dessa sintaxe.</span><span class="sxs-lookup"><span data-stu-id="70c3f-130">ADSI does not perform value checking to ensure that only numerals and spaces appear in values of this syntax.</span></span> <span data-ttu-id="70c3f-131">Active Directory aceita qualquer conteúdo para uma cadeia de caracteres numérica; Ele não verifica se os caracteres são numéricos.</span><span class="sxs-lookup"><span data-stu-id="70c3f-131">Active Directory accepts any content for a numeric string; it does not verify that the characters are numeric.</span></span>

## <a name="utc-time"></a><span data-ttu-id="70c3f-132">Hora UTC</span><span class="sxs-lookup"><span data-stu-id="70c3f-132">UTC Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="70c3f-133">Essa sintaxe armazena a data e a hora em uma única cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70c3f-133">This syntax stores the date and time in a single string.</span></span> <span data-ttu-id="70c3f-134">O formato da cadeia de caracteres consiste em três partes concatenadas: (1) YYMMDD; (2) HHMM ou HHMMSS (ambos são aceitáveis); e (3) "Z" para indicar que o tempo fornecido é Greenwich Mean Time (GMT) ou "+/-HHMM" para indicar que a hora fornecida é a hora local com o diferencial fornecido do GMT.</span><span class="sxs-lookup"><span data-stu-id="70c3f-134">The string format consists of three concatenated parts: (1) YYMMDD; (2) HHMM or HHMMSS (both are acceptable); and (3) "Z" to indicate that the time given is Greenwich Mean Time (GMT), or "+/-HHMM" to indicate that the time given is local time with the given differential from GMT.</span></span> <span data-ttu-id="70c3f-135">O diferencial é baseado na fórmula: GMT = local + diferencial.</span><span class="sxs-lookup"><span data-stu-id="70c3f-135">The differential is based on the formula: GMT=Local+differential.</span></span>

> [!Note]  
> <span data-ttu-id="70c3f-136">Os dois primeiros dígitos do ano não são armazenados nessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70c3f-136">The first two digits of the year are not stored in this string.</span></span>

 

<span data-ttu-id="70c3f-137">Alguns exemplos de valores válidos são "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503 + 0130".</span><span class="sxs-lookup"><span data-stu-id="70c3f-137">Some examples of legal values are "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130".</span></span> <span data-ttu-id="70c3f-138">Essa cadeia de caracteres é armazenada como caracteres ASCII de byte único e nenhum número de página de código é armazenado com ele.</span><span class="sxs-lookup"><span data-stu-id="70c3f-138">This string is stored as single-byte ASCII characters, and no code page number is stored with it.</span></span>

<span data-ttu-id="70c3f-139">Embora a ordenação tenha suporte, ela é feita apenas como uma classificação de cadeia de caracteres que não diferencia maiúsculas de minúsculas, Não interpretando adequadamente o significado das cadeias.</span><span class="sxs-lookup"><span data-stu-id="70c3f-139">Although ordering is supported, it is done only as an ASCII case-insensitive string sort, not by properly interpreting the meaning of the strings.</span></span>

<span data-ttu-id="70c3f-140">Qualquer valor de cadeia de caracteres válido é aceito.</span><span class="sxs-lookup"><span data-stu-id="70c3f-140">Any valid string value is accepted.</span></span> <span data-ttu-id="70c3f-141">Nenhuma tentativa é feita para garantir que a cadeia de caracteres contenha uma cadeia de caracteres de tempo válida.</span><span class="sxs-lookup"><span data-stu-id="70c3f-141">No attempt is made to ensure that the string contains a valid time string.</span></span>

## <a name="generalized-time"></a><span data-ttu-id="70c3f-142">Tempo generalizado</span><span class="sxs-lookup"><span data-stu-id="70c3f-142">Generalized Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="70c3f-143">Se um novo atributo para armazenar valores de tempo estiver sendo definido, a sintaxe GeneralizedTime deverá ser usada.</span><span class="sxs-lookup"><span data-stu-id="70c3f-143">If a new attribute to store time values is being defined, the GeneralizedTime syntax should be used.</span></span> <span data-ttu-id="70c3f-144">A sintaxe GeneralizedTime usa quatro caracteres para representar o ano em vez de dois como com UTCTime.</span><span class="sxs-lookup"><span data-stu-id="70c3f-144">GeneralizedTime syntax uses four characters to represent the year instead of two as with UTCTime.</span></span>

<span data-ttu-id="70c3f-145">O formato da sintaxe GeneralizedTime é "AAAAMMDDHHMMSS. 0Z".</span><span class="sxs-lookup"><span data-stu-id="70c3f-145">The format for the GeneralizedTime syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="70c3f-146">Um exemplo de um valor aceitável é "20010928060000.0 Z".</span><span class="sxs-lookup"><span data-stu-id="70c3f-146">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="70c3f-147">O "Z" indica que não há diferencial de tempo.</span><span class="sxs-lookup"><span data-stu-id="70c3f-147">The "Z" indicates no time differential.</span></span> <span data-ttu-id="70c3f-148">Active Directory armazena data/hora como GMT (hora de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="70c3f-148">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="70c3f-149">Se nenhum diferencial de tempo for especificado, GMT será o padrão.</span><span class="sxs-lookup"><span data-stu-id="70c3f-149">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="70c3f-150">Se o tempo for especificado em um fuso horário diferente de GMT, o diferencial entre o fuso horário e o GMT será acrescentado à cadeia de caracteres em vez de "Z" no formato "AAAAMMDDHHMMSS. 0 \[ +/- \] hhmm".</span><span class="sxs-lookup"><span data-stu-id="70c3f-150">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="70c3f-151">Um exemplo de um valor aceitável é "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="70c3f-151">An example of an acceptable value is "20010928060000.0+0200".</span></span>

<span data-ttu-id="70c3f-152">O diferencial é baseado na fórmula: GMT = local + diferencial.</span><span class="sxs-lookup"><span data-stu-id="70c3f-152">The differential is based on the formula: GMT=Local+differential.</span></span>

## <a name="boolean"></a><span data-ttu-id="70c3f-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="70c3f-153">Boolean</span></span>


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



<span data-ttu-id="70c3f-154">Active Directory aceita apenas um valor de 32 bits assinado para essa sintaxe.</span><span class="sxs-lookup"><span data-stu-id="70c3f-154">Active Directory accepts only a signed 32-bit value for this syntax.</span></span> <span data-ttu-id="70c3f-155">Ele manipula zero como **falso** e todos os valores diferentes de zero como **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="70c3f-155">It handles zero as **FALSE** and all nonzero values as **TRUE**.</span></span>

## <a name="integer"></a><span data-ttu-id="70c3f-156">Integer</span><span class="sxs-lookup"><span data-stu-id="70c3f-156">Integer</span></span>


```VB
Syntax Type: ADSTYPE_INTEGER
```



<span data-ttu-id="70c3f-157">Um valor numérico assinado de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="70c3f-157">A 32-bit signed numeric value.</span></span>

## <a name="large-integer"></a><span data-ttu-id="70c3f-158">Inteiro grande</span><span class="sxs-lookup"><span data-stu-id="70c3f-158">Large Integer</span></span>


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



<span data-ttu-id="70c3f-159">Um valor numérico assinado de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="70c3f-159">A 64-bit signed numeric value.</span></span> <span data-ttu-id="70c3f-160">Inteiros grandes são realmente implementados como objetos COM na interface [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) .</span><span class="sxs-lookup"><span data-stu-id="70c3f-160">Large integers are actually implemented as COM objects on the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface.</span></span> <span data-ttu-id="70c3f-161">Os métodos **HighPart** e **LowPart** são usados para acessar as metades de 2 32 bits do valor inteiro grande.</span><span class="sxs-lookup"><span data-stu-id="70c3f-161">The **HighPart** and **LowPart** methods are used to access the two 32-bit halves of the large integer value.</span></span>

<span data-ttu-id="70c3f-162">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="70c3f-162">Example:</span></span>


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a><span data-ttu-id="70c3f-163">Cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="70c3f-163">Octet String</span></span>


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



<span data-ttu-id="70c3f-164">Uma cadeia de caracteres de octeto é retornada como uma matriz variante de bytes.</span><span class="sxs-lookup"><span data-stu-id="70c3f-164">An octet string is returned as a variant array of bytes.</span></span> <span data-ttu-id="70c3f-165">Isso consiste em uma contagem de tamanho (número de octetos) seguida por uma série de octetos.</span><span class="sxs-lookup"><span data-stu-id="70c3f-165">This consists of a size count (number of octets) followed by a series of octets.</span></span> <span data-ttu-id="70c3f-166">Um octeto é um byte de 8 bits, portanto, uma série de octetos é uma cadeia de caracteres de dados binários.</span><span class="sxs-lookup"><span data-stu-id="70c3f-166">An octet is an 8-bit byte, so a series of octets is a string of binary data.</span></span>

## <a name="object-class"></a><span data-ttu-id="70c3f-167">Classe de objeto</span><span class="sxs-lookup"><span data-stu-id="70c3f-167">Object Class</span></span>


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



<span data-ttu-id="70c3f-168">A classe de objeto é um identificador de objeto exclusivo para uma determinada classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="70c3f-168">Object Class is a unique object identifier for a given schema class.</span></span> <span data-ttu-id="70c3f-169">A classe de cada instância de objeto é identificada pelo atributo **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="70c3f-169">The class of each object instance is identified by the **objectClass** attribute.</span></span> <span data-ttu-id="70c3f-170">Quando criado, você nunca pode alterar uma classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="70c3f-170">When created, you can never change an object class.</span></span> <span data-ttu-id="70c3f-171">**objectClass** é um atributo com vários valores.</span><span class="sxs-lookup"><span data-stu-id="70c3f-171">**objectClass** is a multiple valued attribute.</span></span> <span data-ttu-id="70c3f-172">Ele lista a classe específica do objeto e as classes de todas as classes estruturais ou abstratas das quais a classe específica foi derivada.</span><span class="sxs-lookup"><span data-stu-id="70c3f-172">It lists the specific class of the object, and the classes of all structural or abstract classes from which the specific class was derived.</span></span> <span data-ttu-id="70c3f-173">Isso inclui top, a classe da qual todas as outras classes são derivadas basicamente.</span><span class="sxs-lookup"><span data-stu-id="70c3f-173">This includes Top, the class from which all other classes are ultimately derived.</span></span> <span data-ttu-id="70c3f-174">Active Directory não listar as classes auxiliares no atributo **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="70c3f-174">Active Directory does not list auxiliary classes in the **objectClass** attribute.</span></span>

## <a name="security-descriptor"></a><span data-ttu-id="70c3f-175">Descritor de Segurança</span><span class="sxs-lookup"><span data-stu-id="70c3f-175">Security Descriptor</span></span>


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



<span data-ttu-id="70c3f-176">Os direitos de acesso definem quais capacidades uma entidade de segurança tem ao tentar executar uma operação em um objeto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="70c3f-176">Access rights define what abilities a security principal has when it attempts to perform an operation on an Active Directory object.</span></span> <span data-ttu-id="70c3f-177">Um descritor de segurança descreve as informações de controle de acesso associadas a um objeto.</span><span class="sxs-lookup"><span data-stu-id="70c3f-177">A security descriptor describes the access control information associated with an object.</span></span>

<span data-ttu-id="70c3f-178">O descritor de segurança é armazenado como uma propriedade de um objeto de diretório na propriedade **nTSecurityDescriptor** .</span><span class="sxs-lookup"><span data-stu-id="70c3f-178">The security descriptor is stored as a property of a directory object in the **nTSecurityDescriptor** property.</span></span> <span data-ttu-id="70c3f-179">Quando um usuário autenticado tenta acessar um objeto de diretório, o servidor de diretório determina o acesso concedido ou negado ao usuário com base no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="70c3f-179">When an authenticated user attempts to access a directory object, the directory server determines the access granted or denied to the user based on the object security descriptor.</span></span>

<span data-ttu-id="70c3f-180">A enumeração de [**\_ \_ \_ enumeração de controle SD do ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) especifica sinalizadores de controle para um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="70c3f-180">The [**ADS\_SD\_CONTROL\_ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) enumeration specifies control flags for a security descriptor.</span></span>

<span data-ttu-id="70c3f-181">O exemplo de código a seguir mostra como obter um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="70c3f-181">The following code example shows how to obtain a security descriptor.</span></span>


```VB
' Obtain a security descriptor.
Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim acl as IADsAccessControlList
 
Set x = GetObject("LDAP://DC=Fabrikam, DC=com")
Set sd = x.Get("nTSecurityDescriptor")
 
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Set acl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
```



## <a name="related-topics"></a><span data-ttu-id="70c3f-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70c3f-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70c3f-183">Sintaxes para atributos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="70c3f-183">Syntaxes for Active Directory Attributes</span></span>](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[<span data-ttu-id="70c3f-184">Escolhendo uma sintaxe</span><span class="sxs-lookup"><span data-stu-id="70c3f-184">Choosing a Syntax</span></span>](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[<span data-ttu-id="70c3f-185">Como especificar valores de comparação</span><span class="sxs-lookup"><span data-stu-id="70c3f-185">How to Specify Comparison Values</span></span>](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 