---
title: Acessando atributos com a interface IDirectoryObject
description: A interface IDirectoryObject fornece um aplicativo cliente escrito em C e C++ com acesso direto aos objetos de serviço de diretório.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Acessando atributos com a interface IDirectoryObject ADSI
- IDirectoryObject ADSI, acessando atributos com
- ADSI ADSI, usando, usando a interface IDirectoryObject para acessar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da62b6a5cf7e1389276475c46faac6455672790
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915925"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a>Acessando atributos com a interface IDirectoryObject

A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornece um aplicativo cliente escrito em C e C++ com acesso direto aos objetos de serviço de diretório. A interface habilita o acesso por meio de um protocolo de rede direto, em vez de pelo cache de atributo ADSI. No lugar das propriedades com suporte pela interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , o **IDirectoryObject** fornece métodos que dão suporte a um subconjunto crítico de métodos de manutenção de um objeto e fornecem acesso a seus atributos. Com o **IDirectoryObject**, um cliente pode obter ou definir qualquer número de atributos de objeto com uma chamada de método. Ao contrário dos métodos de automação correspondentes, que são agrupados em lote, os de **IDirectoryObject** são executados quando chamados. Como os métodos nessa interface não exigem a criação de uma instância de um objeto de diretório de automação, a sobrecarga de desempenho é pequena.

Os clientes escritos em linguagens como C e C++ devem usar os métodos da interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para otimizar o desempenho e aproveitar as interfaces do serviço de diretório nativo. Os clientes de automação não podem usar **IDirectoryObject**. Em vez disso, eles devem usar a interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .

O método [**IDirectoryObject:: Getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) recupera atributos com valores únicos e múltiplos. Esse método usa uma lista de atributos solicitados e retorna uma estrutura de [**\_ \_ informações attr de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) . A ADSI aloca essa estrutura; o chamador deve liberar essa memória quando ela não for mais necessária usando a função [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

A ordem dos valores de atributo retornados não é necessariamente igual à ordem em que os atributos foram solicitados. Portanto, é necessário comparar os nomes de atributo retornados da ADSI.

> [!Note]  
> A estrutura de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) não retorna todos os atributos solicitados. Somente os atributos que contêm valores fazem parte da estrutura retornada.

 

O número de atributos retornados é determinado pelo parâmetro *dwNumberAttributes* passado para o método [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .

O exemplo de código a seguir é associado a um objeto e usa o método [**IDirectoryObject:: Getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar atributos do objeto.


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



 

 




