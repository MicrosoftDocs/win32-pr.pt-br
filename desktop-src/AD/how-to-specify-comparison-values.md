---
title: Como especificar valores de comparação
description: Cada tipo de atributo tem uma sintaxe que determina o tipo de valores de comparação que você pode especificar em um filtro de pesquisa para esse atributo.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Como especificar o anúncio de valores de comparação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f9355bc4853fa6dc62645e1c241d8e26f731f9
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640397"
---
# <a name="how-to-specify-comparison-values"></a><span data-ttu-id="a6ea3-104">Como especificar valores de comparação</span><span class="sxs-lookup"><span data-stu-id="a6ea3-104">How to Specify Comparison Values</span></span>

<span data-ttu-id="a6ea3-105">Cada tipo de atributo tem uma sintaxe que determina o tipo de valores de comparação que você pode especificar em um filtro de pesquisa para esse atributo.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-105">Each attribute type has a syntax that determines the type of comparison values that you can specify in a search filter for that attribute.</span></span>

<span data-ttu-id="a6ea3-106">As seções a seguir descrevem os requisitos para cada sintaxe de atributo.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-106">The following sections describe requirements for each attribute syntax.</span></span> <span data-ttu-id="a6ea3-107">Para obter mais informações sobre sintaxes de atributo, consulte [sintaxes para atributos em Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="a6ea3-107">For more information about attribute syntaxes, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<dl> <dt>

<span data-ttu-id="a6ea3-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span><span class="sxs-lookup"><span data-stu-id="a6ea3-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-109">O valor especificado em um filtro deve ser um valor de cadeia de caracteres que seja "verdadeiro" ou "falso".</span><span class="sxs-lookup"><span data-stu-id="a6ea3-109">The value specified in a filter must be a string value that is either "TRUE" or "FALSE".</span></span> <span data-ttu-id="a6ea3-110">Os exemplos a seguir mostram como especificar uma cadeia de caracteres de comparação booliana.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-110">The following examples show how to specify a Boolean comparison string.</span></span>

<span data-ttu-id="a6ea3-111">O exemplo a seguir pesquisará objetos que têm um **showInAdvancedViewOnly** definido como **true**:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-111">The following example will search for objects that have a **showInAdvancedViewOnly** set to **TRUE**:</span></span>


```C++
(showInAdvancedViewOnly=TRUE)
```



<span data-ttu-id="a6ea3-112">O exemplo a seguir pesquisará objetos que têm um **showInAdvancedViewOnly** definido como **false**:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-112">The following example will search for objects that have a **showInAdvancedViewOnly** set to **FALSE**:</span></span>


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span data-ttu-id="a6ea3-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Inteiro e enumeração</span><span class="sxs-lookup"><span data-stu-id="a6ea3-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer and Enumeration</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-114">O valor especificado em um filtro deve ser um inteiro decimal.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-114">The value specified in a filter must be a decimal Integer.</span></span> <span data-ttu-id="a6ea3-115">Os valores hexadecimais devem ser convertidos em decimal.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-115">Hexadecimal values must be converted to decimal.</span></span> <span data-ttu-id="a6ea3-116">Uma cadeia de caracteres de comparação de valor usa a seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-116">A value comparison string takes the following form:</span></span>


```C++
<attribute name>:<value>
```



<span data-ttu-id="a6ea3-117">" <attribute name> " é o **lDAPDisplayName** do atributo e "</span><span class="sxs-lookup"><span data-stu-id="a6ea3-117">"<attribute name>" is the **lDAPDisplayName** of the attribute and "</span></span><value><span data-ttu-id="a6ea3-118">"é o valor a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-118">" is the value to use for comparison.</span></span>

<span data-ttu-id="a6ea3-119">O exemplo de código a seguir mostra um filtro que pesquisará objetos que têm um valor de **GroupType** igual ao sinalizador **de \_ \_ tipo de \_ grupo \_ do ADS** (8) e o sinalizador de **segurança de tipo de \_ grupo ADS \_ \_ \_ habilitado** (0x80000000).</span><span class="sxs-lookup"><span data-stu-id="a6ea3-119">The following code example shows a filter that will search for objects that have a **groupType** value that is equal to the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** (8) flag and the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000) flag.</span></span> <span data-ttu-id="a6ea3-120">Os dois sinalizadores combinados são iguais a 0x80000008, que é convertido em decimal é 2147483656.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-120">The two flags combined equal 0x80000008, which converted to decimal is 2147483656.</span></span>


