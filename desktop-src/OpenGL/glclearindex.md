---
title: função glClearIndex (GL. h)
description: A função glClearIndex especifica o valor de limpeza para os buffers de índice de cor.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- função glClearIndex OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455321"
---
# <a name="glclearindex-function"></a>função glClearIndex

A função **glClearIndex** especifica o valor de limpeza para os buffers de índice de cor.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*c* 
</dt> <dd>

O índice usado quando os buffers de índice de cor são apagados. O valor padrão é zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glClearIndex** especifica o índice usado pelo [**glClear**](glclear.md) para limpar os buffers de índice de cores. O parâmetro *c* não é clamped. Em vez disso, *c* é convertido em um valor de ponto fixo com precisão não especificada à direita do ponto binário. A parte inteira desse valor é então mascarada com 2 <sup>m</sup>  -1, em que *m* é o número de bits em um índice de cores armazenado no framebuffer.

As funções a seguir recuperam informações relacionadas ao **glClearIndex**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ \_ valor Clear do índice do Argument GL \_

**glGet** com bits de índice do Argument GL \_ \_

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





