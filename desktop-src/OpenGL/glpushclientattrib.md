---
title: função glPushClientAttrib (GL. h)
description: As funções glPushClientAttrib e glPopClientAttrib salvam e restauram grupos de variáveis de estado do cliente na pilha de atributos do cliente. | função glPushClientAttrib (GL. h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- função glPushClientAttrib OpenGL
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
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298405"
---
# <a name="glpushclientattrib-function"></a>função glPushClientAttrib

As funções **glPushClientAttrib** e [**glPopClientAttrib**](glpopclientattrib.md) salvam e restauram grupos de variáveis de estado do cliente na pilha de atributos do cliente.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mascara* 
</dt> <dd>

Uma máscara que indica quais atributos salvar. A seguir estão as constantes de máscara simbólica e seus Estados de cliente OpenGL associados.



| Valor                                                                                                                                                                                                                                            | Significado                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <dt>**\_bit GL Client \_ pixel \_ Store \_**</dt> </dl>                                             | Atributos do modo de armazenamento de pixel.<br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <dt>**\_bit de \_ matriz de vértices do cliente GL \_ \_**</dt> </dl>                                          | Atributos de matriz de vértice.<br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <dt>**\_Cliente GL \_ todos \_ os \_ bits de Atrib.**</dt> </dl> | todos os atributos de estado do cliente empilháveis.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                               | Significado                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_estouro de pilha GL \_**</dt> </dl> | A função foi chamada enquanto a pilha de atributo de cliente estava cheia.<br/> |



## <a name="remarks"></a>Comentários

A função **glPushClientAttrib** usa seu parâmetro Mask para determinar quais grupos de variáveis de estado do cliente são salvos na pilha de atributos do cliente. Você pode usar o operador OR bit a bit para unir constantes simbólicas aceitas para definir bits e construir uma máscara.

A função [**glPopClientAttrib**](glpopclientattrib.md) restaura os valores das variáveis de estado do cliente salvas pela última vez com **glPushclientAttrib**. As variáveis de estado do cliente não salvas anteriormente permanecem inalteradas. Enviar atributos por push para uma pilha completa do atributo do cliente ou remover atributos de uma pilha vazia define um sinalizador de erro e nenhuma outra alteração é feita no estado OpenGL. Por padrão, a pilha de atributos do cliente está vazia.

Alguns valores de estado do cliente OpenGL não podem ser salvos na pilha de atributos do cliente. Por exemplo, você não pode salvar os Estados SELECT ou feedback na pilha de atributos do cliente. A profundidade da pilha de atributos de cliente é pelo menos 16.

As funções **glPushclientAttrib** e **glPopClientAttrib** não são compiladas em listas de exibição, mas são executadas imediatamente.

As funções **glPushClientAttrib** e **glPopClientAttrib** podem apenas enviar por push e pop-up modos de armazenamento de pixel e Estados de cliente de matriz de vértice. Você deve usar [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) para enviar e pop os Estados que são mantidos no servidor.

> [!Note]  
> As funções **glPushClientAttrib** e **glPopClientAttrib** só estão disponíveis no OpenGL versão 1,1 ou posterior.

 

As funções a seguir recuperam informações relacionadas a **glPushClientAttrib** e **glPopClientAttrib**:

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) profundidade de pilha de \_ Atrib de cliente GLGET com Argument GL \_ \_ \_

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ profundidade máxima de pilha de \_ \_ Atrib de \_ cliente \_ glGet com Argument GL

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

 

 





