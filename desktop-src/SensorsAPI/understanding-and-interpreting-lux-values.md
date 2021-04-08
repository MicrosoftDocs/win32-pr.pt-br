---
description: O tipo de dados principal do sensor para sensores de luz ambiente é illuminance em Lux (lumens por metro quadrado). Os princípios descritos neste tópico se baseiam na obtenção de valores de Lux como entrada e na reação a esses dados em um programa.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Compreendendo e interpretando valores de Lux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011358"
---
# <a name="understanding-and-interpreting-lux-values"></a>Compreendendo e interpretando valores de Lux

O tipo de dados principal do sensor para sensores de luz ambiente é illuminance em Lux (lumens por metro quadrado). Os princípios descritos neste tópico se baseiam na obtenção de valores de Lux como entrada e na reação a esses dados em um programa.

As leituras de Lux são diretamente proporcionais à energia por medidor quadrado absorvido por segundo. A percepção humana dos níveis de luz não é tão simples. A percepção humana da luz é complicada porque nossos olhos estão constantemente ajustando e outros processos biológicos estão afetando nossa percepção. No entanto, podemos imaginar essa percepção de uma perspectiva simplificada criando vários intervalos de interesse com limites superiores e inferiores conhecidos.

O conjunto de dados de exemplo a seguir representa limites aproximados para condições de iluminação comuns e a etapa de iluminação correspondente. Aqui, cada etapa de iluminação representa uma alteração no ambiente de iluminação.

> [!Note]  
> Esse conjunto de dados é para ilustração e pode não ser completamente preciso para todos os usuários ou situações.

 



| Condição de iluminação | De (Lux) | Para (Lux) | Valor médio (Lux) | Etapa de iluminação |
|--------------------|------------|----------|------------------|---------------|
| Preto-Tom        | 0          | 10       | 5                | 1             |
| Muito escuro          | 11         | 50       | 30               | 2             |
| Inportais escuras       | 51         | 200      | 125              | 3             |
| Dim inportations        | 201        | 400      | 300              | 4             |
| Inportações normais     | 401        | 1000     | 700              | 5             |
| Inportações brilhantes     | 1001       | 5.000     | 3000             | 6             |
| Dim livre       | 5001       | 10.000   | 7500             | 7             |
| Em nuvem em casa    | 10.001     | 30,000   | 20.000           | 8             |
| Luz solar direta    | 30.001     | 100.000  | 65.000           | 9             |



 

Se visualizarmos esses dados usando os valores médios desta tabela, veremos que a relação Lux-to-Light-Step não é linear, como mostrado no grafo a seguir.

![grafo illuminance linear](images/luxtostep.png)

No entanto, se exibirmos esses dados usando uma escala logarítmica no eixo x, podemos ver que uma relação aproximadamente linear surge.

![grafo illuminance logarítmica](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Um exemplo de transformação

Com base no conjunto de dados de exemplo para sensores de luz ambiente fornecidos anteriormente, você pode chegar à equação a seguir para mapear valores de Lux para a percepção humana. Neste exemplo, os valores esperados variam de 0 Lux a 1 milhão Lux.

![equação de valor de Lux](images/sensor-lux-equation.jpg)

Esta equação resulta em valores que variam de maneira ligeiramente linear entre 0,0 e 1,0. Esse resultado indica como a iluminação percebida pelo homem foi alterada com base no conjunto de dados de exemplo mostrado anteriormente.

 

 



