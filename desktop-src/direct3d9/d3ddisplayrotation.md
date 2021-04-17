---
description: Especifica como o monitor que está sendo usado para exibir um aplicativo de tela inteira é girado.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: Enumeração D3DDISPLAYROTATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 28f4d38dca78f0f34daf931a6bf651b40c1b0a78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811491"
---
# <a name="d3ddisplayrotation-enumeration"></a>Enumeração D3DDISPLAYROTATION

Especifica como o monitor que está sendo usado para exibir um aplicativo de tela inteira é girado.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**\_Identidade D3DDISPLAYROTATION**
</dt> <dd>

A exibição não está girada.

</dd> <dt>

<span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**
</dt> <dd>

A exibição é girada em 90 graus.

</dd> <dt>

<span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**
</dt> <dd>

A exibição é girada em 180 graus.

</dd> <dt>

<span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**
</dt> <dd>

A exibição é girada em 270 graus.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada em [**IDirect3D9Ex:: GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex:: GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)e [**IDirect3DSwapChain9Ex:: GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).

Os aplicativos podem optar por tratar a rotação do monitor usando o [D3DPRESENTFLAG \_ NOAUTOROTATE](d3dpresentflag.md), nesse caso, o aplicativo precisará saber como o monitor é girado para que possa ajustar sua renderização de acordo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




