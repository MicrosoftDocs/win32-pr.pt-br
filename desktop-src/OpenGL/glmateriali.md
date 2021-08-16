---
title: Função glMateriali (Gl.h)
description: A função TheglMateriali especifica parâmetros de material para o modelo de iluminação.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- Função glMateriali OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d850bac6b27672c00dca9b1cafa7b4664dbde5fca0085381b4b166e2106b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358860"
---
# <a name="glmateriali-function"></a>Função glMateriali

A **função glMateriali** especifica parâmetros de material para o modelo de iluminação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
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

O parâmetro de material de valor único da face ou faces que está sendo atualizada. Deve ser \_ GLINESS.



| Valor                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GLINESS**</dt> </dl> | O *parâmetro param* é um único inteiro que especifica o expoente especular RGBA do material. Os valores inteiros são mapeados diretamente. Somente valores no intervalo \[ 0, 128 \] são aceitos. O expoente especular padrão para materiais voltados para frente e para trás é 0. <br/> |



 

</dd> <dt>

*param* 
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

A **função glMateriali** atribui valores a parâmetros de material. Há dois conjuntos de parâmetros de material. Um,  o conjunto voltado para a frente, é usado para sombrear pontos, linhas, bitmaps e todos os polígonos (quando a iluminação de dois lados está desabilitada) ou apenas polígonos voltados para a frente (quando a iluminação de dois lados está habilitada). O outro conjunto, *voltado para trás,* é usado para sombrear polígonos voltados para trás somente quando a iluminação de dois lados está habilitada. Consulte [**glLightModel para**](gllightmodel-functions.md) obter detalhes sobre cálculos de iluminação de um lado e dois lados.

A **função glMateriali** recebe três argumentos. O primeiro, *face*, especifica se os materiais GL FRONT, os materiais GL BACK ou os materiais \_ GL FRONT E BACK serão \_ \_ \_ \_ modificados. O segundo, *pname*, especifica qual dos vários parâmetros em um ou em ambos os conjuntos será modificado. O terceiro, *param*, especifica qual valor será atribuído ao parâmetro especificado.

Parâmetros de material são usados na equação de iluminação que é opcionalmente aplicada a cada vértice. A equação é discutida em [**glLightModel.**](gllightmodel-functions.md)

Os parâmetros de material podem ser atualizados a qualquer momento. Em particular, **glMateriali** pode ser chamado entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md) No entanto, se apenas um único parâmetro de material for alterado por vértice, [**glColorMaterial**](glcolormaterial.md) será preferencial em vez de **glMateriali.**

A função a seguir recupera informações relacionadas a **glMateriali**:

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

 

 





