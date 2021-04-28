---
description: Função D3DXGetPixelShaderProfile – retorna o nome do perfil de HLSL (linguagem de sombreamento de alto nível) com suporte de um determinado dispositivo.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Função D3DXGetPixelShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d24e19d49a8a96f91847892f519ef6c06d25ef5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114427"
---
# <a name="d3dxgetpixelshaderprofile-function"></a>Função D3DXGetPixelShaderProfile

Retorna o nome do perfil de HLSL (linguagem de sombreamento de alto nível) com suporte de um determinado dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
LPCSTR D3DXGetPixelShaderProfile(
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

## <a name="return-value"></a>Valor retornado

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

O nome do perfil HLSL.

Se o dispositivo não oferecer suporte a sombreadores de pixel, a função retornará **NULL**.

## <a name="remarks"></a>Comentários

Um perfil de sombreador especifica a versão do sombreador de assembly a ser usada e os recursos disponíveis para o compilador HLSL ao compilar um sombreador. A tabela a seguir lista os perfis de sombreador de pixel com suporte.



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
<td>ps_1_1</td>
<td>Compilar para ps_1_1 versão.</td>
</tr>
<tr class="even">
<td>ps_1_2</td>
<td>Compilar para ps_1_2 versão.</td>
</tr>
<tr class="odd">
<td>ps_1_3</td>
<td>Compilar para ps_1_3 versão.</td>
</tr>
<tr class="even">
<td>ps_1_4</td>
<td>Compilar para ps_1_4 versão.</td>
</tr>
<tr class="odd">
<td>ps_2_0</td>
<td>Compilar para ps_2_0 versão.</td>
</tr>
<tr class="even">
<td>ps_2_a</td>
<td>O mesmo que o perfil de ps_2_0, com os seguintes recursos adicionais disponíveis para o compilador visar:
<ul>
<li>O número de registros temporários (r #) é maior ou igual a 22.</li>
<li>Swizzle de origem arbitrária.</li>
<li>Instruções de gradiente: DSX, DSY.</li>
<li>Predicação.</li>
<li>Nenhum limite de leitura de textura dependente.</li>
<li>Nenhum limite para o número de instruções de textura.</li>
</ul></td>
</tr>
<tr class="odd">
<td>ps_2_b</td>
<td>O mesmo que o perfil de ps_2_0, com os seguintes recursos adicionais disponíveis para o compilador visar:
<ul>
<li>O número de registros temporários (r #) é maior ou igual a 32.</li>
<li>Nenhum limite para o número de instruções de textura.</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_3_0</td>
<td>Compilar para ps_3_0 versão.</td>
</tr>
</tbody>
</table>



 

Para obter mais informações sobre as diferenças entre versões de sombreador, consulte [diferenças de sombreador de pixel](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
