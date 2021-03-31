---
description: O provedor View é uma instância e um provedor de métodos que cria novas classes com base em instâncias de outras classes.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Exibir provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829261"
---
# <a name="view-provider"></a>Exibir provedor

O provedor View é uma instância e um provedor de métodos que cria novas classes com base em instâncias de outras classes. Você pode usar o provedor de exibição para obter propriedades de diferentes classes de origem, namespaces diferentes ou computadores diferentes e combinar as propriedades como uma única classe.

Como um provedor de método e instância, o provedor de exibição oferece suporte à interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) padrão e aos seguintes métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) :

-   [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Para obter mais informações sobre os qualificadores usados para definir as classes do provedor de exibição, consulte [qualificadores específicos para o provedor de exibição](qualifiers-specific-to-the-view-provider.md).

Para obter mais informações sobre exibições, consulte [vincular classes juntas](linking-classes-together.md).

Duas versões do provedor de exibição estão disponíveis em plataformas de 64 bits. Para obter mais informações, consulte [obter e fornecer dados em um computador de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).

O provedor de exibição é implementado no ViewProv.dll.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> </dl>

 

 



