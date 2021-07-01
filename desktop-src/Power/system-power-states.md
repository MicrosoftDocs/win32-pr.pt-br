---
description: Para o usuário, o sistema parece estar on ou off.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: Estados de energia do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efde8a130d6dbe2b44c34e8ab45b973a64f3b255
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120811"
---
# <a name="system-power-states"></a>Estados de energia do sistema

Para o usuário, o sistema parece estar on ou off. Não há outros estados detectáveis. No entanto, o sistema dá suporte a vários estados de energia que correspondem aos estados de energia definidos na especificação Interface de Energia e Configuração Avançada (ACPI). Também há variações desses estados, como união híbrida e inicialização rápida. Este tópico apresenta esses estados e descreve como eles se relacionam entre si.

> [!NOTE]
> Os integradores do sistema e os desenvolvedores que criam drivers ou aplicativos com um serviço do sistema devem ter cuidado especial com problemas de qualidade do driver, como vazamentos de memória. Embora a qualidade do driver sempre tenha sido importante, o tempo de inativo entre as reinicializações do kernel pode ser significativamente maior do que nas versões anteriores do sistema operacional porque, em suspensão e desligamentos iniciados pelo usuário, o kernel, os drivers e os serviços serão preservados e restaurados, não reiniciados.

 

A tabela a seguir lista os estados de energia do ACPI do consumo de energia mais alto para o menor.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado de energia</th>
<th>Estado de ACPI</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Funcionando<br/></td>
<td>S0<br/></td>
<td>O sistema é totalmente acessível. Componentes de hardware que não estão em uso podem economizar energia inserindo um estado de energia inferior.<br/></td>
</tr>
<tr class="even">
<td>Modo de suspensão<br/> (Espera moderna)<br/></td>
<td>S0 de baixa potência ociosa<br/></td>
<td>Alguns sistemas SoC suportam um estado ocioso de baixa potência conhecido como <a href="/windows-hardware/design/device-experiences/modern-standby">Espera Moderna.</a> Nesse estado, o sistema pode mudar muito rapidamente de um estado de baixa energia para um estado de alta potência, para que ele possa responder rapidamente a eventos de hardware e rede. Sistemas que suportam Espera Moderna não usam S1-S3.<br/></td>
</tr>
<tr class="odd">
<td>Modo de suspensão<br/></td>
<td>S1<br/> S2<br/> S3<br/></td>
<td>O sistema parece estar desligado. A energia consumida nesses estados (S1-S3) é menor que S0 e mais que S4; S3 consome menos energia do que S2 e S2 consome menos energia do que S1. Os sistemas normalmente suportam um desses três estados, não todos os três.<br/> Nesses estados (S1-S3), a memória volátil é mantida atualizada para manter o estado do sistema. Alguns componentes permanecem alimentados para que o computador possa ser acionado da entrada do teclado, da LAN ou de um dispositivo USB.<br/> <em>O compartilhamento</em>híbrido , usado em áreas de trabalho, é onde um sistema usa um arquivo de hibernação com S1-S3. O arquivo de hibernação salva o estado do sistema caso o sistema perca energia enquanto está em sleep.<br/>
<blockquote>
[!Note]<br />
Sistemas soC que suportam espera moderna (o estado ocioso de baixa potência) não usam S1-S3.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Hibernar<br/></td>
<td>S4<br/></td>
<td>O sistema parece estar desligado. O consumo de energia é reduzido para o nível mais baixo. O sistema salva o conteúdo da memória volátil em um arquivo de hibernação para preservar o estado do sistema. Alguns componentes permanecem alimentados para que o computador possa ser acionado da entrada do teclado, da LAN ou de um dispositivo USB. O contexto de trabalho poderá ser restaurado se ele for armazenado em mídia nãovolatile. <br/> <em>A inicialização</em> rápida é o local em que o usuário é desconectado antes que o arquivo de hibernação seja criado. Isso permite um arquivo de hibernação menor, mais apropriado para sistemas com menos recursos de armazenamento.<br/></td>
</tr>
<tr class="odd">
<td>Soft-off<br/></td>
<td>S5<br/></td>
<td>O sistema parece estar desligado. Esse estado é composto por um ciclo completo de desligamento e inicialização.<br/></td>
</tr>
<tr class="even">
<td>Mecânico desligado<br/></td>
<td>G3<br/></td>
<td>O sistema está completamente desligado e não consome energia. O sistema retorna para o estado de trabalho somente após uma reinicialização completa.<br/></td>
</tr>
</tbody>
</table>



 

