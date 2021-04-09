---
description: A luz ambiente está voltada para a luz que radia de todas as direções. Para obter informações sobre como o Direct3D usa a luz ambiente, consulte matemática de iluminação (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Estado de iluminação ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bd604941961f5b4abdb301d5c23efba9980791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089414"
---
# <a name="ambient-lighting-state-direct3d-9"></a>Estado de iluminação ambiente (Direct3D 9)

A luz ambiente está voltada para a luz que radia de todas as direções. Para obter informações sobre como o Direct3D usa a luz ambiente, consulte [matemática de iluminação (Direct3D 9)](mathematics-of-lighting.md).

Um aplicativo C++ define a cor da iluminação de ambiente invocando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e passando o valor enumerado D3DRS \_ ambiente como o primeiro parâmetro. O segundo parâmetro é um valor de cor. O valor padrão é zero.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 
