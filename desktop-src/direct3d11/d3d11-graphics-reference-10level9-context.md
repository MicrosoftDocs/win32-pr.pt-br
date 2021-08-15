---
title: Métodos 10Level9 ID3D11DeviceContext
description: Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso do D3D \_ \_ \_ 11 \_ 0 e superior para os métodos ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cb055e6a290a9500f65ad2d64cdd69b0eaa224e6a81359595688ba1aca657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990066"
---
# <a name="10level9-id3d11devicecontext-methods"></a>Métodos 10Level9 ID3D11DeviceContext

Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso do D3D \_ \_ \_ 11 \_ 0 e superior para os métodos [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

-   [ID3D11DeviceContext::CopySubresourceRegion](#id3d11devicecontextcopysubresourceregion)
-   [ID3D11DeviceContext::CopyResource](#id3d11devicecontextcopyresource)
-   [ID3D11DeviceContext::CopyStructureCount](#id3d11devicecontextcopystructurecount)
-   [ID3D11DeviceContext::ClearUnorderedAccessViewFloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [ID3D11DeviceContext::ClearUnorderedAccessViewUint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [ID3D11DeviceContext::ClearRenderTargetView](#id3d11devicecontextclearrendertargetview)
-   [ID3D11DeviceContext::CSSetConstantBuffers](#id3d11devicecontextcssetconstantbuffers)
-   [ID3D11DeviceContext::CSSetSamplers](#id3d11devicecontextcssetsamplers)
-   [ID3D11DeviceContext::CSSetShader](#id3d11devicecontextcssetshader)
-   [ID3D11DeviceContext::CSSetShaderResources](#id3d11devicecontextcssetshaderresources)
-   [ID3D11DeviceContext::CSSetUnorderedAccessViews](#id3d11devicecontextcssetunorderedaccessviews)
-   [ID3D11DeviceContext::D ispatch](#id3d11devicecontextdispatch)
-   [ID3D11DeviceContext::D ispatchIndirect](#id3d11devicecontextdispatchindirect)
-   [ID3D11DeviceContext::Draw](#id3d11devicecontextdraw)
-   [ID3D11DeviceContext::DrawAuto](#id3d11devicecontextdrawauto)
-   [ID3D11DeviceContext::DrawIndexed](#id3d11devicecontextdrawindexed)
-   [ID3D11DeviceContext::DrawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [ID3D11DeviceContext::D rawIndexedInstancedIndirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [ID3D11DeviceContext::DrawInstanced](#id3d11devicecontextdrawinstanced)
-   [ID3D11DeviceContext::D rawInstancedIndirect](#id3d11devicecontextdrawinstancedindirect)
-   [ID3D11DeviceContext::D SSetConstantBuffers](#id3d11devicecontextdssetconstantbuffers)
-   [ID3D11DeviceContext::D SSetSamplers](#id3d11devicecontextdssetsamplers)
-   [ID3D11DeviceContext::D SSetShader](#id3d11devicecontextdssetshader)
-   [ID3D11DeviceContext::D SSetShaderResources](#id3d11devicecontextdssetshaderresources)
-   [ID3D11DeviceContext::GSSetConstantBuffers](#id3d11devicecontextgssetconstantbuffers)
-   [ID3D11DeviceContext::GSSetSamplers](#id3d11devicecontextgssetsamplers)
-   [ID3D11DeviceContext::GSSetShader](#id3d11devicecontextgssetshader)
-   [ID3D11DeviceContext::GSSetShaderResources](#id3d11devicecontextgssetshaderresources)
-   [ID3D11DeviceContext::HSSetConstantBuffers](#id3d11devicecontexthssetconstantbuffers)
-   [ID3D11DeviceContext::HSSetSamplers](#id3d11devicecontexthssetsamplers)
-   [ID3D11DeviceContext::HSSetShader](#id3d11devicecontexthssetshader)
-   [ID3D11DeviceContext::HSSetShaderResources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [ID3D11DeviceContext::IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [ID3D11DeviceContext::OMSetBlendState](#id3d11devicecontextomsetblendstate)
-   [ID3D11DeviceContext::OMSetRenderTargets](#id3d11devicecontextomsetrendertargets)
-   [ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [ID3D11DeviceContext::P SSetConstantBuffers](#id3d11devicecontextpssetconstantbuffers)
-   [ID3D11DeviceContext::P SSetSamplers](#id3d11devicecontextpssetsamplers)
-   [ID3D11DeviceContext::P SSetShader](#id3d11devicecontextpssetshader)
-   [ID3D11DeviceContext::P SSetShaderResources](#id3d11devicecontextpssetshaderresources)
-   [ID3D11DeviceContext::RSSetScissorRects](#id3d11devicecontextrssetscissorrects)
-   [ID3D11DeviceContext::RSSetViewports](#id3d11devicecontextrssetviewports)
-   [ID3D11DeviceContext::SetPredication](#id3d11devicecontextsetpredication)
-   [ID3D11DeviceContext::SOSetTargets](#id3d11devicecontextsosettargets)
-   [ID3D11DeviceContext::VSSetConstantBuffers](#id3d11devicecontextvssetconstantbuffers)
-   [ID3D11DeviceContext::VSSetSamplers](#id3d11devicecontextvssetsamplers)
-   [ID3D11DeviceContext::VSSetShader](#id3d11devicecontextvssetshader)
-   [ID3D11DeviceContext::VSSetShaderResources](#id3d11devicecontextvssetshaderresources)
-   [Tópicos relacionados](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>ID3D11DeviceContext::CopySubresourceRegion



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Somente Texture2D e buffers podem ser copiados na memória acessível por GPU.<br/> Texture3D não pode ser copiado da memória acessível por GPU para a memória acessível pela CPU.<br/> Qualquer recurso que tenha apenas D3D10_BIND_SHADER_RESOURCE não pode ser copiado da memória acessível por GPU para memória acessível por CPU.<br/> Não é possível copiar as texturas do volume mipmapped. <br/> $ {REMOVER} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a>ID3D11DeviceContext::CopyResource



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Somente Texture2D e buffers podem ser copiados na memória acessível por GPU.<br/> Texture3D não pode ser copiado da memória acessível por GPU para a memória acessível pela CPU.<br/> Qualquer recurso que tenha apenas D3D10_BIND_SHADER_RESOURCE não pode ser copiado da memória acessível por GPU para memória acessível por CPU.<br/> $ {REMOVER} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a>ID3D11DeviceContext::CopyStructureCount



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>ID3D11DeviceContext::ClearUnorderedAccessViewFloat



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>ID3D11DeviceContext::ClearUnorderedAccessViewUint



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a>ID3D11DeviceContext::ClearRenderTargetView



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Somente a primeira fatia da matriz será limpa. Os aplicativos devem criar uma exibição de destino de renderização para cada fatia de face ou matriz e, em seguida, limpar cada exibição individualmente.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>ID3D11DeviceContext::CSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a>ID3D11DeviceContext::CSSetSamplers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a>ID3D11DeviceContext::CSSetShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a>ID3D11DeviceContext::CSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>ID3D11DeviceContext::CSSetUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a>ID3D11DeviceContext::D ispatch



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a>ID3D11DeviceContext::D ispatchIndirect



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext::Draw



| Nível de recursos             | Diferenças de comportamento                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | O número de primitivos pode não exceder 65535.<br/> Texturas não podem se repetir em um primitivo mais de 128 vezes.<br/>    |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | O número de primitivos pode não exceder 1048575.<br/> As texturas não podem se repetir em um primitivo mais de 2048 vezes.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | O número de primitivos pode não exceder 1048575.<br/> Texturas não podem se repetir em um primitivo mais de 8192 vezes.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext::DrawAuto



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext::DrawIndexed



| Nível de recursos             | Diferenças de comportamento                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | O número de primitivos pode não exceder 65535.<br/> Texturas não podem se repetir em um primitivo mais de 128 vezes.<br/> Os valores de índice não podem exceder 65534.<br/> Não há suporte para listas de pontos indexados.<br/>      |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | O número de primitivos pode não exceder 1048575.<br/> As texturas não podem se repetir em um primitivo mais de 2048 vezes.<br/> Os valores de índice não podem exceder 1048575.<br/> Não há suporte para listas de pontos indexados.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | O número de primitivos pode não exceder 1048575.<br/> Texturas não podem se repetir em um primitivo mais de 8192 vezes.<br/> Os valores de índice não podem exceder 1048575.<br/> Não há suporte para listas de pontos indexados.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext::DrawIndexedInstanced



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Sem suporte${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>O número de primitivos pode não exceder 1048575.<br/> Texturas não podem se repetir em um primitivo mais de 8192 vezes.<br/> Os valores de índice não podem exceder 1048575.<br/>
<blockquote>
[!Note]<br />
Quando você chama o método <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> com um sombreador de vértice que está associado ao pipeline e que não importa nenhum dado por instância, alguns hardwares de gráficos do Direct3D 9 podem não desenhar nada. Em particular, se o sombreador de vértice não usar nenhum dado por instância, chamar <strong>DrawIndexedInstanced</strong> com 1 instância não será equivalente a chamar <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>draw</strong></a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>ID3D11DeviceContext::D rawIndexedInstancedIndirect



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext::DrawInstanced



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>ID3D11DeviceContext::D rawInstancedIndirect



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>ID3D11DeviceContext::D SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a>ID3D11DeviceContext::D SSetSamplers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a>ID3D11DeviceContext::D SSetShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a>ID3D11DeviceContext::D SSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>ID3D11DeviceContext::GSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a>ID3D11DeviceContext::GSSetSamplers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a>ID3D11DeviceContext::GSSetShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a>ID3D11DeviceContext::GSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>ID3D11DeviceContext::HSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a>ID3D11DeviceContext::HSSetSamplers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a>ID3D11DeviceContext::HSSetShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a>ID3D11DeviceContext::HSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>O formato pode ser diferente daquele especificado na criação do buffer, mas uma tradução cara será incorrida.<br/> Permite apenas buffers de índice com o formato DXGI_FORMAT_R16_UINT. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> O formato pode ser diferente daquele especificado na criação do buffer, mas uma tradução cara será incorrida.<br/> Permite buffers de índice com os formatos DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 e superior. <br/> $ {REMOVER} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext::IASetPrimitiveTopology



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para topologias primitivas com adjacência $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a>ID3D11DeviceContext::OMSetBlendState



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">SampleMask não pode ser zero $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a>ID3D11DeviceContext::OMSetRenderTargets



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Somente um destino de renderização tem suporte para $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Somente quatro destinos de renderização têm suporte e todos os recursos associados devem ter a mesma profundidade de bits.</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>ID3D11DeviceContext::P SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Consulte nível de recurso 10,0, mas o número total de constantes usadas pelo sombreador não pode exceder 32 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a>ID3D11DeviceContext::P SSetSamplers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No máximo 16 amostras podem ser associadas $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a>ID3D11DeviceContext::P SSetShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Somente ps_4_0_level_9_1 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Somente ps_4_0_level_9_3 ou ps_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a>ID3D11DeviceContext::P SSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não mais que 8 recursos de sombreador vinculados simultaneamente $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a>ID3D11DeviceContext::RSSetScissorRects



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Somente a rect de tesoura zero está disponível${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a>ID3D11DeviceContext::RSSetViewports



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Somente o zero viewport está disponível${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

Embora você especifique valores float para os membros da estrutura [**\_ VIEWPORT D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) para a matriz *pViewports* em uma chamada para [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para níveis de recurso [9](overviews-direct3d-11-devices-downlevel-intro.md) \_ x, **RSSetViewports** usa DWORDs internamente. Devido a esse comportamento, quando você usa um canto superior esquerdo negativo para o viewport, a chamada para **RSSetViewports** para níveis de recurso 9 \_ x falha. Essa falha ocorre porque **RSSetViewports** para 9 x transforma os valores de ponto flutuante em inteiros sem sinal sem validação, o que resulta em estouro \_ de inteiro.

A chamada para [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para os níveis [de](overviews-direct3d-11-devices-downlevel-intro.md) recurso 10 x e 11 x funciona como esperado mesmo quando você usa um canto superior esquerdo negativo para o \_ \_ viewport.

## <a name="id3d11devicecontextsetpredication"></a>ID3D11DeviceContext::SetPredication



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a>ID3D11DeviceContext::SOSetTargets



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>ID3D11DeviceContext::VSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Consulte o nível de recurso 10.0, mas o número total de constantes usadas pelo sombreador não pode exceder 255${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a>ID3D11DeviceContext::VSSetSamplers



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a>ID3D11DeviceContext::VSSetShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Somente vs_4_0_level_9_1${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Somente vs_4_0_level_9_3 ou vs_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a>ID3D11DeviceContext::VSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





