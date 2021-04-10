---
description: Depois de ajustar a intensidade de luz para efeitos de atenuação, o mecanismo de iluminação calcula quanto da luz restante reflete de um vértice, dado o ângulo da normal do vértice e a direção da luz incidente.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Iluminação difusa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087224"
---
# <a name="diffuse-lighting-direct3d-9"></a>Iluminação difusa (Direct3D 9)

Depois de ajustar a intensidade de luz para efeitos de atenuação, o mecanismo de iluminação calcula quanto da luz restante reflete de um vértice, dado o ângulo da normal do vértice e a direção da luz incidente. O mecanismo de iluminação ignora essa etapa para luzes direcionais, porque elas não são atenuadas com a distância. O sistema considera dois tipos de reflexão, difusa e especular, e usa uma fórmula diferente para determinar a quantidade de luz que é refletida para cada um. Depois que calcular os valores de luz refletida, o Direct3D aplica esses novos valores às propriedades de reflexão difusa e especular do material atual. Os valores de cor resultantes são os componentes difusos e especulares que o rasterizador usa para produzir o sombreamento Gouraud e o realce especular.

A iluminação difusa é descrita pela seguinte equação.

Iluminação difusa = soma \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* Atten \* Spot\]



| Parâmetro       | Valor padrão | Tipo          | Description                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | N/D           | N/D           | Referência de cada componente difuso da luz.                                                                  |
| C<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | Cor difusa.                                                                                                |
| L<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | Cor difusa clara.                                                                                          |
| N               | N/D           | D3DVECTOR     | Normal de vértice                                                                                                 |
| F<sub>dir</sub> | N/D           | D3DVECTOR     | Vetor de direção do vértice de objeto à luz.                                                             |
| Atten           | N/D           | FLOAT         | Atenuação de luz. Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| À Vista            | N/D           | FLOAT         | Fator de destaque. Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).  |



 

O valor de C<sub>d</sub> é:

-   Vertex color1, If DIFFUSEMATERIALSOURCE = D3DMCS \_ color1 e a primeira cor de vértice é fornecida na declaração de vértice.
-   Vertex color2, If DIFFUSEMATERIALSOURCE = D3DMCS \_ color2, e a segunda cor de vértice é fornecida na declaração de vértice.
-   cor difusa do material

> [!Note]  
> Se a opção DIFFUSEMATERIALSOURCE for usada e a cor do vértice não for fornecida, a cor difusa do material será usada.

 

Para calcular a atenuação (Atten) ou as características de destaque (spot), veja [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).

Componentes difusos são vinculados para estar entre 0 e 255, depois que todas as luzes são processadas e interpoladas separadamente. O valor de iluminação difusa resultante é uma combinação dos valores de luz ambiente, difusa e emissiva.

## <a name="example"></a>Exemplo

Neste exemplo, o objeto é colorido usando a cor difusa clara e uma cor difusa de material. O código é mostrado abaixo.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



De acordo com a equação, a cor resultante para os vértices do objeto é uma combinação da cor do material e da cor da luz.

As duas ilustrações a seguir mostram a cor de material, que é cinza, e a cor de luz, que é vermelho brilhante.

![ilustração de uma esfera cinza](images/amb1.jpg)![ilustração de uma esfera vermelha](images/lightred.jpg)

A cena resultante é mostrada na ilustração a seguir. O único objeto na cena é uma esfera. O cálculo de iluminação difusa considera a cor difusa da luz e do material e a modifica pelo ângulo entre a direção da luz e a normal do vértice usando o produto de ponto. Como resultado, o verso da esfera obtém fica escuro à medida que a superfície das curvas da esfera se afasta da luz.

![ilustração de uma esfera com iluminação difusa](images/lightd.jpg)

Combinar a iluminação difusa com a iluminação ambiente dos exemplos anteriores sobreará toda a superfície do objeto. A luz ambiente sombreia toda a superfície e a luz difusa ajuda a revelar a forma do objeto 3D, conforme mostrado na ilustração a seguir.

![Ilustração de uma esfera com iluminação difusa e iluminação ambiente](images/lightad.jpg)

A iluminação difusa é mais intensa para se calcular do que a iluminação ambiente. Como ela depende das normais de vértice e da direção da luz, você pode ver a geometria de objetos no espaço 3D, o que produz uma iluminação mais realística do que a iluminação ambiente. Você pode usar realces especulares para obter uma aparência mais realista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Matemática de iluminação](mathematics-of-lighting.md)
</dt> </dl>

 

 



