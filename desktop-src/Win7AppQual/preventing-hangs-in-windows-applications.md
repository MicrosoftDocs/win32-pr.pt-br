---
description: Saiba como evitar travas em aplicativos Windows para Windows 7 e Windows Server 2008 R2.
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: Prevenção de interrupções em aplicativos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5509b8733e45b105694a8bfdadddae0d67096b92c390ed98b3dd937817823b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994806"
---
# <a name="preventing-hangs-in-windows-applications"></a>Prevenção de interrupções em aplicativos do Windows

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  









## <a name="description"></a>Descrição

**Trava – Perspectiva do Usuário**

Usuários como aplicativos responsivos. Quando clicam em um menu, querem que o aplicativo reaja instantaneamente, mesmo que ele está imprimindo seu trabalho no momento. Quando eles salvam um documento longo em seu processador de palavras favorito, eles querem continuar digitando enquanto o disco ainda está girando. Os usuários são bastante rápidos quando o aplicativo não reage em tempo hábil às suas entradas.

Um programador pode reconhecer muitos motivos legítimos para um aplicativo não responder instantaneamente à entrada do usuário. O aplicativo pode estar ocupado recalculando alguns dados ou simplesmente aguardando a conclusão de sua E/S de disco. No entanto, na pesquisa de usuários, sabemos que os usuários ficam frustrados e frustrados após apenas alguns segundos de falta de resposta. Após 5 segundos, eles tentarão encerrar um aplicativo suspenso. Ao lado de falhas, travamentos de aplicativo são a fonte mais comum de interrupção do usuário ao trabalhar com aplicativos Win32.

Há muitas causas raiz diferentes para travas do aplicativo e nem todas elas se manifestam em uma interface do usuário sem resposta. No entanto, uma interface do usuário sem resposta é uma das experiências de travamento mais comuns, e esse cenário atualmente recebe mais suporte do sistema operacional para detecção e recuperação. Windows detecta automaticamente, coleta informações de depuração e, opcionalmente, encerra ou reinicia aplicativos suspensos. Caso contrário, o usuário talvez tenha que reiniciar o computador para recuperar um aplicativo suspenso.

**Trava – Perspectiva do Sistema Operacional**

Quando um aplicativo (ou com mais precisão, um thread) cria uma janela na área de trabalho, ele entra em um contrato implícito com o DWM (Gerenciador de Janelas da Área de Trabalho) para processar mensagens de janela em tempo hábil. O DWM posta mensagens (entrada de teclado/mouse e mensagens de outras janelas, bem como de si mesma) na fila de mensagens específicas do thread. O thread recupera e expedi essas mensagens por meio de sua fila de mensagens. Se o thread não for atendido pela fila chamando GetMessage(), as mensagens não serão processadas e a janela trava: ele não poderá redesenhar nem aceitar a entrada do usuário. O sistema operacional detecta esse estado anexando um temporizador a mensagens pendentes na fila de mensagens. Se uma mensagem não tiver sido recuperada dentro de 5 segundos, o DWM declarará que a janela será enforcada. Você pode consultar esse estado de janela específico por meio da API IsHungAppWindow().

A detecção é apenas a primeira etapa. Neste ponto, o usuário ainda não pode terminar o aplicativo – clicar no botão X (Fechar) resultaria em uma mensagem WM CLOSE, que estaria presa na fila de mensagens, assim como qualquer outra \_ mensagem. O Gerenciador de Janelas da Área de Trabalho ajuda ocultando e, em seguida, substituindo a janela suspenso por uma cópia 'fantasma' exibindo um bitmap da área de cliente anterior da janela original (e adicionando "Não Respondendo" à barra de título). Desde que o thread da janela original não recupere mensagens, o DWM gerencia as duas janelas simultaneamente, mas permite que o usuário interaja apenas com a cópia fantasma. Usando essa janela fantasma, o usuário só pode mover, minimizar e, o mais importante, fechar o aplicativo sem resposta, mas não alterar seu estado interno.

Toda a experiência de fantasma tem esta aparência:

![Captura de tela que mostra a caixa Bloco de notas "não está respondendo".](images/preventinghangs-ghostwindow.gif)

