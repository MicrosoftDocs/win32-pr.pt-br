---
description: Renderiza uma textura em um arquivo e retorna o resultado para o host de forma assíncrona.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPixEngine5::RenderTextureAsync
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400ade8aa962a73234efbfb710d9ab6b178dfd4e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626562"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5::RenderTextureAsync

Renderiza uma textura em um arquivo e retorna o resultado para o host de forma assíncrona.

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

*textureId*   
A ID da textura a ser renderização.

*sliceIndex*   
O índice da fatia dentro da textura a ser renderização.

*formatOverride*   
A substituição de formato de cor.

*Inferior*   

*Superior*   

*shaderFileName*   
Uma cadeia de caracteres COM que contém o nome do caminho do arquivo de sombreador.

*numFloatShaderVars*   
O número de variáveis de sombreador de ponto flutuante

*count6 \_ shaderFloatVarName*   
Cadeias de caracteres COM que conotam os nomes das variáveis de sombreador de ponto flutuante.

*count6 \_ shaderFloatVarValue*   
As variáveis do sombreador de ponto flutuante.

*numBoolShaderVars*   
O número de variáveis de sombreador boolianas.

*count9 \_ shaderBoolVarName*   
Cadeias de caracteres COM que conotam os nomes das variáveis de sombreador booliano.

*count9 \_ shaderBoolVarValue*   
As variáveis de sombreador boolianas.

*renderContentFileName*   
Uma cadeia de caracteres COM que contém o nome do caminho do arquivo em que a textura renderizada foi escrita.

*Retornos*   
O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.

*requestCookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*progressIntervalMsecs*   
Não usado.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
