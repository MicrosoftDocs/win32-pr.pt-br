---
title: Função glPushClientAttrib (Gl.h)
description: As funções glPushClientAttrib e glPopClientAttrib salvam e restauram grupos de variáveis de estado do cliente na pilha cliente-atributo. | Função glPushClientAttrib (Gl.h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- Função glPushClientAttrib OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f378ec3ff735ed916567ea91e211a1d8a1685580b1f1ea80d448b92203b39a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492606"
---
# <a name="glpushclientattrib-function"></a>Função glPushClientAttrib

As **funções glPushClientAttrib** e [**glPopClientAttrib**](glpopclientattrib.md) salvam e restauram grupos de variáveis de estado do cliente na pilha cliente-atributo.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mask* 
</dt> <dd>

Uma máscara que indica quais atributos salvar. A seguir estão as constantes de máscara simbólica e seus estados de cliente OpenGL associados.



| Valor                                                                                                                                                                                                                                            | Significado                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <dt>**BIT DO \_ \_ ARMAZENAMENTO DE \_ PIXELS DO \_ CLIENTE GL**</dt> </dl>                                             | Atributos de modo de armazenamento de pixel.<br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <dt>**BIT DA \_ MATRIZ \_ DE VÉRTICE \_ DO \_ CLIENTE GL**</dt> </dl>                                          | Atributos de matriz de vértice.<br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <dt>**GL \_ CLIENT \_ ALL \_ ATTRIB \_ BITs**</dt> </dl> | todos os atributos de estado do cliente que podem ser empilhados.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                               | Significado                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl> | A função foi chamada enquanto a pilha cliente-atributo estava cheia.<br/> |



## <a name="remarks"></a>Comentários

A **função glPushClientAttrib** usa seu parâmetro mask para determinar quais grupos de variáveis de estado do cliente são salvos na pilha cliente-atributo. Você pode usar o operador OR bit a bit para unir constantes simbólicas aceitas para definir bits e construir uma máscara.

A [**função glPopClientAttrib restaura**](glpopclientattrib.md) os valores das variáveis de estado do cliente salvas pela última vez com **glPushclientAttrib**. As variáveis de estado do cliente não salvas anteriormente são deixadas inalteradas. Efetuar o esmaeamento de atributos para uma pilha de atributo de cliente completa ou a ressarção de atributos de uma pilha vazia define um sinalizador de erro e nenhuma outra alteração é feita no estado OpenGL. Por padrão, a pilha de atributos do cliente está vazia.

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

 

 





