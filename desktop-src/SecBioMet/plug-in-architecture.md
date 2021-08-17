---
title: Arquitetura de plug-in
description: As unidades biométricas expõem os recursos de um dispositivo para a estrutura por meio de uma interface padrão que consiste em adaptadores de sensor, mecanismo e armazenamento.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33a82f85387698f7fb80c65525004ac541a1108635ca3d929adda7b0cbb932cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411056"
---
# <a name="plug-in-architecture"></a>Arquitetura de plug-in

Os dispositivos biométricos são fabricados em uma ampla variedade de tipos e configurações. O Windows Biometric Framework aborda essa variedade fornecendo uma arquitetura extensível que permite que desenvolvedores de terceiros criem componentes de plug-in personalizados. O componente primário é um objeto de software chamado unidade biométrica. As unidades biométricas expõem os recursos de um dispositivo para a estrutura por meio de uma interface padrão que consiste em adaptadores de sensor, mecanismo e armazenamento. Unidades biométricas e seus componentes constituintes são discutidos nos tópicos a seguir.

## <a name="biometric-unit"></a>Unidade biométrica

O componente central da arquitetura de plug-in do Windows Biometric Framework é a unidade biométrica, um objeto de software que expõe os recursos de um dispositivo biométrico para a estrutura por meio de uma interface padrão.

