---
title: Função glLightModeliv (Gl.h)
description: A função glLightModeliv define parâmetros de modelo de iluminação.
ms.assetid: 5998bb7e-d97a-47a0-b612-e6b0046aa5d2
keywords:
- Função glLightModeliv OpenGL
topic_type:
- apiref
api_name:
- glLightModeliv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e106fdccf39fdf002c83b45c190073d20c7432eb5252d736e00cf4259dcd8af1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493056"
---
# <a name="gllightmodeliv-function"></a>Função glLightModeliv

A [**função glLightModeliv**](gllightiv.md) define parâmetros de modelo de iluminação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLightModeliv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

Um parâmetro de modelo de iluminação. Os valores a seguir são aceitos.



| Valor                                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <dt>**AMBIENTE \_ DO MODELO DE LUZ \_ \_ GL**</dt> </dl>                 | O *parâmetro params* contém quatro valores inteiros que especificam a intensidade de RGBA do ambiente de toda a cena. Os valores inteiros são mapeados linearmente de modo que o valor representável mais positivo seja mapeado para 1,0 e o valor representável mais negativo seja mapeado para -1,0. Os valores de ponto flutuante são mapeados diretamente. Nem inteiro nem valores de ponto flutuante são fixados. A intensidade da cena ambiente padrão é (0,2, 0,2, 0,2, 1,0). <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**VISUALIZADOR \_ LOCAL DO MODELO DE LUZ \_ \_ \_ GL**</dt> </dl> | O *parâmetro params* é um único valor inteiro que especifica como ângulos de reflexão especular são computados. Se *param* for 0 (ou 0,0), os ângulos de reflexão especular levarão a direção de exibição em paralelo para e na direção do eixo *- z,* independentemente do local do vértice nas coordenadas de olho. Caso contrário, as reflexões especular serão calculadas da origem do sistema de coordenadas ocular. O padrão é 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE**</dt> </dl>             | O *parâmetro params* é um único valor inteiro que especifica se os cálculos de iluminação lado a lado ou de dois lados são feitos para polígonos. Ele não tem nenhum efeito sobre os cálculos de iluminação para pontos, linhas ou bitmaps. Se *param* for 0 (ou 0,0), a iluminação de um lado será especificada e somente os parâmetros de material frontal serão usados na equação de iluminação. Caso contrário, a iluminação de dois lados será especificada. <br/> Nesse caso, os vértices de polígonos voltados para trás são claros usando os parâmetros de material de fundo e têm seus normais invertidos antes que a equação de iluminação seja avaliada. Os vértices de polígonos voltados para a frente sempre são claros usando os parâmetros de material frontal, sem nenhuma alteração em seus normais. O padrão é 0.<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Um ponteiro para o valor ou valores para os quais *os params* serão definidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *pname* não era um valor aceito.<br/>                                                                                         |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glLightModeliv** define o parâmetro do modelo de iluminação. O *parâmetro pname* nomeia um parâmetro *e o parâmetro param* fornece o novo valor.o valor ou os valores de parâmetros de fonte de luz individuais.

No modo RGBA, a cor clara de um vértice é a soma da intensidade de emissão do material, o produto da reflexão do ambiente do material e a intensidade do ambiente de cena inteira do modelo de iluminação e a contribuição de cada fonte de luz habilitada. Cada fonte de luz contribui com a soma de três termos: ambiente, difuso e especular.

-   A contribuição da fonte de luz ambiente é o produto da reflexão do ambiente do material e da intensidade do ambiente da luz.
-   A contribuição difusa da fonte de luz é o produto da reflexão difusa do material, da intensidade difusa da luz e do produto de ponto do normal do vértice com o vetor normalizado do vértice para a fonte de luz.
-   A contribuição da fonte de luz especular é o produto da reflexão especular do material, da intensidade especular da luz e do produto de ponto dos vetores de vértice para olho normalizados e vértice para luz, elevados à potência da prontidão do material.

Todas as três contribuições de fonte de luz são atenuadas igualmente com base na distância do vértice para a fonte de luz e na direção da fonte de luz, propagam o expoente e estendem o ângulo de corte. Todos os produtos de ponto serão substituídos por zero se avaliarem como um valor negativo.

O componente alfa da cor clara resultante é definido como o valor alfa da reflexão difusa do material.

No modo de índice de cores, o valor do índice claro de um vértice varia do ambiente até os valores especular passados para [**glMaterial**](glmaterial-functions.md) usando GL \_ COLOR \_ INDEXES. Coeficientes difusos e especular, calculados com uma ponderação (.30, .59, .11) das cores da luz, a prontidão do material e as mesmas equações de reflexão e atenuação que no caso RGBA, determinam o nível acima do ambiente do índice resultante.

As funções a seguir recuperam informações relacionadas à **função glLightModeliv:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ LIGHT MODEL LOCAL \_ \_ \_ VIEWER

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ LIGHT MODEL TWO \_ \_ \_ SIDE

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ LIGHTING

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

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