```C++
(groupType=2147483656)
```



<span data-ttu-id="a6ea3-121">Os operadores de regra de correspondência de LDAP também podem ser usados para executar comparações bit a bit.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-121">The LDAP matching rule operators can also be used to perform bitwise comparisons.</span></span> <span data-ttu-id="a6ea3-122">Para obter mais informações sobre regras de correspondência, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="a6ea3-122">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span> <span data-ttu-id="a6ea3-123">O exemplo de código a seguir mostra um filtro que pesquisará objetos que têm um **GroupType** com **o \_ tipo de grupo ADS \_ \_ Security \_ Enabled** (0x80000000 = 2147483648) conjunto de bits.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-123">The following code example shows a filter that will search for objects that have a **groupType** with the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) bit set.</span></span>


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span data-ttu-id="a6ea3-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>Octetstring</span><span class="sxs-lookup"><span data-stu-id="a6ea3-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-125">O valor especificado em um filtro são os dados a serem encontrados.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-125">The value specified in a filter is the data to be found.</span></span> <span data-ttu-id="a6ea3-126">Os dados devem ser representados como uma cadeia de caracteres de byte codificada de dois caracteres, em que cada byte é precedido por uma barra invertida ( \) .</span><span class="sxs-lookup"><span data-stu-id="a6ea3-126">The data must be represented as a two character encoded byte string where each byte is preceded by a backslash (\).</span></span> <span data-ttu-id="a6ea3-127">Por exemplo, o valor 0x05 será exibido na cadeia de caracteres como " \\ 05".</span><span class="sxs-lookup"><span data-stu-id="a6ea3-127">For example, the value 0x05 will appear in the string as "\\05".</span></span>

<span data-ttu-id="a6ea3-128">A função [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) pode ser usada para criar uma representação de cadeia de caracteres codificada de dados binários.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-128">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function can be used to create an encoded string representation of binary data.</span></span> <span data-ttu-id="a6ea3-129">A função **ADsEncodeBinaryData** não codifica valores de bytes que representam caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-129">The **ADsEncodeBinaryData** function does not encode byte values that represent alpha-numeric characters.</span></span> <span data-ttu-id="a6ea3-130">Em vez disso, coloque o caractere na cadeia de caracteres sem codificá-lo.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-130">It will, instead, place the character into the string without encoding it.</span></span> <span data-ttu-id="a6ea3-131">Isso resulta na cadeia de caracteres que contém uma mistura de caracteres codificados e não codificados.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-131">This results in the string containing a mixture of encoded and unencoded characters.</span></span> <span data-ttu-id="a6ea3-132">Por exemplo, se os dados binários forem 0x05 \| 0x1A \| 0x1B \| 0x43 \| 0x32, a cadeia de caracteres codificada conterá " \\ 05 \\ 1a \\ 1BC2".</span><span class="sxs-lookup"><span data-stu-id="a6ea3-132">For example, if the binary data is 0x05\|0x1A\|0x1B\|0x43\|0x32, the encoded string will contain "\\05\\1A\\1BC2".</span></span> <span data-ttu-id="a6ea3-133">Isso não tem efeito sobre o filtro e os filtros de pesquisa funcionarão corretamente com esses tipos de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-133">This has no effect on the filter and the search filters will work correctly with these types of strings.</span></span>

<span data-ttu-id="a6ea3-134">Caracteres curinga são aceitos.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-134">Wildcards are accepted.</span></span>

<span data-ttu-id="a6ea3-135">O exemplo de código a seguir mostra um filtro que contém uma cadeia de caracteres codificada para **schemaIDGUID** com o valor de GUID de "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span><span class="sxs-lookup"><span data-stu-id="a6ea3-135">The following code example shows a filter that contains encoded string for **schemaIDGUID** with GUID value of "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span></span>


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span data-ttu-id="a6ea3-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>SIDs</span><span class="sxs-lookup"><span data-stu-id="a6ea3-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-137">O valor especificado em um filtro é a representação de cadeia de caracteres de byte codificada do SID.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-137">The value specified in a filter is the encoded byte string representation of the SID.</span></span> <span data-ttu-id="a6ea3-138">Para obter mais informações sobre cadeias de caracteres de bytes codificados, consulte a seção anterior neste tópico que discute a sintaxe de Octetstring.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-138">For more information about encoded byte strings, see the previous section in this topic which discusses OctetString syntax.</span></span>