A [**\_ enumeração SYSTEM POWER \_ STATE**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) define valores usados para especificar estados de energia do sistema.

## <a name="working-state-s0"></a>Estado de trabalho (S0)

Durante o estado de trabalho, o sistema é ativo e em execução. Em termos simples, o dispositivo está "on". Se a tela está ligado ou desligado, o dispositivo está em um estado de execução completa. Para economizar energia, especialmente em dispositivos com bateria, é altamente recomendável a energia dos componentes de hardware quando eles não estão sendo usados.

> [!IMPORTANT]
> A energia dos componentes de hardware sempre que eles não estão sendo usados , independentemente do estado. O baixo consumo de energia é uma consideração importante para os consumidores de dispositivo móvel.

 

## <a name="sleep-state-modern-standby"></a>Estado de espera (espera moderna)

No modo ocioso de baixa potência S0 do estado de trabalho, também conhecido como Espera [Moderna,](/windows-hardware/design/device-experiences/modern-standby)o sistema permanece parcialmente em execução. Durante a Espera Moderna, o sistema pode se manter atualizado sempre que uma rede adequada estiver disponível e também ser a wake quando uma ação em tempo real for necessária, como a manutenção do sistema operacional. O Modo de Espera Moderno é muito mais rápido do que o S1-S3. Para obter mais informações, consulte [Modern Standby](/windows-hardware/design/device-experiences/modern-standby).

> [!Note]  
> O Modo de Espera Moderno só está disponível em alguns sistemas SoC. Quando há suporte, o sistema não dá suporte a S1-S3.

 

## <a name="sleep-state-s1-s3"></a>Estado de sleep (S1-S3)

O sistema entra em sleep com base em vários **critérios,** incluindo a atividade do usuário ou do aplicativo e as preferências que o usuário define na página **de avaliação** do Power & do aplicativo Configurações. Por padrão, o sistema usa o estado de enseada mais baixo com suporte por todos os dispositivos de acionados habilitados. Para obter mais informações sobre como o sistema determina quando entrar em suspensão, consulte [Critérios de suspensão do sistema.](system-sleep-criteria.md)

Antes que o sistema entre em suspensão, ele determina o estado de suspensão apropriado, notifica aplicativos e drivers da transição pendente e, em seguida, faz a transição do sistema para o estado de suspensão. No caso de uma transição crítica, como quando o limite crítico da bateria é atingido, o sistema não notifica aplicativos e drivers. Os aplicativos precisam estar preparados para isso e tomar as medidas apropriadas quando o sistema retornar ao estado de trabalho.

Nesses estados (S1-S3), a memória volátil é mantida atualizada para manter o estado do sistema. Alguns componentes permanecem alimentados para que o computador possa ser acionado da entrada do teclado, da LAN ou de um dispositivo USB.

O sistema também é desapertado em resposta à atividade do usuário ou a um evento de a wake-up definido por um aplicativo. Para obter mais informações, consulte [Eventos de a wake-up do sistema.](system-wake-up-events.md) A quantidade de tempo que o sistema leva para ser a wake depende do estado de sleep do seu estado. O sistema leva mais tempo para ser acionado de um estado de alimentação inferior (S3) do que de um estado de maior potência (S1) devido ao trabalho extra que o hardware pode ter que fazer (estabilizar a fonte de alimentação, reinicializar o processador e assim por diante).

> [!Caution]  
> Ao chamar [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate), o valor DE **ES \_ AWAYMODE \_ REQUIRED** deve ser usado somente quando absolutamente necessário por aplicativos de mídia que exigem que o sistema execute tarefas em segundo plano, como gravação de conteúdo de tv ou mídia de streaming para outros dispositivos enquanto o sistema parece estar em união. Aplicativos que não exigem processamento crítico em segundo plano ou que são executados em computadores portáteis não devem habilitar o modo de distância, pois impedem que o sistema conservar energia inserindo o sleep verdadeiro.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Sleep híbrido (S1-S3 + arquivo de hibernação)

