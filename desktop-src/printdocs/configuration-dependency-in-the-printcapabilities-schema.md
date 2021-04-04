---
title: Dependência de configuração de PrintCapabilities
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7f376d8bd0dab823adb3a2e0665db27508b1d7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103837700"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Dependência de configuração no esquema de PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O esquema PrintCapabilities é bastante paralelo à estrutura de esquema de impressão, em termos dos elementos usados e da estrutura geral expressa pelos elementos pai e filho. As dependências de configuração, que pertencem especificamente aos recursos de PrintCapabilities, são listadas aqui como uma extensão para a estrutura geral. As dependências de configuração referem-se ao fato de que alguns elementos, incluindo seu conteúdo, podem ser alterados ou até mesmo excluídos de um documento de PrintCapabilities para o próximo, como resultado de dependências na configuração. Mesmo que um elemento pai seja necessário para ser independente da configuração, seus elementos filho podem ter dependências. Essas dependências são expressas usando \* construções switch/ \* case em arquivos GPD.

Como exemplo de uma dependência de configuração, considere os valores associados a cada propriedade no documento PrintCapabilities. Cada documento de PrintCapabilities pode diferir nas instâncias de propriedade definidas e nas instâncias de valor atribuídas a essas instâncias de propriedade.



| Tipo de elemento                                                                                                                                                                             | Dependência de configuração                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recurso <br/> Opção<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Propriedade<br/> ScoredProperty<br/> | Esses elementos não devem ter dependências de configuração.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | Elementos e elementos ParameterDef contidos neles em qualquer nível de aninhamento não devem ter nenhuma dependência de configuração.<br/>                                                                                        |
| Propriedade <br/>                                                                                                                                                                     | Elementos de propriedade podem ter dependências de configuração, exceto quando aparecem dentro de elementos ParameterDef.<br/>                                                                                                       |
| Valor <br/>                                                                                                                                                                        | Elementos de valor que aparecem em elementos ScoredProperty não devem ter nenhuma dependência de configuração. Elementos de valor que aparecem dentro de um elemento de propriedade podem ter dependências arbitrárias na configuração.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




