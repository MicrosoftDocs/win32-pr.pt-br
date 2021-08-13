---
description: As APIs inkAnalysis fornecem aos desenvolvedores de tablets ferramentas poderosas para examinar programaticamente a entrada de tinta. A API classifica tinta em categorias significativas, como palavras, linhas, parágrafos e desenhos.
ms.assetid: d9521a8c-f61a-40ea-8603-e8afbba75a4e
title: Visão geral da análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3056a5e5fbff8be82f6df2de2a34fadd9761e50f451ee2d48c112589d1aff397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718899"
---
# <a name="ink-analysis-overview"></a>Visão geral da análise de tinta

As APIs inkAnalysis fornecem aos desenvolvedores de tablets ferramentas poderosas para examinar programaticamente a entrada de tinta. A API classifica tinta em categorias significativas, como palavras, linhas, parágrafos e desenhos.

Você pode usar cada classificação de várias maneiras, incluindo melhorar os resultados de reconhecimento para manuscrito.

## <a name="ink-analysis-basics"></a>Noções básicas de análise de tinta

Esta seção apresenta a tecnologia de análise de tinta da Plataforma de Tablet PC e explica quando e como usá-la.

As APIs inkAnalysis combinam efetivamente duas tecnologias distintas, mas complementares: reconhecimento de manuscrito e classificação de layout. Combinar essas duas tecnologias fornece resultados definitivamente maiores do que as partes tomadas por si só.

O reconhecimento de manuscrito é a análise computacional da tinta digital manuscrita para retornar a interpretação baseada em caracteres em um determinado idioma. Ou seja, o reconhecimento de manuscrito é como o computador "lê" o manuscrito de uma pessoa.

A Análise de Tinta Pode ser dividida ainda mais em classificação de tinta e análise de layout. A classificação de tinta é a divisão computacional da tinta em unidades semanticamente significativas, como parágrafos, linhas, palavras e desenhos. A análise de layout é o exame computacional da entrada de tinta para determinar a posição da tinta na superfície de tinta e como os traços se relacionam espacialmente e até mesmo semanticamente. Por exemplo, a análise de layout pode dizer que uma determinada parte da tinta é uma anotação ou uma chamada.

### <a name="recognition"></a>Reconhecimento

Um exemplo de como a combinação de reconhecimento com análise de tinta na API inkAnalysis ajuda o desenvolvedor é a melhoria nos resultados de reconhecimento. Os mecanismos de reconhecimento de manuscrito do tablet PC foram projetados principalmente para reconhecer uma única linha horizontal de tinta. No entanto, as pessoas tendem a escrever várias linhas ao fazer anotações, e não há garantia de que essas linhas sejam horizontais em relação à página. Com a API inkAnalysis, a tinta é pré-processada pelo analisador de tinta antes de ser enviada ao reconhecedor. A tinta analisada é transformada em horizontal antes de ser reconhecida, melhorando os resultados de reconhecimento.

Outros benefícios para o reconhecimento são derivados por fazer com que o analisador de tinta corrija informações incorretas de ordem de traço antes de enviar a tinta para o reconhecedor. Além disso, os resultados de reconhecimento agora estão disponíveis de maneira seletiva. Ou seja, o desenvolvedor pode recuperar rapidamente os resultados de reconhecimento para uma única palavra, linha ou parágrafo em uma única chamada.

### <a name="ink-classification"></a>Classificação de tinta

É claro que há uma variedade de cenários em que você pode manter os dados de tinta intactos, em vez de convertê-los imediatamente em texto. A análise de tinta também oferece benefícios aqui. Especificamente, as APIs inkAnalysis fornecem a capacidade de dividir traços de tinta de acordo com a escrita ou os desenhos. Traços de tinta classificados como escrita são aqueles que compoem uma palavra ou caracteres. Todos os outros traços são desenhos. Isso fornece uma nova maneira de acessar dados de tinta, permitindo novos cenários de usuário. Por exemplo, você pode implementar a seleção para que ela seja diferente com base em qual tipo de traço o usuário toca; Se um usuário tocar em um traço de gravação, o aplicativo selecionará todo o conjunto de traços que compõem a palavra. Se o usuário tocar em um desenho, o aplicativo selecionará apenas esse traço.

### <a name="layout-analysis"></a>Análise de layout

A análise de layout útil vai muito além do detalhamento relativamente simples da tinta em componentes de escrita e desenho.

A análise de tinta também inclui um detalhamento mais rico dos traços de escrita e desenho. Como um exemplo muito simples, pegue um blob de tinta, conforme mostrado na ilustração a seguir.