<span data-ttu-id="a6ea3-139">O exemplo de código a seguir mostra um filtro que contém uma cadeia de caracteres codificada para **objectSid** com o valor de cadeia de caracteres Sid de "S-1-5-21-1935655697-308236825-1417001333":</span><span class="sxs-lookup"><span data-stu-id="a6ea3-139">The following code example shows a filter that contains an encoded string for **objectSid** with SID string value of "S-1-5-21-1935655697-308236825-1417001333":</span></span>


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span data-ttu-id="a6ea3-140"><span id="DN"></span><span id="dn"></span>IGNORA</span><span class="sxs-lookup"><span data-stu-id="a6ea3-140"><span id="DN"></span><span id="dn"></span>DN</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-141">O nome distinto inteiro, a ser correspondido, deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-141">The entire distinguished name, to be matched, must be supplied.</span></span>

<span data-ttu-id="a6ea3-142">Caracteres curinga não são aceitos.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-142">Wildcards are not accepted.</span></span>

<span data-ttu-id="a6ea3-143">Lembre-se de que o atributo **objectCategory** também permite que você especifique o **lDAPDisplayName** da classe definida no atributo.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-143">Be aware that the **objectCategory** attribute also enables you to specify the **lDAPDisplayName** of the class set on the attribute.</span></span>

<span data-ttu-id="a6ea3-144">O exemplo a seguir mostra um filtro que especifica um **membro** que contém "CN = testuser, DC = Fabrikam, DC = com":</span><span class="sxs-lookup"><span data-stu-id="a6ea3-144">The following example shows a filter that specifies a **member** that contains "CN=TestUser,DC=Fabrikam,DC=COM":</span></span>


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span data-ttu-id="a6ea3-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span><span class="sxs-lookup"><span data-stu-id="a6ea3-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-146">O valor especificado em um filtro deve ser um inteiro decimal.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-146">The value specified in a filter must be a decimal integer.</span></span> <span data-ttu-id="a6ea3-147">Converta valores hexadecimais em decimal.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-147">Convert hexadecimal values to decimal.</span></span>

<span data-ttu-id="a6ea3-148">O exemplo de código a seguir mostra um filtro que especifica um **CreationTime** definido como um [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de "1999-12-31 23:59:59 (UTC/GMT)":</span><span class="sxs-lookup"><span data-stu-id="a6ea3-148">The following code example shows a filter that specifies a **creationTime** set to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) of "1999-12-31 23:59:59 (UTC/GMT)":</span></span>


```C++
(creationTime=125911583990000000)
```



<span data-ttu-id="a6ea3-149">As funções a seguir criam um filtro de correspondência exata (=) para um atributo inteiro grande e verificam o atributo no esquema e sua sintaxe:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-149">The following functions create an exact match (=) filter for a large integer attribute and verify the attribute in the schema and its syntax:</span></span>


