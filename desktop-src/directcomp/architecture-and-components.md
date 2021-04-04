---
title: Arquitetura e componentes
description: Este tópico descreve os componentes que compõem o Microsoft DirectComposition.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2de495aa170560b1e7082cacf1893a8c94905a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007982"
---
# <a name="architecture-and-components"></a>Arquitetura e componentes

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico descreve os componentes que compõem o Microsoft DirectComposition. Ele consiste nas seções a seguir.

-   [Componentes de software](#software-components)
-   [Biblioteca de aplicativos](#application-library)
-   [Mecanismo de composição](#composition-engine)
-   [Tópicos relacionados](#related-topics)

## <a name="software-components"></a>Componentes de software

O DirectComposition consiste nos principais componentes de software a seguir.

-   Uma biblioteca de aplicativos no modo de usuário (dcomp.dll) que implementa a API pública baseada em Component Object Model (COM).
-   Um mecanismo de composição de modo de usuário (dwmcore.dll) hospedado no processo de Gerenciador de Janelas da Área de Trabalho (DWM) (dwm.exe) e executa a composição real da área de trabalho.
-   Um banco de dados de objetos no modo kernel (parte do win32k.sys) que realiza marshaling de comandos do aplicativo para o mecanismo de composição.

Uma única instância do mecanismo de composição manipula as árvores de composição DirectComposition para todos os aplicativos e a árvore de composição do DWM, que representa a área de trabalho inteira. Tanto o banco de dados de objetos do modo kernel quanto o mecanismo de composição do modo de usuário são instanciados uma vez por sessão, de modo que um computador Terminal Server com vários usuários tenha várias instâncias de ambos os componentes.

O diagrama a seguir mostra os principais componentes do DirectComposition e como eles se relacionam uns com os outros.

![arquitetura de nível superior do directcomposition](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Biblioteca de aplicativos

A biblioteca de aplicativos DirectComposition é uma API pública baseada em com com um único ponto de entrada simples que é exportado de dcomp.dll e retorna um ponteiro de interface para um objeto de dispositivo. O objeto de dispositivo, por sua vez, tem métodos para criar todos os outros objetos, cada um dos quais é representado por um ponteiro de interface. Todas as interfaces DirectComposition herdam de e implementam totalmente a interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Todos os métodos que aceitam interfaces DirectComposition verificam se a interface é implementada dentro de dcomp.dll ou se ela é implementada por outro componente. Como DirectComposition não é extensível, os métodos que usam interfaces como parâmetros retornam E \_ INVALIDARG se as interfaces não estiverem implementadas no dcomp.dll. A API não requer nenhum privilégio especial; Ele pode ser chamado por processos em execução no nível mais baixo de acesso. No entanto, como a API não opera na sessão 0, ela não é adequada para serviços. Nesses aspectos, a API DirectComposition é semelhante a outras APIs do Microsoft DirectX, principalmente Direct2D, Microsoft Direct3D e Microsoft DirectWrite.

Como o mecanismo de composição é projetado exclusivamente para execução assíncrona, as propriedades de objeto na API DirectComposition são somente gravação. Todas as propriedades têm métodos setter, mas não métodos getter. A leitura de propriedades não faz uso intensivo de recursos, mas também pode ser imprecisa, pois qualquer valor retornado pelo mecanismo de composição pode se tornar imediatamente inválido. Isso pode acontecer se, por exemplo, uma animação independente estiver associada à propriedade que está sendo lida.

A API é thread-safe. Um aplicativo pode chamar qualquer método de qualquer thread a qualquer momento. No entanto, como muitos métodos de API devem ser chamados em uma determinada sequência, sem qualquer sincronização, um aplicativo pode ter um comportamento imprevisível dependendo de como os threads se intercalam. Por exemplo, se dois threads alterarem a mesma Propriedade do mesmo objeto para valores diferentes ao mesmo tempo, o aplicativo não poderá prever qual dos dois valores será o valor final da propriedade. Da mesma forma, se dois threads chamarem [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) no mesmo dispositivo, nenhum thread terá um comportamento verdadeiramente transacional porque uma chamada para **Commit** em um thread enviará o lote de todos os comandos emitidos por ambos os threads, não apenas aquele que chamou **Commit**.

O sistema mantém todo o estado interno por objeto de dispositivo. Se um aplicativo criar dois ou mais objetos de dispositivo DirectComposition, o aplicativo poderá manter lotes independentes e outro estado entre os dois.

Todos os objetos DirectComposition têm afinidade de objeto de dispositivo; os objetos criados por um determinado objeto de dispositivo podem ser usados somente com esse objeto de dispositivo e podem ser associados somente a outros objetos criados pelo mesmo objeto de dispositivo. Em outras palavras, cada objeto de dispositivo é uma ilha de funcionalidade separada. A única exceção é a classe Visual, que permite a criação de árvores visuais em que um visual pode pertencer a um objeto de dispositivo diferente do seu pai. Isso permite cenários em que um aplicativo e um controle podem gerenciar uma única árvore de composição sem também precisar compartilhar um único objeto de dispositivo DirectComposition.

## <a name="composition-engine"></a>Mecanismo de composição

O mecanismo de composição DirectComposition é executado em um processo dedicado, separado de qualquer processo de aplicativo. Um único processo de composição, dwm.exe, dá suporte a todos os aplicativos em uma sessão. Cada aplicativo pode criar duas árvores visuais para cada janela que ela possui. Todas as árvores são realmente implementadas como subárvores de uma árvore visual maior que também abrange as estruturas de composição do DWM. O DWM constrói uma árvore visual grande para cada área de trabalho em uma sessão. Estas são as principais vantagens dessa arquitetura:

-   O mecanismo de composição tem acesso a todos os bitmaps de aplicativo e árvores visuais, o que permite a dioperabilidade e composição de janelas entre processos.
-   O mecanismo de composição é executado em um processo de sistema confiável que é separado de qualquer processo de aplicativo, permitindo que os aplicativos que têm direitos de acesso sejam muito baixos para compor com segurança o conteúdo protegido.
-   O mecanismo de composição pode detectar quando uma janela específica é totalmente obstruído e evitar desperdiçar recursos de CPU e unidade de processamento gráfico (GPU) para a janela.
-   O mecanismo de composição pode compor diretamente para o buffer de fundo da tela, evitando a necessidade de uma cópia extra necessária para mecanismos de composição por processo.
-   Todos os aplicativos compartilham um único dispositivo Direct3D para composição, o que oferece economia de memória considerável

A árvore visual é uma estrutura retida. A API DirectComposition expõe métodos para editar a estrutura em lotes de alterações processadas atomicamente. O objeto raiz na API DirectComposition é o objeto de dispositivo, que serve como o alocador para todos os outros objetos DirectComposition e contém um método chamado [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). O mecanismo de composição não reflete as alterações que o aplicativo faz na árvore visual até que o aplicativo chame **Commit**; nesse ponto todas as alterações desde a última **confirmação** são processadas como uma única transação.

O requisito para chamar [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) é semelhante ao conceito de um "frame", exceto que, como o mecanismo de composição é executado de forma assíncrona, ele pode apresentar vários quadros diferentes entre chamadas para **Commit**. No DirectComposition, um *quadro* é uma única iteração do mecanismo de composição e o intervalo gasto por um aplicativo entre duas chamadas a serem **confirmadas** é chamado de *lote*.

O DirectComposition batche todas as chamadas de aplicativo para a API DirectComposition. O banco de dados de objeto de kernel, que é implementado no driver de sessão de win32k.sys, armazena todas as informações de estado associadas às chamadas à API.

O mecanismo de composição produz um quadro para cada vertical em branco na exibição. O quadro é iniciado em um vertical em branco e tem como alvo a vertical subseqüente em branco. Quando o quadro é iniciado, o mecanismo de composição pega todos os lotes pendentes e inclui seus comandos nesse quadro. Os lotes são colocados em uma fila pendente quando o aplicativo chama [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)e a fila pendente é liberada atomicamente no início do quadro. Portanto, há um único ponto no tempo que marca o início de um quadro. Todos os lotes enviados antes desse ponto são incluídos no quadro, enquanto os lotes enviados após devem aguardar até que o próximo quadro seja processado. O loop de composição completo é o seguinte:

1.  Estimar o tempo da próxima vertical em branco.
2.  Recupere todos os lotes pendentes.
3.  Processar os lotes recuperados.
4.  Atualize todas as animações usando o tempo estimado na etapa 1.
5.  Determine as regiões da tela que precisam ser recompostas.
6.  Recrie as regiões sujas.
7.  Apresente o quadro invertendo os buffers traseiros e frontais para cada tela.
8.  Se nada tiver sido composto e apresentado nas etapas 6 e 7, aguarde até que um lote seja confirmado.
9.  Aguarde a próxima vertical em branco.

Se houver vários monitores anexados a um único adaptador de vídeo, o mecanismo de composição usará a vertical em branco do monitor primário para orientar o loop de composição e definir os tempos de amostragem da animação. Cada monitor é representado por uma cadeia de inversão de tela inteira separada; o mecanismo de composição repete as etapas 6 e 7 para cada monitor, em um modo Round Robin, usando um único dispositivo Direct3D. Se também houver vários adaptadores de vídeo, o mecanismo de composição usará um dispositivo Direct3D separado para cada adaptador de vídeo nas etapas 6 e 7.

Os quadros de composição são agendados para sempre começarem em uma vertical em branco, como mostra a ilustração a seguir.

![agendamento de quadro de composição](images/composition-frame-scheduling.png)

Se o mecanismo de composição não tiver nenhum trabalho a ser feito porque a árvore de composição não foi alterada, o thread de composição será suspenso enquanto aguarda um novo lote. Quando um novo lote é enviado, o thread de composição é ativado, mas imediatamente volta para o estado de suspensão até que a próxima vertical fique em branco. Esse comportamento garante tempos de início e de término previsíveis de quadros para aplicativos e para o mecanismo de composição.

O mecanismo de composição publica as horas de apresentação do quadro e a taxa de quadros atual. A publicação dessas informações permite que os aplicativos estimem o tempo de apresentação de seus próprios lotes, o que, por sua vez, permite que as animações sejam sincronizadas. Em particular, um aplicativo pode usar uma combinação de estatísticas de quadro do mecanismo de composição e um modelo histórico de quanto tempo seu thread de interface do usuário leva para produzir um lote, para determinar o período de amostragem para suas próprias animações.

Por exemplo, no início do lote do aplicativo mostrado na ilustração anterior, o aplicativo pode consultar o mecanismo de composição para determinar o tempo de apresentação exato do próximo quadro. O aplicativo pode usar a hora atual, juntamente com informações sobre os lotes anteriores que ele produziu, para determinar se o aplicativo pode concluir o lote atual antes da próxima vertical em branco. Portanto, o aplicativo usa o tempo de apresentação do quadro como o tempo de amostragem para suas próprias animações. Se o aplicativo determinar que é improvável que você conclua seu trabalho na vertical atual em branco, o aplicativo poderá usar o período de quadro subsequente como o tempo de amostragem, usando as informações de taxa de quadros retornadas pelo mecanismo de composição para calcular esse tempo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 