---
description: Para o usuário, o sistema parece estar ligado ou desligado.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: Estados de energia do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb93931326b67c7469b6a8ae256892e2dd77d4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469903"
---
# <a name="system-power-states"></a>Estados de energia do sistema

Para o usuário, o sistema parece estar ligado ou desligado. Não há outros Estados detectáveis. No entanto, o sistema dá suporte a vários Estados de energia que correspondem aos Estados de energia definidos na especificação de ACPI (interface de energia e configuração avançada). Também há variações desses Estados, como suspensão híbrida e inicialização rápida. Este tópico apresenta esses Estados e descreve como eles se relacionam entre si.

> [!NOTE]
> Os integradores de sistema e desenvolvedores que criam drivers ou aplicativos com um serviço de sistema devem ser especialmente cautelosos com problemas de qualidade de driver, como vazamentos de memória. Embora a qualidade do driver sempre tenha sido importante, o tempo de backup entre as reinicializações do kernel pode ser significativamente maior do que nas versões anteriores do sistema operacional porque, em suspensão e desligamentos iniciados pelo usuário, o kernel, os drivers e os serviços serão preservados e restaurados, não reiniciados.

 

A tabela a seguir lista os Estados de energia ACPI do consumo de energia mais alto para o mais baixo.




| Estado de energia | Estado da ACPI | Descrição | 
|-------------|------------|-------------|
| Funcionando<br /> | S0<br /> | O sistema é totalmente utilizável. Os componentes de hardware que não estão em uso podem economizar energia digitando um estado de energia menor.<br /> | 
| Modo de suspensão<br /> (Espera moderna)<br /> | Ociosidade de baixa energia em S0<br /> | Alguns sistemas SoC dão suporte a um estado ocioso de baixa energia conhecido como em <a href="/windows-hardware/design/device-experiences/modern-standby">espera moderna</a>. Nesse estado, o sistema pode mudar rapidamente de um estado de baixa energia para um estado de alta energia, para que ele possa responder rapidamente a eventos de hardware e de rede. Os sistemas que dão suporte à espera moderna não usam S1-S3.<br /> | 
| Modo de suspensão<br /> | S1<br /> S2<br /> S3<br /> | O sistema parece estar desativado. A energia consumida nesses Estados (S1-S3) é menor que S0 e mais de S4; O S3 consome menos energia do que S2 e S2 consome menos energia do que o s1. Normalmente, os sistemas dão suporte a um desses três Estados, e não todos os três.<br /> Nesses Estados (S1-S3), a memória volátil é mantida atualizada para manter o estado do sistema. Alguns componentes permanecem ligados para que o computador possa sair da entrada do teclado, da LAN ou de um dispositivo USB.<br />A <em>suspensão híbrida</em>, usada em desktops, é onde um sistema usa um arquivo de hibernação com S1-S3. O arquivo de hibernação salva o estado do sistema caso o sistema perca energia enquanto estiver em suspensão.<br /><blockquote>[!Note]<br />Os sistemas SoC que dão suporte à espera moderna (o estado ocioso de baixa energia) não usam S1-S3.</blockquote><br /><br /> | 
| Hibernar<br /> | S4<br /> | O sistema parece estar desativado. O consumo de energia é reduzido para o nível mais baixo. O sistema salva o conteúdo da memória volátil em um arquivo de hibernação para preservar o estado do sistema. Alguns componentes permanecem ligados para que o computador possa sair da entrada do teclado, da LAN ou de um dispositivo USB. O contexto de trabalho pode ser restaurado se estiver armazenado em mídia não volátil. <br /><em>Inicialização rápida</em> é onde o usuário está desconectado antes de o arquivo de hibernação ser criado. Isso permite um arquivo de hibernação menor, mais apropriado para sistemas com menos recursos de armazenamento.<br /> | 
| Soft off<br /> | S5<br /> | O sistema parece estar desativado. Esse estado é composto por um ciclo completo de desligamento e inicialização.<br /> | 
| Mecânico desativado<br /> | G3<br /> | O sistema está completamente desligado e não consome energia. O sistema retorna ao estado de trabalho somente após uma reinicialização completa.<br /> | 




 

A enumeração do [**\_ \_ estado de energia do sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) define os valores que são usados para especificar Estados de energia do sistema.

