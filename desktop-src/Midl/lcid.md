---
title: Atributo lcid
description: O atributo \ lcid\ especifica um identificador de localidade e habilita o suporte ao compilador MIDL específico da localidade.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- Atributo lcid MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87d1b6105d7e6ae561d7409cbf256b67f965c61e235ffc5782594cb5623497c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806792"
---
# <a name="lcid-attribute"></a>Atributo lcid

O **\[ atributo \] lcid** especifica um identificador de localidade e habilita o suporte ao compilador MIDL específico da localidade.

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uuid-number* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a [**biblioteca**](library.md).

</dd> <dt>

*Localeid* 
</dt> <dd>

Especifica o identificador de localidade de 32 bits usado no suporte Windows Idioma Nacional. Normalmente, o identificador de localidade é dado em hexadecimal.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Zero ou mais atributos a aplicar à [**biblioteca**](library.md).

</dd> <dt>

*nome da biblioteca* 
</dt> <dd>

O nome pelo qual os componentes de software se referem à [**biblioteca**](library.md).

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Uma ou mais instruções MIDL que definem o conteúdo da [**biblioteca**](library.md).

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Zero ou mais atributos MIDL que serão aplicados ao parâmetro de função.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica o nome do parâmetro no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\[ sintaxe \] lcid** tem duas formas diferentes; o efeito do atributo [](library.md) depende de qual sintaxe você usa – a sintaxe da instrução da biblioteca ou a sintaxe do parâmetro.

Quando aplicado à [](library.md) instrução de biblioteca, juntamente com um argumento localeID, conforme mostrado no primeiro exemplo, o atributo **\[ lcid \]** identifica a localidade para uma biblioteca de tipos ou para um argumento de função e permite que você use caracteres internacionais dentro do bloco de biblioteca.

Em vigor com a versão 3.01.75 do compilador MIDL, o identificador de localidade fornecido por esse atributo não apenas decora a biblioteca de tipos resultante, mas, na verdade, altera o comportamento do compilador. Em uma [**instrução**](library.md) de biblioteca, do ponto em que o atributo **\[ lcid \]** é usado, MIDL aceitará a entrada localizada de acordo com a localidade especificada. Em particular, há suporte completo para idiomas asiáticos, como japonês, chinês e coreano (suporte completo a DBCS). Os recursos com suporte na localização são: comentários, cadeias de caracteres, helpstrings e identificadores.

Use a opção do compilador [**/lcid**](-lcid.md) para ter esse suporte de localização disponível para todo o arquivo de entrada, incluindo o nome do arquivo e o caminho do diretório, em vez de apenas dentro do bloco de biblioteca.

Quando aplicado a um parâmetro, o atributo **\[ lcid \]** permite que você passe um identificador de localidade para uma função, conforme mostrado no segundo exemplo. As seguintes restrições se aplicam aos **\[ parâmetros lcid: \]**

-   Uma função pode ter no máximo um **\[ parâmetro lcid. \]**
-   O tipo de dados do parâmetro deve ser [**longo.**](long.md)
-   A direção do parâmetro deve estar **\[** [**apenas**](in.md) **\]** em .
-   O **\[ parâmetro \] lcid** deve seguir quaisquer outros parâmetros, exceto um **\[** [**parâmetro retval.**](retval.md) **\]**
-   Não é possível aplicar o **\[ atributo \] lcid** a um parâmetro [**dispinterface**](dispinterface.md) ou [**coclass.**](coclass.md)

## <a name="examples"></a>Exemplos

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**/lcid**](-lcid.md)
</dt> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 