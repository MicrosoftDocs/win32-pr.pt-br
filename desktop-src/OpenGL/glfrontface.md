---
title: função glFrontFace (GL. h)
description: A função glFrontFace define polígonos de front-face e voltados para o verso.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- função glFrontFace OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d288b4e6380ab845af9a05381963444e28ddf50739ecd3f5563d9f2dc729fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580156"
---
# <a name="glfrontface-function"></a>função glFrontFace

A função **glFrontFace** define polígonos de front-face e voltados para o verso.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

A orientação dos polígonos front-face. O GL \_ CW e o GL \_ CCW são aceitos. O valor padrão é GL \_ CCW.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Em uma cena composta inteiramente de superfícies fechadas opacas, polígonos voltados nunca são visíveis. A eliminação desses polígonos invisíveis tem o benefício óbvio de acelerar a renderização da imagem. Você habilita e desabilita a eliminação de polígonos voltados com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) usando o tipo de seleção Argument GL \_ \_ .

A projeção de um polígono para as coordenadas da janela é indicada para ter o enrolamento no sentido horário se um objeto imaginário após o caminho de seu primeiro vértice, seu segundo vértice e assim por diante, para seu último vértice e, finalmente, voltar ao seu primeiro vértice, se mover em uma direção no sentido horário sobre o interior do polígono. O enrolamento do polígono é considerado no sentido anti-horário se o objeto imaginário após o mesmo caminho se mover em uma direção no sentido anti-horário sobre o interior do polígono. A função **glFrontFace** especifica se polígonos com o enrolamento no sentido horário nas coordenadas da janela ou o retrocesso anti-horário nas coordenadas da janela são levados para ser front-face. Passar \_ o GL CCW para o *modo* seleciona polígonos no sentido anti-horário como front-face; O GL em \_ PV seleciona polígonos no sentido horário como front-face. Por padrão, polígonos no sentido anti-horário são levados a voltar para a frente.

A função a seguir recupera informações sobre **glFrontface**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a \_ face frontal do Argument GL \_

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

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





