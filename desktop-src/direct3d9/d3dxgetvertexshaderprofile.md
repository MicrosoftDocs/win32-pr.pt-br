---
description: Retorna o nome do perfil de HLSL (linguagem de sombreamento de alto nível) com suporte de um determinado dispositivo.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Função D3DXGetVertexShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764168"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>Função D3DXGetVertexShaderProfile

Retorna o nome do perfil de HLSL (linguagem de sombreamento de alto nível) com suporte de um determinado dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para o dispositivo. Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

O nome do perfil HLSL.

Se o dispositivo não oferecer suporte a sombreadores de vértice, a função retornará **NULL**.

## <a name="remarks"></a>Comentários

Um perfil de sombreador especifica a versão do sombreador de assembly a ser usada e os recursos disponíveis para o compilador HLSL ao compilar um sombreador. A tabela a seguir lista os perfis de sombreador de vértice que têm suporte.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Perfil do sombreador</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vs_1_1</td>
<td>Compilar para vs_1_1 versão.</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>Compilar para vs_2_0 versão.</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>O mesmo que o perfil de vs_2_0, com os seguintes recursos adicionais disponíveis para o compilador visar:
<ul>
<li>O número de registros temporários (r #) é maior ou igual a 13.</li>
<li>Instrução de controle de fluxo dinâmico.</li>
<li>Predicação.</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>Compilar para vs_3_0 versão.</td>
</tr>
</tbody>
</table>



 

Para obter mais informações sobre as diferenças entre versões de sombreador, consulte [diferenças de sombreador de vértice](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
