---
title: função glLightModelf (GL. h)
description: A função glLightModelf define os parâmetros do modelo de iluminação.
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- função glLightModelf OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2c17f7dc82080544a9055805cf62726227c200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008890"
---
# <a name="gllightmodelf-function"></a>função glLightModelf

A função **glLightModelf** define os parâmetros do modelo de iluminação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* 
</dt> <dd>

Um parâmetro de modelo de iluminação de valor único. Os valores a seguir são aceitos.



| Valor                                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <dt>**\_ \_ Visualizador local de modelo Light \_ GL \_**</dt> </dl> | O parâmetro *param* é um único valor de ponto flutuante que especifica como os ângulos de reflexão especular são computados. Se *param* for 0 (ou 0,0), os ângulos de reflexo especular usam a direção de exibição para serem paralelos e na direção do eixo-*z* , independentemente do local do vértice em coordenadas de olho. Caso contrário, os reflexos especulares são computados a partir da origem do sistema de coordenadas de olho. O padrão é 0. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <dt>**\_Método Light \_ GL \_ dois \_ lados**</dt> </dl>             | O parâmetro *param* é um único valor de ponto flutuante que especifica se os cálculos de iluminação com um ou dois lados são feitos para polígonos. Ele não tem nenhum efeito sobre os cálculos de iluminação para pontos, linhas ou bitmaps. Se *param* for 0 (ou 0,0), a iluminação unidirecional será especificada e somente os parâmetros de material frontal serão usados na equação de iluminação. Caso contrário, a iluminação em dois lados será especificada. <br/> Nesse caso, os vértices de polígonos voltados são iluminados usando os parâmetros de material de apoio e têm seus normais invertidos antes que a equação de iluminação seja avaliada. Os vértices de polígonos front-end sempre são iluminados usando os parâmetros de material frontal, sem nenhuma alteração em seus normais. O padrão é 0.<br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

O valor para o qual *param* será definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *pname* não era um valor aceito.<br/>                                                                                         |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glLightModelf** define o parâmetro do modelo de iluminação. O parâmetro *pname* nomeia um parâmetro e *param* fornece o novo valor. o valor ou os valores de parâmetros de fonte de luz individuais.

No modo RGBA, a cor clara de um vértice é a soma da intensidade de emissão de material, do produto do material de reflexão de ambiente e da intensidade de ambiente de cena completa e a contribuição de cada fonte de luz habilitada. Cada fonte de luz contribui com a soma de três termos: ambiente, difuso e especular.

-   A contribuição de fonte de luz ambiente é o produto da reflexão de ambiente material e a intensidade de ambiente da luz.
-   A contribuição de origem da luz difusa é o produto da reflexão difusa do material, a intensidade difusa da luz e o produto do ponto do vértice normal com o vetor normalizado do vértice para a fonte de luz.
-   A contribuição de fonte de luz especular é o produto da reflexão de especulação de material, a intensidade especular da luz e o produto de ponto dos vetores de vértice-to-light e de vértice para claro, aumentados para o poder da luminosidade do material.

Todas as três contribuições de fonte de luz são atenuadas igualmente com base na distância do vértice até a fonte de luz e na direção da fonte de luz, no expoente de espalhamento e no ângulo de corte de espalhamento. Todos os produtos de ponto serão substituídos por zero se forem avaliados como um valor negativo.

O componente alfa da cor declarada resultante é definido como o valor alfa da reflexão difusa do material.

No modo de índice de cor, o valor do índice claro de um vértice varia do ambiente para os valores especulares passados para [**glMaterial**](glmaterial-functions.md) usando índices de \_ cores GL \_ . Coeficientes difusas e especulares, computados com um peso (. 30,. 59, .11) das cores da luz, da luminosidade do material e das mesmas equações de reflexão e atenuação que no caso de RGBA, determinam o quanto acima do ambiente o índice resultante é.

As funções a seguir recuperam informações relacionadas à função **glLightModelf** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Light \_ modelo \_ local \_ Viewer

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Light de \_ \_ dois \_ lados

[**glIsEnabled**](glisenabled.md) com iluminação do argumento GL \_

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

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





