---
description: Os componentes do CRM podem ser instalados em um aplicativo de servidor COM+ ou em um aplicativo de biblioteca COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configurando componentes COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79f8c9716a9a4db2888231c886d3d1a4d929dd1a8dfb9f9f359ab03ec7670b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307445"
---
# <a name="configuring-com-crm-components"></a>Configurando componentes COM+ CRM

Os componentes do CRM podem ser instalados em um aplicativo de servidor COM+ ou em um aplicativo de biblioteca COM+. No entanto, eles sempre devem ser executados em um aplicativo de servidor COM+. Se eles estão instalados em um aplicativo de biblioteca COM+, eles não estão disponíveis para uso em processos de cliente.

Se os componentes crm são instalados em um aplicativo de biblioteca, eles estão disponíveis para mais de um aplicativo de servidor. Se instalados em um aplicativo de servidor específico, eles estarão disponíveis somente para esse aplicativo de servidor específico.

Para habilitar o uso de um CRM em um aplicativo de servidor, use as seguintes etapas:

1.  Em Serviços de Componentes, na página de propriedades do aplicativo do servidor, clique na **guia** Avançado.

2.  Selecione a **opção Habilitar a compensação de Gerenciadores** de Recursos para esse aplicativo de servidor. Se essa opção não estiver selecionada, as tentativas de usar um CRM dentro desse aplicativo de servidor falharão.

    > [!Note]  
    > Se instalado em um aplicativo de biblioteca,  não é necessário selecionar a opção Habilitar compensação de Gerenciadores de Recursos para esse aplicativo de biblioteca, mas essa opção deve ser selecionada para o aplicativo de servidor no qual o CRM deve ser executado.

     

É recomendável que os componentes crm worker e crm compensator para um CRM específico sejam instalados no mesmo aplicativo.

As configurações recomendadas para componentes crm são as a seguir.



| Componente           | Configurações                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **CRM Worker**      | transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)     |
| **Compensador de CRM** | transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment) |



 

> [!Note]  
> Os componentes que usam o CRM devem especificar explicitamente um modelo de threading quando são registrados. Não há suporte para o padrão 'Main Thread Apartment'. Os únicos dois modelos de threading com suporte são Apartment e Both.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



