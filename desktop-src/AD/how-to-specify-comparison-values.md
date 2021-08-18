---
title: Como especificar valores de comparação
description: Cada tipo de atributo tem uma sintaxe que determina o tipo de valores de comparação que você pode especificar em um filtro de pesquisa para esse atributo.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Como especificar o anúncio de valores de comparação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5babc7d9781895c9671594214e4e036a85ef951cdb4b97ba34d708d160dd8fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188117"
---
# <a name="how-to-specify-comparison-values"></a>Como especificar valores de comparação

Cada tipo de atributo tem uma sintaxe que determina o tipo de valores de comparação que você pode especificar em um filtro de pesquisa para esse atributo.

As seções a seguir descrevem os requisitos para cada sintaxe de atributo. Para obter mais informações sobre sintaxes de atributo, consulte [sintaxes para atributos em Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean
</dt> <dd>

O valor especificado em um filtro deve ser um valor de cadeia de caracteres que seja "verdadeiro" ou "falso". Os exemplos a seguir mostram como especificar uma cadeia de caracteres de comparação booliana.

O exemplo a seguir pesquisará objetos que têm um **showInAdvancedViewOnly** definido como **true**:


```C++
(showInAdvancedViewOnly=TRUE)
```



O exemplo a seguir pesquisará objetos que têm um **showInAdvancedViewOnly** definido como **false**:


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Inteiro e enumeração
</dt> <dd>

O valor especificado em um filtro deve ser um inteiro decimal. Os valores hexadecimais devem ser convertidos em decimal. Uma cadeia de caracteres de comparação de valor usa a seguinte forma:


```C++
<attribute name>:<value>
```



" <attribute name> " é o **lDAPDisplayName** do atributo e "<value>"é o valor a ser usado para comparação.

O exemplo de código a seguir mostra um filtro que pesquisará objetos que têm um valor de **GroupType** igual ao sinalizador **de \_ \_ tipo de \_ grupo \_ do ADS** (8) e o sinalizador de **segurança de tipo de \_ grupo ADS \_ \_ \_ habilitado** (0x80000000). Os dois sinalizadores combinados são iguais a 0x80000008, que é convertido em decimal é 2147483656.


```C++
(groupType=2147483656)
```



Os operadores de regra de correspondência de LDAP também podem ser usados para executar comparações bit a bit. Para obter mais informações sobre regras de correspondência, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax). O exemplo de código a seguir mostra um filtro que pesquisará objetos que têm um **GroupType** com **o \_ tipo de grupo ADS \_ \_ Security \_ Enabled** (0x80000000 = 2147483648) conjunto de bits.


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>Octetstring
</dt> <dd>

O valor especificado em um filtro são os dados a serem encontrados. Os dados devem ser representados como uma cadeia de caracteres de byte codificada de dois caracteres, em que cada byte é precedido por uma barra invertida ( \\ ). Por exemplo, o valor 0x05 será exibido na cadeia de caracteres como " \\ 05".

A função [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) pode ser usada para criar uma representação de cadeia de caracteres codificada de dados binários. A função **ADsEncodeBinaryData** não codifica valores de bytes que representam caracteres alfanuméricos. Em vez disso, coloque o caractere na cadeia de caracteres sem codificá-lo. Isso resulta na cadeia de caracteres que contém uma mistura de caracteres codificados e não codificados. Por exemplo, se os dados binários forem 0x05 \| 0x1A \| 0x1B \| 0x43 \| 0x32, a cadeia de caracteres codificada conterá " \\ 05 \\ 1a \\ 1BC2". Isso não tem efeito sobre o filtro e os filtros de pesquisa funcionarão corretamente com esses tipos de cadeias de caracteres.

Caracteres curinga são aceitos.

O exemplo de código a seguir mostra um filtro que contém uma cadeia de caracteres codificada para **schemaIDGUID** com o valor de GUID de "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>SIDs
</dt> <dd>

O valor especificado em um filtro é a representação de cadeia de caracteres de byte codificada do SID. Para obter mais informações sobre cadeias de caracteres de bytes codificados, consulte a seção anterior neste tópico que discute a sintaxe de Octetstring.

O exemplo de código a seguir mostra um filtro que contém uma cadeia de caracteres codificada para **objectSid** com o valor de cadeia de caracteres Sid de "S-1-5-21-1935655697-308236825-1417001333":


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>IGNORA
</dt> <dd>

O nome distinto inteiro, a ser correspondido, deve ser fornecido.

Caracteres curinga não são aceitos.

Lembre-se de que o atributo **objectCategory** também permite que você especifique o **lDAPDisplayName** da classe definida no atributo.

O exemplo a seguir mostra um filtro que especifica um **membro** que contém "CN = testuser, DC = Fabrikam, DC = com":


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

