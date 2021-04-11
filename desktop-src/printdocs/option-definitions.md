---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Definições de opção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10016b295cc2da7ede4e6a4f8944f279a25f6f9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172569"
---
# <a name="option-definitions"></a>Definições de opção

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A consideração principal quando você define uma opção é fazê-lo de forma que possa ser comparada de modo significativo com outras instâncias de opção contidas no mesmo recurso. A comparação deve ser significativa porque a instância de opção é usada para definir a configuração não apenas do dispositivo, mas do trabalho, independentemente do dispositivo ou de PrintCapabilities que foram usados para criar a configuração. As outras instâncias de opção no recurso podem aparecer no mesmo documento de PrintCapabilities ou em outro documento de PrintCapabilities que representa um dispositivo diferente, um documento de PrintCapabilities que é definido por outra parte que trabalha de forma independente. Depois que um cliente seleciona a configuração do dispositivo a ser usada para renderizar um trabalho ou documento, essa configuração normalmente é salva, juntamente com o trabalho ou o documento, na forma de um PrintTicket. O PrintTicket contém um conjunto de instâncias de opção, normalmente um para cada recurso definido no documento PrintCapabilities. As instâncias de opção devem ser portáteis e devem preservar a intenção de impressão, para que a intenção possa ser comunicada quando esse PrintTicket for fornecido a um dispositivo diferente, mesmo um que tenha um documento de PrintCapabilities diferente que foi escrito por um autor diferente. O principal benefício dessa portabilidade é que, se um dispositivo diferente não oferecer suporte especificamente a uma opção contida no PrintTicket, o driver ou o subsistema do dispositivo poderá identificar e selecionar a opção mais próxima da funcionalidade.

Uma das principais funções de PrintTicket do driver é identificar a opção de dispositivo no documento PrintCapabilities que mais se aproximar de uma determinada opção listada no PrintTicket. Durante essa correspondência ou o processo de Pontuação definido pelo driver de dispositivo, a opção no PrintTicket é referida como a opção de *referência* , enquanto a opção no documento PrintCapabilities é conhecida como a opção *candidato* . A métrica de correspondência geral é o número de instâncias de ScoredProperty correspondentes nas instâncias de opção de candidato e de referência; um número maior de correspondências geralmente indica melhor preservação da intenção de impressão. No processo de pontuação, você pode optar por fornecer mais peso a alguns elementos ScoredProperty do que a outras pessoas.

Você pode tornar as instâncias de opção portáveis, garantindo que todas as instâncias de opção que pertencem ao mesmo recurso tenham um ou mais *elementos ScoredProperty em comum*. Isso significa que há um conjunto de elementos ScoredProperty que aparece em cada instância de opção (que pertence ao mesmo recurso). Por exemplo, as instâncias de opção para o recurso PageMediaSize podem ser portáteis se cada instância de opção contiver elementos ScoredProperty que definem as propriedades intrínsecas PageMediaSize: MediaSizeWidth e MediaSizeHeight. O código do subsistema ou driver de dispositivo pode então determinar o quanto duas instâncias de opção concordam comparando as diferenças nesses valores de ScoredProperty. Se não houver nenhuma opção no documento PrintCapabilities que corresponda exatamente à que está no PrintTicket, o driver de dispositivo poderá determinar e selecionar facilmente a opção que tem as dimensões de mídia correspondentes mais próximas.

Dois objetos (instâncias de opção, nesse caso) devem ter *elementos em comum*, ou equivalente, têm *elementos correspondentes*, se as três condições a seguir forem satisfeitas.

1.  Os dois elementos são do mesmo tipo de elemento.

2.  Os atributos de nome dos dois elementos são idênticos (ou nenhum elemento contém um atributo de nome).

3.  A cadeia de pais dos elementos que estão sendo comparados, até os dois objetos em consideração, deve satisfazer as condições 1 e 2.

Por exemplo, considere uma situação em que há duas instâncias de opção, onde cada uma contém uma instância de ScoredProperty e que cada uma dessas instâncias de ScoredProperty contém uma instância de propriedade. Claramente, a primeira condição é satisfeita (as duas instâncias de propriedade são do mesmo tipo) e parte da terceira condição é satisfeita (os pais das instâncias de propriedade são do mesmo tipo, ScoredProperty e os pais desses elementos são as instâncias de opção, que também são do mesmo tipo). Se os atributos de nome de, respectivamente, as instâncias de propriedade, as instâncias ScoredProperty e as instâncias de opção forem idênticas ou não forem fornecidas, as duas instâncias de opção terão elementos em comum.

