---
title: Enumerando objetos em uma coleção
description: Enumerando objetos em uma coleção
ms.assetid: 664e4d99-48ed-4948-b816-e92ad1ca3ece
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f3c543e01f3c8f154628c6e204aff53c6ad210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810292"
---
# <a name="enumerating-objects-in-a-collection"></a><span data-ttu-id="1d7c7-103">Enumerando objetos em uma coleção</span><span class="sxs-lookup"><span data-stu-id="1d7c7-103">Enumerating Objects in a Collection</span></span>

> [!Note]  
> <span data-ttu-id="1d7c7-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1d7c7-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1d7c7-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="1d7c7-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1d7c7-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="1d7c7-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1d7c7-107">O código a seguir enumera os protocolos na coleção de protocolos do NPS.</span><span class="sxs-lookup"><span data-stu-id="1d7c7-107">The following code enumerates the protocols in the NPS protocols collection.</span></span>


```C++
   HRESULT hr;

   //
   // Retrieve the protocols collection object
   //
   _variant_t vtIASProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection> pIASProtocolsCollection;
   hr = vtIASProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the enumeration interface, IEnumVARIANT
   //
   CComPtr<IUnknown> pUnknownProtocol;
   hr = pIASProtocolsCollection->get__NewEnum(&pUnknownProtocol);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<IEnumVARIANT> pEnumProtocols;
   hr = pUnknownProtocol->QueryInterface(
      __uuidof(IEnumVARIANT), 
      (void **) &pEnumProtocols
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the first protocol from the collection
   //
   DWORD      dwRetrieved = 1;
   _variant_t vtProtocol;
   hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
   if (FAILED(hr))
   {
      return hr;
   }

   while (hr != S_FALSE) {
      // 
      // Retrieve the name of the protocol
      //
      CComPtr<ISdo> pLocalSdo;
      hr = vtProtocol.pdispVal->QueryInterface(
         __uuidof(ISdo), 
         (void**)&pLocalSdo
      );
      if (FAILED(hr))
      {
         return hr;
      }

      _variant_t vtName;
      hr = pLocalSdo->GetProperty(PROPERTY_SDO_NAME, &vtName);
      if (FAILED(hr))
      {
         return hr;
      }

      vtProtocol.Clear();
      vtName.Clear();

      //
      // Retrieve the next protocol from the collection
      //
      dwRetrieved = 1;
      hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
      if (FAILED(hr))
      {
         return hr;
      }
   }

```



## <a name="remarks"></a><span data-ttu-id="1d7c7-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d7c7-108">Remarks</span></span>

<span data-ttu-id="1d7c7-109">As variáveis vtName e vtProtocol são do tipo [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="1d7c7-109">The vtName and vtProtocol variables are of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="1d7c7-110">Um objeto [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) encapsula ou inclui o tipo de dados **Variant** .</span><span class="sxs-lookup"><span data-stu-id="1d7c7-110">A [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) object encapsulates, or encloses, the **VARIANT** data type.</span></span> <span data-ttu-id="1d7c7-111">A classe gerencia a alocação de recursos e a desalocação e faz chamadas de função para [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) e [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="1d7c7-111">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d7c7-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d7c7-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1d7c7-113">[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="1d7c7-113">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="1d7c7-114">Adicionando um cliente</span><span class="sxs-lookup"><span data-stu-id="1d7c7-114">Adding a Client</span></span>](/windows/desktop/Nps/sdo-adding-a-client)
</dt> <dt>

[<span data-ttu-id="1d7c7-115">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="1d7c7-115">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties)
</dt> <dt>

[<span data-ttu-id="1d7c7-116">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="1d7c7-116">**IEnumVARIANT**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[<span data-ttu-id="1d7c7-117">**ISdo:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="1d7c7-117">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="1d7c7-118">Recuperando um SDO de serviço</span><span class="sxs-lookup"><span data-stu-id="1d7c7-118">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="1d7c7-119">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="1d7c7-119">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="1d7c7-120">**VariantInit**</span><span class="sxs-lookup"><span data-stu-id="1d7c7-120">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="1d7c7-121">**VARIANTE**</span><span class="sxs-lookup"><span data-stu-id="1d7c7-121">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 