---
title: Recurso STRINGTABLE
description: Define um ou mais recursos de cadeia de caracteres para um aplicativo. Os recursos de cadeia de caracteres são simplesmente seqüências Unicode ou ASCII terminadas em nulo que podem ser carregadas quando necessário no arquivo executável, usando a função LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menus de recursos do STRINGTABLE e outros recursos
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084537"
---
# <a name="stringtable-resource"></a>Recurso STRINGTABLE

Define um ou mais recursos de cadeia de caracteres para um aplicativo. Os recursos de cadeia de caracteres são simplesmente seqüências Unicode ou ASCII terminadas em nulo que podem ser carregadas quando necessário no arquivo executável, usando a função [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) .

Há duas maneiras de Formatar uma instrução **STRINGTABLE** :

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- ou –

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*
</dt> <dd>

Esse parâmetro pode ser zero ou mais das instruções a seguir.



| Instrução                                                        | Descrição                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Características**](characteristics-statement.md) *DWORD*     | Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. Para obter mais informações, consulte [**características**](characteristics-statement.md). |
| [](language-statement.md) *Idioma* do idioma, *subidioma* | Especifica o idioma do recurso. Para obter mais informações, consulte [**Language**](language-statement.md).                                                                              |
| [](version-statement.md) *DWORD* da versão                     | Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. Para obter mais informações, consulte [**versão**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

Inteiro de 16 bits sem sinal que identifica o recurso.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*Strings*
</dt> <dd>

Uma ou mais cadeias de caracteres, entre aspas. A cadeia de caracteres não deve ter mais de 4097 caracteres e deve ocupar uma única linha no arquivo de origem. Para adicionar um retorno de carro à cadeia de caracteres, use esta sequência de caracteres: \\ 012. Por exemplo, "linha um \\ 012Line dois" define uma cadeia de caracteres que é exibida da seguinte maneira:

``` syntax
Line one
Line two
```

Para inserir aspas na cadeia de caracteres, use a seguinte sequência: "". Por exemplo, "" "linha três" "" define uma cadeia de caracteres que é exibida da seguinte maneira:

``` syntax
"Line three"
```

Para codificar caracteres Unicode, use um "L" seguido dos caracteres Unicode entre aspas. Consulte a seção de exemplos para obter um exemplo.

O compilador de recurso também dá suporte a continuaçãos de linha na *cadeia de caracteres*. Consulte a seção de exemplos para obter um exemplo.

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="remarks"></a>Comentários

O RC aloca 16 cadeias de caracteres por seção e usa o valor do identificador para determinar qual seção deve conter a cadeia de caracteres. Cadeias de caracteres cujos identificadores diferem apenas nos quatro bits inferiores são colocados na mesma seção. Para obter mais informações, consulte [Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução **STRINGTABLE** para exibir cadeias de caracteres ASCII:

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

O exemplo a seguir mostra como codificar caracteres Unicode:

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

O exemplo a seguir mostra cadeias de caracteres com ASCII e Unicode. Observe que as cadeias de caracteres sem o "L" inicial usam o formato de escape de 2 dígitos:

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

O exemplo a seguir mostra como as continuaçãos de linha podem ser usadas:

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Cadeia de caracteres LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**IDIOMA**](language-statement.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Versão**](version-statement.md)
</dt> </dl>

 

 