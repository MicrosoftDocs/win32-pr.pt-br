---
title: Recuperando uma coleção
description: Recuperando uma coleção
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517acfa320069f9c94ee291e9215459d27ba25ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917484"
---
# <a name="retrieving-a-collection"></a>Recuperando uma coleção

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

O código a seguir recupera a coleção de clientes para o servidor de políticas de rede.


```C++
// Retrieve the clients collection 
   HRESULT hr;
   CComPtr<ISdo>  pSdo;
   hr = pSdoServiceControl->QueryInterface(
      __uuidof(ISdo),
      (void**) &pSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // First Retrieve the protocols collection
   //
   _variant_t  vtProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection>  pProtocolsCollection;
   hr = vtProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the RADIUS protocol
   //
   CComPtr<IDispatch> pRadiusDispatch;
   _variant_t  vtProtocolName = L"Microsoft Radius Protocol";
   hr = pProtocolsCollection->Item(&vtProtocolName, &pRadiusDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pRadiusSdo;
   hr = pRadiusDispatch->QueryInterface(      
      __uuidof(ISdo), 
      (void **) &pRadiusSdo
   );

   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the clients collection
   //
   _variant_t  vtClientsCollection;
   hr = pRadiusSdo->GetProperty(PROPERTY_RADIUS_CLIENTS_COLLECTION, &vtClientsCollection);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoCollection> pClientsCollection;
   hr = vtClientsCollection.pdispVal->QueryInterface(      
      __uuidof(ISdoCollection), 
      (void **) &pClientsCollection
   );

   if (FAILED(hr))
   {
      return hr;
   }

```



## <a name="remarks"></a>Comentários

A variável pSdoServiceControl contém um ponteiro para um objeto de dados de servidor para NPS. Para obter mais informações, consulte o tópico [recuperando um serviço de SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).

A variável vtClientsCollection é do tipo [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Um \_ \_ objeto Variant t encapsula ou inclui o tipo de dados [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . A classe gerencia a alocação de recursos e a desalocação e faz chamadas de função para [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) e [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) conforme apropriado.

Após a chamada para "pSdo->GetProperty ()", a variável vtProtocolsCollection especifica um objeto. O membro **pdispVal** de vtProtocolsCollection contém um ponteiro para a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para o objeto.

O código de exemplo acima pode ser adaptado para recuperar outras coleções de NPS, por exemplo, as coleções de manipuladores de solicitação do NPS. Os valores enumerados do tipo de enumeração [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) que correspondem às coleções de NPS disponíveis.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[Recuperando um SDO de serviço](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**VARIANTE**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 