*O compartilhamento* híbrido é um estado especial que é uma combinação dos estados de sleep e hibernação, é quando um sistema usa um arquivo de hibernação com S1-S3. Ele só está disponível em alguns sistemas. Quando habilitada, o sistema grava um arquivo de hibernação, mas entra em um estado de sleep de maior potência. Se a energia for perdida enquanto o sistema estiver em restabelecimento, o sistema será desaperdado da hibernação, o que leva mais tempo, mas restaura o estado do sistema do usuário.

## <a name="hibernate-state-s4"></a>Estado de hibernação (S4)

O Windows usa a hibernação para fornecer uma experiência de inicialização rápida. Quando disponível, ele também é usado em dispositivos móveis para estender a vida útil da bateria de um sistema, dando um mecanismo para salvar todo o estado do usuário antes de desligar o sistema. Em uma transição de Hibernação, todo o conteúdo da memória é gravado em um arquivo na unidade do sistema primário, o *arquivo de hibernação*. Isso preserva o estado do sistema operacional, aplicativos e dispositivos. No caso em que o volume de memória combinado consome toda a memória física, o arquivo de hibernação deve ser grande o suficiente para garantir que haja espaço para salvar todo o conteúdo da memória física. Como os dados são gravados em armazenamento não volátil, o DRAM não precisa manter a atualização automática e pode ser desligado, o que significa que o consumo de energia de hibernação é muito baixo, quase o mesmo que desligar.

Durante um desligamento completo e a inicialização (S5), toda a sessão do usuário é dividida e reiniciada na próxima inicialização. Por outro lado, durante uma hibernação (S4), a sessão do usuário é fechada e o estado do usuário é salvo.

### <a name="fast-startup-reduced-hibernation-file"></a>Inicialização rápida (arquivo de hibernação reduzido)

*A inicialização* rápida é um tipo de desligamento que usa um arquivo de hibernação para acelerar a inicialização subsequente. Durante esse tipo de desligamento, o usuário é desconectado antes que o arquivo de hibernação seja criado. A inicialização rápida permite um arquivo de hibernação menor, mais apropriado para sistemas com menos recursos de armazenamento. Para obter mais informações, consulte [tipos de arquivo de hibernação](#hibernation-file-types).

Ao usar a inicialização rápida, o sistema aparece para o usuário como se houvesse um desligamento completo (S5), mesmo que o sistema tenha sido realmente passado por meio de S4. Isso inclui como o sistema responde aos alarmes de ativação do dispositivo.

Os logs de inicialização rápida desativam sessões de usuário, mas o conteúdo do kernel (sessão 0) é gravado no disco rígido. Isso permite uma inicialização mais rápida.

Para iniciar programaticamente um desligamento rápido no estilo de inicialização, chame a função [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) com o sinalizador **\_ híbrido de desligamento** ou a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) com o sinalizador de **\_ \_ desligamento híbrido EWX** .

> [!Note]  
> A partir do Windows 8, a inicialização rápida é a transição padrão quando um desligamento do sistema é solicitado. Um desligamento completo (S5) ocorre quando uma reinicialização do sistema é solicitada (ou um aplicativo chama uma API de desligamento).

 

### <a name="entering-hibernation"></a>Entrando na hibernação

Quando uma solicitação de hibernação é feita, as seguintes etapas ocorrem quando o sistema entra em hibernação:

1.  Aplicativos e serviços são notificados
2.  Os drivers são notificados
3.  O usuário e o estado do sistema são salvos em disco em um formato compactado
4.  O firmware é notificado

> [!Note]  
> A partir do Windows 8, todos os núcleos no sistema são usados para compactar os dados na memória e gravá-los em disco.

 

