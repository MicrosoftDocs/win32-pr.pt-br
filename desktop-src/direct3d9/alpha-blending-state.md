---
description: O valor alfa de uma cor controla sua transparência. Habilitar a mesclagem alfa permite que cores, materiais e texturas em uma superfície sejam mescladas com transparência em outra superfície.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Estado de mistura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370452"
---
# <a name="alpha-blending-state-direct3d-9"></a>Estado de mistura alfa (Direct3D 9)

O valor alfa de uma cor controla sua transparência. Habilitar a mesclagem alfa permite que cores, materiais e texturas em uma superfície sejam mescladas com transparência em outra superfície.

Para obter mais informações, consulte [mesclagem de textura alfa (Direct3D 9)](alpha-texture-blending.md) e [mesclagem de textura (Direct3D 9)](texture-blending.md).

Os aplicativos escritos em C++ usam o estado de renderização [**D3DRS \_ ALPHABLENDENABLE**](./d3drenderstatetype.md) para habilitar a mesclagem de transparência alfa. A API do Direct3D permite muitos tipos de mistura alfa. No entanto, é importante observar que o hardware 3D do usuário pode não dar suporte a todos os Estados de mesclagem permitidos pelo Direct3D.

O tipo de mistura alfa que é feito depende dos Estados de renderização [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) e **D3DRS \_ DESTBLEND** . Os Estados de mesclagem de origem e destino são usados em pares. O exemplo de código a seguir demonstra como o estado de mesclagem de origem é definido como D3DBLEND \_ SRCCOLOR e o estado de mesclagem de destino é definido como D3DBLEND \_ INVSRCCOLOR.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



Alterar os Estados de mesclagem de origem e destino pode dar a aparência dos objetos emissiva em uma atmosfera de Foggy ou poeira. Por exemplo, se seu aplicativo modela chamas, força campos, emissões de plasma ou objetos de radiante da mesma forma em um ambiente Foggy, defina os Estados de mesclagem de origem e destino como D3DBLEND \_ um.

Outra aplicação da mistura alfa é controlar a iluminação em uma cena 3D, também chamada de mapeamento leve. Definir o estado de mesclagem de origem como D3DBLEND \_ zero e o estado de mesclagem de destino como D3DBLEND \_ SRCALPHA escurece uma cena de acordo com as informações de alfa de origem. O primitivo de origem é usado como um mapa claro que dimensiona o conteúdo do buffer de quadro para escurecer quando apropriado. Isso produz o mapeamento de luz monocromática.

Você pode obter o mapeamento de luz de cor definindo o estado de mesclagem alfa de origem como D3DBLEND \_ zero e o estado de mesclagem de destino como D3DBLEND \_ SRCCOLOR.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 
