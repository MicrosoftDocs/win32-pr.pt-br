---
description: 'Há duas maneiras de implementar um provedor de classe: implemente a interface como um provedor de Push ou como um provedor de pull.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementando a interface primária para um provedor de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296994"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a>Implementando a interface primária para um provedor de classe

Há duas maneiras de implementar um provedor de classe: implemente a interface como um provedor de Push ou como um provedor de pull.

As seções a seguir são discutidas neste tópico:

-   [Implementando a interface primária para um provedor de classe push](#implementing-the-primary-interface-for-a-push-class-provider)
-   [Implementando a interface primária para um provedor de classe pull](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a>Implementando a interface primária para um provedor de classe push

Enquanto todos os provedores implementam [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para inicialização e pelo menos uma outra interface como sua interface primária, um provedor de push implementa apenas **IWbemProviderInit**.

Certifique-se de que sua implementação execute as seguintes tarefas:

-   Recupera os dados de classe apropriados.
-   Coloca os dados no repositório WMI.
-   Exclui dados obsoletos.

Depois de concluir o processo de inicialização, o WMI manipula todas as solicitações de aplicativo para classes que pertencem ao provedor de push sem nenhuma interação adicional do provedor. Depois disso, o provedor de push atua efetivamente como um cliente do WMI em vez de um provedor. Para obter mais informações sobre como implementar [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), consulte [inicializando um provedor](initializing-a-provider.md).

> [!Note]  
> Ao chamar o WMI para criar, atualizar ou remover dados em um provedor de push, defina o parâmetro *lFlags* para incluir o sinalizador de **atualização do \_ proprietário do sinalizador \_ \_ WBEM** em todas as chamadas para métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a>Implementando a interface primária para um provedor de classe pull

Um provedor de pull de classe deve implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como a interface primária. A interface **IWbemServices** dá suporte à recuperação de dados, à atualização de dados, à remoção de dados, à enumeração e ao processamento de consultas. No entanto, como **IWbemServices** também é usado por aplicativos e provedores para solicitar serviços de WMI, **IWbemServices** contém muitos métodos que são irrelevantes para um provedor de classe. Sua implementação deve dar suporte à recuperação e à enumeração de classe, por meio dos métodos [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) e [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) , respectivamente. A tabela a seguir lista os métodos de **IWbemServices** assíncronos adicionais que você pode implementar para um provedor de classe.



| Método                                                     | Recurso      |
|------------------------------------------------------------|--------------|
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | Modification |
| [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | Exclusão     |



 

> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

Seu provedor de classe deve fornecer uma implementação de stub que retorne o **\_ provedor WBEM E \_ \_ não \_ compatível** com todos os outros métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que não dão suporte ao seu conjunto de recursos. Especificamente, o WMI não dá suporte ao processamento de consultas para provedores de classe. Como tal, um provedor de classe deve retornar o **\_ provedor WBEM E \_ \_ não \_ capaz** de sua implementação de [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), definir sua propriedade de registro **QuerySupportLevels** como **NULL** ou ambos.

As interfaces que um provedor de classe implementa são muito semelhantes às interfaces para um provedor de instância e um provedor de método. Na verdade, um único provedor pode atuar como todos os três tipos de provedor implementando todos os métodos e registrando-se corretamente.

 

 



