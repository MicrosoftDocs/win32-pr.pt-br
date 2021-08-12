---
title: Recuperando um SDO de serviço
description: Recuperando um SDO de serviço
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f1ec3f8537cbf6e9a7be82f8152bc764a263093fe0ebeee46ed1499abfd346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618952"
---
# <a name="retrieving-a-service-sdo"></a>Recuperando um SDO de serviço

> [!Note]  
> O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede) a partir do Windows Server 2008.

 

O código a seguir recupera um objeto de dados de servidor (SDO) para o Servidor de Política de Rede .


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

Você deve [anexar](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) a um computador antes de chamar qualquer um dos [**métodos ISdoMachine.**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anexando a um computador SDO-Enabled computador](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 