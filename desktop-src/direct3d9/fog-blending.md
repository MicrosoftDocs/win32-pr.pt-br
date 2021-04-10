---
description: A fusão de neblina refere-se à aplicação do fator de neblina às cores de neblina e objeto para produzir a cor final que aparece em uma cena, conforme discutido em fórmulas de neblina (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Fusão de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087216"
---
# <a name="fog-blending-direct3d-9"></a>Fusão de neblina (Direct3D 9)

A fusão de neblina refere-se à aplicação do fator de neblina às cores de neblina e objeto para produzir a cor final que aparece em uma cena, conforme discutido em [fórmulas de neblina (Direct3D 9)](fog-formulas.md). A combinação de D3DRS \_ FOGENABLE renderizar controles de estado de neblina. Defina esse estado de renderização como **true** para habilitar a mesclagem de neblina, conforme mostrado no código de exemplo a seguir. O padrão é **false**.


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



Você deve habilitar a mesclagem de neblina para sombra de pixel e sombra de vértice. Para obter informações sobre como usar esses tipos de neblina, consulte [sombra de pixel (Direct3D 9)](pixel-fog.md) e [neblina de vértice (Direct3D 9)](vertex-fog.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de neblina](fog-types.md)
</dt> </dl>

 

 



