---
description: As extensões em processo são carregadas em todos os processos que as disparam.
title: Diretrizes para implementar extensões In-Process dados
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ccbee300cbfe1b08bc0509472ac3afcaa9ea3db54f6f1e38131cc08d2e8381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858171"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Diretrizes para implementar extensões In-Process dados

As extensões em processo são carregadas em todos os processos que as disparam. Por exemplo, uma extensão de namespace do Shell pode ser carregada em qualquer processo que acesse o namespace do Shell direta ou indiretamente. O namespace do Shell é usado por muitas operações do Shell, como a exibição de uma caixa de diálogo de arquivo comum, o lançamento de um documento por meio de seu aplicativo associado ou a obtenção do ícone usado para representar um arquivo. Como as extensões em processo podem ser carregadas em processos arbitrários, é necessário ter cuidado para que elas não acariem negativamente o aplicativo host ou outras extensões em processo.

Um runtime de observação específica é o *CLR (Common Language Runtime),* também conhecido como código gerenciado *ou* o *.NET Framework*. **A Microsoft recomenda não escrever extensões gerenciadas em processo no Windows Explorer ou Windows Internet Explorer e não as considera um cenário com suporte.**

Este tópico discute os fatores a considerar ao determinar se qualquer runtime diferente do CLR é adequado para uso por extensões em processo. Exemplos de outros runtimes incluem Java, Visual Basic, JavaScript/ECMAScript,Script e a biblioteca de runtime C/C++. Este tópico também fornece alguns motivos pelos quais o código gerenciado não tem suporte em extensões em processo.

## <a name="version-conflicts"></a>Conflitos de versão

Um conflito de versão pode surgir por meio de um runtime que não dá suporte ao carregamento de várias versões de runtime em um único processo. As versões do CLR anteriores à versão 4.0 se enquadram nessa categoria. Se o carregamento de uma versão de um runtime impedir o carregamento de outras versões desse mesmo runtime, isso poderá criar um conflito se o aplicativo host ou outra extensão em processo usar uma versão conflitante. No caso de um conflito de versão com outra extensão em processo, o conflito pode ser difícil de reproduzir porque a falha requer as extensões conflitantes corretas e o modo de falha depende da ordem na qual as extensões conflitantes são carregadas.

Considere uma extensão em processo escrita usando uma versão do CLR antes da versão 4.0. Todos os aplicativos no  computador que usam uma caixa de diálogo Abrir arquivo podem potencialmente ter o código gerenciado da caixa de diálogo e sua dependência CLR oficial carregada no processo do aplicativo. O aplicativo ou extensão que é o primeiro a carregar uma versão anterior à 4.0 do CLR no processo do aplicativo restringe quais versões do CLR podem ser usadas posteriormente por esse processo. Se um aplicativo  gerenciado com uma caixa de diálogo Abrir for criado em uma versão conflitante do CLR, a extensão poderá falhar ao ser executado corretamente e poderá causar falhas no aplicativo. Por outro lado, se a extensão for a primeira a ser carregada em um processo e uma versão conflitante do código gerenciado tentar iniciar depois disso (talvez um aplicativo gerenciado ou um aplicativo em execução carregue o CLR sob demanda), a operação falhará. Para o usuário, parece que alguns recursos do aplicativo param de funcionar aleatoriamente ou o aplicativo falha de forma incorretamente.

Observe que as versões do CLR iguais ou posteriores à versão 4.0 geralmente não são suscetíveis ao problema de versão porque são projetadas para coexistir entre si e com a maioria das versões anteriores à 4.0 do CLR (com exceção da versão 1.0, que não pode coexistir com outras versões). No entanto, problemas diferentes de conflitos de versão podem surgir conforme discutido no restante deste tópico.

## <a name="performance-issues"></a>Problemas de desempenho

Podem surgir problemas de desempenho com runtimes que impõem uma penalidade de desempenho significativa quando são carregados em um processo. A penalidade de desempenho pode estar na forma de uso de memória, uso da CPU, tempo decorrido ou até mesmo consumo de espaço de endereço. O CLR, JavaScript/ECMAScript e Java são conhecidos como runtimes de alto impacto. Como as extensões em processo podem ser carregadas em muitos processos e geralmente são feitas em momentos sensíveis ao desempenho (como ao preparar um menu para ser exibido ao usuário), runtimes de alto impacto podem afetar negativamente a capacidade de resposta geral.

