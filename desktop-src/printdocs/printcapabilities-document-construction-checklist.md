---
description: Este artigo fornece uma lista de verificação que os autores de documentos PrintCapabilities podem usar para criar um documento PrintCapabilities que descreve um dispositivo.
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: Lista de verificação de construção de documentos PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee309c96cf7b2d70cb78f125e7783668fb2298da
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407109"
---
# <a name="printcapabilities-document-construction-checklist"></a>Lista de verificação de construção de documentos PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O [Resumo dos Tipos de Elemento](summary-of-element-types.md) aborda os vários elementos que comprimem um documento PrintCapabilities. Esta seção fornece uma lista de verificação que os autores de documentos PrintCapabilities podem usar para criar um documento PrintCapabilities que descreve um dispositivo.

1.  Identifique todos os atributos de dispositivo que contribuem para a configuração do dispositivo. Para cada atributo de dispositivo desse tipo, determine se ele deve ser representado como um constructo de Recurso/Opção ou como um constructo de parâmetro.

2.  Para cada recurso de dispositivo, determine se ele pode ser representado por um Recurso definido nas Palavras-chave de esquema de impressão. Caso não seja, você precisará introduzir um novo Recurso definido de forma privada (e um atributo de nome correspondente).

    -   Para Instâncias de recurso definidas por palavras-chave de esquema de impressão, identifique cada um dos estados disponíveis para os quais esse Recurso pode ser definido. Cada estado corresponde a uma Opção da instância de Recurso. Determine qual desses estados corresponde às instâncias de Opção definidas pelo esquema de impressão associadas a esse Recurso e quais estados exigem uma instância de Opção personalizada. O [tópico Definições de](option-definitions.md) Opção apresenta informações sobre como construir novas instâncias de Opção e como derivar novas instâncias option de instâncias option existentes.

    -   Para instâncias de recurso não padrão, identifique as características que podem ser usadas para distinguir uma Opção de outra. Represente cada característica por um elemento ScoredProperty e, em cada instância option, atribua a cada ScoredProperty um Valor específico a essa Opção. Verifique se há elementos ScoredProperty suficientes para que cada Opção de um determinado Recurso seja exclusiva. As instâncias de Recurso e Opção não padrão são por natureza nãoportáveis. Ou seja, outro driver não poderá encontrar nenhum Recurso ou Opção equivalente para corresponder a um Recurso ou Opção não padrão especificado no PrintTicket que o driver cria.

3.  Determine se qualquer Opção deve conter elementos ParameterRef. Para obter mais informações, consulte [Constructos de parâmetro e](parameter-constructs.md) [elementos de referência de parâmetro](parameter-reference-elements.md).

4.  Para parâmetros, determine se uma das instâncias parameterDef definidas nas Palavras-chave de esquema de impressão é uma combinação adequada. Em caso afirmativo, copie a instância ParameterDef das Palavras-chave de Esquema de Impressão e ajuste o Valor de cada instância de Propriedade mutável para o melhor ajuste. Se nenhuma das instâncias parameterDef nas Palavras-chave de esquema de impressão for uma combinação adequada, crie sua própria instância parameterDef. Para obter mais informações, [consulte Parâmetros no documento PrintCapabilities](parameters-in-the-printcapabilities-document.md).

5.  Verifique se todas as instâncias Property e ScoredProperty exigidas pelo documento Imprimir Palavras-chave de esquema estão presentes no documento PrintCapabilities e se elas foram inicializadas corretamente.

6.  Adicione instâncias de propriedade e subpropriedade adicionais conforme desejado. Você pode introduzir instâncias de Propriedade definidas de forma privada se houver aspectos do dispositivo que você precisa caracterizar que não são cobertos pelas instâncias de propriedade definidas nas Palavras-chave de esquema de impressão.

7.  Observe a Convenção de Namespace para atributos de nome. Isso se aplica a atributos de nome definidos de forma privada, bem como aos definidos nas Palavras-chave de esquema de impressão.

8.  Os filhos do mesmo tipo de elemento podem não aninhar a uma profundidade de mais de 10 elementos. Essa regra se aplica independentemente a cada tipo de elemento que pode ser definido.

Observe que o conteúdo XML do documento Funcionalidades de Impressão DEVE ser codificado usando UTF-8 ou UTF-16.

Observe que o conjunto de instâncias Feature, Option e ParameterDef relatadas não deve ser alterado, independentemente do instantâneo. As instâncias ScoredProperty que comporem cada instância option e o Valor atribuído a cada elemento ScoredProperty também não devem mudar. O mesmo se mantém verdadeiro para as instâncias de Propriedade que comem cada instância parameterDef.

Para obter uma lista de instâncias de propriedade adicionais que devem ser fornecidas para definir totalmente constructos e parâmetros de Recurso/Opção, consulte [ParameterDef](parameterdef.md) e [ParameterInit](parameterinit.md). Por exemplo, cada Recurso deve especificar seu comportamento de interface do usuário, especificamente se exatamente uma ou várias instâncias option podem ser selecionadas para cada Recurso de uma vez. O documento Palavras-chave de esquema de impressão define essas instâncias de Propriedade, em que elas devem aparecer no documento PrintCapabilities e quais instâncias value definidas nas Palavras-chave de esquema de impressão estão disponíveis.

O provedor PrintCapabilities é responsável por emitir o Valor apropriado para todas as instâncias de Propriedade dependentes de configuração. Por exemplo, se a taxa de impressão depender do modo de cor e da resolução usada, o provedor PrintCapabilities deverá observar as configurações de modo de cor e resolução especificadas no PrintTicket fornecido pelo cliente e deverá relatar o valor adequado para a taxa de impressão. Observe que cada instância ScoredProperty deve ter valor único; sua instância de Valor não pode ser alterável quando a configuração do dispositivo é mudada.

Observe também que as instâncias de Propriedade definidas nas Palavras-chave de Esquema de Impressão devem aparecer no local especificado. Eles não podem aparecer em locais arbitrários dentro de um documento PrintCapabilities. Instâncias de Propriedade definidas de forma privada podem aparecer em qualquer lugar, mesmo como subpropriedades dentro de instâncias de Propriedade definidas pelo esquema.

Observe que um conflito funcional entre as configurações é definido como dois elementos de Esquema de Impressão não conflitantes que têm uma função semelhante, mas são recursos diferentes. Um exemplo seria JobDuplexAllDocumentsContiguously e DocumentDuplex; ambos representam a função duplex do dispositivo, mas diferem na aplicação da função, uma aplicando-se a todo o trabalho de forma contígua e outra aos documentos. Caso dois elementos desse tipo sejam especificados, a precedência é determinada pelo produtor PrintCapabilities e pelo consumidor PrintTicket. É responsabilidade do produtor PrintCapabilities indicar corretamente as restrições entre elementos conflitantes por meio do atributo "restrito". Elementos no Esquema de Impressão público que exibem esse conflito semântico são identificados em sua definição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