Desde o precedente, a primeira etapa na criação de instâncias de opção é definir um conjunto de elementos ScoredProperty que estão presentes na maioria ou em todas as instâncias de opção. Se o atributo de configuração do dispositivo puder ser representado por um recurso padrão (um listado nas palavras-chave do esquema de impressão), observe os elementos ScoredProperty em comum nas instâncias de opção padrão. Você deve garantir que qualquer nova instância de opção introduzida também contenha esses elementos ScoredProperty. Você está sempre livre para adicionar outros elementos ScoredProperty conforme necessário para diferenciar suas instâncias de opção das instâncias de opção padrão. Você pode até mesmo excluir um ou mais dos elementos ScoredProperty em comum se houver um bom motivo, embora isso reduza a portabilidade de tal opção. É claro que as considerações de portabilidade sugerem usar as instâncias de opção padrão não modificadas, a menos que haja alguma diferença intrínseca entre sua opção e a instância de opção padrão que deve ser refletida na nova instância de opção.

O exemplo a seguir ilustra uma situação para a qual você pode desejar adicionar um elemento ScoredProperty a uma instância de opção. Todas as instâncias de opção padrão para o recurso PageMediaSize têm os elementos MediaSizeWidth e MediaSizeHeight ScoredProperty em comum. Suponha que seu dispositivo possa dar suporte a um dos tamanhos de mídia de carta padrão alimentando o papel de forma inverso (LongEdgeFirst) ou longitudinally (ShortEdgeFirst). Supondo que você não deseja introduzir um novo recurso de direção de feed para expor esse grau de liberdade, você pode modificar as duas instâncias de opção de PageMediaSize para carta para incorporar a orientação do feed de papel. Para essas duas instâncias de opção de letra, comece com a instância de opção PageMediaSize padrão e adicione um novo elemento ScoredProperty para representar o FeedDirection. Em uma instância de opção, defina FeedDirection ScoredProperty como LongEdgeFirst; na outra instância de opção, defina FeedDirection como ShortEdgeFirst. Observe que essas novas instâncias de opção mantêm sua portabilidade. Se a opção que representa a letra, ShortEdgeFirst for salva em um PrintTicket e um dispositivo diferente que dá suporte apenas à opção padrão de letra for selecionado para renderizar o trabalho, o código de correspondência de opção poderá determinar rapidamente que a letra de opção padrão é a melhor correspondência com a letra de opção, ShortEdgeFirst. O motivo pelo qual essa é a melhor correspondência é que todas as instâncias de ScoredProperty concordam, com exceção do FeedDirection ScoredProperty, que não existe na opção de letra padrão.

Você também pode encontrar casos em que as modificações na opção realmente alterem o significado, tanto que a opção modificada não possa mais ser considerada um caso especializado do original. Nesses casos, você deve alterar o nome da opção para refletir a diferença entre a instância de opção modificada e a não modificada. Somente o autor do documento PrintCapabilities de um determinado dispositivo pode decidir se a opção oferecida pelo dispositivo difere suficientemente de uma instância de opção padrão para garantir uma definição incompatível.

Agora, considere o caso em que o dispositivo tem um atributo de configuração de dispositivo que não corresponde a nenhuma das instâncias de recurso padrão. Nesse caso, você não pode contar com as instâncias de opção padrão para fornecer a lista de elementos ScoredProperty em comum. Quando você cria uma instância ScoredProperty, seu objetivo principal é diferenciar cada opção dos outros no recurso e descrever por que um usuário deve selecionar uma opção em relação a outra. A linha de base é caracterizar cada opção com um atributo de nome exclusivo e o ScoredProperty que mantém o atributo de nome se torna aquele usado para determinar os elementos em comum.

Depois que um conjunto de elementos ScoredProperty em comum tiver sido estabelecido, é uma questão simples de atribuir valores apropriados a cada ScoredProperty para criar cada opção. Como no exemplo anterior, para determinadas instâncias de opção, talvez seja necessário adicionar instâncias ScoredProperty adicionais ou excluir alguns dos elementos em comum para criar uma instância de opção apropriada.

Deve-se observar que o esquema de impressão requer que o conjunto de instâncias ScoredProperty, suas localizações e os valores atribuídos a cada ScoredProperty em uma opção deva permanecer constante, independentemente da configuração. O conceito completo do esquema de impressão depende de instâncias de opção que tenham uma propriedade fixa e identificável e instâncias de ScoredProperty que são compartilhadas entre vários dispositivos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



