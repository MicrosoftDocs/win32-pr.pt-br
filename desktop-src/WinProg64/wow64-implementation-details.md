---
title: Detalhes da implementação do WOW64
description: O emulador WOW64 é executado no modo de usuário.
ms.assetid: 93daf9d0-dfdb-42c3-8c3d-397b21991e83
keywords:
- Programação WOW64 de 64 bits do Windows, variáveis de ambiente
- Programação do Windows para WOW64 de 64 bits, implementação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7d095369b883171e39bffd4dc629b7f80a7f39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084637"
---
# <a name="wow64-implementation-details"></a>Detalhes da implementação do WOW64

O emulador WOW64 é executado no modo de usuário. Ele fornece uma interface entre a versão de 32 bits do Ntdll.dll e o kernel do processador e intercepta chamadas de kernel. O emulador WOW64 consiste nas seguintes DLLs:

-   Wow64.dll fornece a infraestrutura de emulação de núcleo e as conversões para o Ntoskrnl.exe funções de ponto de entrada.
-   Wow64Win.dll fornece conversões para o Win32k.sys funções de ponto de entrada.
-   (somente x64) Wow64Cpu.dll fornece suporte para a execução de programas x86 em x64.
-   (Somente Intel Itanium) IA32Exec. bin contém o emulador de software x86.
-   (Somente Intel Itanium) Wowia32x.dll fornece a interface entre IA32Exec. bin e WOW64.
-   (Somente ARM64) xtajit.dll contém o emulador de software x86.
-   (Somente ARM64) wowarmw.dll fornece suporte para a execução de programas do ARM32 no ARM64.

Essas DLLs, juntamente com a versão de 64 bits do Ntdll.dll, são os únicos binários de 64 bits que podem ser carregados em um processo de 32 bits. No Windows 10 no ARM, os binários CHPE (compilação portátil híbrida compilado) também podem ser carregados em um processo x86 de 32 bits.

Na inicialização, Wow64.dll carrega a versão x86 do Ntdll.dll (ou a versão CHPE, se habilitada) e executa seu código de inicialização, que carrega todas as DLLs de 32 bits necessárias. Quase todas as DLLs de 32 bits são cópias não modificadas de binários do Windows de 32 bits, embora algumas sejam carregadas como CHPE por motivos de desempenho. Algumas dessas DLLs são escritas para se comportar de forma diferente no WOW64 do que nas janelas de 32 bits, geralmente porque compartilham memória com componentes de sistema de 64 bits. Todo o espaço de endereço de modo de usuário acima do limite de 32 bits é reservado pelo sistema. Para obter mais informações, consulte [desempenho e consumo de memória em WOW64](performance-and-memory-consumption.md).

Em vez de usar a sequência de chamada de serviço do sistema x86, os binários de 32 bits que fazem chamadas do sistema são recriados para usar uma sequência de chamada personalizada. Essa sequência de chamada é barata para o WOW64 interceptar porque permanece inteiramente no modo de usuário. Quando a sequência de chamada personalizada é detectada, a CPU do WOW64 faz a transição de volta para o modo de 64 bits nativo e chama Wow64.dll. A conversão é feita no modo de usuário para reduzir o impacto no kernel de 64 bits e reduzir o risco de um bug na conversão que pode causar uma falha no modo kernel, corrupção de dados ou uma brecha de segurança. As conversões extraem argumentos da pilha de 32 bits, estendem-as para 64 bits e, em seguida, fazem a chamada nativa do sistema.

## <a name="environment-variables"></a>Variáveis de ambiente

Quando um processo de 32 bits é criado por um processo de 64 bits, ou quando um processo de 64 bits é criado por um processo de 32 bits, o WOW64 define as variáveis de ambiente para o processo criado, conforme mostrado na tabela a seguir.



| Processar                   | Variáveis de ambiente                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| processo de 64 bits<br/> | Arquitetura do processador \_ = AMD64 ou \_ arquitetura do processador = arquitetura do processador/IA64 = \_ ARM64<br/> ProgramFiles =% ProgramFiles%<br/> ProgramW6432 =% ProgramFiles%<br/> CommonProgramFiles =% CommonProgramFiles%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** As variáveis de ambiente ProgramW6432 e CommonProgramW6432 foram adicionadas a partir do Windows 7 e do Windows Server 2008 R2. <br/> |
| processo de 32 bits<br/> | Arquitetura do processador \_ = x86<br/> ARCHITEW6432 do processador \_ =% \_ arquitetura do processador%<br/> ProgramFiles =% ProgramFiles (x86)%<br/> ProgramW6432 =% ProgramFiles%<br/> CommonProgramFiles =% CommonProgramFiles (x86)%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/>                                                                                                                                                                                                                  |



 

## <a name="global-hooks"></a>Ganchos globais

A função [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) pode ser usada para injetar uma dll em outro processo se as seguintes condições forem atendidas:

-   Uma DLL de 32 bits pode ser injetada somente em um processo de 32 bits, e uma DLL de bits de 64 pode ser injetada somente em um processo de 64 bits. Não é possível injetar uma DLL de 32 bits em um processo de 64 bits ou vice-versa.
-   As DLLs de 32 bits e 64 bits devem ter nomes diferentes.
-   As arquiteturas da DLL e o processo devem corresponder. Por exemplo, você não pode injetar uma DLL x86 de 32 bits em um processo ARM de 32 bits.

Para obter mais informações, consulte [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).

Lembre-se de que o **\_ mouse do qu**, o **\_ teclado** do qu, o **\_ diário \*** do qu, o **\_ shell do qu** e os ganchos de nível baixo podem ser chamados no thread que instalou o gancho, em vez do thread que está processando o gancho. Para esses ganchos, é possível que os ganchos de 32 bits e 64 bits sejam chamados se um gancho de 32 bits estiver à frente de um gancho de 64 bits na cadeia de ganchos. Para obter mais informações, consulte [usando ganchos](../winmsg/using-hooks.md).

 

