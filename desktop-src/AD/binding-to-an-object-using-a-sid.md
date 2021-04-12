---
title: Associação a um objeto usando um SID
description: No Windows Server 2003, é possível associar a um objeto usando o SID (identificador de segurança do objeto), bem como um GUID. O SID do objeto é armazenado no atributo objectSid. A associação a um SID não funciona no Windows 2000.
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- Associação a um objeto usando um AD do SID
- Active Directory, usando, associação, associação a um objeto usando um SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad4ecf2d6faa385ab8085730e4f1cb0689e403
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453958"
---
# <a name="binding-to-an-object-using-a-sid"></a>Associação a um objeto usando um SID

No Windows Server 2003, é possível associar a um objeto usando o SID (identificador de segurança do objeto), bem como um GUID. O SID do objeto é armazenado no atributo **objectSid** . A associação a um SID não funciona no Windows 2000.

O provedor LDAP para Active Directory Domain Services fornece um método para associar a um objeto usando o SID do objeto. O formato da cadeia de vinculação é:


```C++
LDAP://servername/<SID=XXXXX>
```



Neste exemplo, "servername" é o nome do servidor de diretório e "XXXXX" é a representação de cadeia de caracteres do valor hexadecimal do SID. O "servername" é opcional. A cadeia de caracteres de SID é especificada em um formulário em que cada caractere na cadeia de caracteres é a representação hexadecimal de cada byte do SID. Por exemplo, se a matriz for:


```C++
0xAB 0x14 0xE2
```



a cadeia de vinculação de SID seria " &lt; Sid = AB14E2 &gt; ". A função [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) não deve ser usada para converter a matriz Sid em uma cadeia de caracteres porque ela precede cada caractere de byte com uma barra invertida, que não é um formato de cadeia de vinculação válido.

A cadeia de caracteres de SID também pode assumir o formato " &lt; Sid = S-x-x-XX-xxxxxxxxxx-xxxxxxxxxx-xxxxxxxxx-XXX &gt; ", em que a parte "S-X-x-XX-XXXXXXXXXX-xxxxxxxxxx-xxxxxxxxx-xxx" é igual à cadeia de caracteres retornada pela função [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .

Ao vincular usando o SID do objeto, não há suporte para alguns métodos e propriedades [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) . As seguintes propriedades **IADs** não são suportadas por objetos obtidos pela Associação usando o SID do objeto:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nome**](/windows/desktop/ADSI/iads-property-methods)
-   [**Pai**](/windows/desktop/ADSI/iads-property-methods)

Os objetos **IADsContainer** a seguir não são compatíveis com aqueles obtidos pela Associação usando o SID do objeto:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Criar**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Apagar**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Para usar esses métodos e propriedades após a associação a um objeto usando o SID do objeto, use o método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar o nome diferenciado do objeto e, em seguida, use o nome distinto para associar ao objeto novamente.

O exemplo de código a seguir mostra como converter um **objectSid** em uma cadeia de caracteres vinculável.


```C++
HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes);

/********

    GetSIDBindStringFromVariant()

    Converts a SID in VARIANT form, such as an objectSid value, and 
    converts it into a bindable string in the form:

    LDAP://<SID=xxxxxxx...>

    The returned string is allocated with AllocADsMem and must be 
    freed by the caller with FreeADsMem.

*********/

LPWSTR GetSIDBindStringFromVariant(VARIANT vSID)
{
    LPWSTR pwszReturn = NULL;

    if(VT_ARRAY & vSID.vt) 
    {
        HRESULT hr;
        LPBYTE pByte;
        DWORD dwBytes = 0;

        hr = VariantArrayToBytes(vSID, &pByte, &dwBytes);
        if(S_OK == hr)
        {
            // Convert the BYTE array into a string of hex 
            // characters.
            CComBSTR sbstrTemp = "LDAP://<SID=";

            for(DWORD i = 0; i < dwBytes; i++)
            {
                WCHAR wszByte[3];

                swprintf_s(wszByte, L"%02x", pByte[i]);
                sbstrTemp += wszByte;
            }

            sbstrTemp += ">";
            pwszReturn = 
               (LPWSTR)AllocADsMem((sbstrTemp.Length() + 1) * 
                sizeof(WCHAR));
            if(pwszReturn)
            {
                wcscpy_s(pwszReturn, sbstrTemp.m_str);
            }

            FreeADsMem(pByte);
        }
    }

    return pwszReturn;
}

/*********

    VariantArrayToBytes()

    This function converts a VARIANT array into an array of BYTES. 
    This function allocates the buffer using AllocADsMem. The 
    caller must free this memory with FreeADsMem when it is no 
    longer required.

**********/

HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes)
{
    if(!(Variant.vt & VT_ARRAY) ||
        !Variant.parray ||
        !ppBytes ||
        !pdwBytes)
    {
        return E_INVALIDARG;
    }

    *ppBytes = NULL;
    *pdwBytes = 0;

    HRESULT hr = E_FAIL;
    SAFEARRAY *pArrayVal = NULL;
    CHAR HUGEP *pArray = NULL;
    
    // Retrieve the safe array.
    pArrayVal = Variant.parray;
    DWORD dwBytes = pArrayVal->rgsabound[0].cElements;
    *ppBytes = (LPBYTE)AllocADsMem(dwBytes);
    if(NULL == *ppBytes) 
    {
        return E_OUTOFMEMORY;
    }

    hr = SafeArrayAccessData(pArrayVal, (void HUGEP * FAR *) &pArray);
    if(SUCCEEDED(hr))
    {
        // Copy the bytes to the safe array.
        CopyMemory(*ppBytes, pArray, dwBytes);
        SafeArrayUnaccessData( pArrayVal );
        *pdwBytes = dwBytes;
    }
    
    return hr;
}
```



 

 