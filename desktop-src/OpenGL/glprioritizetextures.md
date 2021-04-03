---
title: função glPrioritizeTextures (GL. h)
description: A função glPrioritizeTextures define a prioridade de residência de texturas.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- função glPrioritizeTextures OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644436"
---
# <a name="glprioritizetextures-function"></a>função glPrioritizeTextures

A função **glPrioritizeTextures** define a prioridade de residência de texturas.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

O número de texturas a serem priorizadas.

</dd> <dt>

*textura* 
</dt> <dd>

Um ponteiro para o primeiro elemento de uma matriz que contém os nomes das texturas a serem priorizadas.

</dd> <dt>

*suas* 
</dt> <dd>

Um ponteiro para o primeiro elemento de uma matriz que contém as prioridades de textura. Uma prioridade fornecida em um elemento do parâmetro de *prioridades* se aplica à textura nomeada pelo elemento correspondente do parâmetro *Textures* .

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

A função **glPrioritizeTextures** atribui as *n* prioridades de textura especificadas no parâmetro *prioridades* para as texturas *n* chamadas no parâmetro *texturas* . Em computadores com uma quantidade limitada de memória de textura, o OpenGL estabelece um "conjunto de trabalho" de texturas que são residentes na memória de textura. Essas texturas podem ser associadas a um destino de textura de forma muito mais eficiente do que as texturas que não são residentes.

Ao especificar uma prioridade para cada textura, a função **glPrioritizeTextures** permite que você determine quais texturas devem ser residentes.

Os elementos de prioridades de textura em *prioridades* são clamped ao intervalo de \[ 0,0, 1,0 \] antes de serem atribuídos. Zero indica a prioridade mais baixa; Portanto, as texturas com prioridade zero são menos prováveis de serem residentes. O valor 1,0 indica a prioridade mais alta; Portanto, as texturas com prioridade 1,0 têm maior probabilidade de serem residentes. No entanto, não há garantia de que as texturas sejam residentes até que sejam associadas.

A função **glPrioritizeTextures** ignora as tentativas de priorizar a textura 0 ou qualquer nome de textura que não corresponda a uma textura existente. Nenhuma das funções nomeadas pelo parâmetro de *texturas* precisa estar associada a um destino de textura.

Se uma textura estiver associada no momento, você também poderá usar a função [**glTexParameter**](gltexparameter-functions.md) para definir sua prioridade. Essa é a única maneira de definir a prioridade de uma textura padrão.

Você pode incluir **glPrioritizeTextures** em listas de exibição.

A função a seguir recupera a prioridade de uma textura atualmente associada relacionada a **glPrioritizeTextures**:

-   [**glGetTexParameter**](glgettexparameter.md) com prioridade de textura de nome de parâmetro GL \_ \_

> [!Note]  
> A função **glPrioritizeTextures** só está disponível no OpenGL versão 1,1 ou posterior.

 

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





