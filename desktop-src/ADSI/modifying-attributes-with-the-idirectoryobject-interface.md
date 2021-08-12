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
ms.openlocfilehash: 30fa7d75d3e0dce489f676dafb36992c95a1cba2e9856bbbaf49f14806a6c1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179024"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Modificando atributos com a interface IDirectoryObject

Além de [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex), você pode usar o método [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) para modificar valores de atributo. Para usar esse método, você deve preencher uma estrutura [**de \_ \_ informações attr de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo a ser modificado.

O método [**IDirectoryObject:: Setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) permite que você modifique os atributos de valor único e de valores múltiplos. Essa função fornece controles operacionais semelhantes, como Clear, acrescente, DELETE e Update, àqueles encontrados no método [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) . As constantes de controle incluem:

-   [**\_atributo attr do ADS \_ Clear**](adsi-attribute-modification-types.md)
-   [**\_atualização de attr ADS \_**](adsi-attribute-modification-types.md)
-   [**\_atributo attr do ADS \_ Append**](adsi-attribute-modification-types.md)
-   [**\_exclusão de attr ADS \_**](adsi-attribute-modification-types.md)

A especificação dos [**ADS \_ \_ atualização attr**](adsi-attribute-modification-types.md) disparará uma operação no lado do servidor que pode usar muitos recursos. Um exemplo seria iniciar a operação para atualizar uma longa lista de associações de grupo. Em geral, evite usar essa operação, a menos que a modificação envolva um pequeno número de atributos no diretório. Para modificar uma longa lista de associações de grupo, a abordagem mais eficiente seria ler a lista do diretório subjacente, fazer modificações e armazenar a lista atualizada de volta no diretório.

> [!Note]  
> Como [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) com [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), as alterações de atributo são completamente confirmadas ou descartadas em Active Directory. Se uma ou mais das modificações não forem permitidas e, portanto, não puderem ser executadas, nenhuma das modificações coletiva feitas nos atributos será confirmada no diretório.

 

## <a name="example"></a>Exemplo

O exemplo de código a seguir mostra como modificar atributos únicos e com vários valores com o método [**IDirectoryObject:: Setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .


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



 

 




