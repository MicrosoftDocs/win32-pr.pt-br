---
title: função glColorMask (GL. h)
description: A função glColorMask habilita e desabilita a gravação de componentes de cores do buffer de quadros.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- função glColorMask OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e8b3e9e00eaa294f77813f8e994358cbb473fc4e5c02fce8e5115dc517cae20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081716"
---
# <a name="glcolormask-function"></a>função glColorMask

A função **glColorMask** habilita e desabilita a gravação de componentes de cores do buffer de quadros.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vermelho* 
</dt> <dd>

Especifique se o vermelho pode ou não ser gravado no framebuffer. Os valores padrão são GL \_ verdadeiro, indicando que o componente de cor pode ser escrito.

</dd> <dt>

*amarela* 
</dt> <dd>

Especifique se o verde pode ou não ser gravado no framebuffer. O valor padrão é GL \_ true, indicando que o componente de cor pode ser escrito.

</dd> <dt>

*azul* 
</dt> <dd>

Especifique se azul pode ou não ser gravado no framebuffer. O valor padrão é GL \_ true, indicando que o componente de cor pode ser escrito.

</dd> <dt>

*alfa* 
</dt> <dd>

Especifique se alfa pode ou não ser gravado no framebuffer. O valor padrão é GL \_ true, indicando que o componente de cor pode ser escrito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glColorMask** especifica se os componentes de cor individuais no framebuffer podem ou não ser gravados. Se *vermelho* é GL \_ falso, por exemplo, nenhuma alteração é feita no componente vermelho de qualquer pixel em qualquer um dos buffers de cor, independentemente da tentativa de operação de desenho.

As alterações em bits individuais de componentes não podem ser controladas. Em vez disso, as alterações são habilitadas ou desabilitadas para componentes inteiros de cor.

As funções a seguir recuperam informações relacionadas ao **glColorMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a cor do argumento GL \_ \_ WRITEMASK

**glGet** com o modo do Argument GL \_ RGBA \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





