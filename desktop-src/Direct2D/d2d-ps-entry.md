---
title: Função D2D_PS_ENTRY (D2d1effecthelpers. h)
description: Uma macro que define um ponto de entrada de sombreador de pixel com o nome de função fornecido.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- Função D2D_PS_ENTRY Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755373"
---
# <a name="d2d_ps_entry-function"></a>Função de entrada do \_ PS D2D \_

Uma macro que define um ponto de entrada de sombreador de pixel com o nome de função fornecido.

## <a name="syntax"></a>Sintaxe

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Entryname* \[ no\]
</dt> <dd>

O nome do ponto de entrada do sombreador de pixel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use essa macro em vez de especificar a assinatura de entrada do ponto de entrada da maneira normal: todos os parâmetros são implícitos e adicionados pelo Direct2D durante a compilação, dependendo do tipo de destino de compilação (sombreador completo ou função de exportação).

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

Neste exemplo curto, observe que nenhum parâmetro de função é declarado, que o número de entradas e o tipo de cada entrada é declarado antes da função de entrada, a entrada é recuperada chamando [D2DGetInput](d2dgetinput.md)e as diretivas de pré-processador devem ser definidas antes de o arquivo auxiliar ser incluído.

Um sombreador compatível com vinculação deve fornecer um sombreador de pixel de passagem simples regular e uma função de sombreador de exportação. A \_ macro de entrada do PS D2D \_ permite que cada um deles seja gerado a partir do mesmo código, quando usado em conjunto com o script de compilação do sombreador.

Ao compilar um sombreador completo, as macros são expandidas no código a seguir, que tem uma assinatura de entrada compatível com efeitos de D2D.

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

Ao compilar uma versão de função de exportação do mesmo código, o código a seguir é gerado:

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

Observe que a entrada de textura, normalmente recuperada por amostragem de um Texture2D, foi substituída por um input0 de entrada de função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vinculação de Sombreador de Efeito](effect-shader-linking.md)
</dt> <dt>

[Auxiliares de HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





