---
description: Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089363"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a>Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) são usados juntos para envolver uma área de código que é executada em seu próprio contexto e pode usar serviços com+ sem a necessidade de componentes com+. Os serviços COM+ que são usados neste contexto são configurados por meio do objeto [**CServiceConfig**](cserviceconfig.md) que é passado para **CoEnterServiceDomain**. O código que está circundado por **CoEnterServiceDomain** e **CoLeaveServiceDomain** se comporta como se fosse um método chamado em um objeto criado dentro desse contexto.

Um aplicativo de script pode usar esse par de funções para fornecer suporte em tempo de execução de serviços COM+ sem componentes. Por exemplo, um aplicativo de script pode ser desenvolvido para fornecer marcas que permitem que os gravadores de script insiram e deixem um domínio de serviço dentro do script. Quando o mecanismo de script processa o script e encontra as marcas, ele pode chamar [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) com um objeto [**CServiceConfig**](cserviceconfig.md) pré-configurado, executar o código necessário e, em seguida, chamar [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

O fragmento de código a seguir ilustra como usar os serviços COM+ entre chamadas para [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain). O tratamento de erros foi omitido para fins de brevidade. Este fragmento de código usa o objeto [**CServiceConfig**](cserviceconfig.md) que foi criado e configurado na [configuração de serviços com+ com CServiceConfig](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Configurando serviços COM+ com CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Usando os serviços COM+ por meio do CoCreateActivity](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



