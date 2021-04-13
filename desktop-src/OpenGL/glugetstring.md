---
title: função gluGetString (Glu. h)
description: A função gluGetString Obtém uma cadeia de caracteres que descreve o número de versão do GLU ou as chamadas de extensão GLU com suporte.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- função gluGetString OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369517"
---
# <a name="glugetstring-function"></a>função gluGetString

A função **gluGetString** Obtém uma cadeia de caracteres que descreve o número de versão do Glu ou as chamadas de extensão Glu com suporte.

## <a name="syntax"></a>Sintaxe


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* 
</dt> <dd>

O número de versão do GLU ( \_ versão Glu) ou as chamadas de extensão específicas do fornecedor disponíveis ( \_ extensões Glu).

</dd> </dl>

## <a name="remarks"></a>Comentários

A função **gluGetString** retorna um ponteiro para uma cadeia de caracteres estática, terminada em nulo. Quando *Name* for Glu \_ version, a cadeia de caracteres retornada será um valor que representa o número de versão de Glu. O formato do número de versão é o seguinte:

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

O número de versão tem o formato " \_ número principal. \_ número secundário" ou " \_ número principal. \_ número secundário. \_ número de versão". As informações específicas do fornecedor são opcionais, e o formato e o conteúdo dependem da implementação.

Quando *Name* é GLU \_ Extensions, a cadeia de caracteres retornada contém uma lista de nomes de extensões de Glu com suporte que são separadas por espaços. O formato da lista de nomes retornada é o seguinte:

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

Os nomes de extensão não podem conter espaços.

A função **gluGetString** é válida para o GLU versão 1,1 ou posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



 

 





