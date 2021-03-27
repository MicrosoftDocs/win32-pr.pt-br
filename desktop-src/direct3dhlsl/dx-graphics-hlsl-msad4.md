---
title: msad4
description: Compara um valor de referência de 4 bytes e um valor de origem de 8 bytes e acumula um vetor de quatro somas. Cada soma corresponde à soma mascarada de diferenças absolutas de um alinhamento de byte diferente entre o valor de referência e o valor de origem.
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
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104967254"
---
# <a name="msad4"></a>msad4

Compara um valor de referência de 4 bytes e um valor de origem de 8 bytes e acumula um vetor de quatro somas. Cada soma corresponde à soma mascarada de diferenças absolutas de um alinhamento de byte diferente entre o valor de referência e o valor de origem.



| uint4 Result = msad4 (referência uint, fonte uint2, uint4 Accum); |
|------------------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="reference"></span><span id="REFERENCE"></span>*referência*
</dt> <dd>

\[na \] matriz de referência de 4 bytes em um valor **uint** .

</dd> <dt>

<span id="source"></span><span id="SOURCE"></span>*original*
</dt> <dd>

\[na \] matriz de origem de 8 bytes em dois valores de **uint2** .

</dd> <dt>

<span id="accum"></span><span id="ACCUM"></span>*Accum*
</dt> <dd>

\[em \] um vetor de quatro valores. **msad4** adiciona esse vetor à soma mascarada de diferenças absolutas dos diferentes alinhamentos de byte entre o valor de referência e o valor de origem.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Um vetor de quatro somas. Cada soma corresponde à soma mascarada de diferenças absolutas de diferentes alinhamentos de bytes entre o valor de referência e o valor de origem. **msad4** não inclui uma diferença na soma se essa diferença for mascarada (ou seja, o byte de referência é 0).

## <a name="remarks"></a>Comentários

Para usar o **msad4** intrínseco no código do sombreador, chame o método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com [**\_ \_ \_ as opções D3D11 Feature D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para verificar se o dispositivo Direct3D dá suporte à opção de recurso [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . O **msad4** intrínseco requer um driver de vídeo WDDM 1,2 e todos os drivers de exibição do WDDM 1,2 devem dar suporte a **msad4**. Se seu aplicativo cria um dispositivo de renderização com [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 ou 11,1 e o destino de compilação é o modelo de sombreador 5 ou posterior, o código-fonte HLSL pode usar o intrínseco **msad4** .

Os valores de retorno só são precisos até 65535. Se você chamar o **msad4** intrínseco com entradas que podem resultar em valores de retorno maiores que 65535, **msad4** produzirá resultados indefinidos.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                | Com suporte |
|-------------------------------------------------------------|-----------|
| [Modelo do sombreador 5 ou posterior](d3d11-graphics-reference-sm5.md) | sim       |



 

## <a name="examples"></a>Exemplos

Aqui está um exemplo de cálculo de resultado para **msad4**:


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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>           |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

