---
description: Os componentes de iluminação especular e difusa da equação de iluminação global contêm termos que descrevem a atenuação de luz e o cone em destaque. Esses termos são descritos a seguir.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Atenuação e fator de destaque (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80fff287749e2979a89f2e20c830fdad3961d90ec05bf90a4ee2f6a51f8bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850607"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Atenuação e fator de destaque (Direct3D 9)

Os componentes de iluminação especular e difusa da equação de iluminação global contêm termos que descrevem a atenuação de luz e o cone em destaque. Esses termos são descritos a seguir.

## <a name="attenuation"></a>Atenuação

A atenuação de uma luz depende do tipo de luz e da distância entre a luz e a posição do vértice. Para calcular a atenuação, use uma das seguintes equações.

Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* dAtend)

Em que:



| Parâmetro        | Valor padrão | Tipo  | DESCRIÇÃO                                     | Intervalo          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0,0           | FLOAT | Fator de atenuação constante                     | 0 para + infinito |
| att1<sub>i</sub> | 0,0           | FLOAT | Fator de atenuação linear                       | 0 para + infinito |
| att2<sub>i</sub> | 0,0           | FLOAT | Fator de atenuação quadrática                    | 0 para + infinito |
| d                | N/D           | FLOAT | Distância da posição de vértice até a posição da luz | N/D            |



 

-   Atten = 1, se a luz é uma luz direcional.
-   Atten = 0, se a distância entre a luz e o vértice exceder o intervalo da luz.

Os valores att0, att1, att2 são especificados pelos membros Attenuation0, Attenuation1 e Attenuation2 [**de D3DLIGHT9.**](d3dlight9.md)

A distância entre a luz e a posição do vértice é sempre positiva.

d = \| L<sub>dir</sub>\|

Em que:



| Parâmetro       | Valor padrão | Tipo      | Descrição                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dir</sub> | N/D           | D3DVECTOR | Vetor de direção da posição de vértice para a posição da luz |



 

Se d for maior que o intervalo da luz, ou seja, o membro Range de uma estrutura [**D3DLIGHT9,**](d3dlight9.md) o Direct3D não fará mais cálculos de atenuação e não aplicará nenhum efeito da luz ao vértice.

As constantes de atenuação atuam como coeficientes na fórmula - você poderá produzir uma variedade de curvas de atenuação fazendo ajustes simples nelas. Você pode definir Attenuation1 como 1.0 para criar uma luz sem atenuação, mas que ainda é limitada por intervalo, ou você pode fazer experiências com valores diferentes para obter vários efeitos de atenuação.

A atenuação no intervalo máximo da luz não é 0.0. Para impedir que luzes apareçam repentinamente quando estiverem no intervalo de luz, um app pode aumentar o intervalo de luz. Ou então, o app pode configurar constantes de atenuação para que o fator de atenuação fique próximo de 0.0 no intervalo de luz. O valor de atenuação é multiplicado pelos componentes em vermelho, verde e azul de cor da luz para dimensionar a intensidade da luz, à medida que um fator de luz de distância transita para um vértice.

## <a name="spotlight-factor"></a>Fator de destaque

A seguinte equação especifica o fator de destaque.

![equação de fator de destaque](images/dx8light9.png)



| Parâmetro         | Valor padrão | Tipo  | DESCRIÇÃO                              | Intervalo                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| <sub>oi</sub>   | N/D           | FLOAT | cosseno(ângulo) para destaque i            | N/D                      |
| phi<sub>i</sub>   | 0,0           | FLOAT | Ângulo de penumbra de destaque i em radianos | \[theta<sub>i</sub>, pi) |
| theta<sub>i</sub> | 0,0           | FLOAT | Ângulo de penumbra de destaque i em radianos    | \[0, pi)                 |
| queda           | 0,0           | FLOAT | Fator de queda                           | (-infinito + infinito)   |



 

Em que:

rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)

e:



| Parâmetro       | Valor padrão | Tipo      | Descrição                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dcs</sub> | N/D           | D3DVECTOR | O negativo da direção da luz no espaço da câmera         |
| L<sub>dir</sub> | N/D           | D3DVECTOR | Vetor de direção da posição de vértice para a posição da luz |



 

Depois de computar a atenuação de luz, o Direct3D também considera os efeitos de destaque, se aplicável, o ângulo que a luz reflete de uma superfície e a reflexão do material atual para calcular os componentes difuso e especular para esse vértice. Para obter mais informações, consulte [Spotlight](light-types.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Matemática de iluminação](mathematics-of-lighting.md)
</dt> </dl>

 

 



