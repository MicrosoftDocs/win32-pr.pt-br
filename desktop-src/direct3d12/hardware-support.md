---
title: Camadas de hardware
description: Os níveis de hardware da camada 1 para a camada 3 têm recursos crescentes disponíveis para o pipeline.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548206"
---
# <a name="hardware-tiers"></a>Camadas de hardware

Os níveis de hardware da camada 1 para a camada 3 têm recursos crescentes disponíveis para o pipeline.

-   [Limites dependentes de hardware](#limits-dependant-on-hardware)
-   [Limites de invariável](#invariable-limits)
-   [Tópicos relacionados](#related-topics)

## <a name="limits-dependant-on-hardware"></a>Limites dependentes de hardware



| Recursos disponíveis para o pipeline                                                                                                              | Camada 1                                                                   | Camada 2        | Nível 3        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| Níveis de recursos                                                                                                                                   | 11.0 +                                                                    | 11.0 +         | 11.1 +         |
| Número máximo de descritores em uma CBV (exibição de buffer constante), Modo de Exibição de Recursos de sombreador (SRV) ou heap de exibição de acesso não ordenado (UAV) usado para renderização | 1\.000.000                                                                | 1\.000.000     | 1000000 +    |
| Número máximo de exibições de buffer de constantes em todas as tabelas de descritores por estágio do sombreador                                                                | 14                                                                       | 14            | **heap completo** |
| Número máximo de exibições de recurso de sombreador em todas as tabelas de descritores por estágio de sombrea                                                                | 128                                                                      | **heap completo** | heap completo     |
| Número máximo de exibições de acesso não ordenado em todas as tabelas de descritores em todos os estágios                                                              | 64 para os níveis de recurso 11.1 +<br/> 8 para nível de recurso 11<br/> | 64            | **heap completo** |
| Número máximo de amostras em todas as tabelas de descritores por estágio do sombreador                                                                             | 16                                                                       | **2048** | 2.048     |



 

As entradas em **negrito** realçam melhorias significativas na camada anterior.

Há uma restrição adicional para o hardware de camada 1 que se aplica a todos os heaps e para o hardware de camada 2 que se aplica a heaps CBV e UAV, que todas as entradas de heap de descritor cobertas por tabelas de descritores na assinatura raiz *devem* ser preenchidas com descritores quando o sombreador for executado, mesmo se o sombreador (talvez devido à ramificação) não Não há nenhuma restrição para o hardware da camada 3. Uma mitigação para essa restrição é o uso cuidadoso de [descritores nulos](descriptors.md).

## <a name="invariable-limits"></a>Limites de invariável

O número máximo de amostras em um heap de descritor visível do sombreador é 2048.

O número máximo de amostras estáticas exclusivas entre assinaturas raiz dinâmicas é 2032 (que deixa 16 para drivers que precisam de seus próprios exemplos).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> <dt>

[Níveis de recursos de hardware](hardware-feature-levels.md)
</dt> </dl>

 

 





