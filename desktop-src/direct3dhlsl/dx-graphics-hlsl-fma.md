---
title: FMA (Corecrt \_ Math. h)
description: Retorna a adição de multiplicação cruzada de precisão dupla de a \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- FMA HLSL
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
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369591"
---
# <a name="fma"></a>fma

Retorna a adição de multiplicação de precisão dupla de um \* b + c.



| *RET* FMA (duplo *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="a"></span><span id="A"></span>*um*
</dt> <dd>

\[no \] primeiro valor da adição de multiplicação com fusível.

</dd> <dt>

<span id="b"></span><span id="B"></span>*b*
</dt> <dd>

\[no \] segundo valor da adição de multiplicação com fusível.

</dd> <dt>

<span id="c"></span><span id="C"></span>*&*
</dt> <dd>

\[no \] terceiro valor da adição de multiplicação com fusível.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

A adição de precisão dupla combinada de parâmetros *a* \* *b*  +  *c*. O valor retornado deve ser preciso para 0,5 unidades de menos precisão (ULP).

## <a name="remarks"></a>Comentários

O **FMA** intrínseco deve dar suporte a Nans, INFs e normas.

Para usar o **FMA** intrínseco em seu código de sombreador, chame o método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com [**\_ \_ \_ as opções D3D11 Feature D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para verificar se o dispositivo Direct3D dá suporte à opção de recurso [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . O **FMA** intrínseco requer um driver de vídeo WDDM 1,2 e todos os drivers de exibição do WDDM 1,2 devem oferecer suporte a **FMA**. Se seu aplicativo cria um dispositivo de renderização com [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 ou 11,1 e o destino de compilação é o modelo de sombreador 5 ou posterior, o código-fonte HLSL pode usar o **FMA** intrínseco.

### <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *um*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**Clique**](/windows/desktop/WinProg/windows-data-types)                       | any                          |
| *b*   | igual à entrada *a*                                                                                              | [**Clique**](/windows/desktop/WinProg/windows-data-types)                       | mesmas dimensões como entrada *a* |
| *c*   | igual à entrada *a*                                                                                              | [**Clique**](/windows/desktop/WinProg/windows-data-types)                       | mesmas dimensões como entrada *a* |
| *RET* | igual à entrada *a*                                                                                              | [**Clique**](/windows/desktop/WinProg/windows-data-types)                       | mesmas dimensões como entrada *a* |



 

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                | Com suporte |
|-------------------------------------------------------------|-----------|
| [Modelo do sombreador 5 ou posterior](d3d11-graphics-reference-sm5.md) | sim       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

