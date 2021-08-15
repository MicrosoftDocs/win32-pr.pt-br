---
description: No Windows Vista, os Contadores de Desempenho implementaram uma nova arquitetura (versão 2.0) para fornecer dados do contador.
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

Os componentes de software que publicam dados Windows contadores de desempenho são chamados de provedores de dados de desempenho.

Windows dá suporte a dois tipos de provedores de dados de desempenho. Provedores de dados de desempenho herddos (**provedores V1**) são implementados usando um arquivo .INI e uma DLL de desempenho. Provedores de dados de desempenho modernos (**provedores V2**) usam um . MAN (manifesto XML) e as APIs do provedor de contador de desempenho.

## <a name="manifests"></a>Manifestos

Provedores de dados de desempenho modernos usam um . MAN (manifesto XML) para definir os dados do contador e usar APIs do provedor do contador de desempenho para gerenciar dados dentro do contexto do provedor.

Provedores implementados usando um provedor de contador de desempenho e manifesto geralmente são chamados **de provedores V2.**

Windows dá suporte a provedores de modo de usuário V2 Windows Vista ou posterior. Para obter detalhes do modo de usuário, consulte [Fornecendo dados do contador usando a versão 2.0](providing-counter-data-using-version-2-0.md).

Windows dá suporte a provedores de modo kernel V2 Windows 7 ou posterior. Para obter detalhes do modo kernel, consulte [Monitoramento de desempenho do modo kernel.](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring)

## <a name="performance-dll-deprecated"></a>DLL de desempenho (preterido)

Na arquitetura do contador de desempenho herdado, os provedores implementaram uma DLL de desempenho para que fosse executada no processo do consumidor para coletar e fornecer os dados do contador quando um consumidor solicitou. O provedor usou um arquivo de inicialização (.INI) e entradas do Registro para definir os contadores e configurar a DLL de desempenho.

Provedores implementados usando um arquivo .INI e uma DLL de desempenho geralmente são chamados **de provedores V1.**

> [!CAUTION]
> Embora você ainda possa usar uma DLL de desempenho para fornecer dados de contador, essa arquitetura foi preterida devido a limitações significativas de desempenho e confiabilidade. Além disso, os provedores V1 geralmente são mais difíceis de implementar, pois exigem o envio de uma DLL separada que deve ser executado no processo do consumidor.

Para obter detalhes, consulte [Fornecendo dados de contador usando uma DLL de desempenho](providing-counter-data-using-a-performance-dll.md).
