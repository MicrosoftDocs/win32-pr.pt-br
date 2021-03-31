---
title: Dicionário de nome para exibição do conjunto de propriedades
description: Um dicionário de nomes de exibição de propriedade permite que os usuários do conjunto de propriedades anexem significado a propriedades, além daquelas fornecidas pelo indicador de tipo.
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd844b4d37d4f10434fc5b73f936b4b6565c1506
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641542"
---
# <a name="property-set-display-name-dictionary"></a>Dicionário de nome para exibição do conjunto de propriedades

Um dicionário de nomes de exibição de propriedade permite que os usuários do conjunto de propriedades anexem significado a propriedades, além daquelas fornecidas pelo indicador de tipo.

## <a name="dictionary-structure"></a>Estrutura do dicionário

O dicionário contém uma contagem de entradas na lista, seguida por uma lista de entradas de dicionário.

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a>Estrutura de entrada de dicionário

Cada entrada de dicionário na lista é um par de identificadores/cadeia de caracteres de propriedade. A seguir está uma definição de pseudo-estrutura para uma entrada de dicionário. É uma pseudo estrutura porque o \[ \] membro sz é variável em tamanho.

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a>Dicionário de exemplo

O exemplo de transferência de dados do mercado de ações a seguir pode incluir um nome de ação "cotação de ações" para o conjunto inteiro e "símbolo de marca-ação" para o \_ símbolo PID. Se um conjunto de propriedades contiver apenas um símbolo e o dicionário, a seção conjunto de propriedades teria um fluxo de bytes parecido com o seguinte.

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

Lembre-se dos seguintes problemas relacionados aos dicionários do conjunto de propriedades:

-   A ID de propriedade 0 não tem um indicador de tipo. O tipo de dados **DWORD** que indica a contagem de entradas na posição do indicador de tipo.
-   A contagem de caracteres na cadeia *cch* contém o caractere zero que encerra a cadeia de caracteres. Quando a página de código do conjunto de propriedades não for Unicode, esse campo será, na verdade, uma contagem de **bytes** . Para conjuntos de propriedades com uma versão de formato 0, essa contagem não pode exceder 256. Para conjuntos de propriedades com uma versão de formato 1, essa contagem pode ser tão grande quanto é permitido pelo tamanho total do conjunto de propriedades.
-   O dicionário é opcional. Nem todos os nomes de propriedades no conjunto precisam aparecer no dicionário. Por outro lado, nem todos os nomes no dicionário são necessários para corresponder às propriedades no conjunto. O dicionário deve omitir entradas para propriedades presumidas para serem reconhecidas universalmente por aplicativos que manipulam o conjunto de propriedades. Normalmente, os nomes para os conjuntos de propriedades de base para padrões amplamente aceitos são omitidos, mas os conjuntos de propriedades de uso especial podem incluir dicionários para uso por navegadores.
-   Os nomes de propriedade no dicionário são armazenados na página de código indicada pela [ID de propriedade 1](/windows/desktop/Stg/reserved-property-identifiers). Para páginas de código ANSI, cada entrada de dicionário é alinhada em byte. Portanto, não há nenhum espaçamento entre os nomes de propriedade com a ID de propriedade 0. Esse é o único caso em que os valores de tipos de dados **DWORD** (a ID da propriedade e a propriedade nome-comprimento **DWORD** s) não precisam ser alinhados nos limites de 32 bits. Para páginas Unicode, cada entrada de dicionário é alinhada em 32 bits.
-   Os nomes de propriedade que começam com os caracteres Unicode binários 0x0001 por meio de 0x001F são reservados para uso futuro.
-   O nome da propriedade associado à ID de propriedade 0 representa o nome do conjunto de propriedades inteiro.

 

 