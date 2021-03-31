---
description: Alfa também pode ser fornecido em um material. Para habilitar o material alfa, defina o estado de renderização do material difuso para que o tempo de execução use os componentes de cores difusas do material em vez dos componentes de cores difusas do vértice.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Material alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087212"
---
# <a name="material-alpha-direct3d-9"></a>Material alfa (Direct3D 9)

Alfa também pode ser fornecido em um material. Para habilitar o material alfa, defina o estado de renderização do material difuso para que o tempo de execução use os componentes de cores difusas do material em vez dos componentes de cores difusas do vértice.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



Inicialize o material com um valor alfa e defina o material antes do desenho.


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem alfa](alpha-blending.md)
</dt> </dl>

 

 



