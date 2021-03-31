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
# <a name="property-set-display-name-dictionary"></a><span data-ttu-id="b0417-103">Dicionário de nome para exibição do conjunto de propriedades</span><span class="sxs-lookup"><span data-stu-id="b0417-103">Property Set Display Name Dictionary</span></span>

<span data-ttu-id="b0417-104">Um dicionário de nomes de exibição de propriedade permite que os usuários do conjunto de propriedades anexem significado a propriedades, além daquelas fornecidas pelo indicador de tipo.</span><span class="sxs-lookup"><span data-stu-id="b0417-104">A dictionary of property display names enables property set users to attach meaning to properties - beyond those provided by the type indicator.</span></span>

## <a name="dictionary-structure"></a><span data-ttu-id="b0417-105">Estrutura do dicionário</span><span class="sxs-lookup"><span data-stu-id="b0417-105">Dictionary Structure</span></span>

<span data-ttu-id="b0417-106">O dicionário contém uma contagem de entradas na lista, seguida por uma lista de entradas de dicionário.</span><span class="sxs-lookup"><span data-stu-id="b0417-106">The dictionary contains a count of entries in the list, followed by a list of dictionary entries.</span></span>

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a><span data-ttu-id="b0417-107">Estrutura de entrada de dicionário</span><span class="sxs-lookup"><span data-stu-id="b0417-107">Dictionary Entry Structure</span></span>

<span data-ttu-id="b0417-108">Cada entrada de dicionário na lista é um par de identificadores/cadeia de caracteres de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b0417-108">Each dictionary entry in the list is a Property Identifier/String pair.</span></span> <span data-ttu-id="b0417-109">A seguir está uma definição de pseudo-estrutura para uma entrada de dicionário.</span><span class="sxs-lookup"><span data-stu-id="b0417-109">The following is a pseudo-structure definition for a dictionary entry.</span></span> <span data-ttu-id="b0417-110">É uma pseudo estrutura porque o \[ \] membro sz é variável em tamanho.</span><span class="sxs-lookup"><span data-stu-id="b0417-110">It's a pseudo-structure because the sz\[\] member is variable in size.</span></span>

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a><span data-ttu-id="b0417-111">Dicionário de exemplo</span><span class="sxs-lookup"><span data-stu-id="b0417-111">Sample Dictionary</span></span>

<span data-ttu-id="b0417-112">O exemplo de transferência de dados do mercado de ações a seguir pode incluir um nome de ação "cotação de ações" para o conjunto inteiro e "símbolo de marca-ação" para o \_ símbolo PID.</span><span class="sxs-lookup"><span data-stu-id="b0417-112">The following stock market data transfer example might include a displayable name "Stock Quote" for the entire set, and "Ticker Symbol" for PID\_SYMBOL.</span></span> <span data-ttu-id="b0417-113">Se um conjunto de propriedades contiver apenas um símbolo e o dicionário, a seção conjunto de propriedades teria um fluxo de bytes parecido com o seguinte.</span><span class="sxs-lookup"><span data-stu-id="b0417-113">If a property set contained just a symbol and the dictionary, the property set section would have a byte stream that looked like the following.</span></span>

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

<span data-ttu-id="b0417-114">Lembre-se dos seguintes problemas relacionados aos dicionários do conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="b0417-114">Be aware of the following issues regarding property set dictionaries:</span></span>

