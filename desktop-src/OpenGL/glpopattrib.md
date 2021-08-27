---
title: Função glPopAttrib (Gl.h)
description: A pilha de atributos é pop-pop.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- Função glPopAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92034154138ab3747ce190c05716e2df0d82ed3f6b26aba38da780873ce03721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081446"
---
# <a name="glpopattrib-function"></a>Função glPopAttrib

A pilha de atributos é pop-pop.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | A função foi chamada enquanto a pilha de atributos estava vazia.<br/>                                                               |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A [**função glPushAttrib**](glpushattrib.md) aceita um argumento, uma máscara que indica quais grupos de variáveis de estado salvar na pilha de atributos. Constantes simbólicas são usadas para definir bits na máscara. O parâmetro mask normalmente é construído por **OR** ing várias dessas constantes juntas. A máscara especial GL \_ ALL \_ ATTRIB \_ BITS pode ser usada para salvar todos os estados empilhados.

A **função glPopAttrib** restaura os valores das variáveis de estado salvas com o último [**comando glPushAttrib.**](glpushattrib.md) Aqueles não salvos são deixados inalterados.

É um erro fazer push de atributos para uma pilha completa ou para pop-off de atributos de uma pilha vazia. Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.

Inicialmente, a pilha de atributos está vazia.

Nem todos os valores para o estado OpenGL podem ser salvos na pilha de atributos. Por exemplo, o estado do pacote de pixels e desempacotar, o estado do modo de renderização e selecionar e o estado de comentários não podem ser salvos.

A profundidade da pilha de atributos depende da implementação, mas deve ser pelo menos 16.

As funções a seguir recuperam informações relacionadas [**a glPushAttrib**](glpushattrib.md) e **glPopAttrib**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ ATTRIB \_ STACK \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAX \_ ATTRIB \_ STACK \_ DEPTH

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





