---
title: função glGetString (GL. h)
description: A função glGetString retorna uma cadeia de caracteres que descreve a conexão OpenGL atual.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- função glGetString OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919060"
---
# <a name="glgetstring-function"></a>função glGetString

A função **glGetString** retorna uma cadeia de caracteres que descreve a conexão OpenGL atual.

## <a name="syntax"></a>Sintaxe


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* 
</dt> <dd>

Uma das constantes simbólicas a seguir.



| Valor                                                                                                                                                         | Significado                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**\_fornecedor GL**</dt> </dl>             | Retorna a empresa responsável por esta implementação OpenGL. Esse nome não é alterado de Release para Release.<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**\_renderizador GL**</dt> </dl>       | Retorna o nome do renderizador. Esse nome é normalmente específico para uma configuração específica de uma plataforma de hardware. Ele não muda de liberação para liberação.<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**versão do GL \_**</dt> </dl>          | Retorna uma versão ou um número de versão.<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**\_extensões GL**</dt> </dl> | Retorna uma lista separada por espaços de extensões com suporte para OpenGL.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *nome* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGetString** retorna um ponteiro para uma cadeia de caracteres estática que descreve algum aspecto da conexão OpenGL atual.

Como o OpenGL não inclui consultas para as características de desempenho de uma implementação, espera-se que alguns aplicativos sejam gravados para reconhecer plataformas conhecidas e modificarão o uso do OpenGL com base nas características de desempenho conhecidas dessas plataformas. O fornecedor de cadeias de caracteres GL \_ e o \_ renderizador GL juntos especificam exclusivamente uma plataforma e não serão alterados de liberação para liberação. Eles devem ser usados como tais por algoritmos de reconhecimento de plataforma.

O formato e o conteúdo da cadeia de caracteres que o **glGetString** retorna dependem da implementação, exceto pelo fato de que:

-   Os nomes de extensão não incluirão caracteres de espaço e serão separados por caracteres de espaço na cadeia de caracteres de \_ extensões GL.
-   A \_ cadeia de caracteres da versão GL começa com um número de versão. O número de versão usa um destes formulários:

    *\_ número principal*. *\_ número secundário*

    *\_ número principal*. *\_ número secundário*. *\_ número de versão*

-   As informações específicas do fornecedor podem seguir o número de versão. Seu formato depende da implementação, mas um espaço sempre separa o número de versão e as informações específicas do fornecedor.
-   Todas as cadeias de caracteres são terminadas em nulo.

Se um erro for gerado, **glGetString** retornará zero.

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

[**glEnd**](glend.md)
</dt> </dl>

 

 





