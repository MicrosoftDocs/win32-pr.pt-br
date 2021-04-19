---
title: função glIndexMask (GL. h)
description: A função glIndexMask controla a gravação de bits individuais nos buffers de índice de cor.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- função glIndexMask OpenGL
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
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811312"
---
# <a name="glindexmask-function"></a>função glIndexMask

A função **glIndexMask** controla a gravação de bits individuais nos buffers de índice de cor.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mascara* 
</dt> <dd>

Uma máscara de bits para habilitar e desabilitar a gravação de bits individuais nos buffers de índice de cores. Inicialmente, a máscara é tudo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glIndexMask** controla a gravação de bits individuais nos buffers de índice de cor. Os *n* bits menos significativos de *Mask*, em que *1* é o número de bits em um buffer de índice de cor, especifique uma máscara. Sempre que um deles aparecer na máscara, o bit correspondente no buffer de índice de cor (ou buffers) se tornará gravável. Onde um zero é exibido, o bit é protegido contra gravação.

Essa máscara é usada somente no modo de índice de cor e afeta somente os buffers selecionados atualmente para gravação (consulte [**glDrawBuffer**](gldrawbuffer.md)). Inicialmente, todos os bits estão habilitados para gravação.

A função a seguir recupera informações relacionadas a **glIndexMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ index \_ WRITEMASK

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

 

 