-   <span data-ttu-id="b0417-115">A ID de propriedade 0 não tem um indicador de tipo.</span><span class="sxs-lookup"><span data-stu-id="b0417-115">Property ID 0 does not have a type indicator.</span></span> <span data-ttu-id="b0417-116">O tipo de dados **DWORD** que indica a contagem de entradas na posição do indicador de tipo.</span><span class="sxs-lookup"><span data-stu-id="b0417-116">The **DWORD** data type that indicates the count of entries sits in the type-indicator position.</span></span>
-   <span data-ttu-id="b0417-117">A contagem de caracteres na cadeia *cch* contém o caractere zero que encerra a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b0417-117">The count of characters in the *cch* string includes the zero character that terminates the string.</span></span> <span data-ttu-id="b0417-118">Quando a página de código do conjunto de propriedades não for Unicode, esse campo será, na verdade, uma contagem de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="b0417-118">When the codepage of the property set is not Unicode, this field is actually a **byte** count.</span></span> <span data-ttu-id="b0417-119">Para conjuntos de propriedades com uma versão de formato 0, essa contagem não pode exceder 256.</span><span class="sxs-lookup"><span data-stu-id="b0417-119">For property sets with a format version of 0, this count may not exceed 256.</span></span> <span data-ttu-id="b0417-120">Para conjuntos de propriedades com uma versão de formato 1, essa contagem pode ser tão grande quanto é permitido pelo tamanho total do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0417-120">For property sets with a format version of 1, this count may be as large as is allowed by the total property set size.</span></span>
-   <span data-ttu-id="b0417-121">O dicionário é opcional.</span><span class="sxs-lookup"><span data-stu-id="b0417-121">The dictionary is optional.</span></span> <span data-ttu-id="b0417-122">Nem todos os nomes de propriedades no conjunto precisam aparecer no dicionário.</span><span class="sxs-lookup"><span data-stu-id="b0417-122">Not all the names of properties in the set are required to appear in the dictionary.</span></span> <span data-ttu-id="b0417-123">Por outro lado, nem todos os nomes no dicionário são necessários para corresponder às propriedades no conjunto.</span><span class="sxs-lookup"><span data-stu-id="b0417-123">Conversely, not all names in the dictionary are required to correspond to properties in the set.</span></span> <span data-ttu-id="b0417-124">O dicionário deve omitir entradas para propriedades presumidas para serem reconhecidas universalmente por aplicativos que manipulam o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0417-124">The dictionary should omit entries for properties assumed to be universally recognized by applications manipulating the property set.</span></span> <span data-ttu-id="b0417-125">Normalmente, os nomes para os conjuntos de propriedades de base para padrões amplamente aceitos são omitidos, mas os conjuntos de propriedades de uso especial podem incluir dicionários para uso por navegadores.</span><span class="sxs-lookup"><span data-stu-id="b0417-125">Typically, names for the base property sets for widely-accepted standards are omitted, but special-purpose property sets may include dictionaries for use by browsers.</span></span>
-   <span data-ttu-id="b0417-126">Os nomes de propriedade no dicionário são armazenados na página de código indicada pela [ID de propriedade 1](/windows/desktop/Stg/reserved-property-identifiers).</span><span class="sxs-lookup"><span data-stu-id="b0417-126">Property names in the dictionary are stored in the code page indicated by [Property ID 1](/windows/desktop/Stg/reserved-property-identifiers).</span></span> <span data-ttu-id="b0417-127">Para páginas de código ANSI, cada entrada de dicionário é alinhada em byte.</span><span class="sxs-lookup"><span data-stu-id="b0417-127">For ANSI code pages, each dictionary entry is byte-aligned.</span></span> <span data-ttu-id="b0417-128">Portanto, não há nenhum espaçamento entre os nomes de propriedade com a ID de propriedade 0.</span><span class="sxs-lookup"><span data-stu-id="b0417-128">Thus, there is no spacing between property names with Property ID 0.</span></span> <span data-ttu-id="b0417-129">Esse é o único caso em que os valores de tipos de dados **DWORD** (a ID da propriedade e a propriedade nome-comprimento **DWORD** s) não precisam ser alinhados nos limites de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b0417-129">This is the only case where values of **DWORD** data types (the property ID and property name-length **DWORD** s) are not required to be aligned on 32-bit boundaries.</span></span> <span data-ttu-id="b0417-130">Para páginas Unicode, cada entrada de dicionário é alinhada em 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b0417-130">For Unicode pages, each dictionary entry is 32-bit aligned.</span></span>
-   <span data-ttu-id="b0417-131">Os nomes de propriedade que começam com os caracteres Unicode binários 0x0001 por meio de 0x001F são reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b0417-131">Property names that begin with the binary Unicode characters 0x0001 through 0x001F are reserved for future use.</span></span>
-   <span data-ttu-id="b0417-132">O nome da propriedade associado à ID de propriedade 0 representa o nome do conjunto de propriedades inteiro.</span><span class="sxs-lookup"><span data-stu-id="b0417-132">The property name associated with Property ID 0 represents the name of the entire property set.</span></span>

 

 