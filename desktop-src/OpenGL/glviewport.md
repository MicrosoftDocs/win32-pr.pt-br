---
title: função glViewport (GL. h)
description: A função glViewport define o visor.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- função glViewport OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104570400"
---
# <a name="glviewport-function"></a>função glViewport

A função **glViewport** define o visor.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

O canto inferior esquerdo do retângulo do visor, em pixels. O padrão é (0, 0).

</dd> <dt>

*y* 
</dt> <dd>

O canto inferior esquerdo do retângulo do visor, em pixels. O padrão é (0, 0).

</dd> <dt>

*width* 
</dt> <dd>

A largura do visor. Quando um contexto OpenGL é anexado pela primeira vez a uma janela, a *largura* e a *altura* são definidas para as dimensões dessa janela.

</dd> <dt>

*altura* 
</dt> <dd>

A altura do visor. Quando um contexto OpenGL é anexado pela primeira vez a uma janela, a *largura* e a *altura* são definidas para as dimensões dessa janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | A *largura* ou a *altura* era negativa.<br/>                                                                                   |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glViewport** especifica a transformação afim de *x* e *y* de coordenadas de dispositivo normalizadas para coordenadas de janela. Deixe que (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) sejam coordenadas de dispositivo normalizadas. As coordenadas da janela (*x*<sub>w</sub> , *y*<sub>w</sub> ) são computadas da seguinte maneira:

![Equação mostrando a computação das coordenadas da janela.](images/view01.png)

A largura e a altura do visor são silenciosamente clamped a um intervalo que depende da implementação. Esse intervalo é consultado chamando **glGet** com o argumento GL \_ Max \_ viewport \_ esmaece.

As funções a seguir recuperam informações relacionadas ao **glViewport**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com visor do Argument GL \_

**glGet** com Argument GL \_ Max \_ viewport \_ escurece

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

[**glDepthRange**](gldepthrange.md)
</dt> </dl>

 

 





