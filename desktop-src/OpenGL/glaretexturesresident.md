---
title: função glAreTexturesResident (GL. h)
description: A função glAreTexturesResident determina se os objetos de textura especificados são residentes na memória de textura.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- função glAreTexturesResident OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c503cac59bbec912c535120161d27991118dab818a185c1f39d8f48cb2a5939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082236"
---
# <a name="glaretexturesresident-function"></a>função glAreTexturesResident

A função **glAreTexturesResident** determina se os objetos de textura especificados são residentes na memória de textura.

## <a name="syntax"></a>Sintaxe


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

O número de texturas a serem consultadas.

</dd> <dt>

*textura* 
</dt> <dd>

O endereço de uma matriz que contém os nomes das texturas a serem consultadas.

</dd> <dt>

*residências* 
</dt> <dd>

O endereço de uma matriz na qual o status de residência de textura é retornado. O status de residência de uma textura chamada por um elemento de *texturas* é retornado no elemento correspondente de *residências*.

</dd> </dl>

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *n* era um valor negativo, um elemento em *texturas* era zero ou um elemento em *texturas* não continha um identificador de textura.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>     |



## <a name="remarks"></a>Comentários

Em computadores com uma quantidade limitada de memória de textura, o OpenGL estabelece um conjunto de trabalho de texturas que são residentes na memória de textura. Essas texturas podem ser associadas a um destino de textura de forma muito mais eficiente do que as texturas que não são residentes.

A função **glAreTexturesResident** consulta o status de residência de textura das *n* texturas nomeadas pelos elementos de *texturas*. Se todas as texturas nomeadas forem residentes, **glAreTexturesResident** retornará GL \_ true e o conteúdo das *residências* não será incomodado. Se qualquer uma das texturas nomeadas não for residente, **glAreTexturesResident** retornará GL \_ false e o status detalhado será retornado nos elementos *n* de *residências*.

Se um elemento de *residências* for GL \_ verdadeiro, a textura nomeada pelo elemento correspondente de *texturas* será residente na memória de textura.

Para consultar o status de residência de uma única textura acoplada, chame [**glGetTexParameter**](glgettexparameter.md) com o parâmetro de *destino* definido como a textura de destino à qual o destino está associado e defina o parâmetro *pname* para a \_ textura GL \_ residente. Você deve usar esse método para consultar o status residente de uma textura padrão.

Você não pode incluir **glAreTexturesResident** em listas de exibição.

A função **glAreTexturesResident** retorna o status de residência das texturas no momento da invocação. Ele não garante que as texturas permanecerão residentes em qualquer outro momento.

Se as texturas residirem na memória virtual (não há memória de textura), elas serão consideradas sempre residentes.

> [!Note]  
> A função **glAreTexturesResident** só está disponível no OpenGL versão 1,1 ou posterior.

 

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





