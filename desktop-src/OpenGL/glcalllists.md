---
title: função glCallLists (GL. h)
description: A função glCallLists executa uma lista de listas de exibição.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- função glCallLists OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e15c382b23558786443f03f57349b2504ad251301e3e195885e276d7dbebe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082106"
---
# <a name="glcalllists-function"></a>função glCallLists

A função **glCallLists** executa uma lista de listas de exibição.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

O número de listas de exibição a serem executadas.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de valores em *listas*. As constantes simbólicas a seguir são aceitas.



| Valor                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_byte GL**</dt> </dl>                                | O parâmetro *Lists* é tratado como uma matriz de bytes assinados, cada um no intervalo de-128 a 127.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte não assinado GL \_**</dt> </dl>    | O parâmetro *Lists* é tratado como uma matriz de bytes não assinados, cada um no intervalo de 0 a 255.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ curto**</dt> </dl>                             | O parâmetro *Lists* é tratado como uma matriz de inteiros de 2 bytes assinados, cada um no intervalo de-32768 a 32767.<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ não assinado \_ curto**</dt> </dl> | O parâmetro *Lists* é tratado como uma matriz de inteiros de 2 bytes não assinados, cada um no intervalo de 0 a 65535.<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**RAZÃO \_ int**</dt> </dl>                                   | O parâmetro *Lists* é tratado como uma matriz de inteiros de 4 bytes assinados.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ não assinado \_ int**</dt> </dl>       | O parâmetro *Lists* é tratado como uma matriz de inteiros de 4 bytes sem sinal.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ float**</dt> </dl>                             | O parâmetro *Lists* é tratado como uma matriz de valores de ponto flutuante de 4 bytes.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ bytes**</dt> </dl>                      | O parâmetro *Lists* é tratado como uma matriz de bytes não assinados. Cada par de bytes especifica um único nome de lista de exibição. O valor do par é calculado como 256 vezes o valor não assinado do primeiro byte mais o valor não assinado do segundo byte.<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL \_ 3 \_ bytes**</dt> </dl>                      | O parâmetro *Lists* é tratado como uma matriz de bytes não assinados. Cada terceto de bytes especifica um único nome de lista de exibição. O valor de terceto é calculado como 65536 vezes o valor não assinado do primeiro byte, além de 256 vezes o valor não assinado do segundo byte, mais o valor não assinado do terceiro byte.<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**GL \_ 4 \_ bytes**</dt> </dl>                      | O parâmetro *Lists* é tratado como uma matriz de bytes não assinados. Cada quadruplet de bytes especifica um único nome de lista de exibição. O valor de quadruplet é computado como 16777216 vezes o valor não assinado do primeiro byte, além de 65536 vezes o valor não assinado do segundo byte, além de 256 vezes o valor não assinado do terceiro byte, mais o valor não assinado do quarto byte.<br/> |



 

</dd> <dt>

*lista* 
</dt> <dd>

O endereço de uma matriz de deslocamentos de nome na lista de exibição. O tipo de ponteiro é void porque os deslocamentos podem ser bytes, short, ints ou floats, dependendo do valor do *tipo*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glCallLists** faz com que cada lista de exibição na lista de nomes seja passada como *listas* a serem executadas. Como resultado, as funções salvas em cada lista de exibição são executadas em ordem, assim como se elas fossem chamadas sem usar uma lista de exibição. Os nomes das listas de exibição que não foram definidas são ignorados.

A função **glCallLists** fornece um meio eficiente para executar listas de exibição. O parâmetro *n* especifica o número de listas com vários formatos de nome (especificados pelo parâmetro de *tipo* ) **glCallLists** executado.

A lista de nomes de listas de exibição não é terminada em nulo. Em vez disso, *n* especifica quantos nomes devem ser obtidos de *listas*.

A função [**glListBase**](gllistbase.md) torna um nível adicional de indireção disponível. A função **glListBase** especifica um deslocamento não assinado que é adicionado a cada nome de lista de exibição especificado em *listas* antes que a lista de exibição seja executada.

A função **glCallLists** pode aparecer dentro de uma lista de exibição. Para evitar a possibilidade de recursão infinita resultante de listas de exibição chamando uma outra, um limite é colocado no nível de aninhamento das listas de exibição durante a execução da lista de exibição. Esse limite deve ser pelo menos 64 e depende da implementação.

O estado OpenGL não é salvo e restaurado em uma chamada para **glCallLists**. Assim, as alterações feitas no estado OpenGL durante a execução das listas de exibição permanecem após a conclusão da execução. Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md) para preservar o estado do OpenGL entre chamadas de **glCallLists** .

Você pode executar listas de exibição entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md), desde que a lista de exibição inclua apenas funções que são permitidas nesse intervalo.

As funções a seguir recuperam informações relacionadas à função **glCallLists** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com base de lista de argumentos GL \_ \_

 \_ \_ aninhamento de lista de glGet com Argument GL Max \_

[**glIsList**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glListBase**](gllistbase.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





