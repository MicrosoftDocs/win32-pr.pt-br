---
title: Método ID3DX11EffectShaderVariable GetOutputSignatureElementDesc (D3dx11effect.h)
description: Obter uma descrição de assinatura de saída.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Método GetOutputSignatureElementDesc Direct3D 11
- Método GetOutputSignatureElementDesc Direct3D 11 , interface ID3DX11EffectShaderVariable
- ID3DX11EffectShaderVariable interface Direct3D 11 , método GetOutputSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af968b25a00e32b489a520e9d4a3e870329af910caa8ac1bf45ac49a7ea6132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533262"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a>Método ID3DX11EffectShaderVariable::GetOutputSignatureElementDesc

Obter uma descrição de assinatura de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetOutputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Um índice de sombreador baseado em zero.

</dd> <dt>

*Element* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Um índice de elemento baseado em zero.

</dd> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ \_ \_ DESC DESC DE PARÂMETRO DE ASSINATURA**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Um ponteiro para uma descrição de parâmetro (consulte [**D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Um efeito contém um ou mais sombreadores; cada sombreador tem uma assinatura de entrada e saída; cada assinatura contém um ou mais elementos (ou parâmetros). O índice do sombreador identifica o sombreador e o índice do elemento identifica o elemento (ou parâmetro) na assinatura do sombreador.

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

 

