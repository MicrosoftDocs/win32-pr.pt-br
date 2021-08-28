---
title: Função glGetMaterialfv (Gl.h)
description: As funções glGetMaterialfv e glGetMaterialiv retornam parâmetros de material. | Função glGetMaterialfv (Gl.h)
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
keywords:
- Função glGetMaterialfv OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261c8e587b3bc339365d6c1d490bec6b2d9c27c9c4531e08dd1546ee8849baac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741366"
---
# <a name="glgetmaterialfv-function"></a>Função glGetMaterialfv

As **funções glGetMaterialfv** e [**glGetMaterialiv**](glgetmaterialiv.md) retornam parâmetros de material.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetMaterialfv(
   GLenum  face,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cara* 
</dt> <dd>

Especifica qual dos dois materiais está sendo consultado. GL \_ FRONT ou GL BACK são \_ aceitos, representando os materiais frontal e voltar, respectivamente.

</dd> <dt>

*Pname* 
</dt> <dd>

O parâmetro de material a ser retornada. Os valores a seguir são aceitos.



| Valor                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                    | O *parâmetro params* retorna quatro valores inteiros ou de ponto flutuante que representam a reflexão de ambiente do material. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interno, de modo que 1.0 mapeia para o valor inteiro representável mais positivo e -1,0 é mapeado para o valor inteiro representável mais negativo. Se o valor interno estiver fora do intervalo -1,1 , o valor de retorno de inteiro \[ \] correspondente será indefinido.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFUSO**</dt> </dl>                    | O *parâmetro params* retorna quatro valores inteiros ou de ponto flutuante que representam a reflexão difusa do material. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interno, de modo que 1.0 mapeia para o valor inteiro representável mais positivo e -1,0 é mapeado para o valor inteiro representável mais negativo. Se o valor interno estiver fora do intervalo -1,1 , o valor de retorno de inteiro \[ \] correspondente será indefinido.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                 | O *parâmetro params* retorna quatro valores inteiros ou de ponto flutuante que representam a reflexão especular do material. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interno, de modo que 1.0 mapeia para o valor inteiro representável mais positivo e -1,0 é mapeado para o valor inteiro representável mais negativo. Se o valor interno estiver fora do intervalo -1,1 , o valor de retorno de inteiro \[ \] correspondente será indefinido.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**GL \_ EMISSION**</dt> </dl>                 | O *parâmetro params* retorna quatro valores inteiros ou de ponto flutuante que representam a intensidade de luz emitida do material. Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interno, de modo que 1.0 mapeia para o valor inteiro representável mais positivo e -1,0 é mapeado para o valor inteiro representável mais negativo. Se o valor interno estiver fora do intervalo -1,1 , o valor de retorno de inteiro \[ \] correspondente será indefinido.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GLINESS**</dt> </dl>              | O *parâmetro params* retorna um inteiro ou um valor de ponto flutuante que representa o expoente especular do material. Os valores inteiros, quando solicitados, são calculados arredondando o valor de ponto flutuante interno para o valor inteiro mais próximo.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**ÍNDICES \_ DE \_ CORES GL**</dt> </dl> | O *parâmetro params* retorna três valores inteiros ou de ponto flutuante que representam os índices de ambiente, difuso e especular do material. Use esses índices somente para iluminação de índice de cores. (Os outros parâmetros são todos usados apenas para iluminação RGBA.) Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para os valores inteiros mais próximos.<br/>                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* ou *query* não era um valor aceito.<br/>                                                                             |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glGetMaterial** retorna *em parâmetros* o valor ou os valores do *parâmetro pname* da face do *material.*

Se um erro for gerado, nenhuma alteração será feita no conteúdo *de params*.

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

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