Um único sensor físico é associado a cada unidade biométrica. O sensor captura dados biométricos e também pode, dependendo de seus recursos de hardware, executar outras operações biométricas, como correspondência de modelo e armazenamento. Sensores que não são compatíveis com a correspondência de integração ou armazenamento exigem módulos de software adicionais para executar essas funções. Para obter mais informações, consulte [Adaptadores](/previous-versions//dd401508(v=vs.85)).

A ilustração a seguir mostra como os dados fluem por meio de uma unidade biométrica. Essencialmente, o fluxo de dados forma um tipo de pipeline. A entrada inicial para o pipeline é uma amostra biométrica capturada por um sensor físico. O mecanismo tenta corresponder o exemplo a modelos que já existem no armazenamento de modelos ou, se nenhuma combinação for encontrada, criará um novo modelo com base em amostras físicas repetidas e salvará o modelo no armazenamento.

![dados que fluem por uma unidade biométrica](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Ciclo de vida da unidade biométrica

### <a name="creation"></a>Criação

Quando o Serviço Biométrico do Windows é iniciado ou quando recebe uma notificação de hardware do gerenciador do Plug and Play, ele verifica se há qualquer hardware compatível com o CONHECIDO GUID \_ DEVINTERFACE \_ BIOMETRIC \_ READER (E2B5183A-99EA-4cc3-AD6B-80CA8D715B80). Para cada dispositivo biométrico, ele foi descoberto:

-   Abre um alça para o dispositivo.
-   Consulta os recursos do dispositivo usando uma interface de controle Windows Driver Biométrico.
-   Abre a chave do Registro do dispositivo e tenta localizar informações sobre os plug-ins de adaptador associados.
-   Abre a Windows do Registro do Serviço Biométrico e pesquisa informações sobre quaisquer plug-ins globais que devem substituir os valores específicos do dispositivo encontrados na etapa anterior.
-   Cria uma unidade biométrica para representar o dispositivo e passa a unidade para um provedor de serviços biométricos.

### <a name="configuration"></a>Configuração

Depois que um BSP (provedor de serviços biométricos) aceita uma unidade biométrica, ele configura a unidade e a atribui a um pool de sensor. Para obter mais informações, consulte [Pools de sensor](sensor-pools.md). A unidade é configurada carregando os adaptadores apropriados, conectando-se a um armazenamento de modelos e possivelmente alterando o modo de operação. Uma unidade biométrica pode ser configurada para operar em um dos dois modos:

-   No modo básico, a unidade atua como um dispositivo de captura simples. Ele não usa processamento ou armazenamento de integração, mas depende inteiramente de adaptadores de software para suporte adicional. Ele deve ser capaz de gerar exemplos em um formato padrão. Por exemplo, leitores de impressão digital devem gerar amostras que estão em conformidade com ANSI INCITS 381-2004. A finalidade do modo básico é dar suporte à interoperabilidade entre componentes de fornecedores diferentes.
-   No modo avançado, a unidade biométrica usa funções de processamento e armazenamento de integração. Ele deve expor as interfaces padrão, mas pode gerar e processar exemplos em qualquer formato desejado.

Quando uma unidade biométrica é movida de um pool de sensor para outro, seus adaptadores são descarregados e reconfigurados para o novo pool de sensor. A identidade da unidade biométrica permanece constante; somente a configuração de hardware e os plug-ins do adaptador mudam.

### <a name="shut-down"></a>Desligar

Quando o Windows Biométrico é desligado ou quando o Plug and Play de dados notifica que uma unidade foi removida, o serviço exclui todas as unidades biométricas.

## <a name="adapters"></a>Adaptadores

Componentes de software de plug-in chamados adaptadores conectam uma unidade biométrica ao hardware subjacente e fornecem qualquer funcionalidade que possa estar ausente do hardware do sensor. Há três tipos de adaptadores que você pode criar:

-   Um adaptador de sensor envolve um dispositivo biométrico e fornece uma interface padrão para configurar o sensor, capturar exemplos e controlar o fluxo de dados biométricos para o mecanismo de processamento.
-   Um adaptador de mecanismo gera modelos biométricos de exemplos capturados, corresponde exemplos a modelos existentes e indexa modelos.
-   Um adaptador de armazenamento gerencia bancos de dados de modelo.

Os adaptadores podem ser carregados e descarregados em runtime. Isso permite que o Windows Biométrico reconfigure dinamicamente uma unidade biométrica conectando-a a um conjunto diferente de adaptadores.

Por fim, cada uma das interfaces de adaptador de sensor, mecanismo e armazenamento expõe dois métodos, **ControlUnit** e **ControlUnitPrivileged,** que permitem que os aplicativos cliente acessem as funcionalidades personalizadas do adaptador definidas pelo fornecedor. Isso permite que o fornecedor defina um conjunto quase ilimitado de operações de controle para um dispositivo. Além disso, ao escolher qual função implementar, um fornecedor pode optar por disponibilizar algumas operações de controle para usuários sem privilégios, restringindo outras operações a usuários privilegiados.

Para obter mais informações sobre como criar adaptadores, consulte [Criar plug-ins de adaptador](creating-adapter-plug-ins.md).

## <a name="adapter-performance-requirements"></a>Requisitos de desempenho do adaptador

Como o objetivo é uma resposta rápida geral, o desempenho de um adaptador não é especificado em termos de limites de tempo em rotinas específicas. Em vez disso, o desempenho é especificado como um conjunto de requisitos para a experiência geral do usuário.

Há dois requisitos:

-   Qualquer interação entre o usuário e o sistema operacional que envolva biometria deve ser concluída dentro de dois segundos. Esse intervalo mede a hora de início a fim que o usuário percebe desde o momento em que toca ou passa o dedo no sensor até o momento em que algo visível ocorre na tela do dispositivo. (Por exemplo, durante o desbloqueio, não deve haver mais de um atraso de dois segundos entre o usuário tocar ou passar o passar o sensor de impressão digital e a tela de bloqueio confirmando a identidade do usuário.)
-   Para a aparência inicial dos blocos de credencial na tela de login ou bloqueio, permitimos um pouco mais de tempo (três segundos, máximo), mas ainda preferiremos mais cedo do que mais tarde. Especificamente, o painel de bio precisa estar visível na tela em até três segundos após a aparência do painel de bloqueio ou de logon.

Esses números não são arbitrários. Vários estudos mostraram que seres humanos tendem a experimentar tudo o que acontece dentro de um intervalo de dois segundos como parte do momento "agora". Se o evento A e o evento B ocorrerem dentro de dois segundos uns dos outros, as pessoas perceberão esses eventos como simultâneos. Se os eventos são separados por mais de cerca de três segundos, as pessoas pensam que há um atraso– elas acham que algo está "demorando muito". Portanto, esse é um problema de saúde humana com fio.

 

 