## <a name="working-state-s0"></a>Estado de funcionamento (S0)

Durante o estado de funcionamento, o sistema está ativo e em execução. Em termos simples, o dispositivo está "ligado". Se a tela estiver ativada ou desativada, o dispositivo estará em um estado de execução completa. Para conservar energia, especialmente em dispositivos com bateria, é altamente recomendável desligar os componentes de hardware quando eles não estiverem sendo usados.

> [!IMPORTANT]
> Desligue os componentes de hardware sempre que eles não estiverem sendo usados-independentemente do estado. O baixo consumo de energia é uma consideração importante para consumidores de dispositivos móveis.

 

## <a name="sleep-state-modern-standby"></a>Estado de suspensão (espera moderna)

No modo ocioso de baixa energia de S0 do estado de funcionamento, também conhecido como [espera moderna](/windows-hardware/design/device-experiences/modern-standby), o sistema permanece parcialmente em execução. Durante o modo de espera moderno, o sistema pode permanecer atualizado sempre que uma rede adequada estiver disponível e também despertar quando for necessária uma ação em tempo real, como a manutenção do sistema operacional. As ativações em espera modernas são significativamente mais rápidas do que a S1-S3. Para obter mais informações, consulte [modo de espera moderno](/windows-hardware/design/device-experiences/modern-standby).

> [!Note]  
> O modo de espera moderno só está disponível em alguns sistemas SoC. Quando há suporte, o sistema não dá suporte a S1-S3.

 

## <a name="sleep-state-s1-s3"></a>Estado de suspensão (S1-S3)

o sistema entra em suspensão com base em vários critérios, incluindo atividade de usuário ou aplicativo e preferências que o usuário define na página de **suspensão do & de energia** do aplicativo **Configurações** . Por padrão, o sistema usa o estado de suspensão mais baixo com suporte de todos os dispositivos de ativação habilitados. Para obter mais informações sobre como o sistema determina quando entrar em suspensão, consulte [critérios de suspensão do sistema](system-sleep-criteria.md).

Antes de o sistema entrar em suspensão, ele determina o estado de suspensão apropriado, notifica os aplicativos e drivers da transição pendente e, em seguida, faz a transição do sistema para o estado de suspensão. No caso de uma transição crítica, como quando o limite de bateria crítica é atingido, o sistema não notifica aplicativos e drivers. Os aplicativos precisam estar preparados para isso e executar a ação apropriada quando o sistema retornar ao estado de trabalho.

Nesses Estados (S1-S3), a memória volátil é mantida atualizada para manter o estado do sistema. Alguns componentes permanecem ligados para que o computador possa sair da entrada do teclado, da LAN ou de um dispositivo USB.

O sistema também sai do estado de suspensão em resposta à atividade do usuário ou a um evento de ativação definido por um aplicativo. Para obter mais informações, consulte [eventos de ativação do sistema](system-wake-up-events.md). A quantidade de tempo que leva o sistema para despertar depende do estado de suspensão do qual ele está saindo. O sistema leva mais tempo para ser ativado de um estado mais baixo (S3) do que de um estado de alta potência (S1) devido ao trabalho extra que o hardware pode precisar fazer (estabilizar a fonte de energia, reinicializar o processador e assim por diante).

> [!Caution]  
> Ao chamar [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate), o **valor \_ \_ necessário de es ausentes** deve ser usado somente quando absolutamente necessário por aplicativos de mídia que exigem que o sistema execute tarefas em segundo plano, como a gravação de conteúdo de televisão ou streaming de mídia para outros dispositivos enquanto o sistema parece estar em suspensão. Os aplicativos que não exigem processamento em segundo plano crítico ou que são executados em computadores portáteis não devem habilitar o modo ausente porque ele impede que o sistema contenha energia ao entrar em suspensão real.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Suspensão híbrida (S1-S3 + arquivo de hibernação)

A *suspensão híbrida* é um estado especial que é uma combinação dos Estados de suspensão e hibernação, quando um sistema usa um arquivo de hibernação com S1-S3. Ele só está disponível em alguns sistemas. Quando habilitado, o sistema grava um arquivo de hibernação, mas entra em um estado de suspensão de alta potência. Se a energia for perdida enquanto o sistema estiver em suspensão, o sistema será ativado da hibernação, o que leva mais tempo, mas restaura o estado do sistema do usuário.

