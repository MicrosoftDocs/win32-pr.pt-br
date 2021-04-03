---
title: função glLineStipple (GL. h)
description: A função glLineStipple especifica o padrão de linha Stipple.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- função glLineStipple OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644224"
---
# <a name="gllinestipple-function"></a>função glLineStipple

A função **glLineStipple** especifica o padrão de linha Stipple.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*multi-fator* 
</dt> <dd>

Um multiplicador para cada bit no padrão de linha Stipple. Se o *fator* for 3, por exemplo, cada bit no padrão será usado três vezes antes de o próximo bit no padrão ser usado. O parâmetro *factor* é clamped para o intervalo de \[ 1, 256 \] e, por padrão, é um.

</dd> <dt>

*padrão* 
</dt> <dd>

Um inteiro de 16 bits cujo padrão de bit determina quais fragmentos de uma linha serão desenhados quando a linha for rasterizada. O bit zero é usado primeiro e o padrão padrão é todos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glLineStipple** especifica o padrão de linha Stipple. A linha stippling mascara alguns fragmentos produzidos pela rasterização; esses fragmentos não serão desenhados. O mascaramento é obtido usando três parâmetros: o *padrão* de Stipple de linha de 16 bits, o *fator* de contagem de repetição e um número inteiro de Stipple contador *s*.

O contador *s* é redefinido para zero sempre que [**glBegin**](glbegin.md) é chamado e antes de cada segmento de linha de uma sequência de **glBegin**( \_ linhas GL)/**glEnd** ser gerada. Ele é incrementado após a geração *de cada fragmento* de um segmento de linha com alias de largura de unidade, ou após cada um dos fragmentos de um segmento de linha *de largura,* são gerados. Os fragmentos de *i* associados à contagem *s* são mascarados se o bit (*s* factor) do *padrão*  /  mod 16 for zero. Caso contrário, esses fragmentos serão enviados para o framebuffer. O bit zero do *padrão* é o bit menos significativo.

Linhas AntiAlias são tratadas como uma sequência de retângulos de *largura* 1x para fins de stippling. Os *s* de retângulo são rasterizados ou não com base na regra de fragmento descrita para linhas com alias; Ele conta retângulos em vez de grupos de fragmentos.

A linha stippling é habilitada ou desabilitada usando [**glEnable**](glenable.md) e **glDisable** com a linha de argumento GL \_ \_ STIPPLE. Quando habilitado, o padrão de linha Stipple é aplicado conforme descrito acima. Quando desabilitado, é como se o padrão fosse todos. Inicialmente, a linha stippling está desabilitada.

As funções a seguir recuperam informações relacionadas ao **glLineStipple**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com \_ \_ STIPPLE padrão de linha de argumento GL \_

**glGet** com Argument GL \_ linha \_ STIPPLE \_ REPEAT

[**glIsEnabled**](glisenabled.md) com o argumento GL \_ linha \_ STIPPLE

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

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





