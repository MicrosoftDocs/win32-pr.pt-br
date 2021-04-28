---
description: Estrutura D3DCOLORVALUE (Dxgitype. h) – representa um valor de cor com Alfa, que é usado para transparência.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: Estrutura D3DCOLORVALUE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 83ca500493a04f04de5352185c240d20a19009f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107144"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a>Estrutura D3DCOLORVALUE (Dxgitype. h)

Representa um valor de cor com Alfa, que é usado para transparência.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
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

O tipo de cabeçalho DXGItype. h – define [**dxgi \_ RGBA**](dxgi-rgba.md) como um alias de **D3DCOLORVALUE**, da seguinte maneira:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Você pode usar D3DCOLORVALUE ou [**dxgi \_ RGBA**](dxgi-rgba.md) com o [**\_ \_ modo alfa**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode) [**IDXGISwapChain1:: setBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: getBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e dxgi.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Estruturas DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**\_RGBA dxgi**](dxgi-rgba.md)
</dt> </dl>

 

 




