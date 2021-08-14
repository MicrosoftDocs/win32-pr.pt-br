---
title: Adicionando um objeto a uma coleção
description: Adicionando um objeto a uma coleção
ms.assetid: fc62698d-0bb9-478c-91cf-9f8fec36dba4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f359df40b864c6dcbc1e251e35661b137990ebb9473a177423fbf18acb43e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362258"
---
# <a name="adding-an-object-to-a-collection"></a>Adicionando um objeto a uma coleção

O código a seguir adiciona uma nova política à coleção de políticas do IAS. A variável pClientsCollection aponta para uma interface [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) para a coleção. Consulte [recuperando uma coleção](/windows/desktop/Nps/sdo-retrieving-a-collection) para obter informações sobre como recuperar o objeto da coleção.


```C++
   HRESULT hr;
   _bstr_t      bstrClientName = L"Test Client";
   VARIANT_BOOL vbNameUnique = VARIANT_FALSE;

   //
   // Check if the new client's name is unique
   //

   hr = pClientsCollection->IsNameUnique(bstrClientName, &vbNameUnique);
   if (FAILED(hr))
   {
      return hr;
   }

   if (VARIANT_FALSE == vbNameUnique)
   {
      //
      // The name is not unique. Handle the error
      //
      return E_FAIL;
   }

   //
   // Name is unique. Add the client.
   //
   CComPtr<IDispatch> pClientDispatch;
   pClientDispatch.p = NULL;
   hr = pClientsCollection->Add(bstrClientName, &pClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pClientSDO;
   hr = pClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void**) &pClientSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Set the address for the client
   //
   _variant_t  vtClientAddress = L"127.0.0.1";
   hr = pClientSDO->PutProperty(PROPERTY_CLIENT_ADDRESS, &vtClientAddress);
   if (FAILED(hr))
   {
      return hr;
   }
       
   //
   // Set the shared secret for the client
   //
   _variant_t  vtClientSecret = L">@U#'6cc='5Ly9O5QKEj2RTJr*fM";
   hr = pClientSDO->PutProperty(PROPERTY_CLIENT_SHARED_SECRET, &vtClientSecret);
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Apply the changes
   //
   hr = pClientSDO->Apply();
   if (FAILED(hr))
   {
      return hr;
   }   
    
   //
   // Refresh the service using a ISdoServiceControl interface retrieved
   // in the code sample "Retrieve a Service SDO"
   //
   hr = pSdoServiceControl->ResetService();
   if (FAILED(hr))
   {
      //
      // If IAS is not installed or is not running then ignore the error
      //  
   }


```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_\_t BSTR](/previous-versions/visualstudio/visual-studio-6.0/aa278286(v=vs.60))
</dt> <dt>

[**ISdoCollection:: Adicionar**](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-add)
</dt> <dt>

[**ISdoCollection::IsNameUnique**](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-isnameunique)
</dt> <dt>

[Recuperando uma coleção](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[**VARIANTE**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 