## <a name="hibernate-state-s4"></a>Estado de hibernação (S4)

Windows usa a hibernação para fornecer uma experiência de inicialização rápida. Quando disponível, ele também é usado em dispositivos móveis para estender a vida útil da bateria de um sistema, fornecendo um mecanismo para salvar todo o estado do usuário antes de desligar o sistema. Em uma transição de hibernação, todo o conteúdo da memória é gravado em um arquivo na unidade do sistema primário, no *arquivo de hibernação*. Isso preserva o estado do sistema operacional, dos aplicativos e dos dispositivos. No caso em que a superfície de memória combinada consome toda a memória física, o arquivo de hibernação deve ser grande o suficiente para garantir que haverá espaço para salvar todo o conteúdo da memória física. Como os dados são gravados no armazenamento não volátil, a DRAM não precisa manter a autoatualização e pode ser desligada, o que significa que o consumo de energia da hibernação é muito baixo, quase igual ao desligamento.

Durante um desligamento completo e inicialização (S5), toda a sessão do usuário é interrompida e reiniciada na próxima inicialização. Por outro lado, durante uma S4 (hibernação), a sessão do usuário é fechada e o estado do usuário é salvo.

### <a name="fast-startup-reduced-hibernation-file"></a>Inicialização rápida (arquivo de hibernação reduzido)

A *inicialização rápida* é um tipo de desligamento que usa um arquivo de hibernação para acelerar a inicialização subsequente. Durante esse tipo de desligamento, o usuário é desconectado antes de o arquivo de hibernação ser criado. A inicialização rápida permite um arquivo de hibernação menor, mais apropriado para sistemas com menos recursos de armazenamento. Para obter mais informações, consulte [Tipos de arquivo de hibernação](#hibernation-file-types).

Ao usar a inicialização rápida, o sistema aparece para o usuário como se tivesse ocorrido um desligamento completo (S5), mesmo que o sistema tenha realmente passado por S4. Isso inclui como o sistema responde aos alarmes de a wake do dispositivo.

A inicialização rápida faz logon das sessões do usuário, mas o conteúdo do kernel (sessão 0) é gravado no disco rígido. Isso habilita a inicialização mais rápida.

Para iniciar programaticamente um desligamento rápido no estilo de inicialização, chame a função [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) com o sinalizador **HÍBRIDO SHUTDOWN \_** ou a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) com o sinalizador **EWX \_ HYBRID \_ SHUTDOWN.**

> [!Note]  
> Começando no Windows 8, a inicialização rápida é a transição padrão quando um desligamento do sistema é solicitado. Um desligamento completo (S5) ocorre quando uma reinicialização do sistema é solicitada (ou um aplicativo chama uma API de desligamento).

 

### <a name="entering-hibernation"></a>Inserindo hibernação

Quando uma solicitação de hibernação é feita, as seguintes etapas ocorrem à medida que o sistema entra em hibernação:

1.  Aplicativos e serviços são notificados
2.  Os drivers são notificados
3.  O estado do usuário e do sistema é salvo no disco em um formato compactado
4.  O firmware é notificado

> [!Note]  
> A partir Windows 8, todos os núcleos no sistema são usados para compactar os dados na memória e gravar no disco.

 

