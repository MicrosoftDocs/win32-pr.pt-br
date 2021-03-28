---
description: Extensões em processo são carregadas em todos os processos que as disparam.
title: Diretrizes para implementar extensões de In-Process
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e4dc9fd0573f3f98f0ec1110079f95f56a8c42e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922842"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Diretrizes para implementar extensões de In-Process

Extensões em processo são carregadas em todos os processos que as disparam. Por exemplo, uma extensão de namespace de shell pode ser carregada em qualquer processo que acessa o namespace do Shell direta ou indiretamente. O namespace do Shell é usado por muitas operações de Shell, como a exibição de uma caixa de diálogo de arquivo comum, o lançamento de um documento por meio de seu aplicativo associado ou a obtenção do ícone usado para representar um arquivo. Como as extensões em processo podem ser carregadas em processos arbitrários, deve-se tomar cuidado para que elas não afetem negativamente o aplicativo host ou outras extensões em processo.

Um tempo de execução de observação específica é o *Common Language Runtime (CLR)*, também conhecido como *código gerenciado* ou o *.NET Framework*. **A Microsoft recomenda a gravação de extensões em processo gerenciadas no Windows Explorer ou no Windows Internet Explorer e não as considera um cenário com suporte.**

Este tópico discute os fatores a serem considerados quando você determina se algum tempo de execução diferente do CLR é adequado para uso por extensões em processo. Exemplos de outros tempos de execução incluem Java, Visual Basic, JavaScript/ECMAScript, Delphi e a biblioteca de tempo de execução C/C++. Este tópico também fornece alguns motivos pelos quais o código gerenciado não é suportado em extensões em processo.

## <a name="version-conflicts"></a>Conflitos de versão

Um conflito de versão pode surgir por meio de um tempo de execução que não oferece suporte ao carregamento de várias versões de tempo de execução em um único processo. As versões do CLR anteriores à versão 4,0 se enquadram nessa categoria. Se o carregamento de uma versão de um tempo de execução impede o carregamento de outras versões desse mesmo tempo de execução, isso poderá criar um conflito se o aplicativo host ou outra extensão em processo usar uma versão conflitante. No caso de um conflito de versão com outra extensão em processo, o conflito pode ser difícil de reproduzir porque a falha requer as extensões corretas conflitantes e o modo de falha depende da ordem em que as extensões conflitantes são carregadas.

Considere uma extensão em processo escrita usando uma versão do CLR anterior à versão 4,0. Cada aplicativo no computador que usa uma caixa de diálogo de **abertura** de arquivo poderia potencialmente ter o código gerenciado da caixa de diálogo e sua dependência de CLR do atendente carregada no processo do aplicativo. O aplicativo ou a extensão que primeiro é carregar uma versão anterior à 4,0 do CLR no processo do aplicativo restringe quais versões do CLR podem ser usadas posteriormente por esse processo. Se um aplicativo gerenciado com uma caixa de diálogo **aberta** for criado em uma versão conflitante do CLR, a extensão poderá falhar ao ser executada corretamente e poderá causar falhas no aplicativo. Por outro lado, se a extensão for a primeira a ser carregada em um processo e uma versão conflitante do código gerenciado tentar iniciar depois disso (talvez um aplicativo gerenciado ou um aplicativo em execução carregue o CLR sob demanda), a operação falhará. Para o usuário, parece que alguns recursos do aplicativo param de funcionar aleatoriamente ou o aplicativo falha misteriosamente.

Observe que as versões do CLR iguais ou posteriores à versão 4,0 não são geralmente suscetíveis ao problema de controle de versão porque foram projetadas para coexistirem entre si e com a maioria das versões anteriores à 4,0 do CLR (com exceção da versão 1,0, que não pode coexistir com outras versões). No entanto, problemas diferentes de conflitos de versão podem surgir conforme discutido no restante deste tópico.

## <a name="performance-issues"></a>Problemas de desempenho

Problemas de desempenho podem surgir em tempos de execução que impõem uma penalidade de desempenho significativa quando são carregados em um processo. A penalidade de desempenho pode estar na forma de uso de memória, uso de CPU, tempo decorrido ou até mesmo consumo de espaço de endereço. O CLR, o JavaScript/ECMAScript e o Java são conhecidos como tempos de execução de alto impacto. Como as extensões em processo podem ser carregadas em muitos processos e, muitas vezes, são realizadas com momentos sensíveis ao desempenho (por exemplo, ao preparar um menu para ser exibido ao usuário), os tempos de execução de alto impacto podem afetar negativamente a capacidade de resposta geral.

