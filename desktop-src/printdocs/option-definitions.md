---
description: Saiba mais sobre definições de opção no esquema PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Definições de opção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f71f4201bb9bd38860a79fead7fd3e8738429fc34b729981af68c0d2d1f38d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098950"
---
# <a name="option-definitions"></a>Definições de opção

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A principal consideração quando você define uma Opção é fazer isso de forma que ela possa ser significativamente comparada com outras instâncias option contidas no mesmo recurso. A comparação deve ser significativa porque a instância Option é usada para definir a configuração não apenas do dispositivo, mas do trabalho, independentemente do dispositivo ou printCapabilities que foram usados para criar a configuração. As outras instâncias option no recurso podem aparecer no mesmo documento PrintCapabilities ou em outro documento PrintCapabilities que representa um dispositivo diferente, um documento PrintCapabilities definido por outra parte trabalhando independentemente. Depois que um cliente seleciona a configuração do dispositivo a ser usada para renderizar um trabalho ou documento, essa configuração normalmente é salva, juntamente com o trabalho ou documento, na forma de um PrintTicket. O PrintTicket contém um conjunto de instâncias option, normalmente uma para cada Recurso definido no documento PrintCapabilities. As instâncias de opção devem ser portáteis e devem preservar a intenção de impressão, para que a intenção possa ser comunicada quando esse PrintTicket for dado a um dispositivo diferente, mesmo que tenha um documento PrintCapabilities diferente escrito por um autor diferente. O principal benefício dessa portabilidade é que, se um dispositivo diferente não dá suporte especificamente a uma Opção contida no PrintTicket, o driver ou subsistema do dispositivo é capaz de identificar e selecionar a Opção mais próxima na funcionalidade.

Uma das principais funções printTicket do driver é identificar a Opção do dispositivo no documento PrintCapabilities que mais corresponde a uma Opção específica listada no PrintTicket. Durante esse processo de pontuação correspondente ou definido pelo driver de dispositivo, a Opção no PrintTicket é chamada  de Opção de referência, enquanto a Opção no documento PrintCapabilities é conhecida como a Opção candidata.  A métrica de correspondência geral é o número de instâncias ScoredProperty correspondentes nas instâncias de Opção de candidato e de referência; um número maior de corresponde geralmente indica melhor preservação da intenção de impressão. Em seu processo de pontuação, você pode optar por dar mais peso a alguns elementos ScoredProperty do que a outros.

Você pode tornar as instâncias option portáteis garantindo que todas as instâncias option que pertencem ao mesmo Recurso tenham um ou mais elementos ScoredProperty *em comum.* Isso significa que há um conjunto de elementos ScoredProperty que aparece em cada instância option (pertencente ao mesmo recurso). Por exemplo, as instâncias option para o recurso PageMediaSize poderão ser portáteis se cada instância option contiver elementos ScoredProperty que definem as propriedades intrínsecas PageMediaSize: MediaSizeWidth e MediaSizeHeight. O driver de dispositivo ou o código do subsistema pode determinar o quão próximas duas instâncias option concordarem comparando as diferenças nesses valores ScoredProperty. Se não houver nenhuma Opção no documento PrintCapabilities que corresponde exatamente à do PrintTicket, o driver de dispositivo poderá determinar e selecionar facilmente a Opção que tem as dimensões de mídia correspondentes mais próximas.

Dois objetos (Instâncias de opção nesse caso) têm elementos em comum *ou,* de modo equivalente, têm elementos correspondentes *,* se as três condições a seguir são atendidas.

1.  Os dois elementos são do mesmo tipo de elemento.

2.  Os atributos de nome dos dois elementos são idênticos (ou nenhum elemento contém um atributo de nome).

3.  A cadeia de pais dos elementos que estão sendo comparados, até os dois objetos em consideração, deve atender às condições 1 e 2.

Por exemplo, considere uma situação em que há duas instâncias option, em que cada uma contém uma instância ScoredProperty e que cada uma dessas instâncias ScoredProperty contém uma instância property. Claramente, a primeira condição é atendida (as duas instâncias de Propriedade são do mesmo tipo) e parte da terceira condição é atendida (os pais das instâncias de Propriedade são do mesmo tipo, ScoredProperty e os pais desses elementos são as instâncias Option, que também são do mesmo tipo). Se os atributos de nome de, respectivamente, as instâncias property, as instâncias ScoredProperty e as instâncias Option são idênticos ou não são fornecidos, as duas instâncias Option têm elementos em comum.

