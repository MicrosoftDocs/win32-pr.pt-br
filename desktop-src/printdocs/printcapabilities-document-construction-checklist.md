---
description: Este artigo fornece uma lista de verificação que os autores de documentos de PrintCapabilities podem usar para criar um documento de PrintCapabilities que descreve um dispositivo.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Lista de verificação de construção de documentos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5284a480f73151750926d975535ea799457a1ce2cd4c14f197a4fc6519b646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867958"
---
# <a name="printcapabilities-document-construction-checklist"></a>Lista de verificação de construção de documentos de PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O [Resumo dos tipos de elementos](summary-of-element-types.md) aborda os vários elementos que compõem um documento de PrintCapabilities. Esta seção fornece uma lista de verificação que os autores de documentos de PrintCapabilities podem usar para criar um documento de PrintCapabilities que descreve um dispositivo.

1.  Identifique todos os atributos de dispositivo que contribuem para a configuração do dispositivo. Para cada atributo de dispositivo, determine se ele deve ser representado como um constructo de recurso/opção ou como uma construção de parâmetro.

2.  Para cada recurso de dispositivo, determine se ele pode ser representado por um recurso definido nas palavras-chave do esquema de impressão. Caso contrário, será necessário introduzir um novo recurso definido de modo privado (e um atributo de nome correspondente).

    -   Para as palavras-chave do esquema de impressão – instâncias de recurso definidas, identifique cada um dos Estados disponíveis para os quais esse recurso pode ser definido. Cada Estado corresponde a uma opção da instância de recurso. Determine quais desses Estados correspondem para imprimir instâncias de opção definidas pelo esquema associadas a esse recurso e quais Estados exigem uma instância de opção personalizada. O tópico [definições de opção](option-definitions.md) apresenta informações sobre como construir novas instâncias de opção e como derivar novas instâncias de opção de instâncias de opção existentes.

    -   Para instâncias de recurso não padrão, identifique as características que podem ser usadas para distinguir uma opção de outra. Represente cada característica desse tipo por um elemento ScoredProperty e, em cada instância de opção, atribua a cada ScoredProperty um valor que seja específico a essa opção. Verifique se há elementos ScoredProperty suficientes para que cada opção para um determinado recurso seja exclusiva. As instâncias de recurso e opção não padrão são por sua natureza não-Portable. Ou seja, outro driver não conseguirá localizar nenhum recurso equivalente ou opção para corresponder a um recurso ou opção não padrão especificada no PrintTicket que o driver cria.

3.  Determine se qualquer opção deve conter elementos ParameterRef. Para obter mais informações, consulte [construções de parâmetro](parameter-constructs.md) e elementos de referência de [parâmetro](parameter-reference-elements.md).

4.  Para parâmetros, determine se uma das instâncias de ParameterDef definidas nas palavras-chave do esquema de impressão é uma correspondência adequada. Nesse caso, copie a instância ParameterDef das palavras-chave do esquema de impressão e ajuste o valor de cada instância de propriedade mutável para o melhor ajuste. Se nenhuma das instâncias de ParameterDef nas palavras-chave do esquema de impressão for uma correspondência adequada, crie sua própria instância ParameterDef. Para obter mais informações, consulte [parâmetros no documento PrintCapabilities](parameters-in-the-printcapabilities-document.md).

5.  Verifique se todas as instâncias de propriedade e ScoredProperty exigidas pelo documento de palavras-chave do esquema de impressão estão presentes no documento de PrintCapabilities e se elas foram inicializadas corretamente.

6.  Adicione outras instâncias de propriedade e subpropriedade conforme desejado. Você pode introduzir instâncias de propriedade definidas de modo privado se houver aspectos do dispositivo que você precisa para caracterizar que não são cobertos pelas instâncias de propriedade definidas nas palavras-chave do esquema de impressão.

7.  Observe a Convenção de namespace para atributos de nome. Isso se aplica a atributos de nome definidos de forma privada, bem como àqueles definidos nas palavras-chave do esquema de impressão.

8.  Os filhos do mesmo tipo de elemento não podem aninhar uma profundidade de mais de 10 elementos. Essa regra se aplica de forma independente a cada tipo de elemento que pode ser definido.

Observe que o conteúdo XML do documento de recursos de impressão deve ser codificado usando UTF-8 ou UTF-16.

Observe que o conjunto de instâncias Feature, Option e ParameterDef relatadas não devem ser alteradas, independentemente do instantâneo. As instâncias de ScoredProperty que compõem cada instância de opção e o valor atribuído a cada elemento ScoredProperty também não devem ser alteradas. O mesmo se aplica às instâncias de propriedade que compõem cada instância de ParameterDef.

Para obter uma lista de instâncias de propriedade adicionais que devem ser fornecidas para definir totalmente os parâmetros e construções de recurso/opção, consulte [ParameterDef](parameterdef.md) e [ParameterInit](parameterinit.md). Por exemplo, cada recurso deve especificar seu comportamento de interface do usuário, especificamente, se exatamente uma ou várias instâncias de opção podem ser selecionadas para cada recurso ao mesmo tempo. O documento de palavras-chave do esquema de impressão define essas instâncias de propriedade, onde elas devem aparecer dentro do documento PrintCapabilities e quais instâncias de valor definidas nas palavras-chave do esquema de impressão estão disponíveis.

O provedor de PrintCapabilities é responsável por emitir o valor apropriado para todas as instâncias de propriedade dependentes de configuração. Por exemplo, se a taxa de impressão depender do modo de cor e da resolução usada, o provedor de PrintCapabilities deverá observar o modo de cor e as configurações de resolução especificadas no PrintTicket fornecido pelo cliente e deve relatar o valor adequado para a taxa de impressão. Observe que cada instância de ScoredProperty deve ter um único valor; sua instância de valor não pode ser alterada quando a configuração do dispositivo é alterada.

Observe também que as instâncias de propriedade definidas nas palavras-chave do esquema de impressão devem aparecer no local especificado lá. Eles não podem aparecer em locais arbitrários em um documento de PrintCapabilities. As instâncias de propriedade definidas de modo privado podem aparecer em qualquer lugar, mesmo como as subpropriedades nas instâncias de propriedade definidas pelo esquema.

Observe que um conflito funcional entre as configurações é definido como dois elementos de esquema de impressão não conflitantes que têm função semelhante, mas são recursos diferentes. Um exemplo seria JobDuplexAllDocumentsContiguously e DocumentDuplex; ambos representam a função duplex do dispositivo, mas diferem no aplicativo da função, um que se aplica a todo o trabalho de forma contígua e um para documentos. No caso em que dois elementos desse tipo são especificados, a precedência é determinada pelo produtor de PrintCapabilities e pelo consumidor PrintTicket. É responsabilidade do produtor de PrintCapabilities indicar corretamente restrições entre elementos conflitantes por meio do atributo "restrito". Elementos no esquema de impressão pública que exibem esse conflito semântico são identificados em sua definição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



