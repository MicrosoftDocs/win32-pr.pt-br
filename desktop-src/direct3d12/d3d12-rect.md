---
title: D3D12_RECT (D3D12. h)
description: D3D12 \_ RECT é declarado como um RECT.
ms.assetid: 39511ACE-7AC5-42A2-896D-7E0977A346C6
keywords:
- D3D12_RECT
topic_type:
- apiref
api_name:
- D3D12_RECT
api_location:
- D3D12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d408832e800413f94e251ee27a57e5b326378c36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788921"
---
# <a name="d3d12_rect"></a>D3D12 \_ Rect

D3D12 \_ RECT é declarado como um RECT. Para obter mais informações sobre essa estrutura de retângulo GDI, consulte [**Rect**](/previous-versions//dd162897(v=vs.85)).

``` syntax
typedef RECT D3D12_RECT;
```

## <a name="remarks"></a>Comentários

Essa estrutura é usada pelos seguintes métodos:

-   [**RSSetScissorRects**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)

Essa estrutura é um membro da estrutura [**de \_ \_ região de descarte de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas principais](direct3d-12-structures.md)
</dt> <dt>

[**CD3DX12 \_ Rect**](cd3dx12-rect.md)
</dt> </dl>

 

