---
description: A reflexão de modelagem especular exige que o sistema não só saiba em que direção a luz está viajando, mas também a direção para o olho do visualizador.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Iluminação especular (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564926"
---
# <a name="specular-lighting-direct3d-9"></a>Iluminação especular (Direct3D 9)

A reflexão de modelagem especular exige que o sistema não só saiba em que direção a luz está viajando, mas também a direção para o olho do visualizador. O sistema usa uma versão simplificada do modelo de reflexo especular Phong, que utiliza um vetor de metade para aproximar a intensidade da reflexão especular.

O estado de iluminação padrão não calcula os realces especulares. Para habilitar a iluminação especular, certifique-se de definir D3DRS \_ SPECULARENABLE como **true**.

## <a name="specular-lighting-equation"></a>Equação de Iluminação Especular

A iluminação especular é descrita pela seguinte equação.



|                                                                             |
|-----------------------------------------------------------------------------|
| Iluminação especular = cs \* Sum \[ ls \* (N · H)<sup>P</sup> \* Atten \* especial\] |



 

A tabela a seguir identifica as variáveis, seus tipos e seus intervalos.



| Parâmetro    | Valor padrão | Tipo          | Descrição                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| Cₛ           | (0,0,0,0)     | D3DCOLORVALUE | Cor especular.                                                                                                     |
| Sum          | N/D           | N/D           | Referência do componente especular cada da luz.                                                                       |
| N            | N/D           | D3DVECTOR     | Normal de vértice.                                                                                                      |
| H            | N/D           | D3DVECTOR     | Vetor de metade. Consulte a seção sobre o vetor de metade.                                                             |
| <sup>P</sup> | 0.0           | FLOAT         | Potência de reflexão especular. Intervalo é 0 até + infinito                                                                  |
| Lₛ           | (0,0,0,0)     | D3DCOLORVALUE | Cor especular clara.                                                                                               |
| Atten        | N/D           | FLOAT         | Valor de atenuação clara. Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| À Vista         | N/D           | FLOAT         | Fator de destaque. Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).        |



 

O valor de Cₛ é:


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   vértice color1, se a origem do material especular for D3DMCS \_ color1 e a primeira cor de vértice for fornecida na declaração de vértice.
-   vértice color2, se a origem do material especular for D3DMCS \_ color2 e a segunda cor de vértice for fornecida na declaração de vértice.
-   cor especular do material

> [!Note]  
> Se a opção fonte de material especular for usada e a cor de vértice não for fornecida, a cor especular material será usada.

 

Componentes especulares são vinculados para estar entre 0 e 255, depois que todas as luzes são processadas e interpoladas separadamente.

## <a name="the-halfway-vector"></a>O vetor de metade

O vetor de metade (H) existe situado entre dois vetores: o vetor de um vértice de objeto para a fonte de luz e o vetor de um vértice de objeto para a posição da câmera. O Direct3D fornece duas maneiras de calcular o vetor de metade. Quando D3DRS \_ LOCALVIEWER é definido como **true**, o sistema calcula o vetor intermediário usando a posição da câmera e a posição do vértice, juntamente com o vetor de direção da luz. A fórmula a seguir mostra isso.



|                                           |
|-------------------------------------------|
| H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>) |



 



| Parâmetro       | Valor padrão | Tipo      | Descrição                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| Cₚ              | N/D           | D3DVECTOR | Posição da câmera.                                             |
| Vₚ              | N/D           | D3DVECTOR | Posição do vértice.                                             |
| F<sub>dir</sub> | N/D           | D3DVECTOR | Vetor de direção da posição de vértice para a posição da luz. |



 

Determinar o vetor de metade dessa maneira pode ser computacionalmente intensa. Como alternativa, a definição de D3DRS \_ LOCALVIEWER = **false** instrui o sistema a agir como se o ponto de vista estivesse infinitamente distante no eixo z. Isso se reflete na seguinte fórmula.



|                                     |
|-------------------------------------|
| H = norm((0,0,1) + L<sub>dir</sub>) |



 

Essa configuração é computacionalmente menos intensa, mas muito menos precisa, portanto, é melhor usada por aplicativos que usam a projeção ortogonal.

## <a name="example"></a>Exemplo

Neste exemplo, o objeto é colorido usando a cor da luz especular da cena e uma cor especular de material. O código é mostrado abaixo.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



De acordo com a equação, a cor resultante para os vértices do objeto é uma combinação da cor do material e da cor da luz.

A ilustração a seguir mostra a cor do material especular, que é cinza, e a cor da luz especular, que é branca.

![ilustração de uma esfera cinza](images/amb1.jpg)![ilustração de um círculo branco](images/lightwhite.jpg)

O destaque especular resultante é mostrado na ilustração a seguir.

![ilustração do realce especular](images/lights.jpg)

Combinar o realce especular com a iluminação ambiente e difusa produz a ilustração a seguir. Com todos os três tipos de iluminação aplicada, isso mais claramente se parece com um objeto realista.

![ilustração da combinação do realce especular, iluminação ambiente e iluminação difusa](images/lightads.jpg)

A iluminação especular é mais intensa para se calcular do que a iluminação difusa. Ela normalmente é usada para fornecer dicas visuais sobre o material da superfície. O realce especular varia em tamanho e cor com o material da superfície.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Matemática de iluminação](mathematics-of-lighting.md)
</dt> </dl>

 

 



