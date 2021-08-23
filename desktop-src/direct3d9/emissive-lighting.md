---
description: A iluminação emissive é descrita por um termo único.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Iluminação emissiva (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3200486118e6b44efc3be31f01b3a10e62c876d673c687619a4e6c8445f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802918"
---
# <a name="emissive-lighting-direct3d-9"></a>Iluminação emissiva (Direct3D 9)

A iluminação emissive é descrita por um termo único.

Iluminação emissiva = Cₑ

Em que:



| Parâmetro | Valor padrão | Tipo          | Descrição     |
|-----------|---------------|---------------|-----------------|
| Cₑ        | (0,0,0,0)     | D3DCOLORVALUE | Cor emissiva. |



 

O valor de C ₑ é:

-   Vertex color1, If EMISSIVEMATERIALSOURCE = D3DMCS \_ color1 e a primeira cor de vértice é fornecida na declaração de vértice.
-   Vertex color2, If EMISSIVEMATERIALSOURCE = D3DMCS \_ color2, e a segunda cor de vértice é fornecida na declaração de vértice.
-   cor do emissiva do material

> [!Note]  
> Se a opção EMISSIVEMATERIALSOURCE for usada e a cor do vértice não for fornecida, a cor do material emissiva será usada.

 

## <a name="example"></a>Exemplo

Neste exemplo, o objeto é colorido usando a luz ambiente da cena e uma cor ambiente de material. O código é mostrado abaixo.


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



De acordo com a equação, a cor resultante para os vértices de objeto é a cor do material.

A ilustração a seguir mostra a cor do material, que é verde. A luz emissiva destaca todos os vértices do objeto com a mesma cor. Não é dependente da normal de vértice ou da direção da luz. Como resultado, o círculo se parece com um círculo 2D porque não há nenhuma diferença na sombreamento ao redor a superfície do objeto.

![ilustração de uma esfera verde](images/lighte.jpg)

A ilustração a seguir mostra como o emissiva Light mistura com os outros três tipos de luzes, dos exemplos anteriores. No lado direito da esfera, há uma mistura de luz emissiva verde e luz ambiente vermelha. No lado esquerdo da esfera, a luz emissiva verde combina com a luz difusa e a luz ambiente vermelha, produzindo um gradiente vermelho. O realce especular é branco no centro e cria um anel de amarelo à medida que o valor da luz especular cai nitidamente deixando os valores de luz emissiva, difusa e ambiente se misturarem para formar o amarelo.

![ilustração de uma esfera verde com luz emissiva](images/lightadse.jpg)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Matemática de iluminação](mathematics-of-lighting.md)
</dt> </dl>

 

 