Um runtime de alto impacto que consome recursos significativos pode causar uma falha no processo de host ou em outra extensão em processo. Por exemplo, um runtime de alto impacto que consome centenas de megabytes de espaço de endereço para seu heap pode fazer com que o aplicativo host não possa carregar um grande conjuntos de dados. Além disso, como as extensões em processo podem ser carregadas em vários processos, o alto consumo de recursos em uma única extensão pode multiplicar rapidamente em alto consumo de recursos em todo o sistema.

Se um runtime permanecer carregado ou continuar consumindo recursos mesmo quando a extensão que usa esse runtime tiver sido descarregada, esse runtime não será adequado para uso em uma extensão.

## <a name="issues-specific-to-the-net-framework"></a>Problemas específicos do .NET Framework

As seções a seguir discutem exemplos de problemas encontrados com o uso de código gerenciado para extensões. Eles não são uma lista completa de todos os possíveis problemas que você pode encontrar. Os problemas discutidos aqui são os dois motivos pelos quais o código gerenciado não tem suporte em extensões e pontos a considerar ao avaliar o uso de outros runtimes.

### <a name="re-entrancy"></a>Re-entrada

Quando o CLR bloqueia um thread STA (single-threaded apartment), por exemplo, devido a uma instrução Monitor.Enter, WaitHandle.WaitOne ou contended [**lock,**](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) o CLR, em sua configuração padrão, entra em um loop de mensagem aninhado enquanto aguarda. Muitos métodos de extensão são proibidos de processar mensagens, e essa reentração imprevisível e inesperada pode resultar em comportamento anômalo que é difícil de reproduzir e diagnosticar.

### <a name="the-multithreaded-apartment"></a>O Multithreaded Apartment

O CLR cria *Runtime Callable Wrappers* para Component Object Model (COM). Esses mesmos Runtime Callable Wrappers são destruídos posteriormente pelo finalizador do CLR, que faz parte do MTA (multithreaded apartment). Mover o proxy do STA para o MTA requer marshaling, mas nem todas as interfaces usadas pelas extensões podem ser marshalladas.

### <a name="non-deterministic-object-lifetimes"></a>Tempo de vida de objeto não determinístico

O CLR tem garantias de tempo de vida de objeto mais fracas do que o código nativo. Muitas extensões têm requisitos de contagem de referência em objetos e interfaces, e o modelo de coleta de lixo empregado pelo CLR não pode atender a esses requisitos.

-   Se um objeto CLR obtiver uma referência a um objeto COM, a referência de objeto COM mantida pelo Runtime Callable Wrapper não será liberada até que o Runtime Callable Wrapper seja coletado como lixo. O comportamento de versão não determinística pode ser conflitante com alguns contratos de interface. Por exemplo, o [**método IPersistPropertyBag::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) exige que nenhuma referência ao pacote de propriedades seja mantida pelo objeto quando o **método Load** retornar.
-   Se uma referência de objeto CLR for retornada ao código nativo, o Runtime Callable Wrapper abandonará sua referência ao [](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) objeto CLR quando a chamada final do Runtime Callable Wrapper para Release for feita, mas o objeto CLR subjacente não será finalizado até que seja coletado como lixo. A finalização não determinística pode ficar em conflito com alguns contratos de interface. Por exemplo, manipuladores de miniaturas são necessários para liberar todos os recursos imediatamente quando sua contagem de referência cair para zero.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Usos aceitáveis de código gerenciado e outros runtimes

É aceitável usar código gerenciado e outros runtimes para implementar extensões fora do processo. Exemplos de extensões de Shell fora de processo incluem o seguinte:

-   Manipuladores de visualização
-   Ações baseadas em linha de comando, como aquelas registradas em sub-chaves de comando \\ *do verbo* \\  do shell.
-   Objetos COM implementados em um servidor local para pontos de extensão do Shell que permitem a ativação fora do processo.

Algumas extensões podem ser implementadas como extensões em processo ou fora do processo. Você poderá implementar essas extensões como extensões fora do processo se elas não atenderem a esses requisitos para extensões em processo. A lista a seguir mostra exemplos de extensões que podem ser implementadas como extensões em processo ou fora do processo:

-   [**IExecuteCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) associado a uma entrada **DelegateExecute** registrada em uma sub-chave de comando do  \\ *verbo* \\ **do** shell.
-   [**IDropTarget associado**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) ao CLSID registrado em uma \\  \\ subkey **DropTarget** do verbo shell.
-   [**IExplorerCommandState**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) associado a uma **entrada CommandStateHandler** registrada em uma subkey de verbo de **shell.** \\ 

 

 
