---
title: Implementando uma interface primária do provedor de instância
description: Um provedor de instância usa os métodos assíncronos de IWbemServices como a interface primária para o WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814170"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>Implementando uma interface primária do provedor de instância

Um provedor de instância usa os métodos assíncronos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como a interface primária para o WMI. Ao implementar apenas os métodos que atendem às necessidades do seu provedor de instância, você pode reduzir a quantidade de recursos gastos com codificação. No entanto, ao implementar métodos reservados para outros tipos de provedores, você pode reduzir o número de provedores que escreve.

Como ele também é usado por aplicativos e provedores para solicitar serviços de WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contém muitos métodos que são irrelevantes para um provedor de instância. A tabela a seguir lista os métodos de **IWbemServices** que você pode implementar para um provedor de instância.



| Método                                                                   | Recurso          |
|--------------------------------------------------------------------------|------------------|
| [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | Recuperação        |
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | Modification     |
| [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | Exclusão         |
| [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | Enumeração      |
| [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | Processamento de consulta |



 

Para métodos que você não usa, seu provedor pode fornecer uma implementação de stub que retorne o **\_ provedor WBEM E \_ \_ não \_ compatível**. Isso inclui todos os métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) não listados na tabela acima.

Um único provedor pode agir simultaneamente como uma classe, instância e provedor de métodos por registro e implementação adequados de todos os métodos relevantes. Para obter mais informações, consulte [escrevendo um provedor de classe](writing-a-class-provider.md) e [escrevendo um provedor de método](writing-a-method-provider.md).

 

 



