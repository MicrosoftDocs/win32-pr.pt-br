---
description: Alfa também pode ser fornecido em um material. Para habilitar o material alfa, defina o estado de renderização do material difuso para que o tempo de execução use os componentes de cores difusas do material em vez dos componentes de cores difusas do vértice.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Material alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a70ed4a3f5bcaf38f4ace079af5b2e1804af0e24340e5004898c9ed26707d40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798973"
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

 

 