```C++
//***************************************************************************
//
//  CheckAttribute()
//
//***************************************************************************

HRESULT CheckAttribute(LPOLESTR szAttribute, LPOLESTR szSyntax)
{
    HRESULT hr = E_FAIL;
    BSTR bstr;
    IADsProperty *pObject = NULL;
    LPWSTR szPrefix = L"LDAP://schema/";
    LPWSTR szPath;
     
    if((!szAttribute) || (!szSyntax))
    {
        return E_POINTER;
    }

    // Allocate a buffer large enough to hold the ADsPath of the attribute.
    szPath = new WCHAR[lstrlenW(szPrefix) + lstrlenW(szAttribute) + 1];
    if(NULL == szPath)
    {
        return E_OUTOFMEMORY;
    }
     
    // Create the ADsPath of the attribute.
    wcscpy_s(szPath, szPrefix);
    wcscat_s(szPath, szAttribute);

    hr = ADsOpenObject( szPath,
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsProperty,
                        (void**)&pObject);
    if(SUCCEEDED(hr)) 
    {
        hr = pObject->get_Syntax(&bstr);
        if (SUCCEEDED(hr)) 
        {
            if (0==lstrcmpiW(bstr, szSyntax)) 
            {
                hr = S_OK;
            }
            else
            {
                hr = S_FALSE;
            }
        }

        SysFreeString(bstr);
    }
    
    if(pObject)
    {
        pObject->Release();
    }

    delete szPath;
    
    return hr;
}

//***************************************************************************
//
//  CreateExactMatchFilterLargeInteger()
//
//***************************************************************************

HRESULT CreateExactMatchFilterLargeInteger( LPOLESTR szAttribute, 
                                            INT64 liValue, 
                                            LPOLESTR *pszFilter)
{
    HRESULT hr = E_FAIL;
     
    if ((!szAttribute) || (!pszFilter))
    {
        return E_POINTER;
    }
     
    // Verify that the attribute exists and has 
    // Integer8 (Large Integer) syntax.
     
    hr = CheckAttribute(szAttribute, L"Integer8");
    if (S_OK == hr) 
    {
        LPWSTR szFormat = L"%s=%I64d";
        LPWSTR szTempFilter = new WCHAR[lstrlenW(szFormat) + lstrlenW(szAttribute) + 20 + 1];

        if(NULL == szTempFilter)
        {
            return E_OUTOFMEMORY;
        }
        
        swprintf_s(szTempFilter, L"%s=%I64d", szAttribute, liValue);
     
        // Allocate buffer for the filter string.
        // Caller must free the buffer using CoTaskMemFree.
        *pszFilter = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (lstrlenW(szTempFilter) + 1));
        if (*pszFilter) 
        {
            wcscpy_s(*pszFilter, szTempFilter);
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        delete szTempFilter;
    }

    return hr;
}
```



</dd> <dt>

<span data-ttu-id="a6ea3-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>Imenablestring</span><span class="sxs-lookup"><span data-stu-id="a6ea3-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-151">Atributos com essas sintaxes devem aderir a conjuntos de caracteres específicos.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-151">Attributes with these syntaxes should adhere to specific character sets.</span></span> <span data-ttu-id="a6ea3-152">Para obter mais informações, consulte [sintaxes para atributos em Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="a6ea3-152">For more information, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="a6ea3-153">No momento, Active Directory Domain Services não impõem esses conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-153">Currently, Active Directory Domain Services do not enforce those character sets.</span></span>

<span data-ttu-id="a6ea3-154">O valor especificado em um filtro é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-154">The value specified in a filter is a string.</span></span> <span data-ttu-id="a6ea3-155">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-155">The comparison is case-sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="a6ea3-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span><span class="sxs-lookup"><span data-stu-id="a6ea3-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-157">O valor especificado em um filtro é uma cadeia de caracteres que representa a data no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-157">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYYYMMDDHHMMSS.0Z
```



<span data-ttu-id="a6ea3-158">"0Z" indica que não há diferencial de tempo.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-158">"0Z" indicates no time differential.</span></span> <span data-ttu-id="a6ea3-159">Lembre-se de que o servidor Active Directory armazena a data/hora como GMT (hora de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="a6ea3-159">Be aware that the Active Directory server stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="a6ea3-160">Se um diferencial de tempo não for especificado, o padrão será GMT.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-160">If a time differential is not specified, the default is GMT.</span></span>

<span data-ttu-id="a6ea3-161">Se o fuso horário local não for GMT, use um valor diferencial para especificar o fuso horário local e aplique o diferencial ao GMT.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-161">If the local time zone is not GMT, use a differential value to specify your local time zone and apply the differential to GMT.</span></span> <span data-ttu-id="a6ea3-162">O diferencial é baseado em: GMT = local + diferencial.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-162">The differential is based on: GMT=Local+differential.</span></span>

<span data-ttu-id="a6ea3-163">Para especificar um diferencial, use:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-163">To specify a differential, use:</span></span>


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



<span data-ttu-id="a6ea3-164">O exemplo a seguir mostra um filtro que especifica um horário de **whenCreated** definido como 3/23/99 8:52:58 PM GMT:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-164">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(whenCreated=19990323205258.0Z)
```



<span data-ttu-id="a6ea3-165">O exemplo a seguir mostra um filtro que especifica um tempo de **whenCreated** definido como 3/23/99 8:52:58 hora padrão da Nova Zelândia (diferencial é + 12 horas):</span><span class="sxs-lookup"><span data-stu-id="a6ea3-165">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is +12 hours):</span></span>


