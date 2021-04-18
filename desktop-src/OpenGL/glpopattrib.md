---
title: função glPopAttrib (GL. h)
description: Exibe a pilha de atributos.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- função glPopAttrib OpenGL
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
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771834"
---
# <a name="glpopattrib-function"></a>função glPopAttrib

Exibe a pilha de atributos.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_estouro negativo de pilha GL \_**</dt> </dl>   | A função foi chamada enquanto a pilha de atributos estava vazia.<br/>                                                               |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função [**glPushAttrib**](glpushattrib.md) usa um argumento, uma máscara que indica quais grupos de variáveis de estado salvar na pilha de atributos. As constantes simbólicas são usadas para definir os bits na máscara. O parâmetro Mask normalmente é construído por **ou** em várias dessas constantes juntas. A máscara especial GL \_ todos \_ os \_ bits de Atrib. pode ser usada para salvar todos os Estados empilháveis.

A função **glPopAttrib** restaura os valores das variáveis de estado salvas com o último comando [**glPushAttrib**](glpushattrib.md) . Aqueles não salvos são deixados inalterados.

É um erro enviar atributos por push para uma pilha completa ou para os atributos pop de uma pilha vazia. Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.

Inicialmente, a pilha de atributos está vazia.

Nem todos os valores para o estado OpenGL podem ser salvos na pilha de atributos. Por exemplo, o pacote de pixel e o estado de desempacotamento, estado do modo de renderização e estado de comentários e de seleção não podem ser salvos.

A profundidade da pilha de atributos depende da implementação, mas deve ser pelo menos 16.

As funções a seguir recuperam informações relacionadas a [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**:

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) profundidade de pilha de Atrib glGet com Argument GL \_ \_ \_

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ profundidade máxima de pilha de \_ ATRIB \_ glGet com Argument GL \_

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

 

 





