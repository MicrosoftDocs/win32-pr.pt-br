---
title: Interfaces de sombreador (gráficos do Direct3D 12)
description: D3d12shader. h declara as interfaces a seguir.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- interfaces, sombreador do Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105762208"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a>Interfaces de sombreador (gráficos do Direct3D 12)

d3d12shader. h declara as interfaces a seguir.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a><br/></td>
<td>Uma interface de função-parâmetro-Reflection acessa informações de parâmetro de função. <br/>
<blockquote>
[!Note]<br />
Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 12 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a><br/></td>
<td>Uma interface de reflexão de função acessa informações de função. <br/>
<blockquote>
[!Note]<br />
Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 12 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a><br/></td>
<td>Uma interface de reflexão de biblioteca acessa informações da biblioteca. <br/>
<blockquote>
[!Note]<br />
Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 12 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a><br/></td>
<td>Uma interface Shader-Reflection acessa informações de sombreador. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>Esta interface Shader-Reflection fornece acesso a um buffer constante. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a><br/></td>
<td>Esta interface Shader-Reflection fornece acesso ao tipo de variável. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a><br/></td>
<td>Essa interface Shader-Reflection fornece acesso a uma variável. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Referência do sombreador](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





