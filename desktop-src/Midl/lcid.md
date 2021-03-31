---
title: atributo LCID
description: O atributo \ LCID \ especifica um identificador de localidade e habilita o suporte a compilador de MIDL específico de localidade.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- atributo LCID MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640548"
---
# <a name="lcid-attribute"></a>atributo LCID

O atributo **\[ LCID \]** especifica um identificador de localidade e habilita o suporte a compilador de MIDL específico de localidade.

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

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para a [**biblioteca**](library.md).

</dd> <dt>

*localeID* 
</dt> <dd>

Especifica o identificador de localidade de 32 bits usado no suporte ao idioma nacional do Windows. Normalmente, o identificador de localidade é fornecido em hexadecimal.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Zero ou mais atributos a serem aplicados à [**biblioteca**](library.md).

</dd> <dt>

*nome da biblioteca* 
</dt> <dd>

O nome pelo qual os componentes de software se referem à [**biblioteca**](library.md).

</dd> <dt>

*bibliotecas-definição-instruções* 
</dt> <dd>

Uma ou mais instruções MIDL que definem o conteúdo da [**biblioteca**](library.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Zero ou mais atributos MIDL que serão aplicados ao parâmetro de função.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica o nome do parâmetro no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe **\[ \] LCID** tem duas formas diferentes; o efeito do atributo depende da sintaxe usada – ou da sintaxe da instrução de [**biblioteca**](library.md) ou da sintaxe do parâmetro.

Quando aplicado à instrução de [**biblioteca**](library.md) , juntamente com um argumento LocaleID, como mostrado no primeiro exemplo, o atributo **\[ LCID \]** identifica a localidade para uma biblioteca de tipos ou para um argumento de função e permite que você use caracteres internacionais dentro do bloco de biblioteca.

Em vigor com a versão 3.01.75 do compilador MIDL, o identificador de localidade fornecido por esse atributo não apenas decora a biblioteca de tipos resultante, mas, na verdade, altera o comportamento do compilador. Dentro de uma instrução de [**biblioteca**](library.md) , do ponto em que o atributo **\[ LCID \]** é usado, MIDL aceitará a entrada localizada de acordo com a localidade especificada. Em particular, o suporte completo para idiomas asiáticos, como japonês, chinês e coreano (suporte completo a DBCS) está disponível. Os recursos com suporte da localização são: comentários, cadeias de caracteres, HelpStrings e identificadores.

Use a opção de compilador [**/LCID**](-lcid.md) para ter esse suporte de localização disponível para todo o arquivo de entrada, incluindo o nome do arquivo e o caminho do diretório, em vez de apenas dentro do bloco de biblioteca.

Quando aplicado a um parâmetro, o atributo **\[ LCID \]** permite passar um identificador de localidade para uma função, conforme mostrado no segundo exemplo. As seguintes restrições se aplicam aos parâmetros **\[ LCID \]** :

-   Uma função pode ter no máximo um parâmetro **\[ LCID \]** .
-   O tipo de dados do parâmetro deve ser [**longo**](long.md).
-   A direção do parâmetro deve estar **\[** [**em**](in.md) **\]** apenas.
-   O parâmetro **\[ LCID \]** deve seguir quaisquer outros parâmetros, exceto um **\[** parâmetro [**retval**](retval.md) **\]** .
-   Você não pode aplicar o atributo **\[ LCID \]** a um parâmetro [**dispinterface**](dispinterface.md) ou [**coclass**](coclass.md) .

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

[**/LCID**](-lcid.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 