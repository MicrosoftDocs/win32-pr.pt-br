---
title: fma (Corecrt \_ math.h)
description: Retorna a adição multiplicada de precisão dupla de um \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- fma HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b9a6932a1b0f0f8f1f7bc674920162def49e556c8d5b757547d4837caa60b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120200"
---
# <a name="fma"></a>fma

Retorna a adição multiplicada de precisão dupla de b \* + c.



| *ret* fma(double *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="a"></span><span id="A"></span>*Um*
</dt> <dd>

\[em \] O primeiro valor na adição de multiplicação mesclada.

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[em \] O segundo valor na adição de multiplicação mesclada.

</dd> <dt>

<span id="c"></span><span id="C"></span>*C*
</dt> <dd>

\[em \] O terceiro valor na adição de multiplicação mesclada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

A adição multiplicada de precisão dupla dos parâmetros *a* \* *b*  +  *c*. O valor retornado deve ser preciso para 0,5 unidades de menor precisão (ULP).

## <a name="remarks"></a>Comentários

O **fma** intrínseco deve dar suporte a NaNs, INFs e Denorms.

Para usar o **fma** intrínseco no código do sombreador, chame o método [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para verificar se o dispositivo Direct3D dá suporte à opção de recurso [**ExtendedDoublesShaderInstructions.**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) O **fma** intrínseco requer um driver de exibição WDDM 1.2 e todos os drivers de exibição do WDDM 1.2 devem dar suporte **a fma**. Se seu aplicativo criar um dispositivo de renderização com o nível [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) recurso 11.0 ou 11.1 e o destino da compilação for o modelo de sombreador 5 ou posterior, o código-fonte HLSL poderá usar o **fma** intrínseco.

### <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *Um*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**Duplo**](/windows/desktop/WinProg/windows-data-types)                       | any                          |
| *b*   | mesmo que a *entrada de um*                                                                                              | [**Duplo**](/windows/desktop/WinProg/windows-data-types)                       | mesmas dimensões que uma *entrada* |
| *c*   | mesmo que a *entrada de um*                                                                                              | [**Duplo**](/windows/desktop/WinProg/windows-data-types)                       | mesmas dimensões que uma *entrada* |
| *Ret* | mesmo que a *entrada de um*                                                                                              | [**Duplo**](/windows/desktop/WinProg/windows-data-types)                       | mesmas dimensões que uma *entrada* |



 

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                | Com suporte |
|-------------------------------------------------------------|-----------|
| [Modelo de sombreador 5 ou posterior](d3d11-graphics-reference-sm5.md) | sim       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

