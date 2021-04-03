---
title: Modificando atributos com a interface IDirectoryObject
description: Além de IADs Put e IADs PutEx, você pode usar o método setobjectattributes do IDirectoryObject para modificar valores de atributo. Para usar esse método, você deve preencher uma estrutura de \_ \_ informações attr de anúncios para cada atributo a ser modificado.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Modificando atributos com a interface IDirectoryObject ADSI
- IDirectoryObject ADSI, usando para modificar atributos
- ADSI ADSI, código de exemplo C/C++, usando IDirectoryObject para modificar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715826d0fc835f3d9ecae914fcc51603883af5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084004"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="214c5-107">Modificando atributos com a interface IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="214c5-107">Modifying Attributes with the IDirectoryObject Interface</span></span>

<span data-ttu-id="214c5-108">Além de [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex), você pode usar o método [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) para modificar valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="214c5-108">In addition to [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex), you can use the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method to modify attribute values.</span></span> <span data-ttu-id="214c5-109">Para usar esse método, você deve preencher uma estrutura [**de \_ \_ informações attr de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="214c5-109">To use this method, you must fill in an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure for each attribute to modify.</span></span>

<span data-ttu-id="214c5-110">O método [**IDirectoryObject:: Setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) permite que você modifique os atributos de valor único e de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="214c5-110">The [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method enables you to modify both single-valued and multi-valued attributes.</span></span> <span data-ttu-id="214c5-111">Essa função fornece controles operacionais semelhantes, como Clear, acrescente, DELETE e Update, àqueles encontrados no método [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="214c5-111">This function provides similar operational controls, such as clear, append, delete, and update, to those found in the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span> <span data-ttu-id="214c5-112">As constantes de controle incluem:</span><span class="sxs-lookup"><span data-stu-id="214c5-112">The control constants include:</span></span>

-   [<span data-ttu-id="214c5-113">**\_atributo attr do ADS \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="214c5-113">**ADS\_ATTR\_CLEAR**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="214c5-114">**\_atualização de attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="214c5-114">**ADS\_ATTR\_UPDATE**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="214c5-115">**\_atributo attr do ADS \_ Append**</span><span class="sxs-lookup"><span data-stu-id="214c5-115">**ADS\_ATTR\_APPEND**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="214c5-116">**\_exclusão de attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="214c5-116">**ADS\_ATTR\_DELETE**</span></span>](adsi-attribute-modification-types.md)

<span data-ttu-id="214c5-117">A especificação dos [**ADS \_ \_ atualização attr**](adsi-attribute-modification-types.md) disparará uma operação no lado do servidor que pode usar muitos recursos.</span><span class="sxs-lookup"><span data-stu-id="214c5-117">Specifying [**ADS\_ATTR\_UPDATE**](adsi-attribute-modification-types.md) will trigger a server side operation that can be resource-intensive.</span></span> <span data-ttu-id="214c5-118">Um exemplo seria iniciar a operação para atualizar uma longa lista de associações de grupo.</span><span class="sxs-lookup"><span data-stu-id="214c5-118">An example would be to initiate the operation to update a long list of group membership.</span></span> <span data-ttu-id="214c5-119">Em geral, evite usar essa operação, a menos que a modificação envolva um pequeno número de atributos no diretório.</span><span class="sxs-lookup"><span data-stu-id="214c5-119">In general, refrain from using this operation unless the modification involves a small number of attributes in the directory.</span></span> <span data-ttu-id="214c5-120">Para modificar uma longa lista de associações de grupo, a abordagem mais eficiente seria ler a lista do diretório subjacente, fazer modificações e armazenar a lista atualizada de volta no diretório.</span><span class="sxs-lookup"><span data-stu-id="214c5-120">To modify a long list of group memberships, the more efficient approach would be to read the list from the underlying directory, make modifications, and store the updated list back to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="214c5-121">Como [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) com [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), as alterações de atributo são completamente confirmadas ou descartadas em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="214c5-121">Like [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) with [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), the attribute changes are either completely committed or discarded in Active Directory.</span></span> <span data-ttu-id="214c5-122">Se uma ou mais das modificações não forem permitidas e, portanto, não puderem ser executadas, nenhuma das modificações coletiva feitas nos atributos será confirmada no diretório.</span><span class="sxs-lookup"><span data-stu-id="214c5-122">If one or more of the modifications are not allowed and therefore not able to be performed, then none of the collective modifications made to the attributes are committed to the directory.</span></span>

 

## <a name="example"></a><span data-ttu-id="214c5-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="214c5-123">Example</span></span>

<span data-ttu-id="214c5-124">O exemplo de código a seguir mostra como modificar atributos únicos e com vários valores com o método [**IDirectoryObject:: Setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="214c5-124">The following code example shows how to modify both single and multi-valued attributes with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span>


```C++
HRESULT hr;
LPCWSTR pwszADsPath = L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com";
IDirectoryObject *pDirObject = NULL;

// Bind to the object.
hr = ADsGetObject(pwszADsPath, IID_IDirectoryObject, (void**)&pDirObject);
if(SUCCEEDED(hr))
{ 
    ADSVALUE adsvFaxNumber;
    ADSVALUE rgadsvOtherTelephones[2];
     
    // Set the new FAX number.
    adsvFaxNumber.dwType = ADSTYPE_CASE_IGNORE_STRING; 
    adsvFaxNumber.CaseIgnoreString = L"425-707-9790";

    // Set the first telephone number.
    rgadsvOtherTelephones[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[0].CaseIgnoreString = L"425-707-9791";

    // Set the second telephone number.
    rgadsvOtherTelephones[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[1].CaseIgnoreString = L"425-707-9792";

    ADS_ATTR_INFO attrInfo[2];

    // Setup the facsimileTelephoneNumber attribute data.
    attrInfo[0].pszAttrName = L"facsimileTelephoneNumber";
    attrInfo[0].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[0].dwADsType = adsvFaxNumber.dwType;
    attrInfo[0].pADsValues = &adsvFaxNumber;
    attrInfo[0].dwNumValues = 1;

    // Setup the otherTelephone attribute data.
    attrInfo[1].pszAttrName = L"otherTelephone";
    attrInfo[1].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[1].dwADsType = rgadsvOtherTelephones[0].dwType;
    attrInfo[1].pADsValues = rgadsvOtherTelephones;
    attrInfo[1].dwNumValues = sizeof(rgadsvOtherTelephones)/sizeof(ADSVALUE);

    DWORD dwReturn;
 
    // Set the new attribute values.
    hr = pDirObject->SetObjectAttributes(attrInfo, 
        sizeof(attrInfo)/sizeof(ADS_ATTR_INFO), 
        &dwReturn);

    pDirObject->Release();
}
```



 

 




