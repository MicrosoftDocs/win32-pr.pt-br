---
description: Renderiza uma textura em um arquivo e retorna o resultado para o host asynchrnously.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5:: RenderTextureAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41189637fd741d22fc566f913b25ddba1109854ed12a0336ffac899c10fd3147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405676"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5:: RenderTextureAsync

Renderiza uma textura em um arquivo e retorna o resultado para o host asynchrnously.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parâmetros

*textureid*   
A ID da textura a ser renderizada.

*sliceIndex*   
O índice da fatia dentro da textura a ser renderizada.

*formatOverride*   
A substituição do formato de cor.

*canto*   

*canto superior*   

*shaderFileName*   
Uma cadeia de caracteres COM que contém o nome do caminho do arquivo do sombreador.

*numFloatShaderVars*   
O número de variáveis do sombreador de ponto flutuante

*count6 \_ shaderFloatVarName*   
Cadeias de caracteres COM contianing os nomes das variáveis do sombreador de ponto flutuante.

*count6 \_ shaderFloatVarValue*   
As variáveis do sombreador de ponto flutuante.

*numBoolShaderVars*   
O número de variáveis de sombreador booliano.

*count9 \_ shaderBoolVarName*   
Cadeias de caracteres COM contianing os nomes das variáveis de sombreador booliano.

*count9 \_ shaderBoolVarValue*   
As variáveis do sombreador booliano.

*renderContentFileName*   
Uma cadeia de caracteres COM que contém o nome do caminho do arquivo onde a textura renderizada foi gravada.

*retornos*   
O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.

*requestCookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*progressIntervalMsecs*   
Não usado.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
