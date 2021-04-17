---
description: Os componentes de iluminação especular e difusa da equação de iluminação global contêm termos que descrevem a atenuação de luz e o cone em destaque. Esses termos são descritos a seguir.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Fator de atenuação e destaque (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568937"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Fator de atenuação e destaque (Direct3D 9)

Os componentes de iluminação especular e difusa da equação de iluminação global contêm termos que descrevem a atenuação de luz e o cone em destaque. Esses termos são descritos a seguir.

## <a name="attenuation"></a>Atenuação

A atenuação de uma luz depende do tipo de luz e da distância entre a luz e a posição do vértice. Para calcular a atenuação, use uma das seguintes equações.

Atten = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + att2<sub>i</sub> \* d ²)

Em que:



| Parâmetro        | Valor padrão | Tipo  | DESCRIÇÃO                                     | Intervalo          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0.0           | FLOAT | Fator de atenuação constante                     | 0 para + infinito |
| att1<sub>i</sub> | 0.0           | FLOAT | Fator de atenuação linear                       | 0 para + infinito |
| att2<sub>i</sub> | 0.0           | FLOAT | Fator de atenuação quadrática                    | 0 para + infinito |
| d                | N/D           | FLOAT | Distância da posição de vértice até a posição da luz | N/D            |



 

-   Atten = 1, se a luz é uma luz direcional.
-   Atten = 0, se a distância entre a luz e o vértice exceder o intervalo da luz.

Os valores att0, Att1, att2 são especificados pelos membros Attenuation0, Attenuation1 e Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).

A distância entre a luz e a posição do vértice é sempre positiva.

d = \| f<sub>dir</sub>\|

Em que:



| Parâmetro       | Valor padrão | Tipo      | Descrição                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| F<sub>dir</sub> | N/D           | D3DVECTOR | Vetor de direção da posição de vértice para a posição da luz |



 

Se d for maior que o intervalo da luz, ou seja, o membro do intervalo de uma estrutura [**D3DLIGHT9**](d3dlight9.md) , o Direct3D não fará mais cálculos de atenuação e não aplicará nenhum efeito da luz ao vértice.

As constantes de atenuação atuam como coeficientes na fórmula - você poderá produzir uma variedade de curvas de atenuação fazendo ajustes simples nelas. Você pode definir Attenuation1 como 1.0 para criar uma luz sem atenuação, mas que ainda é limitada por intervalo, ou você pode fazer experiências com valores diferentes para obter vários efeitos de atenuação.

A atenuação no intervalo máximo da luz não é 0.0. Para impedir que luzes apareçam repentinamente quando estiverem no intervalo de luz, um app pode aumentar o intervalo de luz. Ou então, o app pode configurar constantes de atenuação para que o fator de atenuação fique próximo de 0.0 no intervalo de luz. O valor de atenuação é multiplicado pelos componentes em vermelho, verde e azul de cor da luz para dimensionar a intensidade da luz, à medida que um fator de luz de distância transita para um vértice.

## <a name="spotlight-factor"></a>Fator de destaque

A seguinte equação especifica o fator de destaque.

![equação de fator de destaque](images/dx8light9.png)



| Parâmetro         | Valor padrão | Tipo  | DESCRIÇÃO                              | Intervalo                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| Rô<sub>i</sub>   | N/D           | FLOAT | cosseno(ângulo) para destaque i            | N/D                      |
| phi<sub>i</sub>   | 0.0           | FLOAT | Ângulo de penumbra de destaque i em radianos | \[teta<sub>i</sub>, PI) |
| teta<sub>i</sub> | 0.0           | FLOAT | Ângulo de penumbra de destaque i em radianos    | \[0, PI)                 |
| queda           | 0.0           | FLOAT | Fator de queda                           | (-infinito + infinito)   |



 

Em que:

rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)

e:



| Parâmetro       | Valor padrão | Tipo      | Descrição                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <sub>DCS</sub> do L | N/D           | D3DVECTOR | O negativo da direção da luz no espaço da câmera         |
| F<sub>dir</sub> | N/D           | D3DVECTOR | Vetor de direção da posição de vértice para a posição da luz |



 

Depois de computar a atenuação de luz, o Direct3D também considera os efeitos de destaque, se aplicável, o ângulo que a luz reflete de uma superfície e a reflexão do material atual para calcular os componentes difuso e especular para esse vértice. Para obter mais informações, consulte [Spotlight](light-types.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Matemática de iluminação](mathematics-of-lighting.md)
</dt> </dl>

 

 



