---
description: Função D3DXGetPixelShaderProfile – retorna o nome do perfil HLSL (linguagem de sombreador de alto nível) mais alto com suporte em um determinado dispositivo.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Função D3DXGetPixelShaderProfile (D3DX9Shader.h)
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
ms.openlocfilehash: dc609e742a4f780f3cb8c34e4dbc4cc40842ee51
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473652"
---
# <a name="d3dxgetpixelshaderprofile-function"></a>Função D3DXGetPixelShaderProfile

Retorna o nome do perfil HLSL (linguagem de sombreador de alto nível) mais alto com suporte em um determinado dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para o dispositivo. Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

O nome do perfil HLSL.

Se o dispositivo não for suportado por sombreadores de pixel, a função retornará **NULL.**

## <a name="remarks"></a>Comentários

Um perfil de sombreador especifica a versão do sombreador de assembly a ser usada e os recursos disponíveis para o compilador HLSL ao compilar um sombreador. A tabela a seguir lista os perfis de sombreador de pixel com suporte.




| Perfil do sombreador | Descrição | 
|----------------|-------------|
| ps_1_1 | Compile para ps_1_1 versão. | 
| ps_1_2 | Compile para ps_1_2 versão. | 
| ps_1_3 | Compile para ps_1_3 versão. | 
| ps_1_4 | Compile para ps_1_4 versão. | 
| ps_2_0 | Compile para ps_2_0 versão. | 
| ps_2_a | O mesmo que o ps_2_0, com os seguintes recursos adicionais disponíveis para o compilador ter como destino:<ul><li>O número de Registros Temporários (r#) é maior ou igual a 22.</li><li>Swizzle de origem arbitrária.</li><li>Instruções de gradiente: dsx, dsy.</li><li>Predication.</li><li>Nenhum limite de leitura de textura dependente.</li><li>Nenhum limite para o número de instruções de textura.</li></ul> | 
| ps_2_b | O mesmo que o ps_2_0, com os seguintes recursos adicionais disponíveis para o compilador ter como destino:<ul><li>O número de Registros Temporários (r#) é maior ou igual a 32.</li><li>Nenhum limite para o número de instruções de textura.</li></ul> | 
| ps_3_0 | Compile para ps_3_0 versão. | 




 

Para obter mais informações sobre as diferenças entre as versões do sombreador, consulte [Diferenças do sombreador de pixel.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
