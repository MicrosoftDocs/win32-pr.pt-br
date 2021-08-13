---
description: Saiba como PrintTicket e PrintCapabilities lidam com opções parametrizadas e não parametrizadas.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Opções parametrizadas versus opções não parametrizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb51d2d1df6ed49e389aff9aa614fabb2ace9d462cccbb3d56438f84b363fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731954"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Opções parametrizadas versus opções não parametrizadas

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Os provedores de PrintCapabilities e PrintTicket devem lidar corretamente com instâncias de opção parametrizadas durante o processo de validação PrintTicket. Conforme discutido nas [definições de opção](option-definitions.md), uma etapa executada na validação do PrintTicket é encontrar a opção no documento de PrintCapabilities do dispositivo atual (a opção de candidato) que melhor corresponda à opção especificada no PrintTicket (a opção de referência). Quando uma ou ambas as instâncias de opção são parametrizadas, há três casos possíveis que devem ser tratados pelo processo de Pontuação definido pelo driver de dispositivo: o caso em que ambas as instâncias de opção são parametrizadas e os dois casos em que uma opção é parametrizada e a outra não é. Nos casos a seguir, supõe-se que haja uma correspondência entre as instâncias de ScoredProperty parametrizadas na opção PrintTicket e um ScoredProperty específico na opção PrintCapabilities. Se não houver nenhuma correspondência, o processo de Pontuação poderá tratar essas instâncias de ScoredProperty da mesma maneira que trata de quaisquer outras instâncias de ScoredProperty não correspondentes.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Caso 1-opções de documento PrintTicket e PrintCapabilities com parâmetros

Nesse caso, a opção de referência (no PrintTicket) e a opção de candidato (no documento PrintCapabilities) são parametrizadas. Acesse a instância ParameterDef que é referenciada pela opção candidato (no documento PrintCapabilities) e determine se o valor de ParameterInit especificado no PrintTicket cai no intervalo permitido pela instância ParameterDef. Nesse caso, considere esse ScoredProperty como uma correspondência. Caso contrário, esse ScoredProperty não será uma correspondência.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Caso 2-opção PrintTicket com parâmetros, opção de documento PrintCapabilities não parametrizado

Nesse caso, o PrintTicket contém um recurso com uma opção com parâmetros, enquanto o recurso correspondente no documento PrintCapabilities contém pelo menos uma opção que não é parametrizada. Mesmo que o documento PrintCapabilities também contenha outras instâncias de opção parametrizadas, o processo de Pontuação deve ser aplicado a cada opção, porque o objetivo é identificar a melhor opção de correspondência. O cliente deve ser capaz de comparar os candidatos à opção não parametrizada com uma opção de referência com parâmetros.

Como a opção com parâmetros aparece no PrintTicket, as instâncias de ParameterInit também devem estar presentes conforme ilustrado no caso anterior. O processo de Pontuação pode simplesmente substituir qualquer instância de ParameterRef na opção parametrizada do PrintTicket pelo valor especificado pela instância ParameterInit do PrintTicket. Isso efetivamente converte uma opção parametrizada em uma que não é parametrizada. Neste ponto, o processo de correspondência convencional pode ser usado.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Caso 3-opção PrintTicket não parametrizada, opção de documento de PrintCapabilities com parâmetros

Nesse caso, a opção de referência no PrintTicket não é parametrizada, enquanto a opção candidata no documento PrintCapabilities é parametrizada. Acesse a instância ParameterDef no documento PrintCapabilities que é referenciado pela instância ParameterRef da opção candidata no PrintTicket e determine se o valor definido na opção de referência para o ScoredProperty correspondente se encontra no intervalo permitido pela instância ParameterDef. Nesse caso, considere esse ScoredProperty como uma correspondência. Caso contrário, esse ScoredProperty não é uma correspondência.

Deve-se enfatizar que você faz a determinação de quão próximas duas instâncias de opção correspondem pelo número (e significância) das instâncias de ScoredProperty que correspondem, independentemente de as instâncias de ScoredProperty contiverem instâncias de valor explícitas ou instâncias de ParameterRef. É possível que uma opção de candidato seja a melhor correspondência, embora contenha várias instâncias de propriedade que não correspondam àquelas da opção de referência ou que não tenham nenhuma propriedade correspondente na opção de referência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



