---
description: Examine a lista de verificação de validação do PrintTicket. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Lista de verificação de validação do PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6154b7cabb5825a0f0edcc8f90b8294557001f1a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120141"
---
# <a name="printticket-validation-checklist"></a>Lista de verificação de validação do PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Os provedores PrintTicket devem validar o PrintTicket antes de usá-lo para qualquer finalidade. Depois que o PrintTicket é validado, ele pode ser retornado ao cliente ou pode ser descartado após o uso. Esta lista de verificação aborda as tarefas que o provedor deve executar durante a validação. O processo de validação frequentemente alterará o conteúdo do PrintTicket, embora ele não altere um PrintTicket validado anteriormente.

A validação é sempre executada em um dispositivo específico que tem um conjunto de instâncias Feature, Option e ParameterDef definidas em um documento de PrintCapabilities. O código de validação deve ter acesso ao conjunto de instâncias de recurso (e as instâncias de opção contidas) e instâncias de ParameterDef para o dispositivo específico e não deve ter acesso às PrintCapabilities. As informações das instâncias Feature, Option e ParameterDef são necessárias em determinadas partes do processo de validação.

1.  Durante tentativas de localizar elementos correspondentes ou correspondentes, observe que os namespaces dos elementos devem corresponder antes que qualquer nome qualificado possa ser considerado uma correspondência. Todos os nomes de elementos, nomes de atributo e nomes de instância são qualificados por namespace. Para elementos aninhados, seus locais devem corresponder antes que os elementos sejam considerados uma correspondência.

2.  Verifique se todas as marcas de elemento estão no namespace público, são definidas pelo esquema PrintTicket, contêm os atributos XML adequados e os valores de atributo e se o local de cada tipo de elemento está de acordo com o uso definido pelo esquema PrintTicket.

3.  Determine todos os namespaces relatados pelo documento PrintCapabilities. Remova todos os elementos (e seus descendentes) do PrintTicket cujos nomes de instância pertençam a namespaces não relatados pelo documento PrintCapabilities. Observe a diferença entre esse caso e o seguinte caso, que envolve nomes de instância não reconhecidos em um namespace conhecido.

4.  Devido ao fato de que os esquemas estão sendo continuamente estendidos com a adição de novas definições de instância de elemento, o código de validação não deve ser escrito sob a hipótese de que cada nome de instância em um determinado namespace é conhecido. O código de validação não pode tratar nomes de instância não reconhecidos em um namespace conhecido como erros, nem excluí-los do PrintTicket.

5.  Se qualquer instância de elemento tiver um irmão duplicado que não é permitido pelo esquema PrintTicket, mantenha apenas a primeira ocorrência e exclua as duplicatas, incluindo o conteúdo do elemento duplicado.

6.  Remova do PrintTicket qualquer recurso ou subrecurso (e todos os seus filhos) que não tenha nenhum recurso correspondente no documento de PrintCapabilities.

7.  Verifique a Propriedade SelectionType definida no documento PrintCapabilities para cada uma das instâncias de recurso restantes no PrintTicket. Qualquer recurso cuja Propriedade SelectionType esteja definida como PickOne deve ter exatamente uma instância de opção presente no PrintTicket, enquanto um recurso cuja Propriedade SelectionType é PickMany pode ter mais de um. Se um recurso PrintTicket não tiver nenhuma instância de opção, forneça a instância de opção padrão. Como você é o provedor, sabe qual opção é a opção padrão para cada recurso.

    Para um recurso cuja Propriedade SelectionType seja PickMany, com mais de uma opção selecionada no PrintTicket, verifique se nenhuma opção está designada como IdentityOption. Se houver, exclua todas as outras opções, deixando apenas a IdentityOption designada.

8.  Remova qualquer instância de ParameterInit no PrintTicket que não tenha nenhuma instância ParameterDef correspondente no documento PrintCapabilities.

    Para quaisquer outras instâncias de ParameterInit no PrintTicket, verifique se o valor de cada está em conformidade com a instância ParameterDef do documento PrintCapabilities. Se um valor estiver ausente, forneça o padrão fornecido no ParameterDef.

