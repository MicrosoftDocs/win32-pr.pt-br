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
# <a name="binding-to-an-object-using-a-sid"></a><span data-ttu-id="93afe-107">Associação a um objeto usando um SID</span><span class="sxs-lookup"><span data-stu-id="93afe-107">Binding to an Object Using a SID</span></span>

<span data-ttu-id="93afe-108">No Windows Server 2003, é possível associar a um objeto usando o SID (identificador de segurança do objeto), bem como um GUID.</span><span class="sxs-lookup"><span data-stu-id="93afe-108">In Windows Server 2003, it is possible to bind to an object using the object Security Identifier (SID) as well as a GUID.</span></span> <span data-ttu-id="93afe-109">O SID do objeto é armazenado no atributo **objectSid** .</span><span class="sxs-lookup"><span data-stu-id="93afe-109">The object SID is stored in the **objectSID** attribute.</span></span> <span data-ttu-id="93afe-110">A associação a um SID não funciona no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="93afe-110">Binding to an SID does not work on Windows 2000.</span></span>

<span data-ttu-id="93afe-111">O provedor LDAP para Active Directory Domain Services fornece um método para associar a um objeto usando o SID do objeto.</span><span class="sxs-lookup"><span data-stu-id="93afe-111">The LDAP provider for Active Directory Domain Services provides a method to bind to an object using the object SID.</span></span> <span data-ttu-id="93afe-112">O formato da cadeia de vinculação é:</span><span class="sxs-lookup"><span data-stu-id="93afe-112">The binding string format is:</span></span>


```C++
LDAP://servername/<SID=XXXXX>
```



<span data-ttu-id="93afe-113">Neste exemplo, "servername" é o nome do servidor de diretório e "XXXXX" é a representação de cadeia de caracteres do valor hexadecimal do SID.</span><span class="sxs-lookup"><span data-stu-id="93afe-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the SID.</span></span> <span data-ttu-id="93afe-114">O "servername" é opcional.</span><span class="sxs-lookup"><span data-stu-id="93afe-114">The "servername" is optional.</span></span> <span data-ttu-id="93afe-115">A cadeia de caracteres de SID é especificada em um formulário em que cada caractere na cadeia de caracteres é a representação hexadecimal de cada byte do SID.</span><span class="sxs-lookup"><span data-stu-id="93afe-115">The SID string is specified in a form where each character in the string is the hexadecimal representation of each byte of the SID.</span></span> <span data-ttu-id="93afe-116">Por exemplo, se a matriz for:</span><span class="sxs-lookup"><span data-stu-id="93afe-116">For example, if the array is:</span></span>


```C++
0xAB 0x14 0xE2
```



<span data-ttu-id="93afe-117">a cadeia de vinculação de SID seria " &lt; Sid = AB14E2 &gt; ".</span><span class="sxs-lookup"><span data-stu-id="93afe-117">the SID binding string would be "&lt;SID=AB14E2&gt;".</span></span> <span data-ttu-id="93afe-118">A função [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) não deve ser usada para converter a matriz Sid em uma cadeia de caracteres porque ela precede cada caractere de byte com uma barra invertida, que não é um formato de cadeia de vinculação válido.</span><span class="sxs-lookup"><span data-stu-id="93afe-118">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function should not be used to convert the SID array into a string because it precedes each byte character with a backslash, which is not a valid bind string format.</span></span>

<span data-ttu-id="93afe-119">A cadeia de caracteres de SID também pode assumir o formato " &lt; Sid = S-x-x-XX-xxxxxxxxxx-xxxxxxxxxx-xxxxxxxxx-XXX &gt; ", em que a parte "S-X-x-XX-XXXXXXXXXX-xxxxxxxxxx-xxxxxxxxx-xxx" é igual à cadeia de caracteres retornada pela função [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .</span><span class="sxs-lookup"><span data-stu-id="93afe-119">The SID string can also take the form "&lt;SID=S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX&gt;", where the "S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX" portion is the same as the string returned by the [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) function.</span></span>

<span data-ttu-id="93afe-120">Ao vincular usando o SID do objeto, não há suporte para alguns métodos e propriedades [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="93afe-120">When binding using the object SID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="93afe-121">As seguintes propriedades **IADs** não são suportadas por objetos obtidos pela Associação usando o SID do objeto:</span><span class="sxs-lookup"><span data-stu-id="93afe-121">The following **IADs** properties are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="93afe-122">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="93afe-122">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="93afe-123">**Nome**</span><span class="sxs-lookup"><span data-stu-id="93afe-123">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="93afe-124">**Pai**</span><span class="sxs-lookup"><span data-stu-id="93afe-124">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="93afe-125">Os objetos **IADsContainer** a seguir não são compatíveis com aqueles obtidos pela Associação usando o SID do objeto:</span><span class="sxs-lookup"><span data-stu-id="93afe-125">The following **IADsContainer** methods are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="93afe-126">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="93afe-126">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="93afe-127">**Criar**</span><span class="sxs-lookup"><span data-stu-id="93afe-127">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="93afe-128">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="93afe-128">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="93afe-129">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="93afe-129">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="93afe-130">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="93afe-130">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="93afe-131">Para usar esses métodos e propriedades após a associação a um objeto usando o SID do objeto, use o método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar o nome diferenciado do objeto e, em seguida, use o nome distinto para associar ao objeto novamente.</span><span class="sxs-lookup"><span data-stu-id="93afe-131">To use these methods and properties after binding to an object using the object SID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="93afe-132">O exemplo de código a seguir mostra como converter um **objectSid** em uma cadeia de caracteres vinculável.</span><span class="sxs-lookup"><span data-stu-id="93afe-132">The following code example shows how to convert an **objectSid** into a bindable string.</span></span>


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



 

 