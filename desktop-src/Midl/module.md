---
title: atributo de módulo
description: A instrução Module define um grupo de funções, normalmente um conjunto de pontos de entrada de DLL.
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
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293974"
---
# <a name="module-attribute"></a>atributo de módulo

A instrução **Module** define um grupo de funções, normalmente um conjunto de pontos de entrada de dll.

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

Os \[ atributos [**UUID**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**helptype**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] e \[ [**DllName**](dllname-str-.md) \] são aceitos antes de uma instrução de **módulo** . Consulte [descrições de atributo](/previous-versions/windows/desktop/automat/attribute-descriptions), no livro de automação OLE, para obter mais informações sobre os atributos aceitos antes de uma definição de módulo. O \[ atributo **DllName** \] é necessário. Se o \[ atributo **UUID** \] for omitido, o módulo não será especificado exclusivamente no sistema.

</dd> <dt>

*ModuleName* 
</dt> <dd>

O nome do módulo.

</dd> <dt>

*elementolist* 
</dt> <dd>

Lista de definições de constantes e protótipos de função para cada função na DLL. Qualquer número de definições de função pode aparecer na lista de funções. Uma função na lista de funções tem o seguinte formato:

\[*atributos* \] do *ReturnType* \[ *chamando convenção funcname* \] (*params*);

\[*atributos* \] do [**const**](const.md) constante *constname*  =  *constval*;

Somente os \[ atributos [**HelpString**](helpstring.md) \] e \[ [**HelpContext**](helpcontext.md) \] são aceitos para uma [**const**](const.md).

Os seguintes atributos são aceitos em uma função em um módulo: \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**propput**](propput.md) \] , \[ [**propputref**](propputref.md) \] e \[ [**vararg**](vararg.md) \] . Se \[ **vararg** \] for especificado, o último parâmetro deverá ser uma matriz segura de tipo **Variant** .

A Convenção de chamada opcional pode ser um dos \_ \_ Pascal/ \_ Pascal/Pascal, \_ \_ cdecl/ \_ cdecl/cdecl ou \_ \_ stdcall/ \_ stdcall/stdcall. O *tipo de Convenção de chamada paramName* pode incluir até dois sublinhados à esquerda.

A lista de parâmetros é uma lista delimitada por vírgulas de:

\[*atributos*\]

O tipo pode ser qualquer tipo ou tipo interno declarado anteriormente, um ponteiro para qualquer tipo ou um ponteiro para um tipo interno. Os atributos em parâmetros são:

\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**opcional**](optional.md) \] .

Se \[ [**opcional**](optional.md) \] for usado, os tipos desses parâmetros deverão ser **Variant** ou **Variant** \* .

</dd> </dl>

## <a name="remarks"></a>Comentários

A saída do arquivo de cabeçalho (. h) para módulos é uma série de protótipos de função. A palavra-chave do **módulo** e os colchetes ao redor são removidos da saída do arquivo de cabeçalho (. h), mas um comentário ( **//módulo** *ModuleName*) é inserido antes dos protótipos. A palavra-chave **extern** é inserida antes das declarações.

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

[**nomedadll**](dllname-str-.md)
</dt> <dt>

[**inicial**](entry.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**oculto**](hidden.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 