O Gerenciador de Janelas da Área de Trabalho faz uma última coisa; ele se integra ao Relatório de Erros do Windows, permitindo que o usuário não apenas feche e, opcionalmente, reinicie o aplicativo, mas também envie dados valiosos de depuração de volta para a Microsoft. Você pode obter esses dados de trava para seus próprios aplicativos se insplando no site do Winqual.

Windows 7 adicionou um novo recurso a essa experiência. O sistema operacional analisa o aplicativo suspenso e, em determinadas circunstâncias, oferece ao usuário a opção de cancelar uma operação de bloqueio e tornar o aplicativo responsivo novamente. A implementação atual dá suporte ao cancelamento de chamadas de soquete de bloqueio; mais operações serão canceláveis pelo usuário em versões futuras.

Para integrar seu aplicativo à experiência de recuperação de trava e tirar o máximo dos dados disponíveis, siga estas etapas:

-   Certifique-se de que seu aplicativo se registre para reinicialização e recuperação, tornando uma trava o mais forte possível para o usuário. Um aplicativo registrado corretamente pode reiniciar automaticamente com a maioria de seus dados não savados intactos. Isso funciona para travamentos e falhas do aplicativo.
-   Obter informações de frequência, bem como depurar dados para seus aplicativos suspensos e com queda no site do Winqual. Você pode usar essas informações mesmo durante sua Versão Beta para melhorar seu código. Consulte "Introdução Relatório de Erros do Windows" para uma breve visão geral.
-   Você pode desabilitar o recurso de fantasma em seu aplicativo por meio de uma chamada para DisableProcessWindowsGhosting (). No entanto, isso impede que o usuário médio seja fechado e reiniciado um aplicativo suspenso e geralmente termina em uma reinicialização.

**Trava – Perspectiva do Desenvolvedor**

O sistema operacional define um aplicativo travado como um thread de interface do usuário que não processou mensagens por pelo menos 5 segundos. Bugs óbvios causam algumas travas, por exemplo, um thread aguardando um evento que nunca é sinalizado e dois threads cada um mantendo um bloqueio e tentando adquirir os outros. Você pode corrigir esses bugs sem muito esforço. No entanto, muitas travas não são tão claras. Sim, o thread da interface do usuário não está recuperando mensagens , mas está igualmente ocupado fazendo outro trabalho "importante" e eventualmente voltará ao processamento de mensagens.

No entanto, o usuário percebe isso como um bug. O design deve corresponder às expectativas do usuário. Se o design do aplicativo levar a um aplicativo sem resposta, o design terá que mudar. Por fim, e isso é importante, a falta de resposta não pode ser corrigida como um bug de código; ele requer trabalho inicial durante a fase de design. Tentar retroajustar a base de código existente de um aplicativo para tornar a interface do usuário mais responsiva geralmente é muito cara. As diretrizes de design a seguir podem ajudar.

-   Tornar a capacidade de resposta da interface do usuário um requisito de nível superior; o usuário sempre deve se sentir no controle do seu aplicativo
-   Verifique se os usuários podem cancelar operações que levam mais de um segundo para ser concluídas e/ou que as operações podem ser concluídas em segundo plano; fornecer a interface do usuário de progresso apropriada, se necessário

![Captura de tela que mostra a caixa de diálogo 'Copiando itens'.](images/preventinghangs-progressbar.gif)

-   Enfileie operações de execução longa ou bloqueio como tarefas em segundo plano (isso requer um mecanismo de mensagens bem pensado para informar o thread da interface do usuário quando o trabalho for concluído)
-   Mantenha o código para threads de interface do usuário simples; remover o máximo possível de chamadas à API de bloqueio
-   Mostrar janelas e caixas de diálogo somente quando elas estão prontas e totalmente operacionais. Se a caixa de diálogo precisar exibir informações que são muito intensivas em recursos para calcular, mostre algumas informações genéricas primeiro e atualize-as imediatamente quando mais dados se tornar disponíveis. Um bom exemplo é a caixa de diálogo de propriedades da pasta Windows Explorer. Ele precisa exibir o tamanho total da pasta, informações que não estão prontamente disponíveis no sistema de arquivos. A caixa de diálogo aparece imediatamente e o campo "tamanho" é atualizado de um thread de trabalho:

![Captura de tela que mostra a página "Geral" Windows propriedades com o texto "Tamanho", "Tamanho no disco" e "Contém" entre círculos.](images/preventinghangs-updatingdialog.gif)

