---
title: Uso do Monitor de Rede para exibição de arquivos ETL
description: Monitor de Rede 3,3 permite que os usuários analisem, filtrem e exibam um arquivo ETL (usando o Windows Vista ou posterior).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "103923022"
---
# <a name="using-network-monitor-to-view-etl-files"></a>Uso do Monitor de Rede para exibição de arquivos ETL

[Monitor de Rede 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) permite que os usuários analisem, filtrem e exibam um arquivo ETL (usando o Windows Vista ou posterior). (Se estiver usando o Monitor de Rede 3,2, você precisará baixar e instalar analisadores adicionais do [codeplex](https://www.codeplex.com/NMParsers) para renderizar os eventos de rastreamento de rede.)

Os arquivos ETL correlacionados agrupam os eventos relevantes juntos. O illlustration abaixo mostra um arquivo correlacionado aberto no Monitor de Rede, com a conversa habilitada.

![Captura de tela que mostra a Monitor de Rede, com eventos correlacionados realçados na janela esquerda e UTEvent realçados na lista suspensa.](images/ut-netmon1.png)

Os eventos correlacionados são agrupados por atividade no painel esquerdo. Você pode selecionar um evento no painel Resumo do quadro e clicar com o botão direito do mouse para selecionar a conversa no nível do evento de rede. Isso exibirá uma atividade relacionada no painel esquerdo.

Selecionar uma atividade específica no painel esquerdo e expandi-la mostrará a lista de provedores para os eventos correlacionados.

![Captura de tela que mostra a Monitor de Rede com uma atividade selecionada no painel esquerdo e eventos correspondentes a esse evento no painel direito.](images/ut-netmon2.png)

Quando você seleciona um provedor específico no painel esquerdo, uma lista de eventos específicos para esse provedor e atividade será exibida no painel Resumo do quadro.

![Captura de tela que mostra um provedor específico selecionado no painel esquerdo e uma lista de eventos específicos para o provedor realçado no painel superior direito.](images/ut-netmon3.png)

Os filtros podem ser aplicados no Monitor de Rede para facilitar a exibição e a localização dos eventos ou do pacote corretos. Por exemplo, você pode aplicar um filtro aos eventos de erro selecionados (por exemplo, **UTEvent. Header. Descriptor. Level = = 2**) para exibi-los em uma determinada cor.

![Captura de tela que mostra a caixa de diálogo ' Editar Filtro de cores '.](images/ut-netmon4.png)

Os filtros também podem ser aplicados para marcar provedores diferentes em cores diferentes, de modo que os resultados sejam mais fáceis de exibir.

![Captura de tela que mostra um exemplo de provedores diferentes marcados em cores diferentes.](images/ut-netmon5.png)

Para aplicar um filtro, clique em **ColorFilters** no menu **filtros** .

A tabela a seguir mostra alguns exemplos de filtros úteis.



| Filtrar                                                                        | Descrição                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| UTEvent. Header. Descriptor. nível = = 2                                          | Filtra somente eventos de erro.                                        |
| UTEvent. Header. Descriptor. nível = = 3                                          | Filtra somente eventos de aviso.                                      |
| UTEvent.Header.Descriptor.Id = = 2001                                          | Filtra somente eventos com a ID de evento 2001.                           |
| \_MICROSOFTWINDOWSWLANAUTOCONFIG WLAN                                          | Filtra somente os eventos do serviço WLAN.                            |
| N802 \_ MicrosoftWindowsNWiFi                                                   | Filtra somente os eventos do driver WiFi nativo.                  |
| WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG e UTEvent.Header.Descriptor.ID = = 2001 | Filtra somente eventos com a ID de evento 2001 emitida do serviço de WLAN. |



 

 

 




