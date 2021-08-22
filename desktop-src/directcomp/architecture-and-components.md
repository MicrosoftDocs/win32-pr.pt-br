---
title: Arquitetura e componentes
description: Este tópico descreve os componentes que composição do Microsoft DirectComposition.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125a640f902bc64d55af8cdcdbf816c788e0507a48034dfb52c972fa3f068d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985448"
---
# <a name="architecture-and-components"></a>Arquitetura e componentes

> [!NOTE]
> Para aplicativos Windows 10, recomendamos o uso de APIs Windows.UI.Composition em vez de DirectComposition. Para obter mais informações, consulte [Modernizar seu aplicativo da área de trabalho usando a camada visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico descreve os componentes que composição do Microsoft DirectComposition. Ele consiste nas seções a seguir.

-   [Componentes de software](#software-components)
-   [Biblioteca de aplicativos](#application-library)
-   [Mecanismo de composição](#composition-engine)
-   [Tópicos relacionados](#related-topics)

## <a name="software-components"></a>Componentes de software

DirectComposition consiste nos seguintes componentes de software principais.

-   Uma biblioteca de aplicativos no modo de usuário (dcomp.dll) que implementa a API pública baseada em COMPONENT OBJECT MODEL (COM).
-   Um mecanismo de composição do modo de usuário (dwmcore.dll) que é hospedado no processo Gerenciador de Janelas da Área de Trabalho (DWM) dwm.exe) e executa a composição real da área de trabalho.
-   Um banco de dados de objeto no modo kernel (parte win32k.sys) que faz marshal de comandos do aplicativo para o mecanismo de composição.

Uma única instância do mecanismo de composição lida com as árvores de composição directComposition para todos os aplicativos e a árvore de composição DWM, que representa toda a área de trabalho. O banco de dados de objeto de modo kernel e o mecanismo de composição do modo de usuário são instanciados uma vez por sessão, portanto, um computador do Servidor de Terminal com vários usuários tem várias instâncias de ambos os componentes.

O diagrama a seguir mostra os principais componentes do DirectComposition e como eles se relacionam entre si.

![arquitetura de nível superior directcomposition](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Biblioteca de aplicativos

A biblioteca de aplicativos DirectComposition é uma API pública baseada em COM com um único ponto de entrada simples que é exportado do dcomp.dll e retorna um ponteiro de interface para um objeto de dispositivo. O objeto de dispositivo, por sua vez, tem métodos para criar todos os outros objetos, cada um dos quais é representado por um ponteiro de interface. Todas as interfaces DirectComposition herdam e implementam totalmente a interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) Todos os métodos que aceitam interfaces DirectComposition verificam se a interface é implementada dentro do dcomp.dll ou se ela é implementada por outro componente. Como DirectComposition não é extensível, métodos que levam interfaces como parâmetros retornam E INVALIDARG se as interfaces não são implementadas no \_ dcomp.dll. A API não requer privilégios especiais; ele pode ser chamado por processos em execução no nível mais baixo de acesso. No entanto, como a API não opera na sessão 0, ela não é adequada para serviços. Nesses aspectos, a API directComposition é semelhante a outras APIs do Microsoft DirectX, principalmente Direct2D, Microsoft Direct3D e Microsoft DirectWrite.

Como o mecanismo de composição foi projetado exclusivamente para execução assíncrona, as propriedades do objeto na API DirectComposition são somente gravação. Todas as propriedades têm métodos setter, mas não métodos getter. Ler propriedades não só faz uso intensivo de recursos, mas também pode ser impreciso porque qualquer valor que o mecanismo de composição retorna pode se tornar inválido imediatamente. Isso pode acontecer se, por exemplo, uma animação independente estiver vinculada à propriedade que está sendo lida.

A API é thread-safe. Um aplicativo pode chamar qualquer método de qualquer thread a qualquer momento. No entanto, como muitos métodos de API devem ser chamados em uma sequência específica, sem nenhuma sincronização, um aplicativo pode experimentar um comportamento imprevisível dependendo de como os threads intercalam. Por exemplo, se dois threads alterarem a mesma propriedade do mesmo objeto para valores diferentes ao mesmo tempo, o aplicativo não poderá prever qual dos dois valores será o valor final da propriedade. Da mesma forma, se [](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) dois threads chamarem Commit no mesmo dispositivo,  nenhum thread receberá um comportamento realmente transacional porque uma chamada para Commit em um thread enviará o lote de todos os comandos emitidos por ambos os threads, não apenas aquele que chamou **Commit**.

O sistema mantém todo o estado interno por objeto de dispositivo. Se um aplicativo criar dois ou mais objetos de dispositivo DirectComposition, o aplicativo poderá manter lotes independentes e outro estado entre os dois.

Todos os objetos DirectComposition têm afinidade de objeto de dispositivo; Objetos criados por um objeto de dispositivo específico podem ser usados somente com esse objeto de dispositivo e podem ser associados somente a outros objetos criados pelo mesmo objeto de dispositivo. Em outras palavras, cada objeto de dispositivo é uma ilha separada de funcionalidades diferentes. A única exceção é a classe visual, que permite a criação de árvores visuais em que um visual pode pertencer a um objeto de dispositivo diferente de seu pai. Isso permite cenários em que um aplicativo e um controle podem gerenciar uma única árvore de composição sem também precisar compartilhar um único objeto de dispositivo DirectComposition.

## <a name="composition-engine"></a>Mecanismo de composição

O mecanismo de composição DirectComposition é executado em um processo dedicado, separado de qualquer processo de aplicativo. Um único processo de composição, dwm.exe, dá suporte a todos os aplicativos em uma sessão. Cada aplicativo pode criar duas árvores visuais para cada janela que possui. Todas as árvores são realmente implementadas como subárvores de uma árvore visual maior que também abrange as estruturas de composição do DWM. O DWM constrói uma árvore visual grande para cada área de trabalho em uma sessão. Aqui estão as principais vantagens dessa arquitetura:

-   O mecanismo de composição tem acesso a todos os bitmaps de aplicativo e árvores visuais, o que permite interoperabilidade e composição de janela entre processos.
-   O mecanismo de composição é executado em um processo de sistema confiável separado de qualquer processo de aplicativo, permitindo que aplicativos com direitos de baixo acesso componham com segurança o conteúdo protegido.
-   O mecanismo de composição pode detectar quando uma janela específica está totalmente oclusa e evitar o desperdício de recursos de CPU e GPU (unidade de processamento gráfico) compondo para a janela.
-   O mecanismo de composição pode compor diretamente no buffer de fundo da tela, evitando a necessidade de uma cópia extra necessária para mecanismos de composição por processo.
-   Todos os aplicativos compartilham um único dispositivo Direct3D para composição, o que oferece uma economia considerável de memória

A árvore visual é uma estrutura retida. A API directComposition expõe métodos para editar a estrutura em lotes de alterações processadas atomicamente. O objeto raiz na API directComposition é o objeto de dispositivo, que serve como a fábrica para todos os outros objetos DirectComposition e contém um método [**chamado Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). O mecanismo de composição não reflete as alterações que o aplicativo faz na árvore visual até que o aplicativo chama **Commit**, em que todas as alterações desde o último **Commit** são processadas como uma única transação.

O requisito para chamar [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) é semelhante ao conceito de um "quadro", exceto que, como o mecanismo de composição é executado de forma assíncrona, ele pode apresentar vários quadros diferentes entre chamadas para **Commit**. No DirectComposition,  um quadro é uma única iteração do mecanismo de composição e o intervalo gasto por um aplicativo entre duas chamadas para **Commit** é chamado de *lote*.

O DirectComposition lotes todas as chamadas de aplicativo para a API directComposition. O banco de dados de objeto kernel, que é implementado no driver de sessão win32k.sys, armazena todas as informações de estado associadas às chamadas à API.

O mecanismo de composição produz um quadro para cada espaço em branco vertical na exibição. O quadro é iniciado em um espaço em branco vertical e tem como alvo o espaço em branco vertical subsequente. Quando o quadro é iniciado, o mecanismo de composição escolhe todos os lotes pendentes e inclui seus comandos nesse quadro. Os lotes são colocados em uma fila pendente quando o aplicativo chama [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)e a fila pendente é liberado atomicamente no início do quadro. Portanto, há um único ponto no tempo que marca o início de um quadro. Todos os lotes enviados antes desse ponto são incluídos no quadro, enquanto os lotes enviados após devem aguardar até que o próximo quadro seja processado. O loop de composição completo é o seguinte:

1.  Estimar a hora do próximo espaço em branco vertical.
2.  Recuperar todos os lotes pendentes.
3.  Processe os lotes recuperados.
4.  Atualize todas as animações usando o tempo estimado na etapa 1.
5.  Determine as regiões da tela que precisam ser re compostos.
6.  Recomponha as regiões sujas.
7.  Apresente o quadro invertendo os buffers voltar e frontal para cada tela.
8.  Se nada tiver sido composto e apresentado nas etapas 6 e 7, aguarde até que um lote seja confirmado.
9.  Aguarde o próximo espaço em branco vertical.

Se houver vários monitores anexados a um único adaptador de vídeo, o mecanismo de composição usará o espaço em branco vertical do monitor primário para conduzir o loop de composição e definir os tempos de amostragem de animação. Cada monitor é representado por uma cadeia de invasões de tela inteira separada; O mecanismo de composição repete as etapas 6 e 7 para cada monitor, de forma round robin, usando um único dispositivo Direct3D. Se também houver vários adaptadores de vídeo, o mecanismo de composição usará um dispositivo Direct3D separado para cada adaptador de vídeo nas etapas 6 e 7.

Os quadros de composição são agendados para sempre iniciar em um espaço em branco vertical, como mostra a ilustração a seguir.

![agendamento de quadro de composição](images/composition-frame-scheduling.png)

Se o mecanismo de composição não tiver trabalho a fazer porque a árvore de composição não foi alterada, o thread de composição será suspenso enquanto aguarda um novo lote. Quando um novo lote é enviado, o thread de composição é acionada, mas volta imediatamente para sleep até o próximo espaço em branco vertical. Esse comportamento garante horários de início e término de quadro previsíveis para aplicativos e para o mecanismo de composição.

O mecanismo de composição publica os tempos de apresentação do quadro e a taxa de quadros atual. Publicar essas informações permite que os aplicativos es estimam o tempo de apresentação para seus próprios lotes, o que, por sua vez, permite que as animações sejam sincronizadas. Em particular, um aplicativo pode usar uma combinação de estatísticas de quadro do mecanismo de composição e um modelo histórico de quanto tempo seu thread de interface do usuário leva para produzir um lote, para determinar o tempo de amostragem para suas próprias animações.

Por exemplo, no início do lote de aplicativos mostrado na ilustração anterior, o aplicativo pode consultar o mecanismo de composição para determinar o tempo exato de apresentação do próximo quadro. Em seguida, o aplicativo pode usar a hora atual, juntamente com informações sobre lotes anteriores produzidos, para determinar se o aplicativo pode concluir o lote atual antes do próximo espaço em branco vertical. Portanto, o aplicativo usa o tempo de apresentação do quadro como o tempo de amostragem para suas próprias animações. Se o aplicativo determinar que é improvável concluir seu trabalho no espaço em branco vertical atual, o aplicativo poderá usar o tempo de quadro subsequente como o tempo de amostragem, usando as informações de taxa de quadros retornadas pelo mecanismo de composição para calcular esse tempo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 