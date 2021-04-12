---
title: atributo restrito
description: O atributo \ Restricted \ especifica que uma biblioteca ou membro de um módulo, interface ou Dispinterface não pode ser chamado arbitrariamente.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- atributo restrito MIDL
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365947"
---
# <a name="restricted-attribute"></a>atributo restrito

O atributo **\[ Restricted \]** especifica que uma biblioteca ou membro de um módulo, interface ou Dispinterface não pode ser chamado arbitrariamente.

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*outros atributos* 
</dt> <dd>

Zero ou mais atributos MIDL.

</dd> <dt>

*tipo de instrução* 
</dt> <dd>

Um dos seguintes: [**biblioteca**](library.md), [**módulo**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).

</dd> <dt>

*nome da instrução* 
</dt> <dd>

O identificador pelo qual o software se refere a essa instrução.

</dd> <dt>

*definições* 
</dt> <dd>

Elementos de linguagem MIDL que definem o conteúdo desta instrução.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse atributo permite que você controle o acesso a elementos de interfaces, bibliotecas, módulos e dispinterfaces. Por exemplo, ele pode impedir que um item de dados seja usado por um programador de macro. Você pode aplicar esse atributo a um membro de uma [**coclass**](coclass.md), independentemente de o membro ser uma dispinterface ou interface, e independentemente de o membro ser um coletor (entrada) ou origem (saída). Um membro de uma **coclass** não pode ter os atributos **\[ Default \]** e **\[ Restricted \]** .

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**modulo**](module.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 