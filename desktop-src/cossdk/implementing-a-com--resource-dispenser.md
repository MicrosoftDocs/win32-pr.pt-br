---
description: Implementando um Com+ Resource Dispenser
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementando um Com+ Resource Dispenser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9c37de2a4910af908bdc3f2e38f1c1b55699b133a59a818b8a09236f8c0a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547888"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implementando um Com+ Resource Dispenser

As etapas a seguir descrevem um procedimento geral para implementar um distribuidor de recursos COM+:

1.  Decida sobre **o formato RESTYPID** que categoriza como seus recursos diferem uns dos outros.

2.  Use a biblioteca e o arquivo de header Mtxdm.h e Mtxdm.lib, respectivamente.

3.  Crie uma DLL que implemente a interface [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) e a API que você deseja expor aos aplicativos.

4.  Na inicialização ([*DllMain*](/windows/desktop/Dlls/dllmain) ou primeira chamada para a API do distribuidor), chame a [**função GetDispenserManager.**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) Isso retorna um ponteiro para a interface [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) do gerenciador do distribuidor.

5.  Chame [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passando um ponteiro para sua implementação de [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). Isso faz com que o gerenciador do distribuidor crie um titular (gerenciador de pooling) para o distribuidor de recursos e, em seguida, retorne o ponteiro para a interface [**do IHolder.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)

6.  Armazene esse ponteiro para que você possa chamar [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) [**e IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).

7.  Agora você pode (em resposta a chamadas para sua API) fazer chamadas para [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource). **AllocResource** inicialmente responde chamando de volta para o método [**CreateResource,**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) mas as chamadas posteriores **allocResource** são a serviço do pool crescente de recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Com+ Resource Dispenser](com--resource-dispenser-concepts.md)
</dt> <dt>

[COM+ Resource Dispenser Interfaces](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
