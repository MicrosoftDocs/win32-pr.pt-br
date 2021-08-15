---
description: A função CoCreateActivity é usada para enviar o trabalho em lotes para o sistema COM+. Ele permite que aplicativos baseados em script ofereçam suporte a uma configuração de serviço COM+ em todo o aplicativo.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Usando os serviços COM+ por meio do CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5452c99fa431e7c1927646eec7ad9b5e5fa930f3ba7d0bf242df7690325db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128658"
---
# <a name="using-com-services-through-cocreateactivity"></a>Usando os serviços COM+ por meio do CoCreateActivity

A função [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) é usada para enviar o trabalho em lotes para o sistema com+. Ele permite que aplicativos baseados em script ofereçam suporte a uma configuração de serviço COM+ em todo o aplicativo.

Os serviços COM+ desejados são configurados por meio de um objeto [**CServiceConfig**](cserviceconfig.md) que é passado para a função. A função cria um objeto de atividade e retorna a interface [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) desse objeto. O trabalho em lotes pode ser enviado de forma síncrona ou assíncrona, usando os métodos [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) ou [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) de **IServiceActivity**, respectivamente. Um ponteiro para uma interface [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) é passado para cada um desses métodos, e o trabalho em lotes é implementado pelo desenvolvedor no método [**oncall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) da interface **IServiceCall** .

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

O fragmento de código a seguir ilustra como usar os serviços COM+ por meio do [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity). O tratamento de erros foi omitido para fins de brevidade. Este fragmento de código usa o objeto [**CServiceConfig**](cserviceconfig.md) que foi criado e configurado na [configuração de serviços com+ com CServiceConfig](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[Configurando serviços COM+ com CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



