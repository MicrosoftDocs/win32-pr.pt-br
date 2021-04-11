---
title: Recuperando um SDO de serviço
description: Recuperando um SDO de serviço
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afcea1885e0ed714587e99bc7c2dcd92f2fea422
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162343"
---
# <a name="retrieving-a-service-sdo"></a>Recuperando um SDO de serviço

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.

 

O código a seguir recupera um SDO (objeto de dados do servidor) para o servidor de políticas de rede.


```C++
   HRESULT hr;
   CComPtr<IUnknown> pServiceUnknown;
   _bstr_t bstrServiceName = L"IAS";

   hr = pSdoMachine->GetServiceSDO(
      DATA_STORE_LOCAL,
      bstrServiceName,
      (IUnknown**) &pServiceUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoServiceControl>  pSdoServiceControl;
   hr = pServiceUnknown->QueryInterface(
      __uuidof(ISdoServiceControl),
      (void**) &pSdoServiceControl
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="remarks"></a>Comentários

Você deve [anexar](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) a um computador antes de poder chamar qualquer um dos métodos [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anexando a um computador SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 