Para iniciar programaticamente uma transição de hibernação, chame a [**função SetSuspendState.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

### <a name="resuming-from-hibernation"></a>Retomar da hibernação

Quando um sistema é retomado da hibernação.

Quando um sistema é ligado, as etapas a seguir ocorrem à medida que o sistema é retomado da hibernação.

1.  POST do sistema
2.  A memória do sistema é descompactada e restaurada do arquivo de hibernação
3.  Inicialização do dispositivo
4.  Os drivers são restaurados para o estado em que estavam antes da hibernação
5.  Os serviços são restaurados para o estado em que estavam antes da hibernação
6.  O sistema fica disponível para logon

Um currículo da hibernação começa com um POST do sistema semelhante a um desligamento S5. O gerenciador de inicialização do sistema operacional determina que um resumo da hibernação é necessário detectando um arquivo de hibernação válido. Em seguida, ele direciona o sistema para retomar, restaurando o conteúdo da memória e todos os registros de arquitetura. No caso de uma retomada da hibernação, o conteúdo da memória do sistema é lido novamente do disco, descompactado e restaurado, colocando o sistema no estado exato em que estava quando ele estava hibernado. Depois que a memória é restaurada, os dispositivos são re-iniciados, o computador retorna para um estado de execução, pronto para logon.

> [!Note]  
> Durante uma retomada da hibernação, os drivers e os serviços são notificados, mas não são reiniciados. Eles são restaurados apenas para o estado em que estavam antes da hibernação.

 

### <a name="hibernation-file-types"></a>Tipos de arquivo de hibernação

Os arquivos de hibernação são usados para sleep híbrido, inicialização rápida e hibernação padrão (descritos anteriormente). Há dois tipos, diferenciados por tamanho, um arquivo de hibernação de tamanho completo e reduzido. Somente a inicialização rápida pode usar um arquivo de hibernação reduzido.



| Tipo de arquivo de hibernação | Tamanho padrão           | Suporta...                           |
|-----------------------|------------------------|---------------------------------------|
| Completo                  | 40% da memória física | hibernar, sleep híbrido, inicialização rápida |
| Reduzido               | 20% da memória física | inicialização rápida                          |



 

Para verificar ou alterar o tipo de arquivo de hibernação usado, execute o **utilitáriopowercfg.exe** sistema. Os exemplos a seguir demonstram como. Para obter mais informações, execute `powercfg /? hibernate`.



| Exemplo                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powercfg /a`<br/>                                                | **Verifique o tipo de arquivo de hibernação.** Quando um arquivo de hibernação completa é usado, o estado de resultados é que a hibernação é uma opção disponível. Quando um arquivo de hibernação reduzido é usado, os resultados dizem que não há suporte para hibernação. Se o sistema não tiver nenhum arquivo de hibernação, os resultados vão dizer que a hibernação não foi habilitada.<br/> |
| `powercfg /h /type full`<br/>                                     | **Altere o tipo de arquivo de hibernação para completo.** Isso não é recomendado em sistemas com menos de 32 GB de armazenamento.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Altere o tipo de arquivo de hibernação para reduzido.** Se o comando retornar "o parâmetro está incorreto", consulte o exemplo a seguir.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Tentar alterar novamente o tipo de arquivo de hibernação para reduzido.** Se o arquivo de hibernação for definido como um tamanho personalizado maior que 40%, primeiro você deverá definir o tamanho do arquivo como zero. Em seguida, repetir a configuração reduzida.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>Estado de soft-off (S5)

O estado de desagregação é quando o sistema é completamente desligado sem um arquivo de hibernação. O desligamento automático também é conhecido como um "desligamento completo". Durante um desligamento e inicialização completos, toda a sessão do usuário é dividida e reiniciada na próxima inicialização. Consequentemente, uma inicialização/inicialização desse estado leva significativamente mais tempo do que S1-S4. Um desligamento completo (S5) ocorre quando uma reinicialização do sistema é solicitada (ou um aplicativo chama uma API de desligamento).

## <a name="mechanical-off-state-g3"></a>Estado mecânico desligado (G3)

Nesse estado, o sistema está completamente desligado e não consome energia. O sistema retorna para o estado de trabalho somente após uma reinicialização completa.

## <a name="wake-on-lan-behavior"></a>Comportamento de wake-on-LAN

O recurso WAKE-on-LAN (WOL) parte do computador de um estado de baixa energia quando um adaptador de rede detecta um evento DEVA (normalmente, um pacote Ethernet especialmente construído).

HÁ suporte para o WOL em sleep (S3) ou hibernate (S4). Não há suporte para ela nos estados de inicialização rápida ou desligamento (S5). As NICs não estão sujeitas para a adoção nesses estados porque os usuários não esperam que seus sistemas sejam ativos por conta própria.

> [!Note]  
> NÃO há suporte oficial para o WOL de soft-off (S5). No entanto, o BIOS em alguns sistemas pode dar suporte a NICs de arming para a adoção, embora Windows não está envolvido no processo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciamento de Energia](about-power-management.md)
</dt> </dl>
