---
description: Como o WMI carrega um provedor de alto desempenho em processo para o WMI ou um aplicativo cliente, você deve projetar seu provedor de alto desempenho como um servidor em processo.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementando a High-Performance interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecec9a7b5e5399765adaa7a0e195825493d930ece46c30af3e788795fe08ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108617"
---
# <a name="implementing-the-high-performance-interface"></a>Implementando a High-Performance interface

Como o WMI carrega um provedor de alto desempenho em processo para o WMI ou um aplicativo cliente, você deve projetar seu provedor de alto desempenho como um servidor em processo. Além disso, você deve implementar os métodos de provedor de alto desempenho nas interfaces [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) e [**IWbemRefresher.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Você deve implementar um provedor de alto desempenho como um servidor em processo. Um recurso que você deve estar ciente ao implementar a segurança de um servidor em processo é como o provedor identifica sua própria localização. Quando carregado em processo para WMI, o WMI instania o provedor usando um CLSID. Quando carregado em processo para um aplicativo cliente, o aplicativo cliente instanciou o provedor com a **propriedade ClientLoadableCLSID.** Ao dar valores diferentes a um CLSID e **ClientLoadableCLSID**, você permite que o provedor determine se ele é carregado em processo para o WMI ou para um aplicativo cliente. Se estiver localizado em um processo WMI, o provedor deverá fazer qualquer representação de cliente necessária usando **ClientLoadableCLSID**. Se estiver localizado em um processo de cliente, o provedor herdará o token de acesso do thread em que ele é chamado. Para obter mais informações sobre como implementar um servidor em processo, consulte a [seção COM](https://msdn.microsoft.com/library/aa139695.aspx) do MSDN.

Como um servidor em processo, um provedor de alto desempenho usa um objeto de atualização para manter os dados atualizados para o cliente remoto. A tabela a seguir lista os métodos que você deve implementar para um provedor de alto desempenho.



| Método                                                                                              | Recurso                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider::QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Consultas                                           |
| [**IWbemHiPerfProvider::GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Recuperação de objeto                                  |
| [**IWbemHiPerfProvider::CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Cria um atualizador                               |
| [**IWbemHiPerfProvider::CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Cria um objeto de instância atualizável             |
| [**IWbemHiPerfProvider::CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Cria um enumerador atualizável                  |
| [**IWbemHiPerfProvider::StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Interrompe a atualização de um enumerador ou objeto de instância |
| [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Cria um atualizador                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformando um provedor de instância em um provedor High-Performance dados](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



