---
title: Função glIndexMask (Gl.h)
description: A função glIndexMask controla a escrita de bits individuais nos buffers de índice de cores.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- Função glIndexMask OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e022bb3cbb5be5ac15049b5e8bc128d2ac7e100d5bcec6a87988dd2d14c5d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012194"
---
# <a name="glindexmask-function"></a>Função glIndexMask

A **função glIndexMask** controla a escrita de bits individuais nos buffers de índice de cores.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mask* 
</dt> <dd>

Uma máscara de bits para habilitar e desabilitar a escrita de bits individuais nos buffers de índice de cores. Inicialmente, a máscara é de todos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glIndexMask** controla a escrita de bits individuais nos buffers de índice de cores. Os n *bits menos significativos* da *máscara*, em *que 1* é o número de bits em um buffer de índice de cores, especifique uma máscara. Sempre que um aparece na máscara, o bit correspondente no buffer de índice de cor (ou buffers) se tornou writable. Quando um zero é exibido, o bit é protegido por gravação.

Essa máscara é usada somente no modo de índice de cores e afeta apenas os buffers atualmente selecionados para escrita (consulte [**glDrawBuffer**](gldrawbuffer.md)). Inicialmente, todos os bits estão habilitados para escrita.

A função a seguir recupera informações relacionadas **a glIndexMask:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ INDEX \_ WRITEMASK

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





