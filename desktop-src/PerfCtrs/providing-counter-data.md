---
description: no Windows Vista, os contadores de desempenho implementaram uma nova arquitetura (versão 2,0) para fornecer dados do contador.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Fornecendo dados do contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0a17a6c75a86a7ee86f26350b9ea7680f0ba08338dbe7dc18cd56a8c425ba3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793619"
---
# <a name="providing-counter-data"></a>Fornecendo dados do contador

os componentes de Software que publicam dados por meio de contadores de desempenho Windows são chamados de provedores de dados de desempenho.

o Windows dá suporte a dois tipos de provedores de dados de desempenho. Os provedores de dados de desempenho herdados (**provedores v1**) são implementados usando um arquivo .INI e uma DLL de desempenho. Os provedores de dados de desempenho modernos (**provedores v2**) usam um. O MAN (manifesto XML) e as APIs do provedor do contador de desempenho.

## <a name="manifests"></a>Manifestos

Os provedores de dados de desempenho modernos usam um. MAN (manifesto XML) para definir os dados do contador e usar as APIs do provedor do contador de desempenho para gerenciar dados no contexto do provedor.

Provedores implementados usando um manifesto e APIs de provedor de contador de desempenho geralmente são chamados de **provedores v2**.

o Windows dá suporte a provedores V2 de modo de usuário no Windows Vista ou posterior. Para obter detalhes do modo de usuário, consulte [fornecendo dados do contador usando a versão 2,0](providing-counter-data-using-version-2-0.md).

o Windows dá suporte a provedores V2 do modo kernel no Windows 7 ou posterior. Para obter detalhes do modo kernel, consulte [monitoramento de desempenho do modo kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

## <a name="performance-dll-deprecated"></a>DLL de desempenho (preterida)

Na arquitetura do contador de desempenho herdado, os provedores implementaram uma DLL de desempenho que foi executada no processo do consumidor para coletar e fornecer os dados do contador quando um consumidor o solicitou. O provedor usou um arquivo de inicialização (.INI) e entradas de registro para definir os contadores e configurar a DLL de desempenho.

Os provedores implementados usando um arquivo .INI e uma DLL de desempenho geralmente são chamados de **provedores v1**.

> [!CAUTION]
> Embora você ainda possa usar uma DLL de desempenho para fornecer dados de contador, essa arquitetura é preterida devido a limitações significativas de desempenho e confiabilidade. Além disso, os provedores v1 costumam ser mais difíceis de implementar, pois exigem o envio de uma DLL separada que deve ser executada no processo do consumidor.

Para obter detalhes, consulte [fornecendo dados do contador usando uma DLL de desempenho](providing-counter-data-using-a-performance-dll.md).