Infelizmente, não há uma maneira simples de projetar e gravar um aplicativo responsivo. Windows fornece uma estrutura assíncrona simples que permitiria o agendamento fácil de operações de bloqueio ou de execução longa. As seções a seguir apresentam algumas das práticas recomendadas para evitar travamentos e realçam algumas das armadilhas comuns.

## <a name="best-practices"></a>Práticas Recomendadas

**Manter o thread de interface do usuário simples**

A principal responsabilidade do thread de interface do usuário é recuperar e expedir mensagens. Qualquer outro tipo de trabalho apresenta o risco de suspensão das janelas pertencentes a esse thread.

**Faça:**

-   Mover algoritmos com uso intensivo de recursos ou nãobounds que resultam em operações de longa execução para threads de trabalho
-   Identifique o máximo de chamadas de função de bloqueio possível e tente movê-las para threads de trabalho; qualquer função que chama em outra DLL deve ser suspeita
-   Faça um esforço extra para remover todas as chamadas de API de rede e E/S de arquivo do thread de trabalho. Essas funções podem ser blocos por muitos segundos, se não minutos. Se você precisar fazer qualquer tipo de E/S no thread de interface do usuário, considere o uso de E/S assíncrona
-   Esteja ciente de que o thread da interface do usuário também está atendendo a todos os servidores COM STA (single-threaded apartment) hospedados pelo seu processo; Se você fizer uma chamada de bloqueio, esses servidores COM não responderão até que você faça o serviço da fila de mensagens novamente

**Não:**

-   Aguarde qualquer objeto kernel (como Event ou Mutex) por mais de um período muito curto; Se você tiver que esperar, considere usar MsgWaitForMultipleObjects(), que será desbloqueado quando uma nova mensagem chegar
-   Compartilhe a fila de mensagens da janela de um thread com outro thread usando a função AttachThreadInput(). Não é apenas extremamente difícil sincronizar corretamente o acesso à fila, mas também pode impedir que o Windows operacional detecte corretamente uma janela em espera
-   Use TerminateThread() em qualquer um dos threads de trabalho. Encerrar um thread dessa maneira não permitirá que ele libere bloqueios ou eventos de sinalização e pode resultar facilmente em objetos de sincronização órfãos
-   Chame qualquer código 'desconhecido' do thread da interface do usuário. Isso é especialmente verdadeiro se seu aplicativo tiver um modelo de extensibilidade; não há nenhuma garantia de que o código de terceiros siga suas diretrizes de capacidade de resposta
-   Fazer qualquer tipo de chamada de difusão de bloqueio; SendMessage(HWND BROADCAST) coloca você na frente de cada aplicativo mal \_ escrito atualmente em execução

**Implementar padrões assíncronos**

A remoção de operações de execução longa ou bloqueio do thread da interface do usuário requer a implementação de uma estrutura assíncrona que permite o descarregamento dessas operações para threads de trabalho.

**Faça:**

-   Use APIs de mensagem de janela assíncronas no thread da interface do usuário, especialmente substituindo SendMessage por um de seus pares sem bloqueio: PostMessage, SendNotifyMessage ou SendMessageCallback
-   Use threads em segundo plano para executar tarefas de execução longa ou de bloqueio. Usar a nova API do pool de threads para implementar seus threads de trabalho
-   Forneça suporte de cancelamento para tarefas em segundo plano de execução longa. Para bloquear operações de E/S, use o cancelamento de E/S, mas apenas como último recurso; Não é fácil cancelar a operação "correta"
-   Implementar um design assíncrono para código gerenciado usando o padrão IAsyncResult ou usando Eventos

**Usar bloqueios com cuidado**

Seu aplicativo ou DLL precisa de bloqueios para sincronizar o acesso às estruturas de dados internas. O uso de vários bloqueios aumenta o paralelismo e torna seu aplicativo mais responsivo. No entanto, o uso de vários bloqueios também aumenta a chance de adquirir esses bloqueios em ordens diferentes e fazer com que os threads bloqueem. Se dois threads cada um manterem um bloqueio e tentarem adquirir o bloqueio do outro thread, suas operações formarão uma espera circular que bloqueia qualquer progresso de avanço para esses threads. Você pode evitar esse deadlock apenas garantindo que todos os threads no aplicativo sempre adquira todos os bloqueios na mesma ordem. No entanto, nem sempre é fácil adquirir bloqueios na ordem "correta". Os componentes de software podem ser compostos, mas as aquisições de bloqueio não podem. Se o código chamar algum outro componente, os bloqueios desse componente agora se tornarão parte da ordem de bloqueio implícita, mesmo que você não tenha visibilidade sobre esses bloqueios.

