---
title: Função glNormal3f (Gl.h)
description: Define o vetor normal atual. | Função glNormal3f (Gl.h)
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- Função glNormal3f OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de6edaab0f83c9b05a561eb8f857086fea76f41a84a4869d5d9f99149482df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128146"
---
# <a name="glnormal3f-function"></a>Função glNormal3f

Define o vetor normal atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nx* 
</dt> <dd>

Especifica a coordenada x para o novo vetor normal atual.

</dd> <dt>

*Ny* 
</dt> <dd>

Especifica a coordenada y para o novo vetor normal atual.

</dd> <dt>

*Nz* 
</dt> <dd>

Especifica a coordenada z para o novo vetor normal atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O normal atual é definido para as coordenadas fornecidas sempre que você chama a **função glNormal3f.**

Os argumentos de byte, curto ou inteiro são convertidos em formato de ponto flutuante com um mapeamento linear que mapeia o valor inteiro representável mais positivo para 1,0 e o valor inteiro representável mais negativo para -1,0.

Os normais especificados usando **glNormal3f** não precisam ter comprimento de unidade. Se a normalização estiver habilitada, os normais especificados com **glNormal3f** serão normalizados após a transformação. Você pode controlar a normalização usando [**glEnable e**](glenable.md) [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE. Por padrão, a normalização está desabilitada. Você pode atualizar o normal atual a qualquer momento. Em particular, você pode chamar **glNormal3f** entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md) As funções a seguir recuperam informações relacionadas **a glNormal3f**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ NORMAL

[**glIsEnable com**](glisenabled.md) o argumento GL \_ NORMALIZE

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





