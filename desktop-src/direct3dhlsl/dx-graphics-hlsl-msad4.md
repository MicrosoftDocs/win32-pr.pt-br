---
title: msad4
description: Compara um valor de referência de 4 byte e um valor de origem de 8 byte e acumula um vetor de 4 somas. Cada soma corresponde à soma mascarada de diferenças absolutas de um alinhamento de byte diferente entre o valor de referência e o valor de origem.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- msad4 HLSL
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be09292cad1181c9bac84a4ecb5346b01b0a58c73e2e545d7386658ac54a1f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120110"
---
# <a name="msad4"></a>msad4

Compara um valor de referência de 4 byte e um valor de origem de 8 byte e acumula um vetor de 4 somas. Cada soma corresponde à soma mascarada de diferenças absolutas de um alinhamento de byte diferente entre o valor de referência e o valor de origem.



| uint4 result = msad4(uint reference, uint2 source, uint4 accum); |
|------------------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="reference"></span><span id="REFERENCE"></span>*Referência*
</dt> <dd>

\[em \] A matriz de referência de 4 bytes em um valor **uint.**

</dd> <dt>

<span id="source"></span><span id="SOURCE"></span>*Fonte*
</dt> <dd>

\[em \] A matriz de origem de 8 bytes em dois valores **uint2.**

</dd> <dt>

<span id="accum"></span><span id="ACCUM"></span>*accum*
</dt> <dd>

\[em \] Um vetor de 4 valores. **msad4** adiciona esse vetor à soma mascarada de diferenças absolutas dos diferentes alinhamentos de byte entre o valor de referência e o valor de origem.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Um vetor de 4 somas. Cada soma corresponde à soma mascarada de diferenças absolutas de alinhamentos de byte diferentes entre o valor de referência e o valor de origem. **msad4** não incluirá uma diferença na soma se essa diferença for mascarada (ou seja, o byte de referência é 0).

## <a name="remarks"></a>Comentários

Para usar o intrínseco **msad4** no código do sombreador, chame o método [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para verificar se o dispositivo Direct3D dá suporte à opção de recurso [**SAD4ShaderInstructions.**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) O intrínseco **msad4** requer um driver de exibição WDDM 1.2 e todos os drivers de exibição do WDDM 1.2 devem dar suporte a **msad4**. Se seu aplicativo criar um dispositivo de renderização com o nível [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) recurso 11.0 ou 11.1 e o destino da compilação for o modelo de sombreador 5 ou posterior, o código-fonte HLSL poderá usar o intrínseco **msad4.**

Os valores de retorno são precisos apenas até 65535. Se você chamar o intrínseco **msad4** com entradas que podem resultar em valores de retorno maiores que 65535, **msad4** produzirá resultados indefinido.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                | Com suporte |
|-------------------------------------------------------------|-----------|
| [Modelo de sombreador 5 ou posterior](d3d11-graphics-reference-sm5.md) | sim       |



 

## <a name="examples"></a>Exemplos

Aqui está um exemplo de cálculo de resultado **para msad4:**


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



Aqui está um exemplo de como você pode usar **msad4** para pesquisar um padrão de referência dentro de um buffer:


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>           |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