9.  Emparelhe cada instância de opção no PrintTicket com uma opção listada no recurso correspondente no documento PrintCapabilities, com base nos resultados do processo de pontuação. A pontuação é o processo de encontrar a opção no documento PrintCapabilities que melhor corresponde à opção nomeada no PrintTicket. Para obter uma descrição do que é levado em conta durante o processo de pontuação, consulte [definições de opção](option-definitions.md). Substitua cada opção de referência no PrintTicket pela opção de documento de recursos de PrintCapabilities do candidato de melhor correspondência correspondente. Você também pode classificar todos os candidatos por Pontuação e passar essas informações para o estágio de resolução no caso de um conflito de restrição impedir que o candidato a melhor correspondência seja usado. Nesses casos, o processo de resolução pode usar o segundo candidato mais indicado em vez de escolher outro candidato aleatoriamente.

10. Para um recurso cuja Propriedade SelectionType esteja definida como PickMany e que tenha mais de uma opção selecionada no PrintTicket, verifique se nenhuma opção está designada como IdentityOption. Se essa opção existir, exclua todas as outras opções, deixando apenas a IdentityOption designada. Esta etapa deve ser executada antes e depois que o processo de pontuação for aplicado.

    O motivo pelo qual essa etapa deve ser executada duas vezes é que é possível que o processo de Pontuação mapeie várias instâncias de opção de referência para a mesma opção candidata. Se isso acontecer, exclua todas as instâncias de opção duplicadas para que as opções listadas para um determinado recurso PickMany sejam exclusivas.

11. Adicione ao PrintTicket qualquer recurso presente no documento PrintCapabilities que não aparece no PrintTicket. Para esse recurso, designe a opção padrão como a opção selecionada.

12. Determine se há alguma instância ParameterDef que atenda a todos os seguintes critérios:

    -   A instância ParameterDef aparece no documento PrintCapabilities, mas não no PrintTicket.

    -   A propriedade obrigatória da instância ParameterDef é definida como incondicional ou condicional.

    -   A instância de ParameterDef é referenciada por uma instância de ParameterRef no PrintTicket dentro de uma instância de opção.

    Para cada instância de ParameterDef no documento PrintCapabilities, adicione ao PrintTicket uma instância ParameterInit correspondente. Defina o valor das instâncias ParameterInit adicionadas recentemente ao valor padrão especificado pelas instâncias de ParameterDef correspondentes.

13. Execute a detecção de conflito de restrição e modifique a configuração para eliminar esses conflitos. Este tópico não define um processo específico a ser usado para resolver conflitos de restrição. Você precisa decidir qual instância de recurso ou ParameterInit pode ser alterada, e uma opção ou valor apropriado, respectivamente, para selecionar que tenha o impacto mínimo sobre a intenção geral da configuração especificada no PrintTicket. Conforme mencionado anteriormente, talvez você queira fazer uso da Pontuação de mapeamento de cada opção e usar a opção com a segunda pontuação mais alta. Para determinar qual recurso ou ParameterInit alterar, talvez você queira definir uma propriedade privada que o cliente pode adicionar ao PrintTicket. Essa propriedade pode definir uma prioridade para instâncias de recurso e ParameterInit para que o processo do resolvedor seja informado sobre quais instâncias de recurso ou ParameterInit são importantes para o cliente (e precisam ser preservadas no PrintTicket) e que são menos importantes.

14. Se o processo de resolução de restrição tiver causado alterações no PrintTicket em todas as instâncias de ParameterRef para as quais a propriedade obrigatória está definida como condicional, adicione instâncias ParameterInit com valores padrão para aqueles que agora aparecem e remova qualquer instância de ParameterInit para uma instância ParameterRef que não é mais exibida.

15. Remova todas as instâncias de propriedade e seus conteúdos que aparecem nas instâncias de opção no PrintTicket. Os elementos de propriedade não têm nenhuma função no PrintTicket. Se a opção validada para um recurso específico corresponder perfeitamente à opção pré-validada, transfira todas as instâncias de propriedade nessa opção do PrintTicket de prevalidação para o PrintTicket validado agora, sujeito à condição em que os namespaces das instâncias de propriedade são registrados no documento PrintCapabilities. Observe que, para que duas instâncias de opção sejam consideradas uma correspondência perfeita, para cada ScoredProperty encontrada em uma opção, deve haver um ScoredProperty correspondente na outra opção, e os valores de ambas as instâncias de ScoredProperty devem ser iguais.

16. Se o seu provedor PrintTicket reconhecer e oferecer suporte a qualquer instância de propriedade privada ou pública que tenha sobreviveram a esse ponto, execute a validação nelas. Não exclua uma propriedade neste ponto apenas porque você não a reconhece, ela pode ser destinada a outra fase de processamento de documentos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



