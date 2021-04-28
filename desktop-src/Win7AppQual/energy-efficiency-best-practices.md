---
description: Práticas recomendadas para eficiência energética
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Práticas recomendadas para eficiência energética
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d9a348b9df49531358de2db50acc0936622c36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088384"
---
# <a name="best-practices-for-energy-efficiency"></a>Práticas recomendadas para eficiência energética

## <a name="platform"></a>Plataforma

 **Clientes** – Windows XP Windows \| Vista Windows \| 7  

## <a name="description"></a>Descrição

Os laptops baseados no Windows devem atender aos requisitos regulatórios de eficiência de energia, como os do programa de Estados Unidos agência de proteção ambiental (EPA) Energy Star. Além disso, as pesquisas mostraram que mais tempo a vida útil da bateria continua sendo o que os consumidores mais desejam e precisam em laptops. Para atender às demandas do consumidor, os laptops do Windows devem avançar continuamente nas seguintes áreas:

-   Eficiência energética em todos os cenários de uso, incluindo cargas de trabalho ociosas, de produtividade, reprodução de DVD e mídia e benchmarks do setor
-   Vida útil da bateria do PC móvel – para plataformas de hardware e para Windows

A plataforma Windows é altamente confiável e permite um rápido desempenho on-and-off. No entanto, as extensões fornecidas com sistemas de PC móvel, como serviços, applets da bandeja do sistema, drivers e outros softwares, podem afetar significativamente o desempenho, a confiabilidade e a eficiência energética.

A eficiência energética é um problema complexo, com fatores afetados por e afetando todos os elementos do ecossistema do PC. Pequenos aprimoramentos em vários cenários podem melhorar a eficiência de energia, mas um único recurso de aplicativo, dispositivo ou sistema com baixo desempenho pode aumentar significativamente o consumo de energia.

Hardware e dispositivos formam a base para eficiência energética. No entanto, o software de aplicativo e serviço também deve ser eficiente para permitir que o sistema alcance a vida útil ideal da bateria. Cada componente de software no sistema, incluindo o sistema operacional e os aplicativos e serviços de valor agregado, deve estar em conformidade com as diretrizes básicas de eficiência. Um único aplicativo ou serviço de comportamento inadequado pode eliminar qualquer ganho de eficiência de energia que o processador mais recente, os dispositivos ou o hardware de plataforma foi atingido. Para obter informações mais detalhadas sobre a vida útil da bateria e a eficiência energética, consulte o [Guia de soluções de vida útil da bateria](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).

Os problemas e componentes principais que afetam a vida útil da bateria em um PC móvel são:

**Características da bateria**

-   O tamanho, o tipo e a qualidade da capacidade da bateria afetam a vida útil da bateria
-   Quanto maior a bateria, maior a fonte de energia
-   Baterias maiores são mais caras e mais pesadas; os usuários preferem sistemas mais leves

**Componentes de hardware**

-   Frequência e profundidade em que o hardware pode inserir Estados de energia menores
-   Suporte de hardware de Estados de energia menores
-   Otimização de driver para eficiência energética

**Sistema operacional – gerenciamento de energia direcionado**

-   Eficiência do código do Windows enquanto está sob uma carga versus ociosa
-   Nível de cooperação de todos os componentes com o gerenciamento de energia direcionado ao Windows
-   Configuração adequada do sistema operacional para otimizar o gerenciamento de energia por meio de configurações de política de energia

**Software e serviços de aplicativos**

-   Eficiência de aplicativos, drivers e serviços em uma carga em comparação com o tempo ocioso
-   Nível de cooperação de aplicativos com o gerenciamento de energia direcionado do Windows
-   A concessão de software do sistema ou dos dispositivos para entrar em Estados ociosos de baixa energia

Um único componente de aplicativo ou de serviço pode impedir um sistema de concretizar a vida útil ideal da bateria. Embora o Windows forneça muitas opções de configuração de energia, as configurações de software pré-instalado ou de política de energia em muitos sistemas não são otimizadas para a plataforma de hardware do host.

Um método comum para avaliar o impacto da vida útil da bateria do software pré-instalado é comparar o consumo de energia do sistema com uma instalação limpa do Windows em comparação com uma instalação do Windows que inclui software e serviços de valor agregado. Embora uma instalação limpa não represente a plataforma típica que os OEMs enviam aos clientes, a comparação de consumo de energia pode fornecer informações sobre a eficiência de energia do software pré-instalado.

## <a name="best-practices"></a>Práticas Recomendadas

Para garantir que seu aplicativo seja otimizado em plataformas Windows, siga estas práticas recomendadas ao criar aplicativos ou serviços:

-   **Evitar o uso de temporizadores periódicos de alta resolução**

<dl> Usando temporizadores periódicos de alta resolução (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **Investir em otimizações de desempenho**

<dl> Cada otimização de desempenho é uma otimização da vida útil da bateria. Reduções nos recursos necessários, como o uso de menos tempo do processador ou leituras de disco em lotes/clustering, permitem que o hardware do sistema se torne ocioso e insira os modos de baixa energia.  
</dl>

-   **Ajustar à política de energia do usuário**

<dl> O Windows Vista e versões posteriores facilitam para o usuário escolher o comportamento geral de economia de energia ou de desempenho do sistema. Seu aplicativo deve responder às alterações na política de energia e reduzir o uso de recursos ou aumentar o desempenho de acordo. Por exemplo, um aplicativo deve desabilitar a atividade em segundo plano, como indexação ou verificação do sistema, quando o usuário tiver selecionado um plano de energia de economia de energia.  
</dl>

-   **Reduzir o uso de recursos quando o sistema estiver com energia da bateria**

<dl> Seu aplicativo deve reduzir seu uso de recursos, como frequência de atualização em segundo plano-quando o sistema está com bateria.  
</dl>

-   **Não renderizar para a exibição quando ela estiver desativada**

<dl> A exibição do sistema pode estar desligada para economia de energia. Seu aplicativo não deve executar a renderização de gráficos desnecessária quando a exibição está desativada porque isso desperdiça recursos e energia do sistema.  
</dl>

-   **Evite sondagem e rotação em loops apertados**

<dl> O uso intensivo do processador reduz a eficácia das tecnologias de gerenciamento de energia do processador, como Estados ociosos do processador e Estados de desempenho do processador.  
</dl>

-   **Não impedir que o sistema desative a exibição ou deixar para suspensão**

<dl> Seu aplicativo deve fazer solicitações criteriosas de energia com a API SetThreadExecutionState. O sistema deve fazer essas solicitações somente quando as operações críticas devem atrasar o sistema de desligar a exibição ou entrar em suspensão automaticamente.  
</dl>

-   **Responder a eventos comuns de gerenciamento de energia**

<dl> Seu aplicativo deve se registrar e responder a eventos comuns de gerenciamento de energia, como alterações de fonte de energia do sistema e notificações de energia e desligamento para a exibição.  
</dl>

-   **Não habilite o log de depuração por padrão; Use o rastreamento de eventos para Windows em vez disso**

<dl> O log de depuração periódico pode impedir a rotação do disco.  
</dl>

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Guia de soluções de vida útil da bateria](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [Portal de eficiência de energia](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