Para iniciar programaticamente uma transição de hibernação, chame a função [**Setsuspendestate**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

### <a name="resuming-from-hibernation"></a>Retomando da hibernação

Quando um sistema é retomado da hibernação.

Quando um sistema é ligado, as etapas a seguir ocorrem quando o sistema é retomado da hibernação.

1.  POSTAgem do sistema
2.  A memória do sistema é descompactada e restaurada do arquivo de hibernação
3.  Inicialização do dispositivo
4.  Os drivers são restaurados para o estado em que estavam antes da hibernação
5.  Os serviços são restaurados para o estado em que estavam antes da hibernação
6.  O sistema fica disponível para logon

Um reinício da hibernação começa com uma POSTAgem do sistema que é semelhante a um desligamento de s5. O Gerenciador de inicialização do sistema operacional determina que uma retomada da hibernação é necessária detectando um arquivo de hibernação válido. Em seguida, ele direciona o sistema para retomar, restaurando o conteúdo da memória e todos os registradores de arquitetura. No caso de uma retomada da hibernação, o conteúdo da memória do sistema é lido de volta no disco, descompactado e restaurado, colocando o sistema no estado exato em que estava em hibernação. Depois que a memória é restaurada, os dispositivos são reiniciados, o computador retorna para um estado de execução, pronto para o logon.

> [!Note]  
> Durante um reinício da hibernação, os drivers e serviços são notificados, mas não são reiniciados. Eles são restaurados somente no estado em que estavam antes da hibernação.

 

### <a name="hibernation-file-types"></a>Tipos de arquivo de hibernação

Os arquivos de hibernação são usados para suspensão híbrida, inicialização rápida e hibernação padrão (descrito anteriormente). Há dois tipos, diferenciados por tamanho, um arquivo de hibernação de tamanho completo e reduzido. Somente a inicialização rápida pode usar um arquivo de hibernação reduzido.



| Tipo de arquivo de hibernação | Tamanho padrão           | Dá suporte a...                           |
|-----------------------|------------------------|---------------------------------------|
| Completo                  | 40% da memória física | hibernação, suspensão híbrida, inicialização rápida |
| Reduzido               | 20% da memória física | inicialização rápida                          |



 

Para verificar ou alterar o tipo de arquivo de hibernação usado, execute o utilitário **powercfg.exe** . Os exemplos a seguir demonstram como. Para obter mais informações, execute `powercfg /? hibernate`.



| Exemplo                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powercfg /a`<br/>                                                | **Verifique o tipo de arquivo de hibernação.** Quando um arquivo de hibernação completo é usado, os resultados são o estado em que a hibernação é uma opção disponível. Quando um arquivo de hibernação reduzido for usado, os resultados não terão suporte para hibernação. Se o sistema não tiver nenhum arquivo de hibernação, os resultados irão dizer que a hibernação não foi habilitada.<br/> |
| `powercfg /h /type full`<br/>                                     | **Altere o tipo de arquivo de hibernação para completo.** Isso não é recomendado em sistemas com menos de 32 GB de armazenamento.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Altere o tipo de arquivo de hibernação para reduzido.** Se o comando retornar "o parâmetro está incorreto", consulte o exemplo a seguir.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Repita a alteração do tipo de arquivo de hibernação para reduzido.** Se o arquivo de hibernação for definido como um tamanho personalizado maior que 40%, você deverá primeiro definir o tamanho do arquivo como zero. Em seguida, repita a configuração reduzida.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>Estado de soft off (S5)

O estado soft off é quando o sistema é desligado completamente sem um arquivo de hibernação. O soft off também é conhecido como "desligamento completo". Durante um desligamento completo e uma inicialização, toda a sessão do usuário é interrompida e reiniciada na próxima inicialização. Consequentemente, uma inicialização/inicialização a partir desse Estado leva significativamente mais tempo do que S1-S4. Um desligamento completo (S5) ocorre quando uma reinicialização do sistema é solicitada (ou um aplicativo chama uma API de desligamento).

## <a name="mechanical-off-state-g3"></a>Estado mecânico desligado (G3)

Nesse estado, o sistema está completamente desligado e não consome energia. O sistema retorna ao estado de trabalho somente após uma reinicialização completa.

## <a name="wake-on-lan-behavior"></a>Comportamento de Wake-on-LAN

O recurso WOL (Wake-on-LAN) ativa o computador a partir de um estado de baixa energia quando um adaptador de rede detecta um evento WOL (normalmente, um pacote Ethernet especialmente construído).

O WOL tem suporte do modo de suspensão (S3) ou hibernar (S4). Não há suporte para os Estados de desligamento de inicialização rápida ou S5 (soft off). As NICs não são munidas por despertar nesses Estados porque os usuários não esperam que seus sistemas sejam ativados por conta própria.

> [!Note]  
> O WOL não é oficialmente suportado do soft off (S5). No entanto, o BIOS em alguns sistemas pode dar suporte a NICs preparar para Wake, mesmo que o Windows não esteja envolvido no processo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> </dl>
