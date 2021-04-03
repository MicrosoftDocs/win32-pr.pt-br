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
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="b6104-106">Acessando atributos com a interface IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="b6104-106">Accessing Attributes With the IDirectoryObject Interface</span></span>

<span data-ttu-id="b6104-107">A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornece um aplicativo cliente escrito em C e C++ com acesso direto aos objetos de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="b6104-107">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface provides a client application written in C and C++ with direct access to directory service objects.</span></span> <span data-ttu-id="b6104-108">A interface habilita o acesso por meio de um protocolo de rede direto, em vez de pelo cache de atributo ADSI.</span><span class="sxs-lookup"><span data-stu-id="b6104-108">The interface enables access by means of a direct network protocol, rather than through the ADSI attribute cache.</span></span> <span data-ttu-id="b6104-109">No lugar das propriedades com suporte pela interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , o **IDirectoryObject** fornece métodos que dão suporte a um subconjunto crítico de métodos de manutenção de um objeto e fornecem acesso a seus atributos.</span><span class="sxs-lookup"><span data-stu-id="b6104-109">In place of the properties supported by the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface, **IDirectoryObject** provides methods that support a critical subset of an object's maintenance methods and provide access to its attributes.</span></span> <span data-ttu-id="b6104-110">Com o **IDirectoryObject**, um cliente pode obter ou definir qualquer número de atributos de objeto com uma chamada de método.</span><span class="sxs-lookup"><span data-stu-id="b6104-110">With **IDirectoryObject**, a client can get or set any number of object attributes with one method call.</span></span> <span data-ttu-id="b6104-111">Ao contrário dos métodos de automação correspondentes, que são agrupados em lote, os de **IDirectoryObject** são executados quando chamados.</span><span class="sxs-lookup"><span data-stu-id="b6104-111">Unlike the corresponding Automation methods, which are batched, those of **IDirectoryObject** are executed when called.</span></span> <span data-ttu-id="b6104-112">Como os métodos nessa interface não exigem a criação de uma instância de um objeto de diretório de automação, a sobrecarga de desempenho é pequena.</span><span class="sxs-lookup"><span data-stu-id="b6104-112">Because methods on this interface do not require creating an instance of an Automation directory object, the performance overhead is small.</span></span>

<span data-ttu-id="b6104-113">Os clientes escritos em linguagens como C e C++ devem usar os métodos da interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para otimizar o desempenho e aproveitar as interfaces do serviço de diretório nativo.</span><span class="sxs-lookup"><span data-stu-id="b6104-113">Clients written in languages such as C and C++ should use the methods of the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface to optimize performance and take advantage of native directory service interfaces.</span></span> <span data-ttu-id="b6104-114">Os clientes de automação não podem usar **IDirectoryObject**.</span><span class="sxs-lookup"><span data-stu-id="b6104-114">Automation clients cannot use **IDirectoryObject**.</span></span> <span data-ttu-id="b6104-115">Em vez disso, eles devem usar a interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="b6104-115">Instead, they should use the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>

<span data-ttu-id="b6104-116">O método [**IDirectoryObject:: Getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) recupera atributos com valores únicos e múltiplos.</span><span class="sxs-lookup"><span data-stu-id="b6104-116">The [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method retrieves attributes with both single and multiple values.</span></span> <span data-ttu-id="b6104-117">Esse método usa uma lista de atributos solicitados e retorna uma estrutura de [**\_ \_ informações attr de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) .</span><span class="sxs-lookup"><span data-stu-id="b6104-117">This method takes a list of requested attributes and returns an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure.</span></span> <span data-ttu-id="b6104-118">A ADSI aloca essa estrutura; o chamador deve liberar essa memória quando ela não for mais necessária usando a função [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="b6104-118">ADSI allocates this structure; the caller must free this memory when it is no longer required using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="b6104-119">A ordem dos valores de atributo retornados não é necessariamente igual à ordem em que os atributos foram solicitados.</span><span class="sxs-lookup"><span data-stu-id="b6104-119">The order of returned attribute values is not necessarily the same as the order in which the attributes were requested.</span></span> <span data-ttu-id="b6104-120">Portanto, é necessário comparar os nomes de atributo retornados da ADSI.</span><span class="sxs-lookup"><span data-stu-id="b6104-120">Therefore, it is necessary to compare the attribute names returned from ADSI.</span></span>

> [!Note]  
> <span data-ttu-id="b6104-121">A estrutura de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) não retorna todos os atributos solicitados.</span><span class="sxs-lookup"><span data-stu-id="b6104-121">The [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure does not return all of the attributes requested.</span></span> <span data-ttu-id="b6104-122">Somente os atributos que contêm valores fazem parte da estrutura retornada.</span><span class="sxs-lookup"><span data-stu-id="b6104-122">Only those attributes that contain values are part of the returned structure.</span></span>

 

<span data-ttu-id="b6104-123">O número de atributos retornados é determinado pelo parâmetro *dwNumberAttributes* passado para o método [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="b6104-123">The number of attributes returned is determined by the *dwNumberAttributes* parameter passed to the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>

<span data-ttu-id="b6104-124">O exemplo de código a seguir é associado a um objeto e usa o método [**IDirectoryObject:: Getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar atributos do objeto.</span><span class="sxs-lookup"><span data-stu-id="b6104-124">The following code example binds to an object and uses the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve attributes of the object.</span></span>


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



 

 




