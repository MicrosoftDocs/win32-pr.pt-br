---
title: função glMaterialf (GL. h)
description: A função glMaterialf especifica os parâmetros materiais para o modelo de iluminação.
ms.assetid: c6d183c4-2d1f-4fb9-b24f-c132ebfc708d
keywords:
- função glMaterialf OpenGL
topic_type:
- apiref
api_name:
- glMaterialf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aac97cf68996beb5472ff5f11e559af8b58ded31ab12fe5a33ab33d37b13b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358924"
---
# <a name="glmaterialf-function"></a>função glMaterialf

A função **glMaterialf** especifica os parâmetros materiais para o modelo de iluminação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMaterialf(
   GLenum  face,
   GLenum  pname,
   GLfloat param
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

O parâmetro de material de valor único da face ou faces sendo atualizadas. Deve ter o GL de \_ luminosidade.



| Valor                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**claridade do GL \_**</dt> </dl> | O parâmetro *param* é um único valor de ponto flutuante que especifica o expoente de especular RGBA do material. Os valores inteiros são mapeados diretamente. Somente os valores no intervalo de \[ 0, 128 \] são aceitos. O expoente especular padrão para os materiais front-end e traseiro é 0. <br/> |



 

</dd> <dt>

*param* 
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

A função **glMaterialf** atribui valores a parâmetros materiais. Há dois conjuntos correspondentes de parâmetros materiais. Um, o conjunto *front-end* , é usado para sombrear pontos, linhas, bitmaps e todos os polígonos (quando a iluminação de dois lados está desabilitada) ou apenas polígonos frontais (quando a iluminação de dois lados está habilitada). O outro conjunto, *voltado*, é usado para sombrear polígonos voltados somente quando a iluminação de dois lados é habilitada. Consulte [**glLightModel**](gllightmodel-functions.md) para obter detalhes sobre cálculos de iluminação de um lado e dois lados.

A função **glMaterialf** usa três argumentos. A primeira, *face*, especifica se o \_ material frontal do GL, os \_ materiais traseiros do GL ou os \_ materiais de frente \_ e de trás do GL \_ serão modificados. O segundo, *pname*, especifica qual dos vários parâmetros em um ou ambos os conjuntos serão modificados. O terceiro, *param*, especifica qual valor será atribuído ao parâmetro especificado.

Os parâmetros materiais são usados na equação de iluminação que é opcionalmente aplicada a cada vértice. A equação é discutida em [**glLightModel**](gllightmodel-functions.md).

Os parâmetros de material podem ser atualizados a qualquer momento. Em particular, **glMaterialf** pode ser chamado entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). Se apenas um parâmetro de material único for alterado por vértice, no entanto, [**glColorMaterial**](glcolormaterial.md) será preferencial em relação a **glMaterialf**.

A função a seguir recupera informações relacionadas a **glMaterialf**:

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

 

 





