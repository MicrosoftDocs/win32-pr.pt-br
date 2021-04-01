---
description: A proteção de fluxo de controle (CFG) é um recurso de segurança de plataforma altamente otimizado que foi criado para combater vulnerabilidades de corrupção de memória.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Proteção de Fluxo de Controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cf97a648443135e7fee666ea4c259b1c32104e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091808"
---
# <a name="control-flow-guard"></a>Proteção de Fluxo de Controle

## <a name="what-is-control-flow-guard"></a>O que é a proteção de fluxo de controle?

A proteção de fluxo de controle (CFG) é um recurso de segurança de plataforma altamente otimizado que foi criado para combater vulnerabilidades de corrupção de memória. Ao colocar restrições rígidas sobre onde um aplicativo pode executar código, isso torna muito mais difícil para explorações executar código arbitrário por meio de vulnerabilidades como estouros de buffer. O CFG estende as tecnologias de mitigação de exploração anteriores, como [/GS](/cpp/build/reference/gs-buffer-security-check?view=vs-2019), [DEP](../memory/data-execution-prevention.md)e [ASLR](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista).

Esse recurso está disponível no Microsoft Visual Studio 2015 e é executado em versões "com reconhecimento de CFG" do Windows — as versões x86 e x64 para desktop e servidor do Windows 10 e do Windows 8.1 Update (KB3000850).

Recomendamos que os desenvolvedores habilitem o CFG para seus aplicativos. Você não precisa habilitar o CFG para cada parte do seu código, pois uma combinação de CFG habilitado e código não habilitado para CFG será executada corretamente. Mas a falha ao habilitar CFG para todo o código pode abrir lacunas na proteção. Além disso, o código de CFG habilitado funciona bem em versões "CFG sem reconhecimento" do Windows e, portanto, é totalmente compatível com eles.

## <a name="how-can-i-enable-cfg"></a>Como posso habilitar o CFG?

Na maioria dos casos, não há necessidade de alterar o código-fonte. Tudo o que você precisa fazer é adicionar uma opção ao seu projeto do Visual Studio 2015, e o compilador e o vinculador habilitarão o CFG.

O método mais simples é navegar até **Propriedades de projeto \| configurações de \| configuração \| C/C++ \| geração de código** e escolher **Sim (/Guard: CF)** para proteção de fluxo de controle.

![Propriedade cfg no Visual Studio](images/cfg-vs.png)

Como alternativa, adicione **/Guard: CF** às propriedades do projeto Propriedades de **configuração de linha de \| \| \| comando C/C++ \| \| Opções adicionais** (para o compilador) e **/Guard: CF** às propriedades do projeto Propriedades de **\| \| configuração linha de comando do \| vinculador \| \| Opções adicionais** (para o vinculador).

![Propriedade cfg para o compilador](images/cfg-compiler.png)![Propriedade cfg para o vinculador](images/cfg-linker.png)

Consulte [/Guard (habilitar proteção de fluxo de controle)](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) para obter informações adicionais.

Se você estiver criando seu projeto na linha de comando, poderá adicionar as mesmas opções. Por exemplo, se você estiver Compilando um projeto chamado Test. cpp, use **CL/Guard: CF Test. cpp/link/Guard: CF**.

Você também tem a opção de controlar dinamicamente o conjunto de endereços de destino iCal que são considerados válidos por CFG usando o [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) da API de gerenciamento de memória. A mesma API pode ser usada para especificar se as páginas são destinos inválidos ou válidos para CFG. As funções [**usar VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) e [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) , por padrão, tratam uma região especificada do executável e as páginas confirmadas como destinos de chamada indiretos válidos. É possível substituir esse comportamento, como ao implementar um compilador just-in-time, especificando **destinos de página \_ \_ inválidos** ao chamar o **VirtualAlloc** ou **o \_ direcionamento de página \_ sem \_ atualização** ao chamar **usar VirtualProtect** , conforme detalhado em [**constantes de proteção de memória**](/windows/desktop/Memory/memory-protection-constants).

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>Como faço para dizer que um binário está sob o controle do Flow Guard?

Execute a [ferramenta DUMPBIN](/cpp/build/reference/dumpbin-reference) (incluída na instalação do visual Studio 2015) no prompt de comando do Visual Studio com as opções */Headers* e */loadconfig* : **DUMPBIN/Headers/loadconfig test.exe**. A saída de um binário em CFG deve mostrar que os valores de cabeçalho incluem "Guard" e que os valores de configuração de carga incluem "CF instrumentado" e "tabela FID presente".

![saída de DUMPBIN/Headers](images/cfg-dumpbin-headers.png)

![saída de DUMPBIN/loadconfig](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>Como o CFG realmente funciona?

As vulnerabilidades de software são frequentemente exploradas fornecendo dados pouco, incomuns ou extremos a um programa em execução. Por exemplo, um invasor pode explorar uma vulnerabilidade de estouro de buffer fornecendo mais entrada a um programa do que o esperado e, assim, executando em excesso a área reservada pelo programa para manter uma resposta. Isso pode corromper a memória adjacente que pode conter um ponteiro de função. Quando o programa chama essa função, ele pode então saltar para um local indesejado especificado pelo invasor.

No entanto, uma combinação potente de compilação e suporte de tempo de execução do CFG implementa a integridade do fluxo de controle que restringe rigorosamente onde as instruções de chamada indireta podem ser executadas.

O compilador faz o seguinte:

1.  Adiciona verificações de segurança leves ao código compilado.
2.  Identifica o conjunto de funções no aplicativo que são destinos válidos para chamadas indiretas.

O suporte ao tempo de execução, fornecido pelo kernel do Windows:

1.  Mantém o estado com eficiência que identifica destinos de chamada indiretos válidos.
2.  Implementa a lógica que verifica se um destino de chamada indireta é válido.

Para ilustrar:

![o pseudocódigo de cfg](images/cfg-pseudocode.jpg)

Quando uma verificação de CFG falha em tempo de execução, o Windows imediatamente encerra o programa, interrompendo qualquer exploração que tente chamar indiretamente um endereço inválido.

 

 
