---
title: Recuperando um objeto de uma coleção
description: Recuperando um objeto de uma coleção
ms.assetid: df7cbff5-2d09-4031-8f41-3f4eea51598f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936cde1b897be9fc9fd7855401fdcef16b0754a59ae726a561acebd4ccd93283
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128556"
---
# <a name="retrieving-an-object-from-a-collection"></a>Recuperando um objeto de uma coleção

O código a seguir recupera o endereço IP de um cliente de uma coleção de clientes. A variável pClientsCollection aponta para uma interface [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) para a coleção. Consulte [Recuperando uma coleção para](/windows/desktop/Nps/sdo-retrieving-a-collection) obter informações sobre como recuperar o objeto de coleção.


```C++
   HRESULT hr
   _variant_t vtClientName = L"Test Client";
   
   //
   // Get the client "Test Client" from the collection of clients
   //
   CComPtr<IDispatch> pFoundClientDispatch;
   hr = pClientsCollection->Item(&vtClientName, &pFoundClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pFoundClientSdo;
   hr = pFoundClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void **) &pFoundClientSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the IP address of that client 
   //
   _variant_t vtAddress;
   hr = pFoundClientSdo->GetProperty(PROPERTY_CLIENT_ADDRESS ,&vtAddress);
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ISdoCollection::Item**](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-item)
</dt> <dt>

[Recuperando uma coleção](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[**Sysallocstring**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[**Sysfreestring**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> <dt>

[**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 