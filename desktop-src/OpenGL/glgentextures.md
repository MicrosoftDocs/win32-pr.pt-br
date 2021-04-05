---
title: função glGenTextures (GL. h)
description: A função glGenTextures gera nomes de textura.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- função glGenTextures OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919061"
---
# <a name="glgentextures-function"></a>função glGenTextures

A função **glGenTextures** gera nomes de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

O número de nomes de textura a serem gerados.

</dd> <dt>

*textura* 
</dt> <dd>

Um ponteiro para o primeiro elemento de uma matriz na qual os nomes de textura gerados são armazenados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *n* era um valor negativo.<br/>                                                                                                  |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGenTextures** retorna *n* nomes de textura no parâmetro *Textures* . Os nomes de textura não são necessariamente um conjunto contíguo de inteiros, no entanto, nenhum dos nomes retornados pode estar em uso imediatamente antes de chamar a função **glGenTextures** . As texturas geradas pressupõem a dimensionalidade do destino de textura ao qual elas são vinculadas pela primeira vez com a função [**glBindTexture**](glbindtexture.md) . Os nomes de textura retornados por **glGenTextures** não são retornados por chamadas subsequentes para **glGenTextures** , a menos que sejam excluídos primeiro com a chamada de [**glDeleteTextures**](gldeletetextures.md).

Você não pode incluir **glGenTextures** em listas de exibição.

> [!Note]  
> A função **glGenTextures** só está disponível no OpenGL versão 1,1 ou posterior.

 

A função a seguir recupera informações relacionadas a **glGenTextures**:

-   [**glIsTexture**](glistexture.md)

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





