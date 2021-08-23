---
description: O CFG (Control Flow Guard) é um recurso de segurança de plataforma altamente otimizado que foi criado para combater vulnerabilidades de corrupção de memória.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Proteção de Fluxo de Controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62186a86f821e7eb350381c7dfbc500c80dd040f4321a8f630c7d408937a8460
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622796"
---
# <a name="control-flow-guard"></a>Proteção de Fluxo de Controle

## <a name="what-is-control-flow-guard"></a>O que é o Control Flow Guard?

O CFG (Control Flow Guard) é um recurso de segurança de plataforma altamente otimizado que foi criado para combater vulnerabilidades de corrupção de memória. Ao colocar restrições rígidas sobre onde um aplicativo pode executar código, torna muito mais difícil para explorações executar código arbitrário por meio de vulnerabilidades como estouros de buffer. O CFG estende tecnologias de mitigação de exploração anteriores, como [/GS,](/cpp/build/reference/gs-buffer-security-check?view=vs-2019) [DEP](../memory/data-execution-prevention.md)e [ASLR.](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista)

Esse recurso está disponível no Microsoft Visual Studio 2015 e é executado em versões "com suporte para CFG" do Windows – as versões x86 e x64 para Desktop e Server do Windows 10 e Windows 8.1 Update (KB3000850).

Incentivamos fortemente os desenvolvedores a habilitar o CFG para seus aplicativos. Você não precisa habilitar o CFG para cada parte do código, pois uma combinação de código habilitado para CFG e não habilitado para CFG será executada habilitada. Mas não habilitar o CFG para todo o código pode abrir lacunas na proteção. Além disso, o código habilitado para CFG funciona bem em versões "CFG-Unaware" do Windows e, portanto, é totalmente compatível com elas.

## <a name="how-can-i-enable-cfg"></a>Como habilitar o CFG?

Na maioria dos casos, não há necessidade de alterar o código-fonte. Tudo o que você precisa fazer é adicionar uma opção ao projeto Visual Studio 2015, e o compilador e o linker habilitam o CFG.

O método mais simples é navegar até Project propriedades de configuração **\| \| \| C/C++ \|** Geração de código e escolher **Sim (/guard:cf)** para Control Flow Guard.

![Propriedade cfg no Visual Studio](images/cfg-vs.png)

Como alternativa, adicione **/guard:cf** às propriedades de configuração de propriedades do Project Opções adicionais de linha de comando **\| \| \| C/C++ \| \|** (para o compilador) e **/guard:cf** para opções adicionais de linha de comando do vinculador de propriedades de configuração de propriedades do Project (para o linker). **\| \| \| \| \|**

![Propriedade cfg para o compilador](images/cfg-compiler.png)![Propriedade cfg para o linker](images/cfg-linker.png)

Consulte [/guard (Habilitar Flow Guard) para](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) obter informações adicionais.

Se você estiver criando seu projeto da linha de comando, poderá adicionar as mesmas opções. Por exemplo, se você estiver compilando um projeto chamado test.cpp, use **cl /guard:cf test.cpp /link /guard:cf**.

Você também tem a opção de controlar dinamicamente o conjunto de endereços de destino de icall que são considerados válidos pelo CFG usando [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) da memória API de Gerenciamento. A mesma API pode ser usada para especificar se as páginas são destinos inválidos ou válidos para CFG. As [**funções VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) e [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) tratarão por padrão uma região especificada de páginas executáveis e confirmadas como destinos de chamada indireta válidos. É possível substituir esse comportamento, como ao implementar um compilador Just-In-Time, especificando **PAGE \_ TARGETS \_ INVALID** ao chamar **VirtualAlloc** ou **PAGE \_ TARGETS NO \_ \_ UPDATE** ao chamar **VirtualProtect,** conforme detalhado em [**Constantes**](/windows/desktop/Memory/memory-protection-constants)de proteção de memória.

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>Como fazer para dizer que um binário está sob controle Flow Guard?

Execute a ferramenta [dumpbin](/cpp/build/reference/dumpbin-reference) (incluída na instalação do Visual Studio 2015) no prompt de comando do Visual Studio com as opções */headers* e */loadconfig:* **dumpbin /headers /loadconfig test.exe**. A saída de um binário em CFG deve mostrar que os valores de header incluem "Guard" e que os valores de configuração de carga incluem "CF Instrumentado" e "tabela FID presente".

![saída de dumpbin /headers](images/cfg-dumpbin-headers.png)

![saída de dumpbin /loadconfig](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>Como o CFG realmente funciona?

As vulnerabilidades de software geralmente são exploradas fornecendo dados improváveis, incomuns ou extremos para um programa em execução. Por exemplo, um invasor pode explorar uma vulnerabilidade de estouro de buffer fornecendo mais entrada para um programa do que o esperado, executando, assim, a área reservada pelo programa para conter uma resposta. Isso pode corromper a memória adjacente que pode conter um ponteiro de função. Quando o programa chama por essa função, ele pode ir para um local não intencional especificado pelo invasor.

No entanto, uma combinação perfeita de suporte de compilação e tempo de execução do CFG implementa a integridade do fluxo de controle que restringe firmemente o local em que as instruções de chamada indireta podem ser executadas.

O compilador faz o seguinte:

1.  Adiciona verificações de segurança leves ao código compilado.
2.  Identifica o conjunto de funções no aplicativo que são destinos válidos para chamadas indiretas.

O suporte de runtime, fornecido pelo Windows kernel:

1.  Mantém com eficiência o estado que identifica destinos de chamada indireta válidos.
2.  Implementa a lógica que verifica se um destino de chamada indireta é válido.

Para ilustrar:

![pseudocódigo cfg](images/cfg-pseudocode.jpg)

Quando uma verificação de CFG falha no runtime, Windows encerra imediatamente o programa, descumprindo assim qualquer exploração que tenta chamar indiretamente um endereço inválido.

 

 
