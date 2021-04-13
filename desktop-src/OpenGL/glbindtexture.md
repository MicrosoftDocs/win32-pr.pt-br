---
title: função glBindTexture (GL. h)
description: A função glBindTexture permite a criação de uma textura nomeada associada a um destino de textura.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- função glBindTexture OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369701"
---
# <a name="glbindtexture-function"></a>função glBindTexture

A função **glBindTexture** permite a criação de uma textura nomeada associada a um destino de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O destino ao qual a textura está associada. Deve ter o valor GL \_ Texture \_ 1D ou GL \_ Texture \_ 2D.

</dd> <dt>

*textura* 
</dt> <dd>

O nome de uma textura; o nome da textura não pode estar em uso no momento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | O parâmetro de *destino* não era um valor aceito.<br/>                                                                                                                                                       |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A *textura* do parâmetro não tinha a mesma dimensionalidade que o *destino* ou a função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glBindTexture** permite que você crie uma textura nomeada. Chamar **glBindTexture** com *target* definido como GL \_ Texture \_ 1D ou GL \_ Texture \_ 2D e *Texture* definido como o nome da nova textura que você criou associa o nome da textura ao destino de textura apropriado. Quando uma textura é associada a um destino, a ligação anterior para esse destino não está mais em vigor.

Os nomes de textura são inteiros sem sinal com o valor zero reservado para representar a textura padrão para cada destino de textura. Os nomes de textura e o conteúdo de textura correspondente são locais para o espaço de lista de exibição compartilhado do contexto de renderização OpenGL atual; dois contextos de renderização compartilham nomes de textura somente se eles também compartilham listas de exibição. Você pode gerar um conjunto de novos nomes de textura usando [**glGenTextures**](glgentextures.md).

Quando uma textura é vinculada pela primeira vez, ela assume a dimensionalidade de seu destino de textura; uma textura vinculada à \_ textura GL \_ 1D torna-se unidimensional e uma textura associada à \_ textura GL \_ 2D se torna bidimensional. As operações que você executa em um destino de textura também afetam uma textura associada ao destino. Quando você consulta um destino de textura, o valor de retorno é o estado da textura associada a ele. Os destinos de textura se tornam aliases para texturas atualmente associadas a eles.

Quando você associa uma textura a **glBindTexture**, a associação permanece ativa até que uma textura diferente seja associada ao mesmo destino ou você exclua a textura associada com a função [**glDeleteTextures**](gldeletetextures.md) . Depois de criar uma textura nomeada, você pode associá-la a um destino de textura que tenha a mesma dimensionalidade sempre que necessário.

Geralmente, é muito mais rápido usar **glBindTexture** para associar uma textura nomeada existente a um dos destinos de textura do que recarregar a imagem de textura usando [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md). Para obter mais controle sobre o desempenho do texturing, use [**glPrioritizeTextures**](glprioritizetextures.md).

Você pode incluir chamadas para **glBindTexture** em listas de exibição.

> [!Note]  
> A função **glBindTexture** só está disponível no OpenGL versão 1,1 ou posterior.

 

As funções a seguir recuperam informações relacionadas ao **glBindTexture**:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com associação do Argument GL de \_ textura \_ 1D \_

**glGet** com \_ \_ Associação 2D de textura de Argument GL \_

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

[**glDeleteTextures**](gldeletetextures.md)
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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





