---
title: função glStencilMask (GL. h)
description: A função glStencilMask controla a gravação de bits individuais nos planos de estêncil.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- função glStencilMask OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086462"
---
# <a name="glstencilmask-function"></a>função glStencilMask

A função **glStencilMask** controla a gravação de bits individuais nos planos de estêncil.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mascara* 
</dt> <dd>

Uma máscara de bits para habilitar e desabilitar a gravação de bits individuais nos planos de estêncil. Inicialmente, a máscara é tudo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glStencilMask** controla a gravação de bits individuais nos planos de estêncil. Os *n* bits menos significativos de *Mask*, em que *n* é o número de bits no buffer do estêncil, especifique uma máscara. Sempre que um deles aparecer na máscara, o bit correspondente no buffer do estêncil será gravável. Onde um zero é exibido, o bit é protegido contra gravação. Inicialmente, todos os bits estão habilitados para gravação.

As funções a seguir recuperam informações relacionadas ao **glStencilMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ WRITEMASK de estêncil do Argument GL \_

glGet com bits de estêncil do Argument GL \_ \_

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





