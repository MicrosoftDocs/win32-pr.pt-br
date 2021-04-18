---
title: função glClipPlane (GL. h)
description: A função glClipPlane especifica um plano no qual toda a geometria é recortada.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- função glClipPlane OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760222"
---
# <a name="glclipplane-function"></a>função glClipPlane

A função **glClipPlane** especifica um plano no qual toda a geometria é recortada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*aérea* 
</dt> <dd>

O plano de recorte que está sendo posicionado. Os nomes simbólicos da forma GL o \_ clip do \_ plano *i*, onde *eu* é um inteiro entre 0 e GL o \_ máximo \_ de recortes \_ de clipe-1, são aceitos.

</dd> <dt>

*subscrito* 
</dt> <dd>

O endereço de uma matriz de quatro valores de ponto flutuante de precisão dupla. Esses valores são interpretados como uma equação de plano.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *plano* não era um valor aceito.<br/>                                                                                         |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A geometria é sempre recortada em relação aos limites de um frustum de seis planos em *x*, *y* e *z*. A função **glClipPlane** permite a especificação de planos adicionais, não necessariamente perpendicular ao eixo *x*, eixo *y* ou eixo *z*, em relação ao qual toda a geometria é recortada. Até o GL \_ máximo \_ , os planos de planos de corte \_ podem ser especificados, onde o GL \_ Max \_ recortes \_ é pelo menos seis em todas as implementações. Como a região de recorte resultante é a interseção dos espaços de meia definição, ela é sempre convexa.

A função **glClipPlane** especifica um meio-espaço usando uma equação de plano de quatro componentes. Quando você chama **glClipPlane**, a *equação* é transformada pelo inverso da matriz modelview e armazenada nas coordenadas de olho resultante. As alterações subsequentes na matriz modelview não têm efeito sobre os componentes de equação de plano armazenado. Se o produto de ponto das coordenadas de olho de um vértice com os componentes da equação do plano armazenado for positivo ou zero, o vértice estará em relação a esse plano de recorte. Caso contrário, ele está fora.

Use as funções [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) para habilitar e desabilitar planos de recorte. Chame os planos de recorte com o argumento GL de \_ clipe \_ *i*, onde é o número do plano. 

Por padrão, todos os planos de recorte são definidos como (0, 0, 0, 0) em coordenadas de olho e estão desabilitados.

É sempre o caso que o GL \_ clip \_ avião *i* = GL \_ clip \_ PLANE0 + *i*.

As funções a seguir recuperam informações relacionadas ao **glClipPlane**:

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled**](glisenabled.md) com Argument GL \_ clip \_ avião *i*

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





