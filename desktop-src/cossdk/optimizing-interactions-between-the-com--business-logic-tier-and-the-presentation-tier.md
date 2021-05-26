---
description: Normalmente, a latência entre camadas de um aplicativo distribuído é muito diferente.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Otimizando interações entre a camada lógica de negócios COM+ e a camada de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3258453a16549eacf3a7ed77444674d425c85613
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423496"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Otimizando interações entre a camada lógica de negócios COM+ e a camada de apresentação

Normalmente, a latência entre camadas de um aplicativo distribuído é muito diferente. Chamadas entre a camada de apresentação e a camada de lógica de negócios geralmente são uma ordem de magnitude mais lenta do que as chamadas entre a camada de negócios e a camada de dados. Como resultado, o estado mantido é mais caro ao chamar a camada lógica de negócios.

Os tópicos a seguir discutem maneiras de passar dados entre as camadas de lógica de negócios e apresentação:

-   [Passar parâmetros](#passing-parameters)
-   [Opções de passagem de dados](#data-passing-options)
-   [Usando um padrão de fábrica para passar dados](#using-a-factory-pattern-to-pass-data)
-   [Tópicos relacionados](#related-topics)

## <a name="passing-parameters"></a>Passar parâmetros

Para um determinado conjunto de informações a ser passado entre a camada de apresentação e a camada de lógica de negócios, você pode ter uma única linha, várias linhas ou uma combinação de uma única linha (como um header) e várias linhas de detalhes de dados. A maneira mais eficiente de passar essas informações entre camadas é por uma única chamada de método. Essa única chamada gerenciaria todo o conjunto de informações a ser passado. Isso é necessário, a menos que você opte por controlar a transação da camada de apresentação (e tornar todos os tratamentos de transação na camada de apresentação idênticos na função). A Microsoft não recomenda a realização de transações da camada de apresentação porque chamadas entre essa camada e a camada lógica de negócios geralmente são as chamadas mais lentas em um aplicativo de várias camadas.

Uma maneira de criar esse método é passar linhas de informações como parâmetros e passar várias linhas como registros ADO. Os registros são o núcleo da metodologia de acesso a dados ADO da Microsoft e o uso de registros ADO permite que você passe todas as informações relacionadas a uma única transação em uma única etapa.

## <a name="data-passing-options"></a>Opções de passagem de dados

Há outras opções a considerar ao passar dados. Isso inclui o uso de uma lista de parâmetros e conjuntos de registros ADO (como discutido acima), apenas conjuntos de registros ADO, cadeias de caracteres codificadas em XML ou matrizes de estruturas. Esta seção aborda cada uma dessas opções.

A tabela a seguir mostra áreas em que é necessário ter cuidado extra ao usar qualquer uma das quatro diferentes possibilidades de passagem de argumentos. Um "X" representa áreas em que as compensações precisam ser compreendidas e avaliadas em relação às necessidades de cada projeto. Tente não fazer decisões de passagem de argumentos em uma base por componente. Os benefícios de um modelo de programação consistente em todo o projeto superam muito a vantagem de otimizar em uma base por método ou por componente em todas as circunstâncias mais extremas. As colunas são descritas na lista que segue a tabela.



|     &nbsp;                  | Simultaneidade  | WAN          | Implantação   | Complexidade   |
|-----------------------|--------------|--------------|--------------|--------------|
| Entrada | Valor |
| Conjuntos<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Matrizes<br/>     | X<br/> |              | X<br/> | X<br/> |



 

As quatro colunas definem áreas a serem inspecionadas ao usar essa opção para passar parâmetros.

-   **A coluna Concurrency** representa a necessidade de codificar ou fornecer um mecanismo que gerencia condições de bloqueio em operações de atualização. Como os métodos que executam salvas podem representar atualizações, podem surgir problemas de simultaneidade. Dois tipos de bloqueio são predominantemente otimistas e pessimistas. Os bloqueios pessimistas impedem que um usuário obtenha dados para atualização enquanto outro usuário tem o potencial de executar uma atualização. O bloqueio otimista dá suporte a um grande número maior de usuários, negociando com a probabilidade de que os dois usuários atualizem o mesmo documento ao mesmo tempo. Chamadas de bloqueio otimista para verificação para ver se os dados armazenados correspondem aos dados no ponto em que uma cópia dos dados foi acessada para modificação. Os conjuntos de registros ADO fornecem suporte automático para bloqueio otimista. Cenários de atualização que envolvem listas de parâmetros de linha única não fornecem suporte suficiente para verificação de simultaneidade. O XML sofre a partir desse mesmo problema, pois nenhum reconhecimento de bloqueio está presente nos dados XML.
-   **A coluna Wan representa as** condições em que pode haver contenção de transmissão em uma WAN (rede de longa distância). Quando a WAN não tem capacidade suficiente para gerenciar todos os dados que estão sendo movidos ao mesmo tempo, os usuários do aplicativo experimentam atrasos no tempo de resposta. Para dar suporte à simultrreidade otimista, os registros ADO desconectados passam duas cópias dos dados do servidor para o cliente. A segunda cópia é usada pelo cliente para determinar o menor grupo de linhas de atualização a ser repassado quando uma alteração está sendo confirmada. Embora isso reduza o tráfego da camada de apresentação para os dados, a carga extra da segunda cópia pode ser significativa. O uso de conjuntos de registros como o único meio de passar todas as informações, portanto, faz com que duas vezes mais dados sejam passados entre camadas conforme necessário, exceto quando o conjuntos de linhas de atualização está sendo passado de volta para a camada de dados de uma camada de apresentação.
-   **A coluna Implantação** representa problemas associados à passagem de dados quando a tecnologia especial é necessária no lado do chamador e do componente da rede. Por exemplo, usar os registros ADO exige que os componentes ADO sejam presentes no cliente e no servidor. Os analisadores XML também devem estar presentes em ambos os lados, para evitar a precisar codificar analisadores em seus aplicativos.
-   **A coluna Complexidade é** indicada para todas as quatro opções e é uma questão de preferência ou experiência de modelo de programação anterior que pode já estar estabelecida em sua organização de desenvolvimento. Algumas pessoas acham que a passagem de parâmetros é complicada e acham que ele adiciona muita complexidade ao problema de programação. Manter o controle de qual parâmetro você está manipulando e deixar todos eles visíveis em uma janela de edição pode criar uma complexidade logística que alguns desenvolvedores encontram insumanável.

O método de passagem de parâmetro também pode ter trocas, como as seguintes:

-   Os parâmetros podem envolver o gerenciamento de vários argumentos e tipos de argumentos, bem como a decisão de quando é apropriado tornar um parâmetro de um registro.
-   Os registros ADO podem reduzir as relações hierárquicas nos parâmetros de método para um ou dois argumentos. Isso simplifica drasticamente o modelo de programação e dá suporte à adição de colunas em um momento posterior, mas também oculta a hierarquia de informações. O uso de informações em um conjunto de registros ADO e posteriormente sua extração envolve saber os nomes de cada coluna ou conhecer a ordem das colunas. Essa situação pode adicionar complexidade para outros desenvolvedores de componentes ou aplicativos no projeto.
-   O XML é uma rotação diferente na complicação da hierarquia oculta mencionada acima. O programador precisa entender o uso de um analisador XML para obter acesso às informações e, muitas vezes, deve saber os nomes de cada item no conjunto de dados antes que o conjunto de dados possa ser encontrado.
-   Matrizes de estruturas apresentam a necessidade de uma compreensão comum das informações que estão sendo passadas por parte do chamador e do componente. Essa necessidade de um mapa compartilhado entre dois elementos do sistema pode levar a dificuldades ao lidar com versões diferentes de componentes. Embora a assinatura do método não seja alterada, as alterações nas informações esperadas podem renderizar os programas de chamada incompatíveis.

Como os problemas de complexidade associados a todos os quatro métodos de passagem de parâmetros são tão semelhantes, é um debate de que há uma oportunidade de simplificação significativa associada a uma seleção.

## <a name="using-a-factory-pattern-to-pass-data"></a>Usando um padrão de fábrica para passar dados

Um ponto de design importante é a facilidade de uso. No momento em que você decidiu usar conjuntos de registros ADO para passar um conjunto estruturado de detalhes de volta para a camada de apresentação, você introduziu um problema de complexidade. Os programadores da camada de apresentação precisam entender a estrutura desses conjuntos de registros. Um problema maior de complexidade pode surgir quando você precisa de vários detalhes para que um conjunto de dados seja passado em um conjunto de registros. Para simplificar as coisas, você deve considerar a criação de um método de fábrica do conjunto de registros sempre que pretender exigir que os dados sejam passados em conjuntos de registros ADO estruturados.

A fábrica do conjunto de registros deve retornar um conjunto de registros desconectado vazio, mas gravável para o chamador. Esse registro deve ter os campos apropriados (nomes e tipos de dados) já configurados para que o cliente de chamada não precise saber como fabricar o registro. Essa abordagem geralmente é  chamada de padrão de fábrica e é um padrão de solução comum que resolve a necessidade de criar um objeto de uma determinada complexidade sem precisar conhecer as nuances de sua criação.

Opções de design simples, como escolher o mesmo nome de parâmetro para a mesma parte dos dados em cada método em que essas informações são passadas, facilita a análise de um método e a saber o que é esperado. Garantir que a ordem na qual argumentos semelhantes são passados seja consistente em toda uma família de métodos fornece um ponto de conforto que impõe um modelo consistente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Otimizando interações entre a camada lógica de negócios COM+ e a camada de dados](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




