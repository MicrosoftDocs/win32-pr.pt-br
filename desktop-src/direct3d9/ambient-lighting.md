---
description: A iluminação ambiente fornece iluminação constante para uma cena.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Iluminação de ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500997"
---
# <a name="ambient-lighting-direct3d-9"></a>Iluminação de ambiente (Direct3D 9)

A iluminação ambiente fornece iluminação constante para uma cena. Ele destaca todos os vértices de objeto da mesma forma porque ela não depende de quaisquer outros fatores de iluminação como normais de vértice, direção da luz, posição da luz, intervalo ou atenuação. É o tipo mais rápido de iluminação, mas produz os resultados menos realistas. O Direct3D contém uma única propriedade de luz ambiente global que você pode usar sem criar qualquer luz. Como alternativa, você pode configurar qualquer objeto de luz para fornecer iluminação ambiente. A iluminação ambiente para uma cena é descrita pela seguinte equação.

Iluminação de ambiente = C ₐ \* \[ g ₐ + Sum (Atten<sub>eu</sub> \* ponto<sub>i</sub> \* L<sub>ia</sub>)\]

Em que:



| Parâmetro         | Valor padrão | Tipo          | Descrição                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| Cₐ                | (0,0,0,0)     | D3DCOLORVALUE | Cor ambiente do material                                                                                                         |
| Gₐ                | (0,0,0,0)     | D3DCOLORVALUE | Cor ambiente global                                                                                                           |
| Atten<sub>i</sub> | (0,0,0,0)     | D3DCOLORVALUE | Atenuação de luz da luz ith. Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Ponto<sub>i</sub>  | (0,0,0,0)     | D3DVECTOR     | Fator de destaque da luz ith. Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).  |
| Sum               | N/D           | N/D           | Soma da luz ambiente                                                                                                       |
| L<sub>ia</sub>    | (0,0,0,0)     | D3DVECTOR     | Cor ambiente da luz da luz ith                                                                                           |



 

O valor de Cₐ é:

-   Vertex color1, If AMBIENTMATERIALSOURCE = D3DMCS \_ color1 e a primeira cor de vértice é fornecida na declaração de vértice.
-   Vertex color2, If AMBIENTMATERIALSOURCE = D3DMCS \_ color2, e a segunda cor de vértice é fornecida na declaração de vértice.
-   cor ambiente do material.

> [!Note]  
> Se a opção AMBIENTMATERIALSOURCE for usada e a cor do vértice não for fornecida, a cor do ambiente de material será usada.

 

Para usar a cor ambiente do material, use SetMaterial, conforme mostrado no exemplo de código abaixo.

Gₐ é a cor ambiente global. Ele é definido usando setrenderingstate (D3DRS \_ ambiente). Há uma cor ambiente global em uma cena do Direct3D. Este parâmetro não está associado um objeto de luz do Direct3D.

L<sub>ai</sub> é a cor ambiente da luz ith na cena. Cada luz do Direct3D tem um conjunto de propriedades, uma delas é a cor ambiente. O termo, sum(L<sub>ai</sub>) é a soma de todas as cores ambiente na cena.

## <a name="example"></a>Exemplo

Neste exemplo, o objeto é colorido usando a luz ambiente da cena e uma cor ambiente de material.


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



De acordo com a equação, a cor resultante para os vértices do objeto é uma combinação da cor do material e da cor da luz.

As duas ilustrações a seguir mostram a cor de material, que é cinza, e a cor de luz, que é vermelho brilhante.

![ilustração de uma esfera cinza](images/amb1.jpg)![ilustração de uma esfera vermelha](images/lightred.jpg)

A cena resultante é mostrada na ilustração a seguir. O único objeto na cena é uma esfera. A luz ambiente destaca todos os vértices do objeto com a mesma cor. Não é dependente da normal de vértice ou da direção da luz. Como resultado, o círculo se parece com um círculo 2D porque não há nenhuma diferença na sombreamento ao redor a superfície do objeto.

![ilustração de uma esfera com iluminação](images/lighta.jpg)

Para dar uma aparência mais realista aos objetos, aplique iluminação especular ou difusa além de iluminação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Matemática de iluminação](mathematics-of-lighting.md)
</dt> </dl>

 

 