As coisas ficam ainda mais difíceis porque as operações de bloqueio incluem muito mais do que as funções comuns para Seções Críticas, Mutexes e outros bloqueios tradicionais. Qualquer chamada de bloqueio que cruze os limites do thread tem propriedades de sincronização que podem resultar em um deadlock. O thread de chamada executa uma operação com semântica 'acquire' e não pode desbloquear até que o thread de destino 'versões' essa chamada. Algumas funções User32 (por exemplo, SendMessage), bem como muitas chamadas COM de bloqueio, se enquadram nessa categoria.

Pior ainda, o sistema operacional tem seu próprio bloqueio interno específico do processo que, às vezes, é mantido enquanto o código é executado. Esse bloqueio é adquirido quando as DLLs são carregadas no processo e, portanto, é chamado de 'bloqueio do carregador'. A função DllMain sempre é executada sob o bloqueio do carregador; se você adquirir bloqueios no DllMain (e não deveria), precisará fazer com que o bloqueio do carregador faça parte da ordem de bloqueio. Chamar determinadas APIs win32 também pode adquirir o bloqueio do carregador em seu nome – funções como LoadLibraryEx, GetModuleHandle e, especialmente, CoCreateInstance.

Para unir tudo isso, veja o código de exemplo abaixo. Essa função adquire vários objetos de sincronização e define implicitamente uma ordem de bloqueio, algo que não é necessariamente óbvio na inspeção de cursor. Na entrada de função, o código adquire uma Seção Crítica e não a libera até que a função saia, tornando-a o nó superior em nossa hierarquia de bloqueio. Em seguida, o código chama a função Win32 LoadIcon(), que, nos covers, pode chamar o Carregador do Sistema Operacional para carregar esse binário. Essa operação adquiriria o bloqueio do carregador, que agora também se torna parte dessa hierarquia de bloqueio (certifique-se de que a função DllMain não adquire o bloqueio g \_ cs). Em seguida, o código chama SendMessage(), uma operação de bloqueio entre threads, que não retornará, a menos que o thread da interface do usuário responda. Novamente, certifique-se de que o thread da interface do usuário nunca adquire g \_ cs.

```
bool foo::bar (char* buffer)  
{  
      EnterCriticalSection(&g_cs);  
      // Get 'new data' icon  
      this.m_Icon = LoadIcon(hInst, MAKEINTRESOURCE(5));  
      // Let UI thread know to update icon SendMessage(hWnd,WM_COMMAND,IDM_ICON,NULL);  
      this.m_Params = GetParams(buffer);  
      LeaveCriticalSection(&g_cs);
      return true;  
}  
```

Ao ver esse código, parece claro que implicitamente fizemos de g cs o bloqueio de nível superior em nossa hierarquia de bloqueio, mesmo que só quisessemos sincronizar o acesso às variáveis de membro \_ da classe.

**Faça:**

-   Projete uma hierarquia de bloqueio e obedecê-la. Adicione todos os bloqueios necessários. Há muito mais primitivos de sincronização do que apenas Mutex e CriticalSections; todos eles precisam ser incluídos. Inclua o bloqueio do carregador em sua hierarquia se você tiver algum bloqueio em DllMain()
-   Concorde com o protocolo de bloqueio com suas dependências. Qualquer código que seu aplicativo chama ou que possa chamar seu aplicativo precisa compartilhar a mesma hierarquia de bloqueio
-   Bloquear estruturas de dados não funciona. Mova as aquisições de bloqueio para fora dos pontos de entrada de função e proteger apenas o acesso a dados com bloqueios. Se menos código operar em um bloqueio, haverá menos chance de deadlocks
-   Analise as aquisições de bloqueio e as versões em seu código de tratamento de erro. Geralmente, a hierarquia de bloqueio se esqueceu ao tentar se recuperar de uma condição de erro
-   Substitua bloqueios aninhados por contadores de referência – eles não podem fazer deadlock. Elementos bloqueados individualmente em listas e tabelas são bons candidatos
-   Tenha cuidado ao aguardar uma alça de thread de uma DLL. Sempre suponha que seu código possa ser chamado sob o bloqueio do carregador. É melhor contar os recursos com referência e permitir que o thread de trabalho faça sua própria limpeza (e, em seguida, use FreeLibraryAndExitThread para terminar corretamente)
-   Use a API de Travessia da Cadeia de Espera se quiser diagnosticar seus próprios deadlocks

