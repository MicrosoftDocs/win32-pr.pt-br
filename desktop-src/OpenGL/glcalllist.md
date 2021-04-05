---
title: função glCallList (GL. h)
description: A função glCallList executa uma lista de exibição.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- função glCallList OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085706"
---
# <a name="glcalllist-function"></a>função glCallList

A função **glCallList** executa uma lista de exibição.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*list* 
</dt> <dd>

O nome inteiro da lista de exibição a ser executada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Invocar a função **glCallList** começa a execução da lista de exibição nomeada. As funções salvas na lista de exibição são executadas na ordem, assim como se você as chamou sem usar uma lista de exibição. Se a *lista* não tiver sido definida como uma lista de exibição, **glCallList** será ignorado.

A função **glCallList** pode aparecer dentro de uma lista de exibição. Para evitar a possibilidade de recursão infinita resultante de listas de exibição chamando uma outra, um limite é colocado no nível de aninhamento das listas de exibição durante a execução da lista de exibição. No entanto, esse limite é pelo menos 64, dependendo da implementação.

O estado OpenGL não é salvo e restaurado em uma chamada para **glCallList**. Assim, as alterações feitas no estado OpenGL durante a execução de uma lista de exibição permanecem depois que a execução da lista de exibição é concluída. Para preservar o estado do OpenGL entre chamadas **glCallList** , use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md).

Você pode executar listas de exibição entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md), desde que a lista de exibição inclua apenas funções que são permitidas nesse intervalo.

As funções a seguir recuperam informações relacionadas ao **glCallList**:

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ aninhamento de lista de glGet com Argument GL Max \_

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

[**glCallLists**](glcalllists.md)
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

 

 





