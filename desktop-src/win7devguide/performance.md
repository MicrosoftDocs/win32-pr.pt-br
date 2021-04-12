---
title: Desempenho (guia do desenvolvedor do Windows 7)
description: O Windows 7 maximiza a eficiência de energia de hardware e a escalabilidade, mantendo o alto desempenho.
ms.assetid: db48aa8f-749e-4a56-8a91-ac9b81d6e8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752f66e80265bf7d6b3ea26e7baabdc6550ce921
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294672"
---
# <a name="performance-windows-7-developer-guide"></a>Desempenho (guia do desenvolvedor do Windows 7)

O Windows 7 maximiza a eficiência de energia de hardware e a escalabilidade, mantendo o alto desempenho. A eficiência de energia é aprimorada por meio de uma atividade de segundo plano reduzida e novo suporte para o gatilho a partir dos serviços do sistema. O Windows 7 também oferece melhorias no kernel do Windows que permitem que aplicativos e serviços sejam dimensionados com eficiência entre plataformas. O desempenho de muitos recursos e APIs é aprimorado no Windows 7 em comparação com o Windows Vista. Por exemplo, o desempenho do driver em servidores é otimizado pelo novo modo de usuário e APIs de topologia no modo kernel. A renderização de gráficos é consideravelmente mais suave e mais rápida. O desempenho de acessibilidade também é significativamente mais rápido do que antes.

## <a name="building-power-efficient-applications"></a>Criando Power-Efficient aplicativos

A criação de aplicativos eficientes de energia que aproveitam as mais recentes tecnologias de gerenciamento de energia é um desafio significativo que os desenvolvedores enfrentam hoje. Normalmente, os fabricantes de dispositivos e processadores recebem toda a atenção, pois suas ofertas mais recentes são medidas e benchmarks. No entanto, um único aplicativo pode impedir facilmente a geração mais recente de hardware de perceber seu potencial de eficiência de energia. Por exemplo, um único aplicativo que aumenta a resolução do timer da plataforma pode diminuir a vida útil da bateria em 10%.

A operação estendida com energia da bateria e o uso de tecnologias eficientes em energia são os principais requisitos para os desenvolvedores de hoje. O Windows 7 reduz consideravelmente o número de atividades que o sistema operacional executa para impedir o uso de modos de economia de energia. Ele também dá suporte ao gatilho-iniciando os serviços do sistema para permitir que os processadores se tornem ociosos com mais frequência e fiquem ociosos por mais tempo, o que diminui o consumo de energia. Além disso, o Windows 7 aproveita o hardware mais recente com eficiência de energia, incluindo adaptadores de rede, dispositivos de armazenamento e placas gráficas.

O Windows 7 fornece a infraestrutura e as ferramentas que facilitam para os desenvolvedores a determinação do impacto de energia de seus aplicativos. Um conjunto de retornos de chamada de evento permite que os aplicativos reduzam suas atividades quando o sistema está com energia da bateria e aumenta automaticamente quando o sistema está com *corrente alternada* . Para aplicativos que envolvem um processo ou serviço em segundo plano, o Windows 7 apresenta uma nova infraestrutura para habilitar automaticamente as tarefas em segundo plano quando for mais apropriado para maximizar a eficiência de energia. (Consulte [whdc performance central](https://www.microsoft.com/whdc/system/sysperf/default.mspx) e [Gerenciamento de energia na visão geral do Windows 7](https://www.climatesaverscomputing.org/wordpress/wp-content/uploads/2011/06/Power_Management_in_Windows_7_Overview.pdf).)

## <a name="service-control-manager"></a>Gerenciador de Controle de Serviço

O Windows 7Service Control Manager (SCM) foi estendido para que um serviço possa ser iniciado automaticamente e interrompido quando um evento específico do sistema, ou gatilho, ocorrer no sistema. Recursos de início de gatilho removem a necessidade de serviços para iniciarem automaticamente na inicialização do computador e, em seguida, sondar ou aguardar a ocorrência de um evento, como a chegada do dispositivo. Os eventos de gatilho comuns para os serviços incluem:

-   Chegada da interface de classe de dispositivo: Inicie um serviço somente quando um determinado tipo de dispositivo estiver presente ou anexado ao sistema.
-   Ingresso no domínio: Inicie um serviço somente se o sistema tiver ingressado em um domínio do Windows.
-   Alteração de política de Grupo: iniciar um serviço automaticamente quando as políticas de grupo forem atualizadas no sistema.
-   Chegada do endereço IP: Inicie um serviço somente quando o sistema estiver conectado à rede.

Os desenvolvedores de software podem usar os tipos de gatilho predefinidos para o Windows 7 e as opções de configuração para habilitar o recurso de início de gatilho. O 7SCM do Windows expõe um novo conjunto de APIs que permite que um serviço seja registrado para eventos de gatilho personalizados específicos. (Consulte [Gerenciador de controle de serviço](../services/service-control-manager.md).)

## <a name="windows-troubleshooting-platform"></a>Plataforma de solução de problemas do Windows

O Windows 7 fornece uma plataforma de solução de problemas abrangente e extensível que usa um mecanismo baseado no PowerShell para solucionar problemas. Os principais componentes da plataforma de solução de problemas incluem um pacote de solução de problemas, um mecanismo de solução de problemas e um assistente para solução de problemas. O pacote de solução de problemas é uma coleção de scripts do PowerShell e metadados relevantes. O mecanismo de solução de problemas inicia um tempo de execução do PowerShell para executar um pacote de solução de problemas e expõe um conjunto de interfaces para controlar a execução do pacote de solução de problemas.

O assistente para solução de problemas fornece uma experiência consistente em pacotes de solução de problemas, comunicando-se com o mecanismo de solução de problemas para solucionar problemas e resolver os que são especificados em um pacote de solução de problemas. A execução de um pacote de solução de problemas também pode ser controlada por meio de um conjunto de *commandlets* do PowerShell.

A plataforma de solução de problemas integra-se perfeitamente com o Windows 7PC Solution Center, permitindo que outros aplicativos executem o diagnóstico de maneira semelhante como parte do seu regime de gerenciamento de PC. A plataforma de solução de problemas é configurável por profissionais de ti por meio de *política de grupo* para uso dentro da empresa, e um kit de ferramentas de solução de problemas do Windows que permite aos desenvolvedores criar pacotes de solução de problemas também está disponível. (Consulte [plataforma de solução de problemas do Windows](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal).)

![interface do usuário da plataforma de solução de problemas](images/windows7-devguide-troubleshoot.jpg)

A plataforma de solução de problemas integra-se perfeitamente com o Windows 7PC Solution Center

 

 