![duas linhas simples de manuscrito](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Depois que a plataforma analisar esses traços, ela retornará uma representação de árvore desses traços, conforme mostrado na ilustração a seguir. Para esse caso simples, a árvore contém apenas informações de parágrafo, linha e palavra, mas a complexidade dessa árvore aumenta à medida que a complexidade do documento de tinta aumenta.

![representação de árvore de raiz, parágrafo, linhas e palavras](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Como essas informações agora estão separadas em unidades gerenciáveis, agora você pode criar recursos mais avançados. Por exemplo, o aplicativo pode estender o recurso no qual o usuário toca para selecionar uma palavra em um recurso no qual o usuário toca uma vez para selecionar a palavra, toca duas vezes para selecionar a linha inteira e toca três vezes para selecionar o parágrafo inteiro. Aproveitando a estrutura de árvore retornada pela operação de análise, o aplicativo pode relacionar a área mapeada de volta a um traço na árvore. Depois que o aplicativo encontra um traço, ele pode ir até a árvore para determinar como e quais traços vizinhos selecionar.

Selecionar uma linha inteira é um exemplo simplista dos benefícios da análise de tinta, mas as possibilidades se tornam ótimas quando se considera os diferentes tipos de estruturas hierárquicas que o analisador de tinta é capaz de detectar:

-   Listas ordenadas e não ordenadas
-   Formas
-   Comentários anotativos escritos em linha com o texto

Os tipos de recursos variam de aplicativo para aplicativo e são baseados nos requisitos e nos mecanismos de reconhecimento e análise de tinta disponíveis.

### <a name="key-ink-analysis-features"></a>Recursos de análise de tinta principal

Os principais recursos da API inkAnalysis incluem os seguintes recursos:

-   Análise incremental
-   Persistência
-   Proxy de dados
-   Reconciliação
-   Extensibilidade

### <a name="incremental-analysis"></a>Análise incremental

Quando os usuários finais trabalham com tinta, eles geralmente o tratam como manuscrito. A tinta está continuamente sujeita a operações de edição, como a adição de tinta nova, exclusão de tinta existente e modificação de propriedades de tinta, tudo feito da mesma maneira que o manuscrito é editado continuamente. Essas operações de edição afetam os resultados da análise. Quando ocorrem edições, elas geralmente podem ser isoladas em seções do documento em pontos específicos no tempo. Por exemplo, suponha que um usuário escreva cinco linhas de tinta. A maneira padrão que os aplicativos analisam tinta é aguardar até que o usuário termine de escrever todas as cinco linhas de tinta , um parágrafo, por exemplo, e, em seguida, analisar os resultados, de forma síncrona ou assíncrona.

Você pode otimizar o tempo geral gasto analisando essas cinco linhas isolando as áreas que são analisadas conforme elas estão sendo escritas e, em seguida, reanalise apenas as partes dos resultados que foram alteradas. Depois que a primeira linha for analisada, ela nunca será reconhecida novamente, a menos que seja modificada pelo usuário final. O reconhecimento da segunda linha é tratado como uma operação de reconhecimento independente.

Essa abordagem incremental funciona bem no nível de linha para as operações de reconhecimento, mas precisa funcionar em um nível mais alto para a operação de análise de tinta. Como o analisador de tinta pode detectar diferentes classificações de nível superior para essas cinco linhas de tinta (por exemplo, pode ser um parágrafo padrão ou cinco itens em uma lista), a abordagem incremental para o analisador de tinta é que ele precisa analisar essas estruturas superiores. Ou seja, depois que o analisador de tinta classifica a primeira linha de tinta como uma linha, ele verifica duas vezes se ainda é uma linha quando classifica a segunda linha. No entanto, o analisador de tinta isola essa verificação dupla no parágrafo e ignora o primeiro parágrafo ao analisar um segundo parágrafo, tratando o segundo parágrafo como uma operação independente do analisador de tinta. Essa abordagem incremental para análise economiza drasticamente o tempo de processamento quando grandes quantidades de tinta já existem no aplicativo.

### <a name="persistence"></a>Persistência

A análise incremental funciona bem dentro de uma determinada sessão ou instância de [**um objeto InkAnalyzer.**](inkanalyzer.md) No entanto, as APIs da plataforma tablet pc de primeira geração não podem executar análise incremental depois que a tinta é persistida no disco. A API InkAnalysis permite salvar tinta em disco junto com uma forma persistente dos resultados da análise. Os resultados da análise podem ser carregados quando a tinta é carregada e podem ser injetados em uma nova instância de **um InkAnalyzer.** Uma nova instância do objeto **InkAnalyzer** tem o mesmo estado de resultados que tinha anteriormente e agora pode aceitar quaisquer modificações como alterações incrementais no estado existente, em vez de analisar tudo novamente.

### <a name="data-proxy"></a>Proxy de dados

Muitos aplicativos já têm algum tipo de estrutura de documento existente em seus aplicativos; por exemplo, um grafo ou um banco de dados. O [**InkAnalyzer**](inkanalyzer.md) também apresenta resultados em uma forma estruturada, em uma árvore de [**objetos ContextNode.**](icontextnode.md) A **estrutura InkAnalyzer** e a estrutura existente do aplicativo precisam interoperar em duas direções: os resultados são obtidos do **InkAnalyzer** para o aplicativo e o estado é esvasado do aplicativo **para o InkAnalyzer.**

Se os resultados do [**InkAnalyzer**](inkanalyzer.md) para a estrutura do aplicativo fossem tudo o que era necessário, seria relativamente simples. Os aplicativos iterariam pela árvore de resultados e copiariam (integram) todas as partes dos resultados necessários em sua estrutura de dados existente. No entanto, como muitos aplicativos horizontais exigem análise incremental e persistência no disco, o problema se torna duas direções. O estado (resultados passados) precisa ser retirado da estrutura do aplicativo e esvasado para **o InkAnalyzer.**

Para atender a esse requisito, o [**InkAnalyzer**](inkanalyzer.md) contém uma série de eventos que ele gera no momento apropriado durante uma operação de análise para permitir que os aplicativos proxy da solicitação de dados de volta para suas estruturas existentes. Esses eventos são gerados somente para [**os objetos ContextNode**](icontextnode.md) exigidos pela operação incremental.

### <a name="reconciliation"></a>Reconciliação

A maioria dos aplicativos deseja analisar a tinta em segundo plano para manter as interrupções da interface do usuário no mínimo. A análise de tinta em segundo plano causará problemas, no entanto, se o usuário mudar a tinta (ou tinta vizinho) que está sendo analisada. Por exemplo, se o usuário excluir a tinta durante a operação em segundo plano, a estrutura resultante refletirá o estado do documento quando a operação em segundo plano foi iniciada, em vez de quando ela foi concluída.

Para auxiliar aplicativos, o [**InkAnalyzer**](inkanalyzer.md) reconcilia as diferenças no estado do documento entre o início e o fim da operação de análise. As alterações feitas pelo usuário ou aplicativo enquanto a análise está em execução em segundo plano sempre substituem os resultados calculados em segundo plano. Após a reconciliação, somente as partes da estrutura de resultados que não estão em conflito com alterações de documento são relatadas e os traços conflitantes são marcados para análise futura. Na próxima vez que a operação de análise em segundo plano for executado, os resultados serão recalculados com base no novo estado.

O diagrama a seguir mostra esse processo. O tempo é expresso linearmente de cima para baixo no diagrama.

![processo para reconciliar alterações de estado do documento durante a operação de análise](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

1.  No tempo 1 (T1), o aplicativo está coletando tinta do usuário final, incluindo qualquer tipo de modificação de tinta, como adicionar, remover ou modificar.
2.  Em T2, o aplicativo invoca a operação de análise em segundo plano. O [**InkAnalyzer**](inkanalyzer.md) determina qual tinta não tem resultados e qual tinta precisa ser verificada duas vezes. Ele copia os dados de tinta necessários para permitir que o thread em segundo plano seja executado de forma independente.
3.  No T3, o [**InkAnalyzer**](inkanalyzer.md) retorna a execução do thread da interface do usuário para o aplicativo. O **InkAnalyzer** cria um segundo thread, o thread de análise em segundo plano e os mecanismos de análise e reconhecimento de tinta analisam os dados de tinta copiados.
4.  Enquanto a operação de análise está ocorrendo no segundo thread em segundo plano, o usuário final continua editando o documento, adicionando e removendo dados de traço, em T4 e T5. Essas edições podem entrar em conflito com o trabalho que está sendo processado em segundo plano.
5.  Em T6, o thread em segundo plano concluiu a operação de análise e os resultados estão prontos. Antes que o [**InkAnalyzer**](inkanalyzer.md) comunique os resultados para o aplicativo, ele executa um algoritmo de reconciliação para determinar se as edições do usuário foram feitas enquanto a operação de análise estava sendo calculada (T4 e T5) em conflito com os resultados. Se qualquer colisão for detectada, os traços conflitantes serão sinalizados para reanálise, que ocorrerá na próxima vez que o aplicativo invocar a operação de análise em segundo plano.
6.  Por fim, em T7, com todas as colisões detectadas, o [**InkAnalyzer**](inkanalyzer.md) apresenta os resultados para o aplicativo.

### <a name="extensibility"></a>Extensibilidade

As APIs InkAnalysis permitem que novos tipos de mecanismos de análise sejam usados por aplicativos, de forma a impedir que o aplicativo precise reescrever todos os benefícios da API InkAnalysis, incluindo reconciliação, proxy de dados, persistência e análise incremental.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft. Ink](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 
