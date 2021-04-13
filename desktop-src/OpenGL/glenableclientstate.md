---
title: função glEnableClientState (GL. h)
description: As funções glEnableClientState e glDisableClientState habilitam e desabilitam matrizes, respectivamente. | função glEnableClientState (GL. h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- função glEnableClientState OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e333a51d4c1fe0a5ff11c717790e03aa6d054a09
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298313"
---
# <a name="glenableclientstate-function"></a>função glEnableClientState

As funções **glEnableClientState** e [**glDisableClientState**](gldisableclientstate.md) habilitam e desabilitam matrizes, respectivamente.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*array* 
</dt> <dd>

Uma constante simbólica para a matriz que você deseja habilitar ou desabilitar. Esse parâmetro pode assumir um dos valores a seguir.



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**\_matriz de cores GL \_**</dt> </dl>                          | Se habilitada, use matrizes de cores com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glColorPointer**](glcolorpointer.md).<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**\_matriz do \_ sinalizador do Edge GL \_**</dt> </dl>             | Se habilitada, use matrizes de sinalizador de borda com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glEdgeFlagPointer**](gledgeflagpointer.md).<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**\_matriz de índice GL \_**</dt> </dl>                          | Se habilitada, use matrizes de índice com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glIndexPointer**](glindexpointer.md).<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**matriz do GL \_ normal \_**</dt> </dl>                       | Se habilitada, use matrizes normais com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glNormalPointer**](glnormalpointer.md).<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**\_matriz GL \_ coord de textura \_**</dt> </dl> | Se habilitada, use matrizes de coordenadas de textura com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glTexCoordPointer**](gltexcoordpointer.md).<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**\_matriz de vértice GL \_**</dt> </dl>                       | Se habilitada, use matrizes de vértice com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glVertexPointer**](glvertexpointer.md).<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                             | Significado                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl> | a *matriz* não era um valor aceito.<br/> |



## <a name="remarks"></a>Comentários

As funções **glEnableClientState** e **glDisableClientState** habilitam e desabilitam várias matrizes individuais. Use [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar a configuração atual de qualquer recurso.

Chamar **glEnableClientState** e **glDisableClientState** entre chamadas para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md) pode causar um erro. Se nenhum erro for gerado, o comportamento será indefinido.

> [!Note]  
> As funções **glEnableClientState** e **glDisableClientState** só estão disponíveis no OpenGL versão 1,1 ou posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





