---
title: Função glMaterialiv (Gl.h)
description: A função glMaterialiv especifica parâmetros de material para o modelo de iluminação.
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
keywords:
- Função glMaterialfv OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 922fd0cd90b848f0d5c324451f502faa8fa6b961686b209cb881c752b992a6df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128206"
---
# <a name="glmaterialiv-function"></a>Função glMaterialiv

A **função glMaterialiv** especifica parâmetros de material para o modelo de iluminação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMaterialfv(
         GLenum face,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cara* 
</dt> <dd>

O rosto ou rostos que estão sendo atualizados. Deve ser um dos seguintes: GL \_ FRONT, GL \_ BACK ou GL FRONT e GL \_ \_ BACK.

</dd> <dt>

*Pname* 
</dt> <dd>

O parâmetro material da face ou faces que está sendo atualizada. Os parâmetros que podem ser especificados usando [**glMaterialiv**](glmaterialfv.md)e suas interpretações pela equação de iluminação são os a seguir.



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                       | O parâmetro params contém quatro valores inteiros que especificam a reflexão RGBA do material de ambiente. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para -1,0. Os valores de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. A refleção de ambiente padrão para materiais voltados para frente e para trás é (0,2, 0,2, 0,2, 1.0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFUSO**</dt> </dl>                                       | O parâmetro params contém quatro valores inteiros que especificam a reflexão RGBA difusa do material. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para -1,0. Os valores de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. A refleção difusa padrão para materiais voltados para frente e para trás é (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                    | O parâmetro params contém quatro valores inteiros que especificam a reflexão RGBA especular do material. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para -1,0. Os valores de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. A reflexão especular padrão para materiais voltados para frente e para trás é (0,0, 0,0, 0,0, 1,0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**GL \_ EMISSION**</dt> </dl>                                    | O parâmetro params contém quatro valores inteiros que especificam a intensidade de luz emitida pelo RGBA do material. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para -1,0. Os valores de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. A intensidade de emissão padrão para materiais voltados para frente e para trás é (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GLINESS**</dt> </dl>                                 | O *parâmetro param* é um único inteiro que especifica o expoente especular RGBA do material. Os valores inteiros são mapeados diretamente. Somente valores no intervalo \[ 0, 128 \] são aceitos. O expoente especular padrão para materiais voltados para frente e para trás é 0. <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**AMBIENTE \_ GL \_ E \_ DIFUSO**</dt> </dl> | Equivalente a chamar [**glMaterial**](glmaterial-functions.md) duas vezes com os mesmos valores de parâmetro, uma vez com GL \_ AMBIENT e uma vez com GL \_ DIFFUSE. <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**ÍNDICES \_ DE \_ CORES GL**</dt> </dl>                    | O parâmetro params contém três valores inteiros que especificam os índices de cores para iluminação ambiente, difusa e especular. Esses três valores, e GLLUMININESS, são os únicos valores de material usados pela equação de iluminação do modo de \_ índice de cor. Consulte [**glLightModel para**](gllightmodel-functions.md) ver uma discussão sobre iluminação de índice de cores.<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

O valor para o qual o parâmetro GL \_ GLINESS será definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                              | Significado                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | Face *ou* *pname* não era um valor aceito.<br/>                |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl> | Um expoente especular fora do intervalo de \[ 0, 128 \] foi especificado.<br/> |



## <a name="remarks"></a>Comentários

A [**função glMaterialiv**](glmaterialf.md) atribui valores a parâmetros de material. Há dois conjuntos de parâmetros de material. Um,  o conjunto voltado para a frente, é usado para sombrear pontos, linhas, bitmaps e todos os polígonos (quando a iluminação de dois lados está desabilitada) ou apenas polígonos voltados para a frente (quando a iluminação de dois lados está habilitada). O outro conjunto, *voltado para trás,* é usado para sombrear polígonos voltados para trás somente quando a iluminação de dois lados está habilitada. Consulte [**glLightModel para**](gllightmodel-functions.md) obter detalhes sobre cálculos de iluminação de um lado e dois lados.

A [**função glMaterialiv**](glmaterialf.md) recebe três argumentos. O primeiro, *face*, especifica se os materiais GL FRONT, os materiais GL BACK ou os materiais \_ GL FRONT E BACK serão \_ \_ \_ \_ modificados. O segundo, *pname*, especifica qual dos vários parâmetros em um ou em ambos os conjuntos será modificado. O terceiro, *param*, especifica qual valor será atribuído ao parâmetro especificado.

Parâmetros de material são usados na equação de iluminação que é opcionalmente aplicada a cada vértice. A equação é discutida em [**glLightModel.**](gllightmodel-functions.md)

Os parâmetros de material podem ser atualizados a qualquer momento. Em particular, [**glMaterialiv**](glmaterialf.md) pode ser chamado entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md) No entanto, se apenas um único parâmetro de material for alterado por vértice, [**glColorMaterial**](glcolormaterial.md) será preferencial em vez de **glMaterialiv.**

A função a seguir recupera informações relacionadas a [**glMaterialiv**](glmaterialf.md):

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





