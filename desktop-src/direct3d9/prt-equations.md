---
description: Para entender totalmente um sombreador que implementa PRT, é útil derivar a fórmula que o sombreador usa para calcular o radiance de saída.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Equações prt (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd3dc716349ce46d4e678f0e408e5c964eb5f01d633649e3d512db6115c0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798122"
---
# <a name="prt-equations-direct3d-9"></a>Equações prt (Direct3D 9)

Para entender totalmente um sombreador que implementa PRT, é útil derivar a fórmula que o sombreador usa para calcular o radiance de saída.

Para começar, a equação a seguir é a equação geral para calcular o radiamento de saída resultante da iluminação direta em um objeto difuso com iluminação distante arbitrária.

![equação do radiamento de saída resultante da iluminação direta em um objeto difuso com iluminação distante arbitrária](images/prt-theory-eq1.png)

em que:



| Parâmetro     | Descrição                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| Rp            | O radiance de saída no vértice p. Avaliado em cada vértice na malha.                                   |
| p<sub>d</sub> | O albedo da superfície.                                                                              |
| pi            | Uma constante, usada como um fator de normalização de economia de energia.                                        |
| L(s)          | O ambiente de iluminação (radiação de origem).                                                             |
| Vp₍s₎         | Uma função de visibilidade binária para o ponto p. Será 1 se o ponto puder ver a luz, 0 se não.             |
| Hnp₍s₎        | O termo cosseno da lei de Lambert. Igual a max((Np· s), 0) em que Np é a superfície normal no ponto p. |
| s             | A variável que se integra sobre a esfera.                                                           |



 

Usando funções de base esféricas, como harmônicos esféricos, a equação a seguir aproxima o ambiente de iluminação.

![equação do ambiente de iluminação](images/prt-theory-eq2.png)

em que:



| Parâmetro        | Descrição                                              |
|------------------|----------------------------------------------------------|
| L(s)             | O ambiente de iluminação (radiação de origem).              |
| i                | Um inteiro que soma o número de funções de base. |
| O                | A ordem de harmônicos esféricos.                        |
| l<sub>i</sub>    | Um coeficiente.                                           |
| Y<sub>i(s)</sub> | Alguma função de base sobre a esfera.                     |



 

A coleção desses coeficientes, L', fornece a aproximação ideal para a função L(s) com as funções base Y(s). Substituir e distribuir gera a equação a seguir.

![equação do radiance de saída depois de substituir l(s) e distribuir](images/prt-theory-eq3.png)

A integral de Y<sub>i(s)</sub>Vp₍s₎Hnp₍s₎ é um coeficiente de transferência t<sub>pi</sub> que o simulador pré-comuta para cada vértice na malha. Substituir isso gera a equação a seguir.

![equação do radiance de saída depois de substituir o coeficiente de transferência](images/prt-theory-eq4.png)

Alterar isso para notação de vetor gera a seguinte equação descompactada para calcular o radiamento de saída para cada canal.

![equação do radiamento de saída depois de alterar para notação de vetor](images/prt-theory-eq5.png)

em que:



| Parâmetro     | Descrição                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rp            | O radiance de saída no vértice p.                                                                                                                                                      |
| p<sub>d</sub> | O albedo da superfície.                                                                                                                                                          |
| L'            | O vetor de l<sub>i</sub>e é a projeção do radiance de origem para as funções base esféricas. Esse é um vetor de ordem de coeficientes de coeficientes alfabéticos esféricos. |
| Tp            | Um vetor de transferência orderu para vértice p. O simulador divide os coeficientes de transferência por p.                                                                                       |



 

Esses dois vetores são um vetor de ordem de coeficientes de coeficientes alfabéticos esféricos, portanto, observe que este é simplesmente um produto de ponto. Dependendo da ordem, o ponto pode ser caro para que a compactação possa ser usada. Um algoritmo chamado CPCA (Análise de Componente Principal Clustered) compacta com eficiência os dados. Isso permite o uso de uma aproximação cônica esférica de ordem superior, o que resulta em sombras mais fortes.

A CPCA fornece a equação a seguir para aproximar o vetor de transferência.

![equação do vetor de transferência aproximado](images/prt-theory-eq6.png)

em que:



| Parâmetro      | Descrição                                          |
|----------------|------------------------------------------------------|
| Tp             | O vetor de transferência para vértice p.                    |
| Mk             | A média do cluster k.                              |
| j              | Um inteiro que soma o número de vetores PCA. |
| N              | O número de vetores PCA.                           |
| w<sub>pj</sub> | O peso da PCA jth para o ponto p.                      |
| B<sub>kj</sub> | O vetor base da PCA jth para o cluster k.              |



 

Um cluster é simplesmente um número de vértices que compartilham o mesmo vetor de média. Como obter a média do cluster, os pesos da PCA, os vetores base da PCA e as IDs do cluster para os vértices são discutidos abaixo.

A substituição dessas duas equações gera:

![equação do radiance de saída depois de substituir o vetor de transferência](images/prt-theory-eq7.png)

Em seguida, distribuir o produto de ponto produz a equação a seguir.

![equação do radiance de saída depois de distribuir o produto de ponto](images/prt-theory-eq8.png)

Porque ambos (Mk· L') e (B<sub>kj</sub>· L') são constantes por vértice, o exemplo calcula esses valores com a CPU e os passa como constantes para o sombreador de vértice; como w<sub>pj muda</sub> para cada vértice, o exemplo armazena esses dados por vértice no buffer de vértice.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de Radiance pré-comutada](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



