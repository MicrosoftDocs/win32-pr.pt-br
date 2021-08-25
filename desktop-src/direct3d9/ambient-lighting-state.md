---
description: A luz ambiente está ao redor da luz que radia de todas as direções. Para obter informações sobre como o Direct3D usa a luz ambiente, consulte Matemática da Iluminação (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Estado de iluminação ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc32a6ec654bd30627c853bc00c90e94b6008e769fb3aa708e963a9430e0dc85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952686"
---
# <a name="ambient-lighting-state-direct3d-9"></a>Estado de iluminação ambiente (Direct3D 9)

A luz ambiente está ao redor da luz que radia de todas as direções. Para obter informações sobre como o Direct3D usa a luz ambiente, consulte Matemática da Iluminação [(Direct3D 9)](mathematics-of-lighting.md).

Um aplicativo C++ define a cor da iluminação do ambiente invocando o método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e passando o valor enumerado D3DRS AMBIENT como o primeiro \_ parâmetro. O segundo parâmetro é um valor de cor. O valor padrão é zero.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizar estados](render-states.md)
</dt> </dl>

 

 
