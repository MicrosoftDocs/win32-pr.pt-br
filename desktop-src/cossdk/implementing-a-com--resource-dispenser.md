---
description: Implementando um dispensador de recursos COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementando um dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9c37de2a4910af908bdc3f2e38f1c1b55699b133a59a818b8a09236f8c0a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547888"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implementando um dispensador de recursos COM+

As etapas a seguir descrevem um procedimento geral para implementar um dispensador de recursos COM+:

1.  Decida sobre o formato **RESTYPID** que categoriza como seus recursos diferem uns dos outros.

2.  Use a biblioteca e o arquivo de cabeçalho Mtxdm. h e Mtxdm. lib, respectivamente.

3.  Crie uma DLL que implemente a interface [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) e a API que você deseja expor aos aplicativos.

4.  Na inicialização ([*DllMain*](/windows/desktop/Dlls/dllmain) ou primeiro chamada para a API do dispensador), chame a função [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) . Isso retorna um ponteiro para a interface [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) do Gerenciador do dispensador.

5.  Chame [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passando um ponteiro para a implementação de [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). Isso faz com que o Gerenciador do dispensador crie um detentor (Gerenciador de pooling) para o dispensador de recursos e, em seguida, retorne o ponteiro para a interface [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .

6.  Armazene esse ponteiro para que você possa chamar [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**IHolder:: FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).

7.  Agora você pode (em resposta a chamadas para sua API) fazer chamadas para [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource). Inicialmente, o **AllocResource** responde chamando de volta para o método [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , mas as chamadas de **AllocResource** posteriores são atendidas a partir do pool crescente de recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfaces do dispensador de recursos COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
