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
# <a name="retrieving-a-collection"></a><span data-ttu-id="d35f1-103">Recuperando uma coleção</span><span class="sxs-lookup"><span data-stu-id="d35f1-103">Retrieving a Collection</span></span>

> [!Note]  
> <span data-ttu-id="d35f1-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d35f1-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="d35f1-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="d35f1-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="d35f1-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="d35f1-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="d35f1-107">O código a seguir recupera a coleção de clientes para o servidor de políticas de rede.</span><span class="sxs-lookup"><span data-stu-id="d35f1-107">The following code retrieves the clients collection for the Network Policy Server.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="d35f1-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d35f1-108">Remarks</span></span>

<span data-ttu-id="d35f1-109">A variável pSdoServiceControl contém um ponteiro para um objeto de dados de servidor para NPS.</span><span class="sxs-lookup"><span data-stu-id="d35f1-109">The pSdoServiceControl variable contains a pointer to a Server Data Object for NPS.</span></span> <span data-ttu-id="d35f1-110">Para obter mais informações, consulte o tópico [recuperando um serviço de SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span><span class="sxs-lookup"><span data-stu-id="d35f1-110">For more information, see the topic [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span></span>

<span data-ttu-id="d35f1-111">A variável vtClientsCollection é do tipo [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="d35f1-111">The vtClientsCollection variable is of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="d35f1-112">Um \_ \_ objeto Variant t encapsula ou inclui o tipo de dados [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="d35f1-112">A \_variant\_t object encapsulates, or encloses, the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) data type.</span></span> <span data-ttu-id="d35f1-113">A classe gerencia a alocação de recursos e a desalocação e faz chamadas de função para [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) e [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="d35f1-113">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

<span data-ttu-id="d35f1-114">Após a chamada para "pSdo->GetProperty ()", a variável vtProtocolsCollection especifica um objeto.</span><span class="sxs-lookup"><span data-stu-id="d35f1-114">After the call to "pSdo->GetProperty()", the vtProtocolsCollection variable specifies an object.</span></span> <span data-ttu-id="d35f1-115">O membro **pdispVal** de vtProtocolsCollection contém um ponteiro para a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d35f1-115">The **pdispVal** member of vtProtocolsCollection contains a pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the object.</span></span>

<span data-ttu-id="d35f1-116">O código de exemplo acima pode ser adaptado para recuperar outras coleções de NPS, por exemplo, as coleções de manipuladores de solicitação do NPS.</span><span class="sxs-lookup"><span data-stu-id="d35f1-116">The above sample code can be adapted to retrieve other NPS collections, for example the NPS Request Handlers collections.</span></span> <span data-ttu-id="d35f1-117">Os valores enumerados do tipo de enumeração [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) que correspondem às coleções de NPS disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d35f1-117">The [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type enumerated values that correspond to the available NPS collections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d35f1-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d35f1-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d35f1-119">[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="d35f1-119">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="d35f1-120">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="d35f1-120">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="d35f1-121">**ISdo:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="d35f1-121">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="d35f1-122">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="d35f1-122">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="d35f1-123">Recuperando um SDO de serviço</span><span class="sxs-lookup"><span data-stu-id="d35f1-123">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="d35f1-124">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="d35f1-124">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="d35f1-125">**VariantInit**</span><span class="sxs-lookup"><span data-stu-id="d35f1-125">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="d35f1-126">**VARIANTE**</span><span class="sxs-lookup"><span data-stu-id="d35f1-126">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 