---
title: Função glEnableClientState (Gl.h)
description: As funções glEnableClientState e glDisableClientState habilitam e desabilitam matrizes, respectivamente. | Função glEnableClientState (Gl.h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- Função glEnableClientState OpenGL
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
ms.openlocfilehash: 0d1ebb9b0278ca6a696183da54c40a6463880a24f6a29a7cca3c2fdd9dd1213a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360413"
---
# <a name="glenableclientstate-function"></a>Função glEnableClientState

As **funções glEnableClientState** e [**glDisableClientState**](gldisableclientstate.md) habilitam e desabilitam matrizes, respectivamente.

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
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**MATRIZ \_ DE CORES GL \_**</dt> </dl>                          | Se habilitado, use matrizes de cores com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glColorPointer.**](glcolorpointer.md)<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**MATRIZ \_ DE SINALIZADOR DE BORDA \_ \_ GL**</dt> </dl>             | Se habilitado, use matrizes de sinalizadores de borda com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glEdgeFlagPointer.**](gledgeflagpointer.md)<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL \_ INDEX \_ ARRAY**</dt> </dl>                          | Se habilitado, use matrizes de índice com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glIndexPointer.**](glindexpointer.md)<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**MATRIZ \_ NORMAL \_ GL**</dt> </dl>                       | Se habilitado, use matrizes normais com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glNormalPointer.**](glnormalpointer.md)<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**MATRIZ DE \_ \_ COORD DE TEXTURA \_ GL**</dt> </dl> | Se habilitado, use matrizes de coordenadas de textura com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glTexCoordPointer**](gltexcoordpointer.md).<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**MATRIZ \_ DE VÉRTICE \_ GL**</dt> </dl>                       | Se habilitado, use matrizes de vértice com chamadas para [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Consulte também [**glVertexPointer.**](glvertexpointer.md)<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                             | Significado                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl> | *array* não era um valor aceito.<br/> |



## <a name="remarks"></a>Comentários

As **funções glEnableClientState** e **glDisableClientState** habilitam e desabilitam várias matrizes individuais. Use [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar a configuração atual de qualquer funcionalidade.

Chamar **glEnableClientState** e **glDisableClientState** entre chamadas para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md) pode causar um erro. Se nenhum erro for gerado, o comportamento será indefinido.

> [!Note]  
> As **funções glEnableClientState** e **glDisableClientState** só estão disponíveis no OpenGL versão 1.1 ou posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
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

 

 





