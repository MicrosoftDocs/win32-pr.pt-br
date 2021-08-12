---
title: Função glClipPlane (Gl.h)
description: A função glClipPlane especifica um plano no qual toda a geometria é recortada.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- Função glClipPlane OpenGL
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
ms.openlocfilehash: cb55edd88b8c8dcd6b4481e60dfc05a012bb79f4f484fde8987e9ed23239d837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618036"
---
# <a name="glclipplane-function"></a>Função glClipPlane

A **função glClipPlane** especifica um plano no qual toda a geometria é recortada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*avião* 
</dt> <dd>

O plano de recorte que está sendo posicionado. Nomes simbólicos do formato GL CLIP PLANE i , em que i é um inteiro entre 0 e \_ GL MAX CLIP PLANE - \_   \_ \_ \_ 1, são aceitos.

</dd> <dt>

*Equação* 
</dt> <dd>

O endereço de uma matriz de quatro valores de ponto flutuante de precisão dupla. Esses valores são interpretados como uma equação de plano.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *plane* não era um valor aceito.<br/>                                                                                         |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A geometria sempre é recortada nos limites de um frustum de seis plano *em x*, *y* e *z*. A **função glClipPlane** permite a especificação de planos adicionais, não necessariamente ao eixo *x,* *eixo y* ou eixo *z,* em relação ao qual toda a geometria é recortada. Até planos GL MAX CLIP PLANES podem ser especificados, em que GL MAX CLIP PLANES tem pelo menos \_ seis em todas as \_ \_ \_ \_ \_ implementações. Como a região de recorte resultante é a interseção dos espaços-metade definidos, ela é sempre convexa.

A **função glClipPlane** especifica um meio espaço usando uma equação de plano de quatro componentes. Quando você chama **glClipPlane,***a* equação é transformada pelo inverso da matriz modelview e armazenada nas coordenadas de olho resultantes. As alterações subsequentes na matriz modelview não têm efeito sobre os componentes armazenados da equação do plano. Se o produto de ponto das coordenadas de olho de um vértice com os componentes da equação do plano armazenado for positivo ou zero, o vértice será em relação a esse plano de recorte. Caso contrário, ele está fora.

Use as [**funções glEnable**](glenable.md) e [**glDisable**](gldisable.md) para habilitar e desabilitar planos de recorte. Chame planos de recorte com o argumento GL \_ CLIP PLANE i , em que i \_ *é* o número do plano.

Por padrão, todos os planos de recorte são definidos como (0,0,0,0) em coordenadas de olho e são desabilitados.

É sempre o caso de GL \_ CLIP \_ PLANE *i* = GL \_ CLIP \_ PLANE0 + *i*.

As funções a seguir recuperam informações relacionadas **a glClipPlane:**

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ CLIP PLANE \_ *i*

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

 

 





