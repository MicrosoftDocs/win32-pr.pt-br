---
description: Configurando serviços COM+ com CServiceConfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Configurando serviços COM+ com CServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646287"
---
# <a name="configuring-com-services-with-cserviceconfig"></a>Configurando serviços COM+ com CServiceConfig

A classe [**CServiceConfig**](cserviceconfig.md) é usada para configurar os serviços com+ que podem ser usados sem componentes. Ele agrega o marshaler de thread livre, portanto, ele pode ser usado em diferentes Apartments. Para configurar um serviço individual, você deve chamar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface associada ao serviço e, em seguida, chamar métodos nessa interface para estabelecer a configuração apropriada. A tabela a seguir descreve as interfaces que são implementadas por meio da classe **CServiceConfig** .



| Interface                                                                         | Descrição                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IServiceInheritanceConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | A interface padrão para a classe. Ele é usado para inicializar rapidamente muitos dos serviços COM+.<br/>                                                                                              |
| [**IServiceComTIIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | Usado para configurar as informações intrínsecas do integrador de transações COM (COMTI). O COMTI permite que os desenvolvedores integrem programas de transação baseados em mainframe a aplicativos baseados em componentes.<br/> |
| [**IServiceIISIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | Usado para configurar as informações intrínsecas do Serviços de Informações da Internet (IIS).<br/>                                                                                                             |
| [**IServicePartitionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | Usado para configurar como as partições COM+ são usadas com os serviços.<br/>                                                                                                                             |
| [**IServiceSxSConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | Usado para configurar assemblies lado a lado.<br/>                                                                                                                                                    |
| [**IServiceSynchronizationConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | Usado para configurar os serviços de sincronização COM+.<br/>                                                                                                                                              |
| [**IServiceThreadPoolConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | Usado para configurar o pool de threads para o serviço COM+. O pool de threads só pode ser configurado ao usar a função [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .<br/>                          |
| [**IServiceTrackerConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | Usado para configurar a propriedade do rastreador. Tracker é um mecanismo de relatório usado pelo código de monitoramento para observar qual código está sendo executado quando.<br/>                                                         |
| [**IServiceTransactionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | Usado para configurar o serviço de transação COM+.<br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

O fragmento de código a seguir ilustra como criar e configurar um objeto [**CServiceConfig**](cserviceconfig.md) para usar transações com+.


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Usando os serviços COM+ por meio do CoCreateActivity](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

