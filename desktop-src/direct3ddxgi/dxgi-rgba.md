---
description: Representa um valor de cor com Alfa, que é usado para transparência.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: Estrutura de DXGI_RGBA (DXGItype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645966"
---
# <a name="dxgi_rgba-structure"></a>\_Estrutura RGBA dxgi

Representa um valor de cor com Alfa, que é usado para transparência.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a>Membros

<dl> <dt>

**r**
</dt> <dd>

Valor de ponto flutuante que especifica o componente vermelho de uma cor. Esse valor geralmente está no intervalo de 0,0 a 1,0. Um valor de 0,0 indica a ausência completa do componente vermelho, enquanto um valor de 1,0 indica que o vermelho está totalmente presente.

</dd> <dt>

**m**
</dt> <dd>

Valor de ponto flutuante que especifica o componente verde de uma cor. Esse valor geralmente está no intervalo de 0,0 a 1,0. Um valor de 0,0 indica a ausência completa do componente verde, enquanto um valor de 1,0 indica que o verde está totalmente presente.

</dd> <dt>

**b**
</dt> <dd>

Valor de ponto flutuante que especifica o componente azul de uma cor. Esse valor geralmente está no intervalo de 0,0 a 1,0. Um valor de 0,0 indica a ausência completa do componente azul, enquanto um valor de 1,0 indica que o azul está totalmente presente.

</dd> <dt>

**um**
</dt> <dd>

Valor de ponto flutuante que especifica o componente alfa de uma cor. Esse valor geralmente está no intervalo de 0,0 a 1,0. Um valor de 0,0 indica totalmente transparente, enquanto um valor de 1,0 indica totalmente opaco.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode definir os membros dessa estrutura com valores fora do intervalo de 0 a 1 para implementar alguns efeitos incomuns. Valores maiores que 1 produzem luzes fortes que tendem a desbotar uma cena. Valores negativos produzem luzes escuras que realmente removem a luz de uma cena.

O tipo de cabeçalho DXGItype. h – define **dxgi \_ RGBA** como um alias de [**D3DCOLORVALUE**](d3dcolorvalue.md), da seguinte maneira:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Você pode usar **dxgi \_ RGBA** com o [**\_ \_ modo alfa**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode) [**IDXGISwapChain1:: setBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e dxgi.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 e atualização de plataforma para \[ aplicativos UWP de aplicativos de área de trabalho do Windows 7 \|\]<br/>                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 e atualização de plataforma para \[ aplicativos de aplicativos UWP do Windows server 2008 R2 desktop \|\]<br/> |
| parâmetro<br/>                   | <dl> <dt>DXGItype. h</dt> </dl>                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**D3DCOLORVALUE (no Direct3D 9)**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
