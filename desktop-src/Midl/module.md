---
title: atributo module
description: A instrução module define um grupo de funções, normalmente um conjunto de pontos de entrada de DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- atributo de módulo MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a83528a1ec632fcf2309438e6228220544a32408b310ea90260b8bcfda3cb6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642804"
---
# <a name="module-attribute"></a>atributo module

A **instrução** module define um grupo de funções, normalmente um conjunto de pontos de entrada de DLL.

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*attributes* 
</dt> <dd>

Os \[ [**atributos uuid**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**helpstring**](helpstring.md), \] \[ [**helpcontext,**](helpcontext.md)hidden e dllname são aceitos antes \] de uma \[ [](hidden.md) \] \[ [](dllname-str-.md) \] **instrução de** módulo. Consulte [Descrições de atributo](/previous-versions/windows/desktop/automat/attribute-descriptions), no livro automação OLE, para obter mais informações sobre os atributos aceitos antes de uma definição de módulo. O \[ **atributo dllname** \] é necessário. Se o \[ **atributo uuid** \] for omitido, o módulo não será especificado exclusivamente no sistema.

</dd> <dt>

*Modulename* 
</dt> <dd>

O nome do módulo.

</dd> <dt>

*elementlist* 
</dt> <dd>

Lista de definições constantes e protótipos de função para cada função na DLL. Qualquer número de definições de função pode aparecer na lista de funções. Uma função na lista de funções tem o seguinte formato:

\[*atributos* \] *returntype* \[ *convenção de chamada funcname* \] (*params*);

\[*atributos* \] [**const**](const.md) constanttype *constname*  =  *constval*;

Somente os \[ [**atributos helpstring**](helpstring.md) \] e \[ [**helpcontext**](helpcontext.md) são \] aceitos para um [**const.**](const.md)

Os atributos a seguir são aceitos em uma função em um \[ módulo: [**helpstring**](helpstring.md) \] , \[ [**helpcontext**](helpcontext.md), \] \[ [**string**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md), \] \[ [**propput**](propput.md), \] \[ [**propputref**](propputref.md)e \] \[ [**vararg**](vararg.md) \] . Se \[ **o vararg** \] for especificado, o último parâmetro deverá ser uma matriz segura do **tipo VARIANT.**

A convenção de chamada opcional pode ser um de \_ \_ \_ pascal/pascal/pascal, \_ \_ \_ cdecl/ cdecl/cdecl ou \_ \_ stdcall/stdcall/stdcall. \_ O *nome do tipo de convenção de* chamada pode incluir até dois sublinhados à frente.

A lista de parâmetros é uma lista delimitada por vírgulas de:

\[*Atributos*\]

O tipo pode ser qualquer tipo declarado anteriormente ou um tipo integrado, um ponteiro para qualquer tipo ou um ponteiro para um tipo integrado. Os atributos nos parâmetros são:

\[[**em**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**opcional.**](optional.md) \]

Se \[ [**opcional**](optional.md) \] for usado, os tipos desses parâmetros deverão ser **VARIANT** ou **VARIANT.** \*

</dd> </dl>

## <a name="remarks"></a>Comentários

A saída do arquivo de header (.h) para módulos é uma série de protótipos de função. A **palavra-chave** module e os colchetes ao redor são removidos da saída do arquivo de título (.h), mas um comentário (// *modulename)* é inserido antes dos protótipos.  A **palavra-chave extern** é inserida antes das declarações.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Conteúdo de uma biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**Dllname**](dllname-str-.md)
</dt> <dt>

[**Entrada**](entry.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Escondidos**](hidden.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 