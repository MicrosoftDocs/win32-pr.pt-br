---
description: Para entender totalmente um sombreador que implementa o PRT, é útil derivar a fórmula usada pelo sombreador para calcular Exit radiante.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Equações de PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087705"
---
# <a name="prt-equations-direct3d-9"></a>Equações de PRT (Direct3D 9)

Para entender totalmente um sombreador que implementa o PRT, é útil derivar a fórmula usada pelo sombreador para calcular Exit radiante.

Para começar, a equação a seguir é a equação geral para calcular o radiante de saída resultante da iluminação direta em um objeto difuso com iluminação distante arbitrária.

![equação da radiante de saída resultante da iluminação direta em um objeto difuso com iluminação distante arbitrária](images/prt-theory-eq1.png)

em que:



| Parâmetro     | Descrição                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| RP            | O radiante de saída no vértice p. Avaliado em cada vértice na malha.                                   |
| p<sub>d</sub> | O albedo da superfície.                                                                              |
| pi            | Uma constante, usada como um fator de normalização de conservação de energia.                                        |
| L (s)          | O ambiente de iluminação (radiante de origem).                                                             |
| VP de ₍ s ₎         | Uma função de visibilidade binária para o ponto p. Será 1 se o ponto puder ver a luz, 0 se não for.             |
| HNP ₍ s ₎        | O termo do cosseno da lei do Lambert. Igual a Max ((NP · s), 0), em que NP é a superfície normal no ponto p. |
| s             | A variável que se integra à esfera.                                                           |



 

Usando funções de base esféricas, como harmônicas esféricas, a equação a seguir aproxima o ambiente de iluminação.

![equação do ambiente de iluminação](images/prt-theory-eq2.png)

em que:



| Parâmetro        | Descrição                                              |
|------------------|----------------------------------------------------------|
| L (s)             | O ambiente de iluminação (radiante de origem).              |
| i                | Um inteiro que soma o número de funções de base. |
| O                | A ordem das harmônicas esféricas.                        |
| l<sub>i</sub>    | Um coeficiente.                                           |
| Y<sub>i (s)</sub> | Uma função base sobre a esfera.                     |



 

A coleção desses coeficientes, L ', fornece a aproximação ideal para a função L (s) com as funções de base Y (s). A substituição e a distribuição produz a equação a seguir.

![equação do radiante de saída depois de substituir l (s) e distribuir](images/prt-theory-eq3.png)

O integral de Y<sub>i (s)</sub>VP de ₍ s ₎ HNP ₍ s ₎ é um coeficiente de transferência t<sub>PI</sub> que o simulador computa para cada vértice na malha. Substituir isso produz a equação a seguir.

![equação do radiante de saída depois de substituir o coeficiente de transferência](images/prt-theory-eq4.png)

A alteração dessa notação de vetor produz a seguinte equação descompactada para calcular a saída radiante para cada canal.

![equação da radiante de saída após alterar para notação de vetor](images/prt-theory-eq5.png)

em que:



| Parâmetro     | Descrição                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RP            | O radiante de saída no vértice p.                                                                                                                                                      |
| p<sub>d</sub> | O albedo da superfície.                                                                                                                                                          |
| Debug            | O vetor de l<sub>i</sub>e é a projeção do radiante de origem nas funções de base harmônicas esféricas. Este é um vetor do pedido ² de coeficientes de harmônica esférica. |
| TP            | Um vetor de transferência do pedido ² para o vértice p. O simulador divide os coeficientes de transferência por p.                                                                                       |



 

Esses dois vetores são um vetor de pedido ² de coeficientes de harmônica esférica, portanto, observe que esse é simplesmente um produto de ponto. Dependendo da ordem, o ponto pode ser caro, portanto, a compactação pode ser usada. Um algoritmo chamado análise de componente principal clusterizado (CPCA) compacta os dados com eficiência. Isso permite o uso de uma aproximação harmônica esférica de ordem superior, que resulta em sombras mais nítidas.

O CPCA fornece a equação a seguir para aproximar o vetor de transferência.

![equação do vetor de transferência aproximado](images/prt-theory-eq6.png)

em que:



| Parâmetro      | Descrição                                          |
|----------------|------------------------------------------------------|
| TP             | O vetor de transferência para o vértice p.                    |
| MK             | A média do cluster k.                              |
| j              | Um inteiro que soma o número de vetores do PCA. |
| N              | O número de vetores do PCA.                           |
| w<sub>PJ</sub> | O peso do PCA jth para o ponto p.                      |
| B<sub>KJ</sub> | O vetor de base do PCA do jth para o cluster k.              |



 

Um cluster é simplesmente um número de vértices que compartilham o mesmo vetor médio. Como obter a média do cluster, os pesos do PCA, os vetores de base do PCA e as IDs de cluster para os vértices são discutidos abaixo.

A substituição dessas duas equações gera:

![equação do radiante de saída depois de substituir o vetor de transferência](images/prt-theory-eq7.png)

Em seguida, a distribuição do produto dot produz a equação a seguir.

![equação do radiante de saída após a distribuição do produto dot](images/prt-theory-eq8.png)

Porque ambos (MK · L ') e (B<sub>KJ</sub>· L ') são constantes por vértice, o exemplo calcula esses valores com a CPU e os passa como constantes para o sombreador de vértice; como w<sub>PJ</sub> muda para cada vértice, o exemplo armazena esses dados por vértice no buffer de vértice.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de radiante preputada](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



