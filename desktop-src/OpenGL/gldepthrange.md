---
title: função glDepthRange (GL. h)
description: A função glDepthRange especifica o mapeamento de valores z de coordenadas de dispositivo normalizadas para coordenadas de janela.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- função glDepthRange OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac72155449e70a59265e4ffd2576245059a547906092df2a932e84f221e48fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081646"
---
# <a name="gldepthrange-function"></a>função glDepthRange

A função **glDepthRange** especifica o mapeamento de valores *z* de coordenadas de dispositivo normalizadas para coordenadas de janela.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*zNear* 
</dt> <dd>

O mapeamento do plano de recorte Near para as coordenadas da janela. O valor padrão é zero.

</dd> <dt>

*zFar* 
</dt> <dd>

O mapeamento do plano de recorte distante para as coordenadas da janela. O valor padrão é 1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Após recorte e divisão por *w*, as coordenadas *z* variam de 0,0 a 1,0, correspondentes aos planos de recorte próximo e longe. A função **glDepthRange** especifica um mapeamento linear das coordenadas *z* normalizadas neste intervalo para coordenadas *z* de janela. Independentemente da implementação do buffer de profundidade real, os valores de profundidade de janela de coordenadas são tratados como se estivessem de 0,0 a 1,0 (como componentes de cores). Assim, os valores aceitos por **glDepthRange** são clamped para esse intervalo antes de serem aceitos.

O mapeamento padrão de (0, 1) mapeia o plano próximo para 0 e o plano distante para 1. Com esse mapeamento, o intervalo de buffer de profundidade é totalmente utilizado.

Não é necessário que *zNear* seja menor que *zFar*. Mapeamentos inversos como (1, 0) são aceitáveis.

A função a seguir recupera informações relacionadas a **glDepthRange**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com intervalo de profundidade do argumento GL \_ \_

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