Um tempo de execução de alto impacto que consome recursos significativos pode causar uma falha no processo de host ou em outra extensão em processo. Por exemplo, um tempo de execução de alto impacto que consome centenas de megabytes de espaço de endereço para seu heap pode fazer com que o aplicativo host não consiga carregar um grande conjunto de grandes. Além disso, como as extensões em processo podem ser carregadas em vários processos, o alto consumo de recursos em uma única extensão pode rapidamente multiplicar o alto consumo de recursos em todo o sistema.

Se um tempo de execução permanecer carregado ou continuar a consumir recursos mesmo quando a extensão que usa esse tempo de execução tiver sido descarregada, esse tempo de execução não será adequado para uso em uma extensão.

## <a name="issues-specific-to-the-net-framework"></a>Problemas específicos do .NET Framework

As seções a seguir discutem exemplos de problemas encontrados com o uso de código gerenciado para extensões. Eles não são uma lista completa de todos os possíveis problemas que podem ser encontrados. Os problemas discutidos aqui são os dois motivos pelos quais o código gerenciado não tem suporte em extensões e pontos a serem considerados quando você avalia o uso de outros tempos de execução.

### <a name="re-entrancy"></a>Nova entrada

Quando o CLR bloqueia um thread STA (single-threaded apartment), por exemplo, devido a um monitor. Enter, WaitHandle. WaitOne ou instrução de [**bloqueio**](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) contendeda, o CLR, em sua configuração padrão, entra em um loop de mensagem aninhado enquanto aguarda. Muitos métodos de extensão são proibidos de processar mensagens, e essa reentrância imprevisível e inesperada pode resultar em um comportamento anormal que é difícil de reproduzir e diagnosticar.

### <a name="the-multithreaded-apartment"></a>O apartamento multithread

O CLR cria *wrappers callable em tempo de execução* para objetos COM (Component Object Model). Esses mesmos wrappers callable de tempo de execução são destruídos posteriormente pelo finalizador do CLR, que faz parte do MTA (multithreaded apartment). Mover o proxy do STA para o MTA requer marshaling, mas nem todas as interfaces usadas por extensões podem ser marshalled.

### <a name="non-deterministic-object-lifetimes"></a>Tempos de vida de objeto não determinístico

O CLR tem garantias mais fracas de tempo de vida do objeto do que o código nativo. Muitas extensões têm requisitos de contagem de referência em objetos e interfaces, e o modelo de coleta de lixo empregado pelo CLR não pode atender a esses requisitos.

-   Se um objeto CLR obtiver uma referência a um objeto COM, a referência de objeto COM mantida pelo wrapper callable não será liberada até que o tempo de execução Callable Wrapper seja lixo coletado. O comportamento de versão não determinística pode entrar em conflito com alguns contratos de interface. Por exemplo, o método [**IPersistPropertyBag:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) requer que nenhuma referência ao recipiente de propriedades seja retida pelo objeto quando o método **Load** retornar.
-   Se uma referência de objeto CLR for retornada ao código nativo, o wrapper callable do Runtime cederá sua referência ao objeto CLR quando for feita a chamada final de [**versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de runtime callable wrapper, mas o objeto CLR subjacente não será finalizado até que seja coletado pelo lixo. A finalização não determinística pode entrar em conflito com alguns contratos de interface. Por exemplo, os manipuladores de miniatura são necessários para liberar todos os recursos imediatamente quando sua contagem de referência cai para zero.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Usos aceitáveis de código gerenciado e outros tempos de execução

É aceitável usar código gerenciado e outros tempos de execução para implementar extensões fora do processo. Exemplos de extensões de shell fora do processo incluem o seguinte:

-   Gerenciadores de visualização
-   Ações baseadas em linha de comando, como aquelas registradas em \\  \\ subchaves de **comando** do verbo do Shell.
-   Objetos COM implementados em um servidor local, para pontos de extensão do shell que permitem a ativação fora do processo.

Algumas extensões podem ser implementadas como extensões em processo ou fora do processo. Você pode implementar essas extensões como extensões fora do processo se elas não atenderem a esses requisitos para extensões em processo. A lista a seguir mostra exemplos de extensões que podem ser implementadas como extensões em processo ou fora do processo:

-   [**IExecuteCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) associado a uma entrada **DelegateExecute** registrada em uma \\ subchave de comando de *verbo* de shell \\  .
-   [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) associado ao CLSID registrado em uma  \\  \\ subchave **DropTarget** do verbo do Shell.
-   [**IExplorerCommandState**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) associado a uma entrada **CommandStateHandler** registrada em uma subchave de verbo do **shell** \\  .

 

 