O valor especificado em um filtro deve ser um inteiro decimal. Converta valores hexadecimais em decimal.

O exemplo de código a seguir mostra um filtro que especifica um **CreationTime** definido como um [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de "1999-12-31 23:59:59 (UTC/GMT)":


```C++
(creationTime=125911583990000000)
```



As funções a seguir criam um filtro de correspondência exata (=) para um atributo inteiro grande e verificam o atributo no esquema e sua sintaxe:


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

<span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>Imenablestring
</dt> <dd>

Atributos com essas sintaxes devem aderir a conjuntos de caracteres específicos. Para obter mais informações, consulte [sintaxes para atributos em Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

No momento, Active Directory Domain Services não impõem esses conjuntos de caracteres.

O valor especificado em um filtro é uma cadeia de caracteres. A comparação diferencia maiúsculas de minúsculas.

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime
</dt> <dd>

O valor especificado em um filtro é uma cadeia de caracteres que representa a data no seguinte formato:


```C++
YYYYMMDDHHMMSS.0Z
```



"0Z" indica que não há diferencial de tempo. Lembre-se de que o servidor Active Directory armazena a data/hora como GMT (hora de Greenwich). Se um diferencial de tempo não for especificado, o padrão será GMT.

Se o fuso horário local não for GMT, use um valor diferencial para especificar o fuso horário local e aplique o diferencial ao GMT. O diferencial é baseado em: GMT = local + diferencial.

Para especificar um diferencial, use:


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



O exemplo a seguir mostra um filtro que especifica um horário de **whenCreated** definido como 3/23/99 8:52:58 PM GMT:


```C++
(whenCreated=19990323205258.0Z)
```



O exemplo a seguir mostra um filtro que especifica um tempo de **whenCreated** definido como 3/23/99 8:52:58 hora padrão da Nova Zelândia (diferencial é + 12 horas):


```C++
(whenCreated=19990323205258.0+1200)
```



O exemplo de código a seguir mostra como calcular o diferencial de fuso horário. A função retorna o diferencial entre o fuso horário local atual e o GMT. O valor retornado é uma cadeia de caracteres no seguinte formato:


```C++
[+/-]HHMM
```



Por exemplo, o horário padrão do Pacífico é-0800.


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

<span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime
</dt> <dd>

O valor especificado em um filtro é uma cadeia de caracteres que representa a data no seguinte formato:


```C++
YYMMDDHHMMSSZ
```



Z indica que não há diferencial de tempo. Lembre-se de que o servidor Active Directory armazena data e hora como hora GMT. Se um diferencial de tempo não for especificado, GMT será o padrão.

O valor de segundos ("SS") é opcional.

Se GMT não for o fuso horário local, aplique um valor diferencial local para especificar o fuso horário local. O diferencial é: GMT = local + diferencial.

Para especificar um diferencial, use o seguinte formato:


```C++
YYMMDDHHMMSS[+/-]HHMM
```



O exemplo a seguir mostra um filtro que especifica um horário de **myTimeAttrib** definido como 3/23/99 8:52:58 PM GMT:


```C++
(myTimeAttrib=990323205258Z)
```



O exemplo a seguir mostra um filtro que especifica um tempo de **myTimeAttrib** definido como 3/23/99 8:52:58 PM sem segundos especificado:


```C++
(myTimeAttrib=9903232052Z)
```



O exemplo a seguir mostra um filtro que especifica um tempo de **myTimeAttrib** definido como 3/23/99 8:52:58 hora padrão da Nova Zelândia (diferencial é 12 horas). Isso é equivalente a 3/23/99 8:52:58 AM GMT.


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>Directorystring
</dt> <dd>

O valor especificado em um filtro é uma cadeia de caracteres. Directorystring pode conter caracteres Unicode. A comparação não diferencia maiúsculas de minúsculas.

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OIDs
</dt> <dd>

O OID inteiro a ser correspondido deve ser fornecido.

Caracteres curinga não são aceitos.

O atributo **objectCategory** permite que você especifique o **lDAPDisplayName** do conjunto de classes para o atributo.

O exemplo a seguir mostra um filtro que especifica **governsID** para a classe de volume:


```C++
(governsID=1.2.840.113556.1.5.36)
```



Dois filtros equivalentes que especificam o atributo **systemMustContain** contendo **uncname**, que tem um OID de 1.2.840.113556.1.4.137:


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Outras sintaxes
</dt> <dd>

As sintaxes a seguir são avaliadas em um filtro semelhante a uma cadeia de caracteres de octeto:

-   ObjectSecurityDescriptor
-   AccessPointDN
-   PresentationAddresses
-   ReplicaLink
-   DNWithString
-   DNWithOctetString
-   ORName

</dd> </dl>

 

 