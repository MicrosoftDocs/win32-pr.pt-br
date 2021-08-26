---
description: O tipo de dados do sensor primário para sensores de luz ambiente é a iluminância em todo o ambiente (lumens por medidor quadrado). Os princípios descritos neste tópico baseiam-se na tomada de valores deverão ser considerados como entrada e reagir a esses dados em um programa.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Noções básicas e interpretando valores DeIa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05b4bc9c3efa73f91d54a9c88231180ec2807964b753e175bc13755b54c2743
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126517"
---
# <a name="understanding-and-interpreting-lux-values"></a>Noções básicas e interpretando valores DeIa

O tipo de dados do sensor primário para sensores de luz ambiente é a iluminância em todo o ambiente (lumens por medidor quadrado). Os princípios descritos neste tópico baseiam-se na tomada de valores deverão ser considerados como entrada e reagir a esses dados em um programa.

As leituras de São diretamente proporcionais à energia por medidor quadrado que é absorto por segundo. A percepção humana dos níveis de luz não é tão simples. A percepção humana da luz é complicada porque nossos olhos estão constantemente se ajustando e outros processos de câncer estão afetando nossa percepção. No entanto, podemos pensar nessa percepção de uma perspectiva simplificada criando vários intervalos de interesse com limites superiores e inferiores conhecidos.

O conjunto de dados de exemplo a seguir representa limites aproximados para condições comuns de iluminação e a etapa de iluminação correspondente. Aqui, cada etapa de iluminação representa uma alteração no ambiente de iluminação.

> [!Note]  
> Esse conjunto de dados é para ilustração e pode não ser completamente preciso para todos os usuários ou situações.

 



| Condição de iluminação | De (sempre) | Para (também) | Valor médio (sempre) | Etapa de iluminação |
|--------------------|------------|----------|------------------|---------------|
| Escuro        | 0          | 10       | 5                | 1             |
| Muito escuro          | 11         | 50       | 30               | 2             |
| Dark Indoors       | 51         | 200      | 125              | 3             |
| Esmaecimento interno        | 201        | 400      | 300              | 4             |
| Ambientes internos normais     | 401        | 1000     | 700              | 5             |
| Bright Indoors     | 1001       | 5.000     | 3000             | 6             |
| Esmaecimento ao ar livre       | 5001       | 10.000   | 7500             | 7             |
| Cloudy Outdoors    | 10,001     | 30,000   | 20.000           | 8             |
| Direct S seção    | 30,001     | 100.000  | 65,000           | 9             |



 

Se visualizarmos esses dados usando os valores médios desta tabela, veremos que a relação de passo a iluminação não é linear, como mostra o grafo a seguir.

![grafo de illuminância linear](images/luxtostep.png)

No entanto, se exibirmos esses dados usando uma escala logarítmica no eixo x, podemos ver que surge uma relação aproximadamente linear.

![grafo de illuminância logarítmica](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Uma transformação de exemplo

Com base no conjunto de dados de exemplo para sensores de luz ambiente fornecidos anteriormente, você pode chegar à equação a seguir para mapear os valores de pessoas para a percepção humana. Neste exemplo, os valores esperados variam de 0 ao 1.000.000.

![equação de valor de colocada](images/sensor-lux-equation.jpg)

Essa equação resulta em valores que variam de forma aproximadamente linear entre 0,0 e 1,0. Esse resultado indica como a iluminação percebida por humanos foi alterada com base no conjunto de dados de exemplo mostrado anteriormente.

 

 



