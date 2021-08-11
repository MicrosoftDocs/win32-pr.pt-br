---
title: Acessando atributos com a interface IDirectoryObject
description: A interface IDirectoryObject fornece um aplicativo cliente escrito em C e C++ com acesso direto a objetos de serviço de diretório.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Acessando atributos com a interface IDirectoryObject ADSI
- IDirectoryObject ADSI , acessando atributos com
- ADSI ADSI , usando a interface IDirectoryObject para acessar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fb7f2b8302c2e92a7e604bdc85389fb78acb24a59e467ca42b8bbd3c6c004e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181535"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a>Acessando atributos com a interface IDirectoryObject

A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornece um aplicativo cliente escrito em C e C++ com acesso direto a objetos de serviço de diretório. A interface permite o acesso por meio de um protocolo de rede direto, em vez de por meio do cache de atributo ADSI. No lugar das propriedades com suporte pela interface [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) **IDirectoryObject** fornece métodos que dão suporte a um subconjunto crítico dos métodos de manutenção de um objeto e fornecem acesso a seus atributos. Com **IDirectoryObject**, um cliente pode obter ou definir qualquer número de atributos de objeto com uma chamada de método. Ao contrário dos métodos de Automação correspondentes, que são em lote, os de **IDirectoryObject** são executados quando chamados. Como os métodos nessa interface não exigem a criação de uma instância de um objeto de diretório de Automação, a sobrecarga de desempenho é pequena.

Os clientes escritos em linguagens como C e C++ devem usar os métodos da interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para otimizar o desempenho e aproveitar as interfaces de serviço do diretório nativo. Os clientes de automação **não podem usar IDirectoryObject.** Em vez disso, eles devem usar a interface [**IADs.**](/windows/desktop/api/Iads/nn-iads-iads)

O [**método IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) recupera atributos com valores individuais e múltiplos. Esse método recebe uma lista de atributos solicitados e retorna uma [**estrutura ADS \_ ATTR \_ INFO.**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) A ADSI aloca essa estrutura; O chamador deve liberar essa memória quando ela não for mais necessária usando a [**função FreeADsMem.**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)

A ordem dos valores de atributo retornados não é necessariamente a mesma que a ordem na qual os atributos foram solicitados. Portanto, é necessário comparar os nomes de atributo retornados da ADSI.

> [!Note]  
> A [**estrutura \_ ADS ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) não retorna todos os atributos solicitados. Somente os atributos que contêm valores fazem parte da estrutura retornada.

 

O número de atributos retornados é determinado pelo parâmetro *dwNumberAttributes* passado para o [**método IDirectoryObject::GetObjectAttributes.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes)

O exemplo de código a seguir se vincula a um objeto e usa o método [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar atributos do objeto.


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