```C++
(whenCreated=19990323205258.0+1200)
```



<span data-ttu-id="a6ea3-166">O exemplo de código a seguir mostra como calcular o diferencial de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-166">The following code example shows how to calculate time zone differential.</span></span> <span data-ttu-id="a6ea3-167">A função retorna o diferencial entre o fuso horário local atual e o GMT.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-167">The function returns the differential between the current local time zone and GMT.</span></span> <span data-ttu-id="a6ea3-168">O valor retornado é uma cadeia de caracteres no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-168">The value returned is a string in the following format:</span></span>


```C++
[+/-]HHMM
```



<span data-ttu-id="a6ea3-169">Por exemplo, o horário padrão do Pacífico é-0800.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-169">For example, Pacific Standard Time is -0800.</span></span>


```C++
//***************************************************************************
//
//  GetLocalTimeZoneDifferential()
//
//***************************************************************************

HRESULT GetLocalTimeZoneDifferential(LPOLESTR *pszDifferential)
{
    if(NULL == pszDifferential)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    DWORD dwReturn;
    TIME_ZONE_INFORMATION timezoneinfo;
    LONG lTimeDifferential;
    LONG lHours;
    LONG lMinutes;
    
    dwReturn  = GetTimeZoneInformation(&timezoneinfo);

    switch (dwReturn)
    {
    case TIME_ZONE_ID_STANDARD:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.StandardBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;

        hr = S_OK;
        break;

    case TIME_ZONE_ID_DAYLIGHT:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.DaylightBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        // Apply the additive inverse.
        // Bias is based on GMT=Local+Bias.
        // A differential, based on GMT=Local-Bias, is required.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;
        
        hr = S_OK;
        break;

    case TIME_ZONE_ID_INVALID:
    default:
        hr = E_FAIL;
        break;
    }
     
    if (SUCCEEDED(hr))
    {
        // The caller must free the memory using CoTaskMemFree.
        *pszDifferential = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (3 + 2 + 1));
        if (*pszDifferential)
        {
            swprintf_s(*pszDifferential, L"%+03d%02d", lHours, lMinutes);
            
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
     
    return hr;
}
```



</dd> <dt>

<span data-ttu-id="a6ea3-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span><span class="sxs-lookup"><span data-stu-id="a6ea3-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-171">O valor especificado em um filtro é uma cadeia de caracteres que representa a data no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-171">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYMMDDHHMMSSZ
```



<span data-ttu-id="a6ea3-172">Z indica que não há diferencial de tempo.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-172">Z indicates no time differential.</span></span> <span data-ttu-id="a6ea3-173">Lembre-se de que o servidor Active Directory armazena data e hora como hora GMT.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-173">Be aware that the Active Directory server stores date and time as GMT time.</span></span> <span data-ttu-id="a6ea3-174">Se um diferencial de tempo não for especificado, GMT será o padrão.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-174">If a time differential is not specified, GMT is the default.</span></span>

<span data-ttu-id="a6ea3-175">O valor de segundos ("SS") é opcional.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-175">The seconds value ("SS") is optional.</span></span>

<span data-ttu-id="a6ea3-176">Se GMT não for o fuso horário local, aplique um valor diferencial local para especificar o fuso horário local.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-176">If GMT is not the local time zone, apply a local differential value to specify your local time zone.</span></span> <span data-ttu-id="a6ea3-177">O diferencial é: GMT = local + diferencial.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-177">The differential is: GMT=Local+differential.</span></span>

<span data-ttu-id="a6ea3-178">Para especificar um diferencial, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-178">To specify a differential, use the following form:</span></span>


```C++
YYMMDDHHMMSS[+/-]HHMM
```



<span data-ttu-id="a6ea3-179">O exemplo a seguir mostra um filtro que especifica um horário de **myTimeAttrib** definido como 3/23/99 8:52:58 PM GMT:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-179">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(myTimeAttrib=990323205258Z)
```