Desde o início, a primeira etapa na criação de instâncias option é definir um conjunto de elementos ScoredProperty que estão presentes na maioria ou em todas as instâncias option. Se o atributo de configuração do dispositivo puder ser representado por um Recurso padrão (um listado nas Palavras-chave de esquema de impressão), observe os elementos ScoredProperty em comum nas instâncias de Opção padrão. Você deve garantir que todas as novas instâncias de Opção que você introduz também contenham esses elementos ScoredProperty. Você sempre é livre para adicionar elementos ScoredProperty adicionais conforme necessário para diferenciar suas instâncias de Opção das instâncias de Opção padrão. Você pode até mesmo excluir um ou mais dos elementos ScoredProperty em comum se houver um bom motivo, embora isso reduza a portabilidade de tal opção. É claro que as considerações de portabilidade sugerem o uso das instâncias de Opção padrão não modificadas, a menos que haja alguma diferença intrínseca entre sua Opção e a instância de Opção padrão que deve ser refletida na nova instância option.

O exemplo a seguir ilustra uma situação para a qual talvez você queira adicionar um elemento ScoredProperty a uma instância option. Todas as instâncias de Opção padrão para o recurso PageMediaSize têm os elementos MediaSizeWidth e MediaSizeHeight ScoredProperty em comum. Suponha que seu dispositivo possa dar suporte a um dos tamanhos de mídia de Letra padrão alimentando o papel transversamente (LongEdgeFirst) ou de forma mesiva (ShortEdgeFirst). Supondo que você não queira introduzir uma nova direção do feed Recurso para expor esse grau de liberdade, você pode modificar as duas instâncias de Opção PageMediaSize para Letra incorporar a orientação do feed de papel. Para essas duas instâncias de Opção de Letra, comece com a instância padrão pageMediaSize Option e adicione um novo elemento ScoredProperty para representar o FeedDirection. Em uma instância option, de definir FeedDirection ScoredProperty como LongEdgeFirst; na outra instância option, de definir FeedDirection como ShortEdgeFirst. Observe que essas novas instâncias de Opção mantêm sua portabilidade. Se a Opção que representa Letter, ShortEdgeFirst for salva em um PrintTicket e um dispositivo diferente que dá suporte apenas à Opção Padrão de Letra estiver selecionado para renderizar o Trabalho, o código correspondente à opção poderá determinar rapidamente que a Letra da Opção padrão é a melhor correspondência para a Letra da Opção, ShortEdgeFirst. O motivo pelo qual essa é a melhor correspondência é que todas as instâncias ScoredProperty concordam, com exceção de FeedDirection ScoredProperty, que não existe na Opção Padrão de Letra.

Você também pode encontrar casos em que as modificações na Opção realmente alteram tanto o significado que a Opção modificada não pode mais ser considerada um caso especializado do original. Nesses casos, você deve alterar o nome da Opção para refletir a diferença entre a instância de Opção modificada e a não modificada. Somente o autor do documento PrintCapabilities para um dispositivo específico pode decidir se a Opção oferecida pelo dispositivo difere o suficiente de uma instância de Opção padrão para justificar uma definição incompatível.

Agora considere o caso em que o dispositivo tem um atributo de configuração de dispositivo que não corresponde a nenhuma das instâncias de recurso padrão. Nesse caso, você não pode contar com as instâncias de Opção padrão para fornecer a lista de elementos ScoredProperty em comum. Quando você cria uma instância ScoredProperty, seu objetivo principal é diferenciar cada Opção das outras no Recurso e descrever por que um usuário selecionaria uma Opção em vez de outra. A linha de base é caracterizar cada Opção com um atributo de nome exclusivo, e a ScoredProperty que contém o atributo name torna-se aquela usada para determinar elementos em comum.

Depois que um conjunto de elementos ScoredProperty em comum tiver sido estabelecido, é uma questão simples atribuir valores apropriados a cada ScoredProperty para criar cada Opção. Como no exemplo anterior, para determinadas instâncias option, talvez seja necessário adicionar instâncias adicionais de ScoredProperty ou excluir alguns dos elementos em comum para criar uma instância de Option apropriada.

Deve-se lembrar que o Esquema de Impressão requer que o conjunto de instâncias ScoredProperty, seus locais e os valores atribuídos a cada ScoredProperty em uma Opção permaneçam constantes, independentemente da configuração. Todo o conceito do esquema de impressão se baseia em instâncias de Opção que têm instâncias fixas, de identificação de Propriedade e ScoredProperty que são compartilhadas entre vários dispositivos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



