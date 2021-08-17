---
title: Função glNormal3b (Gl.h)
description: Define o vetor normal atual. | Função glNormal3b (Gl.h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- Função glNormal3b OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff27f8082d384c5c244951b5dd237f21cb60875c0912cf742c4f8b2d3ea1f018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358689"
---
# <a name="glnormal3b-function"></a>Função glNormal3b

Define o vetor normal atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
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

O normal atual é definido para as coordenadas fornecidas sempre que você chama a **função glNormal3b.**

Os argumentos de byte, curto ou inteiro são convertidos em formato de ponto flutuante usando um mapeamento linear que mapeia o valor inteiro representável mais positivo para 1,0 e o valor inteiro representável mais negativo para -1,0.

Os normais especificados com **glNormal3b não** precisam ter comprimento de unidade. Se a normalização estiver habilitada, os normais especificados com **glNormal3b** serão normalizados após a transformação. Você pode controlar a normalização usando [**glEnable e**](glenable.md) [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE. Por padrão, a normalização está desabilitada. Você pode atualizar o normal atual a qualquer momento. Em particular, você pode chamar **glNormal3b** entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md) As funções a seguir recuperam informações relacionadas **a glNormal3b**:

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

 

 