<span data-ttu-id="a6ea3-180">O exemplo a seguir mostra um filtro que especifica um tempo de **myTimeAttrib** definido como 3/23/99 8:52:58 PM sem segundos especificado:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-180">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM without seconds specified:</span></span>


```C++
(myTimeAttrib=9903232052Z)
```



<span data-ttu-id="a6ea3-181">O exemplo a seguir mostra um filtro que especifica um tempo de **myTimeAttrib** definido como 3/23/99 8:52:58 hora padrão da Nova Zelândia (diferencial é 12 horas).</span><span class="sxs-lookup"><span data-stu-id="a6ea3-181">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is 12 hours).</span></span> <span data-ttu-id="a6ea3-182">Isso é equivalente a 3/23/99 8:52:58 AM GMT.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-182">This is equivalent to 3/23/99 8:52:58 AM GMT.</span></span>


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span data-ttu-id="a6ea3-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>Directorystring</span><span class="sxs-lookup"><span data-stu-id="a6ea3-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-184">O valor especificado em um filtro é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-184">The value specified in a filter is a string.</span></span> <span data-ttu-id="a6ea3-185">Directorystring pode conter caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-185">DirectoryString can contain Unicode characters.</span></span> <span data-ttu-id="a6ea3-186">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-186">The comparison is case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="a6ea3-187"><span id="OID"></span><span id="oid"></span>OIDs</span><span class="sxs-lookup"><span data-stu-id="a6ea3-187"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-188">O OID inteiro a ser correspondido deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-188">The entire OID to be matched must be supplied.</span></span>

<span data-ttu-id="a6ea3-189">Caracteres curinga não são aceitos.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-189">Wildcards are not accepted.</span></span>

<span data-ttu-id="a6ea3-190">O atributo **objectCategory** permite que você especifique o **lDAPDisplayName** do conjunto de classes para o atributo.</span><span class="sxs-lookup"><span data-stu-id="a6ea3-190">The **objectCategory** attribute enables you to specify the **lDAPDisplayName** of the class set for the attribute.</span></span>

<span data-ttu-id="a6ea3-191">O exemplo a seguir mostra um filtro que especifica **governsID** para a classe de volume:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-191">The following example shows a filter that specifies **governsID** for volume class:</span></span>


```C++
(governsID=1.2.840.113556.1.5.36)
```



<span data-ttu-id="a6ea3-192">Dois filtros equivalentes que especificam o atributo **systemMustContain** contendo **uncname**, que tem um OID de 1.2.840.113556.1.4.137:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-192">Two equivalent filters that specifies **systemMustContain** attribute containing **uNCName**, which has an OID of 1.2.840.113556.1.4.137:</span></span>


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span data-ttu-id="a6ea3-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Outras sintaxes</span><span class="sxs-lookup"><span data-stu-id="a6ea3-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Other Syntaxes</span></span>
</dt> <dd>

<span data-ttu-id="a6ea3-194">As sintaxes a seguir são avaliadas em um filtro semelhante a uma cadeia de caracteres de octeto:</span><span class="sxs-lookup"><span data-stu-id="a6ea3-194">The following syntaxes are evaluated in a filter similar to an octet string:</span></span>

-   <span data-ttu-id="a6ea3-195">ObjectSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="a6ea3-195">ObjectSecurityDescriptor</span></span>
-   <span data-ttu-id="a6ea3-196">AccessPointDN</span><span class="sxs-lookup"><span data-stu-id="a6ea3-196">AccessPointDN</span></span>
-   <span data-ttu-id="a6ea3-197">PresentationAddresses</span><span class="sxs-lookup"><span data-stu-id="a6ea3-197">PresentationAddresses</span></span>
-   <span data-ttu-id="a6ea3-198">ReplicaLink</span><span class="sxs-lookup"><span data-stu-id="a6ea3-198">ReplicaLink</span></span>
-   <span data-ttu-id="a6ea3-199">DNWithString</span><span class="sxs-lookup"><span data-stu-id="a6ea3-199">DNWithString</span></span>
-   <span data-ttu-id="a6ea3-200">DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="a6ea3-200">DNWithOctetString</span></span>
-   <span data-ttu-id="a6ea3-201">ORName</span><span class="sxs-lookup"><span data-stu-id="a6ea3-201">ORName</span></span>

</dd> </dl>

 

 