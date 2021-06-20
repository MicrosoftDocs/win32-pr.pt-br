---
title: Dependência de configuração printCapabilities
description: As dependências de configuração referem-se ao fato de que alguns elementos podem ser alterados ou até mesmo excluídos de um documento PrintCapabilities para o próximo.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20f01c8e7bd9a036a53048996ec5a38246471f67
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409659"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Dependência de configuração no esquema PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O esquema PrintCapabilities é paralelo à Estrutura de Esquema de Impressão, em termos dos elementos usados e da estrutura geral expressa pelos elementos pai e filho. As dependências de configuração, que pertencem especificamente ao PrintCapabilities, são listadas aqui como uma extensão para a estrutura geral. As dependências de configuração referem-se ao fato de que alguns elementos, incluindo seu conteúdo, podem ser alterados ou até mesmo excluídos de um documento PrintCapabilities para o próximo, como resultado de dependências na configuração. Mesmo se um elemento pai precisar ser independente da configuração, seus elementos filho poderão ter dependências. Essas dependências são expressas usando \* constructos \* Switch/Case em arquivos GPD.

Como exemplo de uma dependência de configuração, considere os valores associados a cada Propriedade no documento PrintCapabilities. Cada documento PrintCapabilities pode ser diferente nas instâncias de Propriedade definidas e nas instâncias de Valor atribuídas a essas instâncias de Propriedade.



| Tipo de elemento                                                                                                                                                                             | Dependência de configuração                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recurso <br/> Opção<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Propriedade<br/> Scoredproperty<br/> | Esses elementos não devem ter dependências de configuração.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | Elementos e elementos ParameterDef contidos neles em qualquer nível de aninhamento não devem ter nenhuma dependência de configuração.<br/>                                                                                        |
| Propriedade <br/>                                                                                                                                                                     | Os elementos de propriedade podem ter dependências de configuração, exceto quando aparecem dentro dos elementos ParameterDef.<br/>                                                                                                       |
| Valor <br/>                                                                                                                                                                        | Os elementos de valor que aparecem em elementos ScoredProperty não devem ter nenhuma dependência de configuração. Os elementos de valor que aparecem dentro de um elemento Property podem ter dependências arbitrárias na configuração.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