**Não:**

-   Faça qualquer coisa que não seja a inicialização muito simples, trabalhe em sua função DllMain(). Consulte Função de retorno de chamada DllMain para obter mais detalhes. Especialmente, não chame LoadLibraryEx ou CoCreateInstance
-   Escreva seus próprios primitivos de bloqueio. O código de sincronização personalizado pode facilmente introduzir bugs sutis em sua base de código. Em vez disso, use a seleção rica de objetos de sincronização do sistema operacional
-   Faça qualquer trabalho nos construtores e destruidores para variáveis globais, eles são executados sob o bloqueio do carregador

**Tenha cuidado com exceções**

As exceções permitem a separação do fluxo de programa normal e do tratamento de erros. Devido a essa separação, pode ser difícil saber o estado preciso do programa antes da exceção e o manipulador de exceção pode perder etapas cruciais na restauração de um estado válido. Isso é especialmente verdadeiro para aquisições de bloqueio que precisam ser liberadas no manipulador para evitar deadlocks futuros.

O código de exemplo abaixo ilustra esse problema. O acesso nãobound à variável "buffer" ocasionalmente resultará em uma AV (violação de acesso). Essa AV é capturada pelo manipulador de exceção nativo, mas não tem nenhuma maneira fácil de determinar se a seção crítica já foi adquirida no momento da exceção (a AV poderia até mesmo ter sido realizada em algum lugar no código EnterCriticalSection).

```
 BOOL bar (char* buffer)  
{  
   BOOL rc = FALSE;  
   __try {  
      EnterCriticalSection(&cs);  
      while (*buffer++ != '&') ;  
      rc = GetParams(buffer);  
      LeaveCriticalSection(&cs);  
   } __except (EXCEPTION_EXECUTE_HANDLER)  
   {  
      return FALSE;  
   } 
   return rc;  
}  
```

**Faça:**

-   Remover \_ \_ \_ \_ try/except sempre que possível; não use SetUnhandledExceptionFilter
-   Wrap your locks in custom auto \_ ptr-like templates if you use C++ exceptions.. O bloqueio deve ser liberado no destruidor. Para exceções nativas, libere os bloqueios em sua \_ \_ instrução finally
-   Tenha cuidado com o código em execução em um manipulador de exceção nativo; a exceção pode ter vazado muitos bloqueios, portanto, o manipulador não deve adquirir nenhum

**Não:**

-   Tratar exceções nativas se não for necessário ou exigido pelas APIs do Win32. Se você usar manipuladores de exceção nativos para relatórios ou recuperação de dados após falhas catastróficas, considere usar o mecanismo de sistema operacional padrão Relatório de Erros do Windows em vez disso
-   Use exceções C++ com qualquer tipo de código de interface do usuário (user32). uma exceção lançada em um retorno de chamada percorrerá as camadas de código C fornecidas pelo sistema operacional. Esse código não sabe sobre a semântica de unroll do C++

## <a name="links-to-resources"></a>Links para recursos

-   [Relatório de Erros do Windows](../wer/windows-error-reporting.md)
-   [Design assíncrono](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [E/S assíncrona](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**Função AttachThreadInput**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**Classe \_ auto ptr**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**Função DisableProcessWindowsGhosting**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**Função de retorno de chamada DllMain**](../dlls/dllmain.md)
-   [Eventos](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**Função GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [Cancelamento de E/S](../fileio/canceling-pending-i-o-operations.md)
-   [**Função IsHungAppWindow**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [Fila de Mensagens](../winmsg/using-messages-and-message-queues.md)
-   [**Função MsgWaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [Nova API do Pool de Threads](../procthread/thread-pool-api.md)
-   [**Função PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [Reinicialização e recuperação](../recovery/registering-for-application-restart.md)
-   [**Função SendMessageCallback**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**Função SendNotifyMessage**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [Objetos de sincronização](../sync/about-synchronization.md)
-   [**Função TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Relatório de Erros do Windows](../wer/windows-error-reporting.md)
-   [Winqual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
