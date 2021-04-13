---
title: função glMaterialfv (GL. h)
description: A função glMaterialfv especifica os parâmetros materiais para o modelo de iluminação.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- função glMaterialfv OpenGL
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
ms.openlocfilehash: b44b200abe0588a657f770902a9a897329e1942a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369208"
---
# <a name="glmaterialfv-function"></a>função glMaterialfv

A função **glMaterialfv** especifica os parâmetros materiais para o modelo de iluminação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sorridente* 
</dt> <dd>

A face ou faces que estão sendo atualizadas. Deve ser um dos seguintes: GL \_ frontal, GL \_ voltar ou GL \_ front e GL de \_ volta.

</dd> <dt>

*pname* 
</dt> <dd>

O parâmetro material da face ou faces sendo atualizadas. Os parâmetros que podem ser especificados usando **glMaterialfv** e suas interpretações pela equação de iluminação são os seguintes.



| Valor                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**\_ambiente GL**</dt> </dl>                                       | O parâmetro params contém quatro valores de ponto flutuante que especificam a reflexão de RGBA de ambiente do material. Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0. Os valores de ponto flutuante são mapeados diretamente. Nenhum valor inteiro nem de ponto flutuante são clamped. A reflexão de ambiente padrão para os materiais voltados para frente e para trás é (0,2, 0,2, 0,2, 1,0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**\_difusão GL**</dt> </dl>                                       | O parâmetro params contém quatro valores de ponto flutuante que especificam a reflexão da difusão de RGBA do material. Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0. Os valores de ponto flutuante são mapeados diretamente. Nenhum valor inteiro nem de ponto flutuante são clamped. A reflexão difusa padrão para os materiais voltados para frente e para trás é (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_ESPECULA GL**</dt> </dl>                                    | O parâmetro params contém quatro valores de ponto flutuante que especificam a reflexão de RGBA de especulação do material. Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0. Os valores de ponto flutuante são mapeados diretamente. Nenhum valor inteiro nem de ponto flutuante são clamped. A reflexão de especulares padrão para os materiais de frente e para trás é (0,0, 0,0, 0,0, 1,0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**\_emissão GL**</dt> </dl>                                    | O parâmetro params contém quatro valores de ponto flutuante que especificam a intensidade de luz emitida de RGBA do material. Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0. Os valores de ponto flutuante são mapeados diretamente. Nenhum valor inteiro nem de ponto flutuante são clamped. A intensidade de emissão padrão para os materiais voltados para frente e para trás é (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**claridade do GL \_**</dt> </dl>                                 | O parâmetro *param* é um único valor inteiro que especifica o expoente de especular RGBA do material. Os valores inteiros são mapeados diretamente. Somente os valores no intervalo de \[ 0, 128 \] são aceitos. O expoente especular padrão para os materiais front-end e traseiro é 0. <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**\_ambiente GL \_ e \_ difuso**</dt> </dl> | Equivalente a chamar [**glMaterial**](glmaterial-functions.md) duas vezes com os mesmos valores de parâmetro, uma vez com o \_ ambiente GL e uma vez com o GL \_ difuso. <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**\_índices de cores GL \_**</dt> </dl>                    | O parâmetro params contém três valores de ponto flutuante que especificam os índices de cores para a iluminação ambiente, difuso e especulação. Esses três valores, e GL \_ luminosidade, são os únicos valores materiais usados pela equação de iluminação do modo de índice de cor. Consulte [**glLightModel**](gllightmodel-functions.md) para uma discussão sobre a iluminação de índice de cor.<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

O valor para o qual o parâmetro GL \_ luminosidade será definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significado                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>  | A *face* ou a *pname* não era um valor aceito.<br/>                |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl> | Um expoente especular fora do intervalo de \[ 0, 128 \] foi especificado.<br/> |



## <a name="remarks"></a>Comentários

A função [**glMaterialfv**](glmaterialf.md) atribui valores a parâmetros materiais. Há dois conjuntos correspondentes de parâmetros materiais. Um, o conjunto *front-end* , é usado para sombrear pontos, linhas, bitmaps e todos os polígonos (quando a iluminação de dois lados está desabilitada) ou apenas polígonos frontais (quando a iluminação de dois lados está habilitada). O outro conjunto, *voltado*, é usado para sombrear polígonos voltados somente quando a iluminação de dois lados é habilitada. Consulte [**glLightModel**](gllightmodel-functions.md) para obter detalhes sobre cálculos de iluminação de um lado e dois lados.

A função [**glMaterialfv**](glmaterialf.md) usa três argumentos. A primeira, *face*, especifica se o \_ material frontal do GL, os \_ materiais traseiros do GL ou os \_ materiais de frente \_ e de trás do GL \_ serão modificados. O segundo, *pname*, especifica qual dos vários parâmetros em um ou ambos os conjuntos serão modificados. O terceiro, *param*, especifica qual valor será atribuído ao parâmetro especificado.

Os parâmetros materiais são usados na equação de iluminação que é opcionalmente aplicada a cada vértice. A equação é discutida em [**glLightModel**](gllightmodel-functions.md).

Os parâmetros de material podem ser atualizados a qualquer momento. Em particular, [**glMaterialfv**](glmaterialf.md) pode ser chamado entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). Se apenas um parâmetro de material único for alterado por vértice, no entanto, [**glColorMaterial**](glcolormaterial.md) será preferencial em relação a **glMaterialfv**.

A função a seguir recupera informações relacionadas a [**glMaterialfv**](glmaterialf.md):

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





