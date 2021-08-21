---
title: Método GetDomainShaderVariable ID3DX11EffectShaderVariable (D3dx11effect.h)
description: Obter um sombreador de domínio.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- Método GetDomainShader Direct3D 11
- Método GetDomainShader Direct3D 11 , interface ID3DX11EffectShaderVariable
- ID3DX11EffectShaderVariable interface Direct3D 11 , método GetDomainShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetDomainShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e66bb99f170e6b638587d7da5a8d3cc57a34d3cab6bb04968b049d39dcb09c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533292"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a>Método ID3DX11EffectShaderVariable::GetDomainShader

Obter um sombreador de domínio.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDomainShader(
   UINT               ShaderIndex,
   ID3D11DomainShader **ppPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Índice do sombreador de domínio.

</dd> <dt>

*Ppp* 
</dt> <dd>

Tipo: **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***

Ponteiro para um [**ponteiro ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) que será definido como o sombreador de domínio no retorno.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

