---
description: Como o WMI carrega um provedor de alto desempenho em processo para o WMI ou um aplicativo cliente, você deve projetar seu provedor de alto desempenho como um servidor em processo.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementando a interface High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813519"
---
# <a name="implementing-the-high-performance-interface"></a>Implementando a interface High-Performance

Como o WMI carrega um provedor de alto desempenho em processo para o WMI ou um aplicativo cliente, você deve projetar seu provedor de alto desempenho como um servidor em processo. Além disso, você deve implementar os métodos de provedor de alto desempenho nas interfaces [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) e [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .

Você deve implementar um provedor de alto desempenho como um servidor em processo. Um recurso que você deve estar atento ao implementar a segurança de um servidor em processo é como o provedor identifica seu próprio local. Quando carregado em processo para WMI, o WMI instancia o provedor usando um CLSID. Quando carregado em processo para um aplicativo cliente, o aplicativo cliente cria uma instância do provedor com a propriedade **ClientLoadableCLSID** . Ao conceder valores diferentes a um CLSID e a um **ClientLoadableCLSID**, você permite que o provedor determine se ele está carregado em processo para WMI ou para um aplicativo cliente. Se estiver localizado em um processo WMI, o provedor deverá fazer qualquer representação de cliente necessária usando **ClientLoadableCLSID**. Se estiver localizado em um processo de cliente, o provedor herdará o token de acesso do thread em que ele é chamado. Para obter mais informações sobre como implementar um servidor em processo, consulte a [seção com](https://msdn.microsoft.com/library/aa139695.aspx) do MSDN.

Como um servidor em processo, um provedor de alto desempenho usa um objeto de atualização para manter os dados atuais para o cliente remoto. A tabela a seguir lista os métodos que você deve implementar para um provedor de alto desempenho.



| Método                                                                                              | Recurso                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider::QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Consultas                                           |
| [**IWbemHiPerfProvider:: GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Recuperação de objeto                                  |
| [**IWbemHiPerfProvider:: createrefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Cria um atualizador                               |
| [**IWbemHiPerfProvider::CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Cria um objeto de instância atualizável             |
| [**IWbemHiPerfProvider::CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Cria um enumerador atualizável                  |
| [**IWbemHiPerfProvider::StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Para a atualização de um enumerador ou objeto de instância |
| [**IWbemRefresher:: atualizar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Cria um atualizador                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



