---
description: Os componentes do CRM podem ser instalados em um aplicativo de servidor COM+ ou em um aplicativo de biblioteca COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configurando componentes de CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765681"
---
# <a name="configuring-com-crm-components"></a>Configurando componentes de CRM do COM+

Os componentes do CRM podem ser instalados em um aplicativo de servidor COM+ ou em um aplicativo de biblioteca COM+. No entanto, eles devem sempre ser executados em um aplicativo de servidor do COM+. Se eles estiverem instalados em um aplicativo de biblioteca COM+, eles não estarão disponíveis para uso em processos de cliente.

Se os componentes do CRM estiverem instalados em um aplicativo de biblioteca, eles estarão disponíveis para mais de um aplicativo de servidor. Se instalado em um aplicativo de servidor específico, ele estará disponível somente para esse aplicativo de servidor específico.

Para habilitar o uso de um CRM em um aplicativo de servidor, use as seguintes etapas:

1.  Em serviços de componentes, na página Propriedades do aplicativo de servidor, clique na guia **avançado** .

2.  Selecione a opção **habilitar gerenciadores de recursos de compensação** para esse aplicativo de servidor. Se essa opção não estiver selecionada, as tentativas de usar um CRM dentro desse aplicativo de servidor falharão.

    > [!Note]  
    > Se instalado em um aplicativo de biblioteca, não é necessário selecionar a opção **habilitar gerenciadores de recursos de compensação** para esse aplicativo de biblioteca, mas essa opção deve ser selecionada para o aplicativo de servidor no qual o CRM deve ser executado.

     

É recomendável que os componentes de trabalho CRM e compensador CRM para um CRM específico sejam instalados no mesmo aplicativo.

As configurações recomendadas para os componentes do CRM são as seguintes.



| Componente           | Configurações                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **Trabalhador do CRM**      | transação = requiredsync = yesJIT = modelo de yesthreading = (ou modelo de Threading = Apartment)     |
| **Compensador de CRM** | transação = disabledsync = disabledJIT = modelo nothreading = (ou modelo de Threading = Apartment) |



 

> [!Note]  
> Os componentes que usam o CRM devem especificar explicitamente um modelo de Threading quando eles são registrados. Não há suporte para o padrão ' Main thread apartment '. Os únicos dois modelos de Threading com suporte são Apartment e both.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



