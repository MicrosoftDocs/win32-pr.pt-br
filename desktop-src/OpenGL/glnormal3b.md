---
title: função glNormal3b (GL. h)
description: Define o vetor normal atual. | função glNormal3b (GL. h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- função glNormal3b OpenGL
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
ms.openlocfilehash: 3a09a92b718881670ed5625fd5aa94a23193cdd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837734"
---
# <a name="glnormal3b-function"></a>função glNormal3b

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

*NX* 
</dt> <dd>

Especifica a coordenada x para o novo vetor normal atual.

</dd> <dt>

*York* 
</dt> <dd>

Especifica a coordenada y para o novo vetor normal atual.

</dd> <dt>

*NZ* 
</dt> <dd>

Especifica a coordenada z para o novo vetor normal atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O normal atual é definido para as coordenadas fornecidas sempre que você chama a função **glNormal3b** .

Os argumentos byte, Short ou Integer são convertidos em formato de ponto flutuante usando um mapeamento linear que mapeia o valor inteiro representável mais positivo para 1,0 e o valor inteiro reapresentável mais negativo para-1,0.

Os normais especificados com **glNormal3b** não precisam ter comprimento de unidade. Se a normalização estiver habilitada, os normais especificados com **glNormal3b** serão normalizados após a transformação. Você pode controlar a normalização usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE. Por padrão, a normalização é desabilitada. Você pode atualizar o normal atual a qualquer momento. Em particular, você pode chamar **glNormal3b** entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md). As funções a seguir recuperam informações relacionadas ao **glNormal3b**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ atual \_ normal

[**glIsEnable**](glisenabled.md) com o Argument GL \_ NORMALIZE

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

 

 





