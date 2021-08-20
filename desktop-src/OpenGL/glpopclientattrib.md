---
title: Função glPopClientAttrib (Gl.h)
description: As funções glPushClientAttrib e glPopClientAttrib salvam e restauram grupos de variáveis de estado do cliente na pilha cliente-atributo. | Função glPopClientAttrib (Gl.h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- Função glPopClientAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8488b689c72f64e20be6871dc95497ac08ce3e0fe45c6ae59471fed0ec0e427b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980788"
---
# <a name="glpopclientattrib-function"></a>Função glPopClientAttrib

As [**funções glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib** salvam e restauram grupos de variáveis de estado do cliente na pilha cliente-atributo.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                               | Significado                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl> | A função foi chamada enquanto a pilha cliente-atributo estava cheia.<br/> |



## <a name="remarks"></a>Comentários

A **função glPushClientAttrib** usa seu parâmetro mask para determinar quais grupos de variáveis de estado do cliente são salvos na pilha cliente-atributo. Você pode usar o operador OR bit a bit para unir constantes simbólicas aceitas para definir bits e construir uma máscara.

A **função glPopClientAttrib restaura** os valores das variáveis de estado do cliente salvas pela última vez com **glPushclientAttrib**. As variáveis de estado do cliente não salvas anteriormente são deixadas inalteradas. Efetuar o esmaeamento de atributos para uma pilha de atributo de cliente completa ou a ressarção de atributos de uma pilha vazia define um sinalizador de erro e nenhuma outra alteração é feita no estado OpenGL. Por padrão, a pilha de atributos do cliente está vazia.

Alguns valores de estado do cliente OpenGL não podem ser salvos na pilha cliente-atributo. Por exemplo, você não pode salvar os estados de seleção ou comentários na pilha cliente-atributo. A profundidade da pilha cliente-atributo é pelo menos 16.

As **funções glPushclientAttrib** e **glPopClientAttrib** não são compiladas em listas de exibição, mas são executadas imediatamente.

As **funções glPushClientAttrib** e **glPopClientAttrib** só podem usar os modos de armazenamento de pixel pop e push e estados de cliente da matriz de vértices. Você deve usar [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) para efetuar push e pop de estados que são mantidos no servidor.

> [!Note]  
> As **funções glPushClientAttrib** e **glPopClientAttrib** só estão disponíveis no OpenGL versão 1.1 ou posterior.

 

As seguintes funções recuperam informações relacionadas **a glPushClientAttrib** e **glPopClientAttrib**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CLIENT \_ ATTRIB \_ STACK \_ DEPTH

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ MAX CLIENT \_ \_ ATTRIB STACK \_ \_ DEPTH

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





