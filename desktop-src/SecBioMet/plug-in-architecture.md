---
title: Arquitetura de plug-in
description: As unidades biométricas expõem os recursos de um dispositivo para a estrutura por meio de uma interface padrão que consiste em adaptadores de sensor, mecanismo e armazenamento.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e43af9c0ea5a8db57cc0e0970b5625b1ba118f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454213"
---
# <a name="plug-in-architecture"></a>Arquitetura de plug-in

Os dispositivos biométricos são fabricados em uma ampla variedade de tipos e configurações. A Windows Biometric Framework aborda essa variedade fornecendo uma arquitetura extensível que permite que desenvolvedores de terceiros criem componentes de plug-ins personalizados. O componente principal é um objeto de software chamado unidade biométrica. As unidades biométricas expõem os recursos de um dispositivo para a estrutura por meio de uma interface padrão que consiste em adaptadores de sensor, mecanismo e armazenamento. As unidades biométricas e seus componentes constituintes são discutidos nos tópicos a seguir.

## <a name="biometric-unit"></a>Unidade biométrica

O componente central da arquitetura de plug-in do Windows Biometric Framework é a unidade biométrica, um objeto de software que expõe os recursos de um dispositivo biométrico à estrutura por meio de uma interface padrão.

Um único sensor físico é associado a cada unidade biométrica. O sensor captura dados biométricos e também pode, dependendo de seus recursos de hardware, executar outras operações biométricas, como correspondência de modelo e armazenamento. Os sensores que não dão suporte à correspondência integrada ou ao armazenamento exigem módulos de software adicionais para executar essas funções. Para obter mais informações, consulte [adaptadores](/previous-versions//dd401508(v=vs.85)).

A ilustração a seguir mostra como os dados fluem por meio de uma unidade biométrica. Essencialmente, o fluxo de dados forma um tipo de pipeline. A entrada inicial para o pipeline é um exemplo biométrico capturado por um sensor físico. O mecanismo tenta corresponder o exemplo aos modelos que já existem no repositório de modelos ou, se nenhuma correspondência for encontrada, criará um novo modelo a partir de amostras físicas repetidas e salvará o modelo na loja.

![fluxo de dados por meio de uma unidade biométrica](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Ciclo de vida da unidade biométrica

### <a name="creation"></a>Criação

Quando o serviço de biometria do Windows é iniciado ou quando recebe uma notificação de hardware do Gerenciador de Plug and Play, ele procura qualquer hardware que dê suporte ao \_ \_ E2B5183A-99EA-4cc3-AD6B-80CA8D715B80 (leitor biométrico DEVINTERFACE) de GUID de interface bem conhecida \_ . Para cada dispositivo biométrico descoberto, então:

-   Abre um identificador para o dispositivo.
-   Consulta os recursos do dispositivo usando uma interface de controle de driver biométrico do Windows.
-   Abre a chave do registro do dispositivo e tenta localizar informações sobre quaisquer plug-ins do adaptador associado.
-   Abre a chave do registro do serviço de biometria do Windows e procura informações sobre quaisquer plug-ins globais que devem substituir os valores específicos do dispositivo encontrados na etapa anterior.
-   Cria uma unidade biométrica para representar o dispositivo e passa a unidade para um provedor de serviços biométricos.

### <a name="configuration"></a>Configuração

Após um provedor de serviços biométricos (BSP) aceitar uma unidade biométrica, ele configurará a unidade e a atribuirá a um pool de sensores. Para obter mais informações, consulte [pools de sensores](sensor-pools.md). A unidade é configurada carregando os adaptadores apropriados, conectando-se a um repositório de modelos e possivelmente alterando o modo de operação. Uma unidade biométrica pode ser configurada para operar em um dos dois modos:

-   No modo básico, a unidade age como um dispositivo de captura simples. Ele não usa o processamento ou o armazenamento integrado, mas se baseia inteiramente em adaptadores de software para obter suporte adicional. Ele deve ser capaz de gerar amostras em um formato padrão. Por exemplo, os leitores de impressão digital devem gerar exemplos que estão em conformidade com ANSI INCITS 381-2004. A finalidade do modo básico é oferecer suporte à interoperabilidade entre componentes de fornecedores diferentes.
-   No modo avançado, a unidade biométrica usa funções de armazenamento e processamento integrado. Ele deve expor as interfaces padrão, mas pode gerar e processar amostras em qualquer formato desejado.

Quando uma unidade biométrica é movida de um pool de sensores para outro, seus adaptadores são descarregados e reconfigurados para o novo pool de sensores. A identidade da unidade biométrica permanece constante; somente a configuração de hardware e os plug-ins de adaptador são alterados.

### <a name="shut-down"></a>Desligar

Quando o serviço de biometria do Windows é desligado ou quando o Plug and Play Manager o notifica de que uma unidade foi removida, o serviço exclui todas as unidades biométricas.

## <a name="adapters"></a>Adaptadores

Os componentes de software de plug-in chamados adaptadores conectam uma unidade biométrica ao seu hardware subjacente e fornecem qualquer funcionalidade que possa estar faltando no hardware do sensor. Há três tipos de adaptadores que você pode criar:

-   Um adaptador de sensor encapsula um dispositivo biométrico e fornece uma interface padrão para configurar o sensor, capturar amostras e controlar o fluxo de dados biométricos para o mecanismo de processamento.
-   Um adaptador de mecanismo gera modelos biométricos de amostras capturadas, corresponde a amostras a modelos existentes e modelos de índices.
-   Um adaptador de armazenamento gerencia bancos de dados de modelo.

Os adaptadores podem ser carregados e descarregados em tempo de execução. Isso permite que o serviço de biometria do Windows reconfigure dinamicamente uma unidade biométrica conectando-a a um conjunto diferente de adaptadores.

Por fim, cada uma das interfaces de sensor, mecanismo e adaptador de armazenamento expõe dois métodos, **ControlUnit** e **ControlUnitPrivileged**, que permitem que os aplicativos cliente acessem os recursos de adaptador personalizado definidos pelo fornecedor. Isso permite que o fornecedor defina um conjunto quase ilimitado de operações de controle para um dispositivo. Além disso, escolhendo qual função implementar, um fornecedor pode optar por disponibilizar algumas operações de controle para usuários sem privilégios, ao mesmo tempo que restringi outras operações a usuários com privilégios.

Para obter mais informações sobre como criar adaptadores, consulte [criar plug-ins de adaptador](creating-adapter-plug-ins.md).

## <a name="adapter-performance-requirements"></a>Requisitos de desempenho do adaptador

Como o objetivo é a rápida resposta geral, o desempenho de um adaptador não é especificado em termos de limites de tempo em rotinas específicas. Em vez disso, o desempenho é especificado como um conjunto de requisitos para a experiência geral do usuário.

Há dois requisitos:

-   Qualquer interação entre o usuário e o sistema operacional que envolve a biometria deve ser concluída dentro de dois segundos. Esse intervalo mede a hora de início a término que o usuário percebe a partir do momento em que toca ou passa o sensor até o momento em que algo visível acontece na tela do dispositivo. (Por exemplo, durante o desbloqueio, não deve haver mais que um atraso de dois segundos entre o usuário tocar ou passar o sensor de impressão digital e a tela de bloqueio confirmando a identidade do usuário.)
-   Para a aparência inicial dos blocos de credencial na tela de entrada ou de bloqueio, permitimos um pouco mais de tempo (três segundos, máximo), mas ainda preferimos mais cedo, em vez de mais tarde. Especificamente, o bloco bio precisa ser visível na tela dentro de três segundos da aparência do painel de bloqueio ou de entrada.

Esses números não são arbitrários. Vários estudos mostraram que seres humanos tendem a experimentar tudo o que acontece dentro de um intervalo de dois segundos como parte do momento "agora". Se o evento A e o evento B ocorrerem dentro de dois segundos um do outro, as pessoas perceberão esses eventos como sendo simultâneos. Se os eventos forem separados por mais de três segundos, as pessoas acham que há um atraso — eles acham que algo está "demorando muito." Esse é um problema de psicologia humana fisicamente.

 

 