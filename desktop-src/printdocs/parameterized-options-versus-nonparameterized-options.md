---
description: Saiba como PrintTicket e PrintCapabilities lidam com opções parametrizadas e não parametrizadas.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Opções parametrizadas versus opções não parametrizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c788eaf2fa08f4f29a541a775d2bcbf523aa51
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407219"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Opções parametrizadas versus opções não parametrizadas

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Os provedores PrintCapabilities e PrintTicket devem lidar corretamente com instâncias de Opção parametrizadas durante o processo de validação printTicket. Conforme discutido em Definições de Opção [,](option-definitions.md)uma etapa executada na validação printTicket é encontrar a Opção no documento PrintCapabilities do dispositivo atual (a opção candidata) que melhor corresponde à Opção especificada no PrintTicket (a opção de referência). Quando uma ou ambas as instâncias option são parametrizadas, há três casos possíveis que devem ser tratados pelo processo de pontuação definido pelo driver de dispositivo: o caso em que ambas as instâncias option são parametrizadas e os dois casos em que uma Opção é parametrizada e a outra não. Nos casos a seguir, supõe-se que haja uma correspondência entre as instâncias de ScoredProperty parametrizadas na Opção PrintTicket e uma ScoredProperty específica na Opção PrintCapabilities. Se não houver correspondência, o processo de pontuação poderá tratar essas instâncias ScoredProperty da mesma maneira que trata qualquer outra instância de ScoredProperty não correspondente.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Caso 1 – Opções de documento PrintTicket e PrintCapabilities parametrizadas

Nesse caso, a opção de referência (no PrintTicket) e a opção candidate (no documento PrintCapabilities) são parametrizadas. Acesse a instância ParameterDef referenciada pela Opção candidata (ambas no documento PrintCapabilities) e determine se o valor ParameterInit especificado no PrintTicket se enquadra no intervalo permitido pela instância parameterDef. Nesse caso, considere essa ScoredProperty como uma combinação. Caso contrário, ScoredProperty não será uma combinação.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Caso 2 – Opção PrintTicket parametrizada, Opção de documento PrintCapabilities não parametrizada

Nesse caso, o PrintTicket contém um Recurso com uma Opção parametrizada, enquanto o Recurso correspondente no documento PrintCapabilities contém pelo menos uma Opção que não está parametrizada. Mesmo que o documento PrintCapabilities também contenha outras instâncias option que são parametrizadas, o processo de pontuação deve ser aplicado a cada Opção, pois o objetivo é identificar a melhor opção correspondente. O cliente deve ser capaz de comparar candidatos de Opção não parametrizados com uma opção de referência que é parametrizada.

Como a Opção parametrizada aparece no PrintTicket, as instâncias parameterInit também devem estar presentes conforme ilustrado no caso anterior. O processo de pontuação pode simplesmente substituir qualquer instância ParameterRef na Opção parametrizada do PrintTicket pelo Valor especificado pela instância ParameterInit do PrintTicket. Isso efetivamente converte uma Opção parametrizada em uma que não está parametrizada. Neste ponto, o processo de correspondência convencional pode ser usado.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Caso 3 – Opção PrintTicket não parametrizada, Opção de documento PrintCapabilities com parâmetros

Nesse caso, a opção de referência no PrintTicket não é parametrizada, enquanto a Opção candidata no documento PrintCapabilities é parametrizada. Acesse a instância ParameterDef no documento PrintCapabilities referenciado pela instância ParameterRef da opção candidata no PrintTicket e determine se o Valor definido na Opção de referência para o ScoredProperty correspondente se enquadra no intervalo permitido pela instância ParameterDef. Nesse caso, considere essa ScoredProperty como uma combinação. Caso não seja, scoredProperty não é uma combinação.

É importante enfatizar que você faz a determinação de quão próximas duas instâncias option são a mesma que o número (e significância) das instâncias ScoredProperty que corresponderem, independentemente de as instâncias ScoredProperty conterem instâncias de Value explícitas ou instâncias ParameterRef. É possível que uma Opção candidata seja a melhor opção, mesmo que ela contenha várias instâncias de Propriedade que não correspondam às da opção de referência ou que não tenham nenhuma Propriedade correspondente na opção de referência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



