---
title: função glDeleteTextures (GL. h)
description: A função glDeleteTextures exclui as texturas nomeadas.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- função glDeleteTextures OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454799"
---
# <a name="gldeletetextures-function"></a>função glDeleteTextures

A função **glDeleteTextures** exclui as texturas nomeadas.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

O número de texturas a serem excluídas.

</dd> <dt>

*textura* 
</dt> <dd>

Uma matriz de texturas a ser excluída.

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

A função **glDeleteTextures** exclui *n* texturas nomeadas pelos elementos das *texturas* de matriz. Depois que uma textura é excluída, ela não tem nenhum conteúdo ou dimensionalidade, e seu nome é gratuito para reutilização (por exemplo, por **glGenTextures**). A função **glDeleteTextures** ignora zeros e nomes que não correspondem a texturas existentes.

Se uma textura atualmente associada for excluída, a associação será revertida para zero (a textura padrão).

Você não pode incluir chamadas para **glDeleteTextures** em listas de exibição.

> [!Note]  
> A função **glDeleteTextures** só está disponível no OpenGL versão 1,1 ou posterior.

 

A função a seguir recupera informações relacionadas a **glDeleteTextures**:

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





